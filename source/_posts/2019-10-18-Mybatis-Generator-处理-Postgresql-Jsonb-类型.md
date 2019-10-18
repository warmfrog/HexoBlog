---
title: Mybatis-Generator-处理-Postgresql-Jsonb-类型
date: 2019-10-18 14:16:35
tags:
---

Postgresql 表数据类型可以是 json 和 jsonb，区别是 jsonb 类型会校验数据是否符合 json 格式，并将解析后的数据存储，而 json 是直接存储。所以 jsonb 插入慢，查询快，json 插入快，查询慢。

当 Postgresql 表中有 jsonb 类型时，通过 Mybatis 来生成 mapper.xml 时，需要自定义 TypeHandler。然后在 Mybatis 的 generater-config.xml 中对应的表配置该 TypeHandler。

``` xml
	<table tableName="traffic_line" domainObjectName="Line">
			<property name="runtimeSchema" value="&quot;tf&quot;" />
			<columnOverride column="stations" jdbcType="OTHER" typeHandler="com.example.handler.JsonTypeHandler" />
			<columnOverride column="middle_points" jdbcType="OTHER" typeHandler="com.example.handler.JsonTypeHandler" />
		</table>
```

上面数据表配置中，列 stations 和 middle_points 都为 jsonb 类型，配置 jdbcType 属性为 `OTHER`, typeHandler 为自定义的 `JsonTypeHandler` 类。

JsonTypeHandler 类

``` Java
import com.eg.egsc.common.component.utils.JsonUtil;
import java.sql.CallableStatement;
import java.sql.PreparedStatement;
import java.sql.ResultSet;
import java.sql.SQLException;
import org.apache.ibatis.type.BaseTypeHandler;
import org.apache.ibatis.type.JdbcType;
import org.apache.ibatis.type.MappedTypes;
import org.postgresql.util.PGobject;

@MappedTypes({Object.class})
public class JsonTypeHandler extends BaseTypeHandler<Object> {
    private static final PGobject JSON_OBJECT = new PGobject();

    public JsonTypeHandler() {
    }

    public void setNonNullParameter(PreparedStatement preparedStatement, int i, Object o, JdbcType jdbcType) throws SQLException {
        JSON_OBJECT.setType("json");
        JSON_OBJECT.setValue(JsonUtil.toJsonString(o));
        preparedStatement.setObject(i, JSON_OBJECT);
    }

    public Object getNullableResult(ResultSet resultSet, String s) throws SQLException {
        return JsonUtil.fromJson(resultSet.getString(s), Object.class);
    }

    public Object getNullableResult(ResultSet resultSet, int i) throws SQLException {
        return JsonUtil.fromJson(resultSet.getString(i), Object.class);
    }

    public Object getNullableResult(CallableStatement callableStatement, int i) throws SQLException {
        return JsonUtil.fromJson(callableStatement.getString(i), Object.class);
    }
}

```


