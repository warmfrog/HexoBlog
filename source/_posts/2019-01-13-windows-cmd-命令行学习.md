
---
layout: post
title: windows 下的cmd命令学习 
tags: [cmd,windows]
---

## 参考网站

* [Windows cmd 命令大全](https://www.jb51.net/article/141568.htm)

* [脚本之家-脚本专栏](https://www.jb51.net/list/index_96.htm)

* [List of Command Prompt Commands](https://www.lifewire.com/list-of-command-prompt-commands-4092302)

* [Batch Script Tutorial](https://www.tutorialspoint.com/batch_script/index.htm)

* [Guide to Windows Batch Scripting](http://steve-jansen.github.io/guides/windows-batch-scripting/)

[Wikibook Windows Batch Scripting](https://en.wikibooks.org/wiki/Windows_Batch_Scripting)

## 常用命令

* robocopy

个人感觉一个强大到没朋友的复制命令，支持更多选项，具体请查看 robocopy /?

镜像目录，当我们要将源目录同步到目的目录时非常有用

    robocopy U:\Books E:\Books /mir

这相当于复制源路径目录到目的地路径，删除目的地路径中在源路径中不存在的文件和文件夹。

* 创建目录
    mkdir -p src/main/java/hello

* 查看目录树
    tree
* 删除目录与子目录及文件

    rmdir /s targetDir

* 静默方式

    rmdir /q /s targetDir

* 命令创建别名
    doskey ls=dir

* 添加用户
    net user wuqilong 123456 /add

* ftp

    open 192.168.103.46 21

    Input username, passwd

    dir,get,put,cd,delete,bye,quit

* regedit

注册表(Registry)是Microsoft Windows中的一个重要数据库，用于存储系统和应用程序的设置信息。其中存储着各种参数，直接控制着windows的启动、硬件驱动程序的装载以及一些windows应用程序的运行。

## [Windows8 Command Promt Commands](https://www.lifewire.com/windows-8-command-prompt-commands-4172073)

在windows8 包含了大约230条命令行命令。在Windows8 上的这些可获得的命令用于各种目的，包括诊断，纠正Windows问题，自动任务等等。以下是win8的命令行命令列表。

<table class="mntl-sc-block-table__table">
<colgroup style="" span="1"></colgroup>
<colgroup style="" span="1"></colgroup>
<thead>
<tr>
<th colspan="2" class="mntl-sc-block-table__title">List of Command Prompt Commands for Windows 8</th>
</tr>
</thead>
<tbody data-check="-1">
<tr>
<td><strong>Command</strong></td>
<td><strong>Description</strong></td>
</tr>
<tr>
<td>Append</td>
<td>The append command can be used by programs to open files in another directory as if they were located in the current directory. The append command is not available in 64-bit versions of Windows 8.</td>
</tr>
<tr>
<td>Arp</td>
<td>The arp command is used to display or change entries in the ARP cache.</td>
</tr>
<tr>
<td>Assoc</td>
<td>The assoc command is used to display or change the file type associated with a particular <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-is-a-file-extension-2625879">file extension</a>.</td>
</tr>
<tr>
<td><a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/attrib-command-2625802">Attrib</a></td>
<td>The attrib command is used to change the attributes of a single file or a directory.</td>
</tr>
<tr>
<td>Auditpol</td>
<td>The auditpol command is used to display or change audit policies.</td>
</tr>
<tr>
<td>Bcdboot</td>
<td>The bcdboot command is used to copy <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-does-booting-mean-2625799">boot</a> files to the system <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-is-a-partition-2625958">partition</a> and to create a new system BCD store.</td>
</tr>
<tr>
<td>Bcdedit</td>
<td>The bcdedit command is used to view or make changes to Boot Configuration Data.</td>
</tr>
<tr>
<td>Bdehdcfg</td>
<td>The bdehdcfg command is sued to prepare a <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-is-a-hard-disk-drive-2618152">hard drive</a> for BitLocker Drive Encryption.</td>
</tr>
<tr>
<td>Bitsadmin</td>
<td>The bitsadmin command is used to create, manage, and monitor download and upload jobs. While the bitsadmin command is available in Windows 8, it is being phased out. The BITS PowerShell cmdlets should be used instead.</td>
</tr>
<tr>
<td>Bootcfg</td>
<td>The bootcfg command is used to build, modify, or view the contents of the boot.ini file, a <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-is-a-hidden-file-2625898">hidden file</a> that is used to identify in what folder, on which partition, and on which hard drive Windows is located. The bootcfg command was replaced by the bcdedit command beginning in Windows Vista. Bootcfg is still available in Windows 8 but it serves no real value since boot.ini is not used.</td>
</tr>
<tr>
<td>Bootsect</td>
<td><p>The bootsect command is used to configure the <a href="https://www.lifewire.com/what-is-the-master-boot-code-2625934">master boot code</a> to one compatible with Windows 8 (BOOTMGR). The bootsect command is only available from the Command Prompt in <a href="https://www.lifewire.com/advanced-startup-options-2625805">Advanced Startup Options</a>.</p></td>
</tr>
<tr>
<td>Break</td>
<td>The break command sets or clears extended <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-is-ctrl-c-used-for-2625834">CTRL+C</a> checking on DOS systems. The break command is available in Windows 8 to provide compatibility with MS-DOS files but it has no effect in Windows itself.</td>
</tr>
<tr>
<td>Cacls</td>
<td>The cacls command is used to display or change access control lists of files. The cacls command is being phased out in favor of the icacls command, which should be used instead.</td>
</tr>
<tr>
<td>Call</td>
<td>The call command is used to run a script or batch program from within another script or batch program. The call command has no effect outside of a script or batch file. In other words, running the call command at the Command Prompt or MS-DOS prompt will do nothing.</td>
</tr>
<tr>
<td>Cd</td>
<td>The cd command is the shorthand version of the chdir command.</td>
</tr>
<tr>
<td>Certreq</td>
<td>The certreq command is used to perform various certification authority (CA) certificate functions.</td>
</tr>
<tr>
<td>Certutil</td>
<td>The certutil command is used to dump and display certification authority (CA) configuration information in addition to other CA functions.</td>
</tr>
<tr>
<td>Change</td>
<td>The change command changes various terminal server settings like install modes, COM port mappings, and logons.</td>
</tr>
<tr>
<td>Chcp</td>
<td>The chcp command displays or configures the active code page number.</td>
</tr>
<tr>
<td>Chdir</td>
<td>The chdir command is used to display the drive letter and folder that you are currently in. Chdir can also be used to change the drive and/or directory that you want to work in.</td>
</tr>
<tr>
<td>Checknetisolation</td>
<td>The checknetisolation command is used to test apps that require network capabilities.</td>
</tr>
<tr>
<td>Chglogon</td>
<td>The chglogon command enables, disables, or drains terminal server session logins. Executing the chglogon command is the same as executing change logon.</td>
</tr>
<tr>
<td>Chgport</td>
<td>The chgport command can be used to display or change COM port mappings for DOS compatibility. Executing the chgport command is the same as executing change port.</td>
</tr>
<tr>
<td>Chgusr</td>
<td>The chgusr command is used to change the install mode for the terminal server. Executing the chgusr command is the same as executing change user.</td>
</tr>
<tr>
<td><a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/chkdsk-command-2625838">Chkdsk</a></td>
<td>The chkdsk command, often referred to as check disk, is used to identify and correct certain hard drive errors.</td>
</tr>
<tr>
<td>Chkntfs</td>
<td>The chkntfs command is used to configure or display the checking of the disk drive during the Windows boot process.</td>
</tr>
<tr>
<td>Choice</td>
<td>The choice command is used within a script or batch program to provide a list of choices and return the value of that choice to the program.</td>
</tr>
<tr>
<td>Cipher</td>
<td>The cipher command shows or changes the encryption status of files and folders on NTFS partitions.</td>
</tr>
<tr>
<td>Clip</td>
<td>The clip command is used to <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/how-to-redirect-command-output-to-a-file-2618084">redirect the output</a> from any command to the clipboard in Windows.</td>
</tr>
<tr>
<td>Cls</td>
<td>The cls command clears the screen of all previously entered commands and other text.</td>
</tr>
<tr>
<td>Cmd</td>
<td>The cmd command starts a new instance of the cmd.exe <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-is-a-command-line-interpreter-2625827">command interpreter</a>.</td>
</tr>
<tr>
<td>Cmdkey</td>
<td>The cmdkey command is used to show, create, and remove stored user names and passwords.</td>
</tr>
<tr>
<td>Cmstp</td>
<td>The cmstp command installs or uninstalls a Connection Manager service profile.</td>
</tr>
<tr>
<td>Color</td>
<td>The color command is used to change the colors of the text and background within the Command Prompt window.</td>
</tr>
<tr>
<td>Command</td>
<td>The command command starts a new instance of the command.com command interpreter. The command command is not available in 64-bit versions of Windows 8.</td>
</tr>
<tr>
<td>Comp</td>
<td>The comp command is used to compare the contents of two files or sets of files.</td>
</tr>
<tr>
<td>Compact</td>
<td>The compact command is used to show or change the compression state of files and directories on <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/ntfs-file-system-2625948">NTFS partitions</a>.</td>
</tr>
<tr>
<td>Convert</td>
<td>The convert command is used to convert FAT or FAT32 formatted volumes to the NTFS format.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/copy-command-2625842">Copy</a></td>
<td>The copy command does simply that - it copies one or more files from one location to another. The xcopy command is considered to be a more "powerful" version of the copy command.</td>
</tr>
<tr>
<td>Cscript</td>
<td>The cscript command is used to execute scripts via Microsoft Script Host. The cscript command is most popularly used to manage printers from the command line using scripts like prncnfg.vbs, prndrvr.vbs, prnmngr.vbs, and others.</td>
</tr>
<tr>
<td>Date</td>
<td>The date command is used to show or change the current date.</td>
</tr>
<tr>
<td>Debug</td>
<td>The debug command starts Debug, a command line application used to test and edit programs. The debug command is not available in 64-bit versions of Windows 8.</td>
</tr>
<tr>
<td>Defrag</td>
<td>The defrag command is used to defragment a drive you specify. The defrag command is the command line version of Microsoft's Disk Defragmenter.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/delete-command-2625859">Del</a></td>
<td>The del command is used to delete one or more files. The del command is the same as the erase command.</td>
</tr>
<tr>
<td>Diantz</td>
<td>The diantz command is used to losslessly compress one or more files. The diantz command is sometimes called Cabinet Maker. The diantz command is the same as the makecab command.</td>
</tr>
<tr>
<td><a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/dir-command-4050018">Dir</a></td>
<td>The dir command is used to display a list of files and folders contained inside the folder that you are currently working in. The dir command also displays other important information like the hard drive's serial number, the total number of files listed, their combined size, the total amount of free space left on the drive, and more.</td>
</tr>
<tr>
<td>Diskcomp</td>
<td>The diskcomp command is used to compare the contents of two floppy disks.</td>
</tr>
<tr>
<td>Diskcopy</td>
<td>The diskcopy command is used to copy the entire contents of one floppy disk to another.</td>
</tr>
<tr>
<td>Diskpart</td>
<td>The diskpart command is used to create, manage, and delete hard drive partitions.</td>
</tr>
<tr>
<td>Diskperf</td>
<td>The diskperf command is used to manage disk performance counters remotely.</td>
</tr>
<tr>
<td>Diskraid</td>
<td>The diskraid command starts the DiskRAID tool which is used to manage and configure RAID arrays.</td>
</tr>
<tr>
<td>Dism</td>
<td>The dism command starts the Deployment Image Servicing and Management tool (DISM). The DISM tool is used to manage features in Windows images.</td>
</tr>
<tr>
<td>Dispdiag</td>
<td>The dispdiag command is used to output a log of information about the display system.</td>
</tr>
<tr>
<td>Djoin</td>
<td>The djoin command is used to create a new computer account in a domain.</td>
</tr>
<tr>
<td>Doskey</td>
<td>The doskey command is used to edit command lines, create macros, and recall previously entered commands.</td>
</tr>
<tr>
<td>Dosx</td>
<td>The dosx command is used to start DOS Protected Mode Interface (DPMI), a special mode designed to give MS-DOS applications access to more than the normally allowed 640 KB. The dosx command is not available in 64-bit versions of Windows 8. The dosx command and DPMI is only available in Windows 8 to support older MS-DOS programs.</td>
</tr>
<tr>
<td>Driverquery</td>
<td>The driverquery command is used to show a list of all installed <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-is-a-device-driver-2625796">drivers</a>.</td>
</tr>
<tr>
<td>Echo</td>
<td>The echo command is used to show messages, most commonly from within script or batch files. The echo command can also be used to turn the echoing feature on or off.</td>
</tr>
<tr>
<td>Edit</td>
<td>The edit command starts the MS-DOS Editor tool which is used to create and modify <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/txt-text-file-4150707">text files</a>. The edit command is not available in 64-bit versions of Windows 8.</td>
</tr>
<tr>
<td>Edlin</td>
<td>The edlin command starts the Edlin tool which is used to create and modify text files from the command line. The edlin command is not available in 64-bit versions of Windows 8.</td>
</tr>
<tr>
<td>Endlocal</td>
<td>The endlocal command is used to end the localization of environment changes inside a batch or script file.</td>
</tr>
<tr>
<td>Erase</td>
<td>The erase command is used to delete one or more files. The erase command is the same as the del command.</td>
</tr>
<tr>
<td>Esentutl</td>
<td>The esentutl command is used to manage Extensible Storage Engine databases.</td>
</tr>
<tr>
<td>Eventcreate</td>
<td>The eventcreate command is used to create a custom event in an event log.</td>
</tr>
<tr>
<td>Exe2bin</td>
<td>The exe2bin command is used to convert a file of the EXE file type (executable file) to a binary file. The exe2bin command is not available in any 64-bit version of Windows 8.</td>
</tr>
<tr>
<td>Exit</td>
<td>The exit command is used to end the cmd.exe (Windows) or command.com (MS-DOS) session that you're currently working in.</td>
</tr>
<tr>
<td>Expand</td>
<td>The expand command is used to extract the files and folders contained in Microsoft Cabinet (CAB) files.</td>
</tr>
<tr>
<td>Extrac32</td>
<td>The extrac32 command is used to extract the files and folders contained in Microsoft Cabinet (CAB) files. The extrac32 command is actually a CAB extraction program for use by Internet Explorer but can be used to extract any Microsoft Cabinet file. Use the expand command instead of the extrac32 command if possible.</td>
</tr>
<tr>
<td>Fastopen</td>
<td>The fastopen command is used to add a program's hard drive location to a special list stored in memory, potentially improving the program's launch time by removing the need for MS-DOS to locate the application on the drive. The fastopen command is not available in 64-bit versions of Windows 8. Fastopen is only available in Windows 8 to support older MS-DOS files.</td>
</tr>
<tr>
<td>Fc</td>
<td>The fc command is used to compare two individual or sets of files and then show the differences between them.</td>
</tr>
<tr>
<td>Find</td>
<td>The find command is used to search for a specified text string in one or more files.</td>
</tr>
<tr>
<td>Findstr</td>
<td>The findstr command is used to find text string patterns in one or more files.</td>
</tr>
<tr>
<td>Finger</td>
<td>The finger command is used to return information about one or more users on a remote computer that's running the Finger service.</td>
</tr>
<tr>
<td>Fltmc</td>
<td>The fltmc command is used to load, unload, list, and otherwise manage Filter drivers.</td>
</tr>
<tr>
<td>Fondue</td>
<td><p>The fondue command, short for Features on Demand User Experience Tool, is used to install any of the several optional Windows 8 features from the <a href="https://www.lifewire.com/what-is-a-command-line-interpreter-2625827">command line</a>. Optional Windows 8 features can also be installed from the Programs and Features applet in <a href="https://www.lifewire.com/control-panel-2625841">Control Panel</a>.</p></td>
</tr>
<tr>
<td>For</td>
<td>The for command is used to run a specified command for each file in a set of files. The for command is most often used within a batch or script file.</td>
</tr>
<tr>
<td>Forfiles</td>
<td>The forfiles command selects one or more files to execute a specified command on. The forfiles command is most often used within a batch or script file.</td>
</tr>
<tr>
<td><a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/format-command-2618091">Format</a></td>
<td>The format command is used to <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-does-it-mean-to-format-something-2625882">format</a> a drive in the file system that you specify. Drive formatting is also available from <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/disk-management-2625863">Disk Management</a>.</td>
</tr>
<tr>
<td>Fsutil</td>
<td>The fsutil command is used to perform various <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-is-file-allocation-table-fat-2625877">FAT</a> and NTFS file system tasks like managing reparse points and sparse files, dismounting a volume, and extending a volume.</td>
</tr>
<tr>
<td>Ftp</td>
<td>The ftp command can used to transfer files to and from another computer. The remote computer must be operating as an FTP server.</td>
</tr>
<tr>
<td>Ftype</td>
<td>The ftype command is used to define a default program to open a specified file type.</td>
</tr>
<tr>
<td>Getmac</td>
<td>The getmac command is used to display the media access control (MAC) address of all the network controllers on a system.</td>
</tr>
<tr>
<td>Goto</td>
<td>The goto command is used in a batch or script file to direct the command process to a labeled line in the script.</td>
</tr>
<tr>
<td>Gpresult</td>
<td>The gpresult command is used to display Group Policy settings.</td>
</tr>
<tr>
<td>Gpupdate</td>
<td>The gpupdate command is used to update Group Policy settings.</td>
</tr>
<tr>
<td>Graftabl</td>
<td>The graftabl command is used to enable the ability of Windows to display an extended character set in graphics mode. The graftabl command is not available in 64-bit versions of Windows 8.</td>
</tr>
<tr>
<td>Graphics</td>
<td>The graphics command is used to load a program that can print graphics. The graphics command is not available in 64-bit versions of Windows 8.</td>
</tr>
<tr>
<td><a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/help-command-2618092">Help</a></td>
<td>The help command provides more detailed information on any of the other Command Prompt or MS-DOS commands.</td>
</tr>
<tr>
<td>Hostname</td>
<td>The hostname command displays the <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-is-a-hostname-2625906">name of the current host</a>.</td>
</tr>
<tr>
<td>Hwrcomp</td>
<td>The hwrcomp command is used to compile custom dictionaries for handwriting recognition.</td>
</tr>
<tr>
<td>Hwrreg</td>
<td>The hwrreg command is used to install a previously compiled custom dictionary for handwriting recognition.</td>
</tr>
<tr>
<td>Icacls</td>
<td>The icacls command is used to display or change access control lists of files. The icacls command is an updated version of the cacls command.</td>
</tr>
<tr>
<td>If</td>
<td>The if command is used to perform conditional functions in a batch file.</td>
</tr>
<tr>
<td>Ipconfig</td>
<td>The ipconfig command is used to display detailed IP information for each network adapter utilizing TCP/IP. The ipconfig command can also be used to release and renew <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-is-an-ip-address-2625920">IP addresses</a> on systems configured to receive them via a <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-is-dhcp-2625848">DHCP</a> server.</td>
</tr>
<tr>
<td>Irftp</td>
<td>The irftp command is used to transmit files over an infrared link.</td>
</tr>
<tr>
<td>Iscsicli</td>
<td>The iscsicli command starts the Microsoft iSCSI Initiator, used to manage iSCSI.</td>
</tr>
<tr>
<td>Kb16</td>
<td>The kb16 command is used to support MS-DOS files that need to configure a keyboard for a specific language. The kb16 command is not available in 64-bit versions of Windows 8. The kb16 command only exists to support older MS-DOS files.</td>
</tr>
<tr>
<td>Klist</td>
<td>The klist command is used to list Kerberos service tickets. The klist command can also be used to purge Kerberos tickets.</td>
</tr>
<tr>
<td>Ksetup</td>
<td>The ksetup command is used to configure connections to a Kerberos server.</td>
</tr>
<tr>
<td>Ktmutil</td>
<td>The ktmutil command starts the Kernel Transaction Manager utility.</td>
</tr>
<tr>
<td>Label</td>
<td>The label command is used to manage the volume label of a disk.</td>
</tr>
<tr>
<td>Licensingdiag</td>
<td>The licensingdiag command is a tool used to generate a text-based log and other data files that contain <a href="https://www.lifewire.com/what-is-product-activation-2625971">product activation</a> and other Windows licensing information.</td>
</tr>
<tr>
<td>Loadfix</td>
<td>The loadfix command is used to load the specified program in the first 64K of memory and then runs the program. The loadfix command is not available in 64-bit versions of Windows 8.</td>
</tr>
<tr>
<td>Lodctr</td>
<td>The lodctr command is used to update registry values related to performance counters.</td>
</tr>
<tr>
<td>Logman</td>
<td>The logman command is used to create and manage Event Trace Session and Performance logs. The logman command also supports many functions of Performance Monitor.</td>
</tr>
<tr>
<td>Logoff</td>
<td>The logoff command is used to terminate a session.</td>
</tr>
<tr>
<td>Lpq</td>
<td>The lpq command displays the status of a print queue on a computer running Line Printer Daemon (LPD). The lpq command is not available by default in Windows 8 but can be enabled by turning on the LPD Print Service and LPR Port Monitor features from Programs and Features in Control Panel.</td>
</tr>
<tr>
<td>Lpr</td>
<td>The lpr command is used to send a file to a computer running Line Printer Daemon (LPD). The lpr command is not available by default in Windows 8 but can be enabled by turning on the LPD Print Service and LPR Port Monitor features from Programs and Features in Control Panel.</td>
</tr>
<tr>
<td>Makecab</td>
<td>The makecab command is used to losslessly <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-is-a-compressed-file-2625829">compress</a> one or more files. The makecab command is sometimes called Cabinet Maker. The makecab command is the same as the diantz command.</td>
</tr>
<tr>
<td>Manage-bde</td>
<td>The manage-bde command is used to configure BitLocker Drive Encryption from the command line.</td>
</tr>
<tr>
<td>Md</td>
<td>The md command is the shorthand version of the mkdir command.</td>
</tr>
<tr>
<td>Mem</td>
<td>The mem command shows information about used and free <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-is-random-access-memory-ram-2618159">memory</a> areas and programs that are currently loaded into memory in the MS-DOS subsystem. The mem command is not available in 64-bit versions of Windows 8.</td>
</tr>
<tr>
<td>Mkdir</td>
<td>The mkdir command is used to create a new folder.</td>
</tr>
<tr>
<td>Mklink</td>
<td>The mklink command is used to create a symbolic link.</td>
</tr>
<tr>
<td>Mode</td>
<td>The mode command is used to configure system devices, most often COM and LPT ports.</td>
</tr>
<tr>
<td><a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/more-command-4041467">More</a></td>
<td>The more command is used to display the information contained in a text file. The more command can also be used to paginate the results of any other Command Prompt or MS-DOS command.</td>
</tr>
<tr>
<td>Mountvol</td>
<td>The mountvol command is used to display, create, or remove volume mount points.</td>
</tr>
<tr>
<td>Move</td>
<td>The move command is used to move one or files from one folder to another. The move command is also used to rename directories.</td>
</tr>
<tr>
<td>Mrinfo</td>
<td>The mrinfo command is used to provide information about a router's interfaces and neighbors.</td>
</tr>
<tr>
<td><a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/msg-command-2618093">Msg</a></td>
<td>The msg command is used to send a message to a user.</td>
</tr>
<tr>
<td>Msiexec</td>
<td>The msiexec command is used to start Windows Installer, a tool used to install and configure software.</td>
</tr>
<tr>
<td>Muiunattend</td>
<td>The muiunattend command starts the Multilanguage User Interface unattended setup process.</td>
</tr>
<tr>
<td>Nbtstat</td>
<td>The nbtstat command is used to show TCP/IP information and other statistical information about a remote computer.</td>
</tr>
<tr>
<td><a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/net-command-2618094">Net</a></td>
<td>The net command is used to display, configure, and correct a wide variety of network settings.</td>
</tr>
<tr>
<td><a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/net-command-2618094">Net1</a></td>
<td>The net1 command is used to display, configure, and correct a wide variety of network settings. The net command should be used instead of the net1 command. The net1 command was made available in Windows NT and Windows 2000 as a temporary fix for a Y2K issue that the net command had, which was corrected before the release of Windows XP. The net1 command remains in later versions of Windows only for compatibility with older programs and scripts that utilized the command.</td>
</tr>
<tr>
<td>Netcfg</td>
<td>The netcfg command is used to install the Windows Preinstallation Environment (WinPE), a lightweight version of Windows used to deploy workstations.</td>
</tr>
<tr>
<td>Netsh</td>
<td>The netsh command is used to start Network Shell, a command-line utility used to manage the network configuration of the local, or a remote, computer.</td>
</tr>
<tr>
<td><a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/netstat-command-2618098">Netstat</a></td>
<td>The netstat command is most commonly used to display all open network connections and listening ports.</td>
</tr>
<tr>
<td>Nlsfunc</td>
<td>The nlsfunc command is used to load information specific to a particular country or region. The nlsfunc command is not available in 64-bit versions of Windows 8. Nlsfunc is only available in Windows 8 to support older MS-DOS files.</td>
</tr>
<tr>
<td>Nltest</td>
<td>The nltest command is used to test secure channels between Windows computers in a domain and between domain controllers that are trusting other domains.</td>
</tr>
<tr>
<td>Nslookup</td>
<td>The nslookup is most commonly used to display the hostname of an entered IP address. The nslookup command queries your configured DNS server to discover the IP address.</td>
</tr>
<tr>
<td>Ocsetup</td>
<td>The ocsetup command starts the Windows Optional Component Setup tool, used to install additional Windows features.</td>
</tr>
<tr>
<td>Openfiles</td>
<td>The openfiles command is used to display and disconnect open files and folders on a system.</td>
</tr>
<tr>
<td>Path</td>
<td>The path command is used to display or set a specific path available to executable files.</td>
</tr>
<tr>
<td>Pathping</td>
<td>The pathping command functions much like the tracert command but will also report information about network latency and loss at each <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-are-hops-hop-counts-2625905">hop</a>.</td>
</tr>
<tr>
<td>Pause</td>
<td>The pause command is used within a batch or script file to pause the processing of the file. When the pause command is used, a "Press any key to continue…" message displays in the command window.</td>
</tr>
<tr>
<td><a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/ping-command-2618099">Ping</a></td>
<td>The ping command sends an Internet Control Message Protocol (ICMP) Echo Request message to a specified remote computer to verify IP-level connectivity.</td>
</tr>
<tr>
<td>Pkgmgr</td>
<td>The pkgmgr command is used to start the Windows Package Manager from the Command Prompt. Package Manager installs, uninstalls, configures, and updates features and packages for Windows.</td>
</tr>
<tr>
<td>Pnpunattend</td>
<td>The pnpunattend command is used to automate the installation of <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/computer-hardware-2625895">hardware</a> device drivers.</td>
</tr>
<tr>
<td>Pnputil</td>
<td>The pnputil command is used to start the Microsoft PnP Utility, a tool used to install a Plug and Play device from the command line.</td>
</tr>
<tr>
<td>Popd</td>
<td>The popd command is used to change the current directory to the one most recently stored by the pushd command. The popd command is most often utilized from within a batch or script file.</td>
</tr>
<tr>
<td>Powercfg</td>
<td>The powercfg command is used to manage the Windows power management settings from the command line.</td>
</tr>
<tr>
<td>Print</td>
<td>The print command is used to print a specified text file to a specified printing device.</td>
</tr>
<tr>
<td>Prompt</td>
<td>The prompt command is used to customize the appearance of the prompt text in Command Prompt or MS-DOS.</td>
</tr>
<tr>
<td>Pushd</td>
<td>The pushd command is used to store a directory for use, most commonly from within a batch or script program.</td>
</tr>
<tr>
<td>Pwlauncher</td>
<td>The pwlauncher command is used to enable, disable, or show the status of your Windows To Go startup options.</td>
</tr>
<tr>
<td>Qappsrv</td>
<td>The qappsrv command is used to display all Remote Desktop Session Host servers available on the network.</td>
</tr>
<tr>
<td>Qprocess</td>
<td>The qprocess command is used to display information about running processes.</td>
</tr>
<tr>
<td>Query</td>
<td>The query command is used to display the status of a specified service.</td>
</tr>
<tr>
<td>Quser</td>
<td>The quser command is used to display information about users currently logged on to the system.</td>
</tr>
<tr>
<td>Qwinsta</td>
<td>The qwinsta command is used to display information about open Remote Desktop Sessions.</td>
</tr>
<tr>
<td>Rasautou</td>
<td>The rasautou command is used to manage Remote Access Dialer AutoDial addresses.</td>
</tr>
<tr>
<td>Rasdial</td>
<td>The rasdial command is used to start or end a network connection for a Microsoft client.</td>
</tr>
<tr>
<td>Rd</td>
<td>The rd command is the shorthand version of the rmdir command.</td>
</tr>
<tr>
<td>Reagentc</td>
<td>The reagentc command is used to configure the Windows Recovery Environment (RE).</td>
</tr>
<tr>
<td>Recover</td>
<td>The recover command is used to recover readable data from a bad or defective disk.</td>
</tr>
<tr>
<td>Reg</td>
<td>The reg command is used to manage the <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/windows-registry-2625992">Windows Registry</a> from the command line. The reg command can perform common registry functions like adding <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-is-a-registry-key-2625999">registry keys</a>, exporting the registry, etc.</td>
</tr>
<tr>
<td>Regini</td>
<td>The regini command is used to set or change registry permissions and <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-is-a-registry-value-2626042">registry values</a> from the command line.</td>
</tr>
<tr>
<td>Register-cimprovider</td>
<td>The register-cimprovider command is used to register a Common Information Model (CIM) Provider in Windows 8.</td>
</tr>
<tr>
<td>Regsvr32</td>
<td>The regsvr32 command is used to <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/regsvr32-what-it-is-how-to-register-dlls-2623958">register a DLL file</a> as a command component in the Windows Registry.</td>
</tr>
<tr>
<td>Relog</td>
<td>The relog command is used to create new performance logs from data in existing performance logs.</td>
</tr>
<tr>
<td>Rem</td>
<td>The rem command is used to record comments or remarks in a batch or script file.</td>
</tr>
<tr>
<td>Ren</td>
<td>The ren command is the shorthand version of the rename command.</td>
</tr>
<tr>
<td>Rename</td>
<td>The rename command is used to change the name of the individual file that you specify.</td>
</tr>
<tr>
<td>Repair-bde</td>
<td>The repair-bde command is used to repair or decrypt a damaged drive that's been encrypted using BitLocker.</td>
</tr>
<tr>
<td>Replace</td>
<td>The replace command is used to replace one or more files with one or more other files.</td>
</tr>
<tr>
<td>Reset</td>
<td>The reset command, executed as reset session, is used to reset the session subsystem software and hardware to known initial values.</td>
</tr>
<tr>
<td>Rmdir</td>
<td>The rmdir command is used to delete an existing or completely empty folder.</td>
</tr>
<tr>
<td>Robocopy</td>
<td>The robocopy command is used to copy files and directories from one location to another. This command is also called Robust File Copy. The robocopy command is superior to the both the copy command and the xcopy command because robocopy supports many more options.</td>
</tr>
<tr>
<td>Route</td>
<td>The route command is used to manipulate network routing tables.</td>
</tr>
<tr>
<td>Rpcping</td>
<td>The rpcping command is used to ping a server using RPC.</td>
</tr>
<tr>
<td>Runas</td>
<td>The runas command is used to execute a program using another user's credentials.</td>
</tr>
<tr>
<td>Rwinsta</td>
<td>The rwinsta command is the shorthand version of the reset session command.</td>
</tr>
<tr>
<td>Sc</td>
<td>The sc command is used to configure information about services. The sc command communicates with the Service Control Manager.</td>
</tr>
<tr>
<td>Schtasks</td>
<td>The schtasks command is used to schedule specified programs or commands to run a certain times. The schtasks command can be used to create, delete, query, change, run, and end scheduled tasks.</td>
</tr>
<tr>
<td>Sdbinst</td>
<td>The sdbinst command is used to deploy customized SDB database files.</td>
</tr>
<tr>
<td>Secedit</td>
<td>The secedit command is used to configure and analyze system security by comparing the current security configuration to a template.</td>
</tr>
<tr>
<td>Set</td>
<td>The set command is used to display, enable, or disable environment variables in MS-DOS or from the Command Prompt.</td>
</tr>
<tr>
<td>Setlocal</td>
<td>The setlocal command is used to start the localization of environment changes inside a batch or script file.</td>
</tr>
<tr>
<td>Setspn</td>
<td>The setspn command is used to manage the Service Principal Names (SPN) for an Active Directory (AD) service account.</td>
</tr>
<tr>
<td>Setver</td>
<td>The setver command is used to set the MS-DOS version number that MS-DOS reports to a program. The setver command is not available in 64-bit versions of Windows 8.</td>
</tr>
<tr>
<td>Setx</td>
<td>The setx command is used to create or change environment variables in the user environment or the system environment.</td>
</tr>
<tr>
<td><a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/sfc-command-system-file-checker-2626020">Sfc</a></td>
<td>The sfc command is used to verify and replace important Windows system files. The sfc command is also referred to as System File Checker or Windows Resource Checker depending on the <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/operating-systems-2625912">operating system</a>.</td>
</tr>
<tr>
<td>Share</td>
<td>The share command is used to install file locking and file sharing functions in MS-DOS. The share command is not available in 64-bit versions of Windows 8. Share is only available in Windows 8 to support older MS-DOS files.</td>
</tr>
<tr>
<td>Shift</td>
<td>The shift command is used to change the position of replaceable parameters in a batch or script file.</td>
</tr>
<tr>
<td><a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/shutdown-command-2618100">Shutdown</a></td>
<td>The shutdown command can be used to shut down, restart, or log off the current system or a remote computer.</td>
</tr>
<tr>
<td>Sort</td>
<td>The sort command is used to read data from a specified input, sort that data, and return the results of that sort to the Command Prompt screen, a file, or another output device.</td>
</tr>
<tr>
<td>Start</td>
<td>The start command is used to open a new command line window to run a specified program or command. The start command can also be used to start an application without creating a new window.</td>
</tr>
<tr>
<td>Subst</td>
<td>The subst command is used to associate a local path with a drive letter. The subst command is a lot like the net use command except a local path is used instead of a shared network path.</td>
</tr>
<tr>
<td>Sxstrace</td>
<td>The sxstrace command is used to start the WinSxs Tracing Utility, a programming diagnostic tool.</td>
</tr>
<tr>
<td>Systeminfo</td>
<td>The systeminfo command is used to display basic Windows configuration information for the local or a remote computer.</td>
</tr>
<tr>
<td>Takeown</td>
<td>The takedown command is used to regain access to a file that that an administrator was denied access to when reassigning ownership of the file.</td>
</tr>
<tr>
<td>Taskkill</td>
<td>The taskkill command is used to terminate a running task. The taskkill command is the command line equivalent of <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/how-to-force-quit-a-program-in-windows-2625781">ending a process in Task Manager</a> in Windows.</td>
</tr>
<tr>
<td>Tasklist</td>
<td>Displays a list of applications, services, and the Process ID (PID) currently running on either a local or a remote computer.</td>
</tr>
<tr>
<td>Tcmsetup</td>
<td>The tcmsetup command is used to setup or disable the Telephony Application Programming Interface (TAPI) client.</td>
</tr>
<tr>
<td>Telnet</td>
<td>The telnet command is used to communicate with remote computers that use the <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-is-telnet-2626026">Telnet protocol</a>. The telnet command is not available by default in Windows 8 but can be enabled by turning on the Telnet Client Windows feature from Programs and Features in Control Panel.</td>
</tr>
<tr>
<td>Tftp</td>
<td>The tftp command is used to transfer files to and from a remote computer that's running the Trivial File Transfer Protocol (TFTP) service or daemon. The tftp command is not available by default in Windows 8 but can be enabled by turning on the TFTP Client Windows feature from Programs and Features in Control Panel.</td>
</tr>
<tr>
<td>Time</td>
<td>The time command is used to show or change the current time.</td>
</tr>
<tr>
<td>Timeout</td>
<td>The timeout command is typically used in a batch or script file to provide a specified timeout value during a procedure. The timeout command can also be used to ignore keypresses.</td>
</tr>
<tr>
<td>Title</td>
<td>The title command is used to set the Command Prompt window title.</td>
</tr>
<tr>
<td>Tlntadmn</td>
<td>The tlntadmn command is used to administer a local or remote computer running Telnet Server. The tlntadmn command is not available by default in Windows 8 but can be enabled by turning on the Telnet Server Windows feature from Programs and Features in Control Panel.</td>
</tr>
<tr>
<td>Tpmvscmgr</td>
<td>The tpmvscmgr command is used to create and destroy TPM virtual smart cards.</td>
</tr>
<tr>
<td>Tracerpt</td>
<td>The tracerpt command is used to process event trace logs or real-time data from instrumented event trace providers.</td>
</tr>
<tr>
<td><a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/tracert-command-2618101">Tracert</a></td>
<td>The tracert command sends Internet Control Message Protocol (ICMP) Echo Request messages to a specified remote computer with increasing Time to Live (TTL) field values and displays the IP address and hostname, if available, of the <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/what-is-a-router-2618162">router</a> interfaces between the source and destination.</td>
</tr>
<tr>
<td>Tree</td>
<td>The tree command is used to graphically display the folder structure of a specified drive or path.</td>
</tr>
<tr>
<td>Tscon</td>
<td>The tscon command is used to attach a user session to a Remote Desktop session.</td>
</tr>
<tr>
<td>Tsdiscon</td>
<td>The tsdiscon command is used to disconnect a Remote Desktop session.</td>
</tr>
<tr>
<td>Tskill</td>
<td>The tskill command is used to end the specified process.</td>
</tr>
<tr>
<td>Type</td>
<td>The type command is used to display the information contained in a text file.</td>
</tr>
<tr>
<td>Typeperf</td>
<td>The typerperf command displays performance data in the Command Prompt window or writes the data to specified log file.</td>
</tr>
<tr>
<td>Tzutil</td>
<td>The tzutil command is used to display or configure the current system's time zone. The tzutil command can also be used to enable or disable Daylight Saving Time adjustments.</td>
</tr>
<tr>
<td>Unlodctr</td>
<td>The unlodctr command removes Explain text and Performance counter names for a service or device driver from the Windows Registry.</td>
</tr>
<tr>
<td>Vaultcmd</td>
<td>The vaultcmd command is used to create, remove, and show stored credentials.</td>
</tr>
<tr>
<td>Ver</td>
<td>The ver command is used to display the current Windows or MS-DOS <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/version-number-2626043">version number</a>.</td>
</tr>
<tr>
<td>Verify</td>
<td>The verify command is used to enable or disable the ability of Command Prompt, or MS-DOS, to verify that files are written correctly to a disk.</td>
</tr>
<tr>
<td><a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/vol-command-2618102">Vol</a></td>
<td>The vol command shows the <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/volume-label-2626045">volume label</a> and <a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/serial-number-2626008">serial number</a> of a specified disk, assuming this information exists.</td>
</tr>
<tr>
<td>Vssadmin</td>
<td>The vssadmin command starts the Volume Shadow Copy Service administrative command line tool which displays current volume shadow copy backups and all installed shadow copy writers and providers.</td>
</tr>
<tr>
<td>W32tm</td>
<td>The w32tm command is used to diagnose issues with Windows Time.</td>
</tr>
<tr>
<td>Waitfor</td>
<td>The waitfor command is used to send or wait for a signal on a system.</td>
</tr>
<tr>
<td>Wbadmin</td>
<td>The wbadmin command is used start and stop backup jobs, display details about a previous backup, list the items within a backup, and report on the status of a currently running backup.</td>
</tr>
<tr>
<td>Wecutil</td>
<td>The wecutil command is used to mange subscriptions to events that are forwarded from WS-Management supported computers.</td>
</tr>
<tr>
<td>Wevtutil</td>
<td>The wevtutil command starts the Windows Events Command Line Utility which is used to manage event logs and publishers.</td>
</tr>
<tr>
<td>Where</td>
<td>The where command is used to search for files that match a specified pattern.</td>
</tr>
<tr>
<td>Whoami</td>
<td>The whoami command is used to retrieve user name and group information on a network.</td>
</tr>
<tr>
<td>Winrm</td>
<td>The winrm command is used to start the command line version of Windows Remote Management, used to manage secure communications with local and remote computers using web services.</td>
</tr>
<tr>
<td>Winrs</td>
<td>The winrs command is used to open a secure command window with a remote host.</td>
</tr>
<tr>
<td>Winsat</td>
<td>The winsat command starts the Windows System Assessment Tool, a program that assesses various features, attributes, and capabilities of a computer running Windows.</td>
</tr>
<tr>
<td>Wmic</td>
<td>The wmic command starts the Windows Management Instrumentation Command line (WMIC), a scripting interface that simplifies the use of Windows Management Instrumentation (WMI) and systems managed via WMI.</td>
</tr>
<tr>
<td>Wsmanhttpconfig</td>
<td>The wsmanhttpconfig command is used to manage aspects of the Windows Remote Management (WinRM) service.</td>
</tr>
<tr>
<td><a class="CMY_Link CMY_Valid" href="https://www.lifewire.com/xcopy-command-2618103">Xcopy</a></td>
<td>The xcopy command can copy one or more files or directory trees from one location to another. The xcopy command is generally considered a more "powerful" version of the copy command though the robocopy command trumps even xcopy. A command by the name of xcopy32 existed in Windows 95 and Windows 98. To avoid a long and confusing explanation here, just know that no matter if you executed the xcopy command or the xcopy32 command, you were always executing the most updated version of the command.</td>
</tr>
<tr>
<td>Xwizard</td>
<td>The xwizard command, short for Extensible Wizard, is used to register data in Windows, often from a preconfigured XML file.</td>
</tr>
</tbody>
</table>


## [lifewire Full list of CMD](https://www.lifewire.com/list-of-command-prompt-commands-4092302)

Windows的命令行提示符提供了了超过280条命令！这些命令用于在命令行执行操作系统任务而不是图形窗口页面。

命令行提示符命令让你从不同的文件夹复制文件，格式化整个磁盘，复制文件，给其他电脑发送信息，重启电脑，等等。同样有些[命令行技巧与hacks](https://www.lifewire.com/command-prompt-tricks-and-hacks-2618104)利用这些命令。

下表包含了win10,8,8,Vista,XP等系统的命令，同样包含了MS-DOS命令。

以下是我从 <https://lifewire.com> 复制的完整的win10命令行列表。

<table class="mntl-sc-block-table__table">
<colgroup style="" span="1"></colgroup>
<colgroup style="" span="1"></colgroup>
<thead>
<tr>
<th colspan="2" class="mntl-sc-block-table__title">Full List of Command Prompt Commands</th>
</tr>
</thead>
<tbody data-check="-1">
<tr>
<td><strong>Command</strong></td>
<td><strong>Description</strong></td>
</tr>
<tr>
<td>Append</td>
<td>The append command can be used by programs to open <a href="https://www.lifewire.com/what-is-a-file-2625878">files</a> in another directory as if they were located in the current directory. The append command is available in MS-DOS as well as in all <a href="https://www.lifewire.com/32-bit-64-bit-2624554">32-bit</a> versions of Windows. The append command is not available in <a href="https://www.lifewire.com/32-bit-64-bit-2624554">64-bit</a> versions of Windows.</td>
</tr>
<tr>
<td>Arp</td>
<td>The arp command is used to display or change entries in the ARP cache. The arp command is available in all versions of Windows.</td>
</tr>
<tr>
<td>Assoc</td>
<td>The assoc command is used to display or change the file type associated with a particular <a href="https://www.lifewire.com/what-is-a-file-extension-2625879">file extension</a>. The assoc command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/at-command-2618090">At</a></td>
<td>The at command is used to schedule commands and other programs to run at a specific date and time. The at command is available in Windows 7, Windows Vista, and Windows XP. Beginning in Windows 8, command line task scheduling should instead be completed with the schtasks command.</td>
</tr>
<tr>
<td>Atmadm</td>
<td>The atmadm command is used to display information related to asynchronous transfer mode (ATM) connections on the system. The atmadm command is available in Windows XP. Support for ATM was removed beginning in Windows Vista, making the atmadm command unnecessary.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/attrib-command-2625802">Attrib</a></td>
<td>The attrib command is used to change the <a href="https://www.lifewire.com/what-is-a-file-attribute-2625793">attributes</a> of a single file or a directory. The attrib command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Auditpol</td>
<td>The auditpol command is used to display or change audit policies. The auditpol command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Bcdboot</td>
<td>The bcdboot command is used to copy <a href="https://www.lifewire.com/what-does-booting-mean-2625799">boot</a> files to the system <a href="https://www.lifewire.com/what-is-a-partition-2625958">partition</a> and to create a new system BCD store. The bcdboot command is available in Windows 8 and Windows 7.</td>
</tr>
<tr>
<td>Bcdedit</td>
<td>The bcdedit command is used to view or make changes to Boot Configuration Data. The bcdedit command is available in Windows 8, Windows 7, and Windows Vista. The bcdedit command replaced the bootcfg command beginning in Windows Vista.</td>
</tr>
<tr>
<td>Bdehdcfg</td>
<td>The bdehdcfg command is used to prepare a <a href="https://www.lifewire.com/what-is-a-hard-disk-drive-2618152">hard drive</a> for BitLocker Drive Encryption. The bdehdcfg command is available in Windows 8 and Windows 7.</td>
</tr>
<tr>
<td>Bitsadmin</td>
<td>The bitsadmin command is used to create, manage, and monitor download and upload jobs. The bitsadmin command is available in Windows 8, Windows 7, and Windows Vista. While the bitsadmin command is available in both Windows 8 and Windows 7, it is being phased out. The BITS PowerShell cmdlets should be used instead.</td>
</tr>
<tr>
<td>Bootcfg</td>
<td>The bootcfg command is used to build, modify, or view the contents of the boot.ini file, a <a href="https://www.lifewire.com/what-is-a-hidden-file-2625898">hidden file</a> that is used to identify in what folder, on which partition, and on which hard drive Windows is located. The bootcfg command is available in Windows 8, Windows 7, Windows Vista, and Windows XP. The bootcfg command was replaced by the bcdedit command beginning in Windows Vista. Bootcfg is still available in Windows 8, 7, and Vista, but it serves no real value since boot.ini is not used in these <a href="https://www.lifewire.com/operating-systems-2625912">operating systems</a>.</td>
</tr>
<tr>
<td>Bootsect</td>
<td>The bootsect command is used to configure the <a href="https://www.lifewire.com/what-is-the-master-boot-code-2625934">master boot code</a> to one compatible with <a href="https://www.lifewire.com/windows-boot-manager-bootmgr-2625813">BOOTMGR</a> (Vista and later) or <a href="https://www.lifewire.com/what-is-ntldr-2625949">NTLDR</a> (XP and earlier). The bootsect command is available in Windows 8. The bootsect command is also available in Windows 7 and Windows Vista but only from the Command Prompt available in <a href="https://www.lifewire.com/system-recovery-options-2626021">System Recovery Options</a>.</td>
</tr>
<tr>
<td>Break</td>
<td>The break command sets or clears extended <a href="https://www.lifewire.com/what-is-ctrl-c-used-for-2625834">CTRL + C</a> checking on DOS systems. The break command is available in all versions of Windows, as well as in MS-DOS. The break command is available in Windows XP and later versions of Windows to provide compatibility with MS-DOS files but it has no effect in Windows itself.</td>
</tr>
<tr>
<td>Cacls</td>
<td>The cacls command is used to display or change access control lists of files. The cacls command is available in Windows 8, Windows 7, Windows Vista, and Windows XP. The cacls command is being phased out in favor of the icacls command, which should be used instead in all versions of Windows after Windows XP.</td>
</tr>
<tr>
<td>Call</td>
<td>The call command is used to run a script or batch program from within another script or batch program. The call command is available in all versions of Windows, as well as in MS-DOS. The call command has no effect outside of a script or <a href="https://www.lifewire.com/bat-file-2619796">batch file</a>. In other words, running the call command at the Command Prompt or MS-DOS prompt will do nothing.</td>
</tr>
<tr>
<td>Cd</td>
<td>The cd command is the shorthand version of the chdir command. The cd command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Certreq</td>
<td>The certreq command is used to perform various certification authority (CA) certificate functions. The certreq command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Certutil</td>
<td>The certutil command is used to dump and display certification authority (CA) configuration information in addition to other CA functions. The certutil command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Change</td>
<td>The change command changes various terminal server settings like install modes, COM port mappings, and logons. The change command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Chcp</td>
<td>The chcp command displays or configures the active code page number. The chcp command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Chdir</td>
<td>The chdir command is used to display the drive letter and folder that you are currently in. Chdir can also be used to change the drive and/or directory that you want to work in. The chdir command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Checknetisolation</td>
<td>The checknetisolation command is used to test apps that require network capabilities. The checknetisolation command is available in Windows 8.</td>
</tr>
<tr>
<td>Chglogon</td>
<td>The chglogon command enables, disables, or drains terminal server session logins. The chglogon command is available in Windows 8, Windows 7, and Windows Vista. Executing the chglogon command is the same as executing <em>change logon</em>.</td>
</tr>
<tr>
<td>Chgport</td>
<td>The chgport command can be used to display or change COM port mappings for DOS compatibility. The chgport command is available in Windows 8, Windows 7, and Windows Vista. Executing the chgport command is the same as executing <em>change port</em>.</td>
</tr>
<tr>
<td>Chgusr</td>
<td>The chgusr command is used to change the install mode for the terminal server. The chgusr command is available in Windows 8, Windows 7, and Windows Vista. Executing the chgusr command is the same as executing <em>change user</em>.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/chkdsk-command-2625838">Chkdsk</a></td>
<td>The chkdsk command, often referred to as check disk, is used to identify and correct certain hard drive errors. The chkdsk command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Chkntfs</td>
<td>The chkntfs command is used to configure or display the checking of the disk drive during the Windows boot process. The chkntfs command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Choice</td>
<td>The choice command is used within a script or batch program to provide a list of choices and return the value of that choice to the program. The choice command is available in MS-DOS and all versions of Windows except Windows XP. Use the set command with the /p switch in place of the choice command in batch files and scripts that you plan to use in Windows XP.</td>
</tr>
<tr>
<td>Cipher</td>
<td>The cipher command shows or changes the <a href="https://www.lifewire.com/file-storage-encryption-2625875">encryption</a> status of files and folders on <a href="https://www.lifewire.com/ntfs-file-system-2625948">NTFS</a> partitions. The cipher command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Clip</td>
<td>The clip command is used to redirect the output from any command to the clipboard in Windows. The clip command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Cls</td>
<td>The cls command clears the screen of all previously entered commands and other text. The cls command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Cmd</td>
<td>The cmd command starts a new instance of the cmd.exe <a href="https://www.lifewire.com/what-is-a-command-line-interpreter-2625827">command interpreter</a>. The cmd command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Cmdkey</td>
<td>The cmdkey command is used to show, create, and remove stored user names and passwords. The cmdkey command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Cmstp</td>
<td>The cmstp command installs or uninstalls a Connection Manager service profile. The cmstp command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Color</td>
<td>The color command is used to change the colors of the text and background within the Command Prompt window. The color command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Command</td>
<td>The command command starts a new instance of the command.com command interpreter. The command command is available in MS-DOS as well as in all 32-bit versions of Windows. The command command is not available in 64-bit versions of Windows.</td>
</tr>
<tr>
<td>Comp</td>
<td>The comp command is used to compare the contents of two files or sets of files. The comp command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Compact</td>
<td>The compact command is used to show or change the <a href="https://www.lifewire.com/what-is-a-compressed-file-2625829">compression</a> state of files and directories on NTFS partitions. The compact command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Convert</td>
<td>The convert command is used to convert <a href="https://www.lifewire.com/what-is-file-allocation-table-fat-2625877">FAT or FAT32</a> formatted volumes to the NTFS format. The convert command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/copy-command-2625842">Copy</a></td>
<td>The copy command does simply that — it <a href="https://www.lifewire.com/how-do-i-copy-a-file-in-windows-2619210">copies one or more files</a> from one location to another. The copy command is available in all versions of Windows, as well as in MS-DOS. The xcopy command is considered to be a more "powerful" version of the copy command.</td>
</tr>
<tr>
<td>Cscript</td>
<td>The cscript command is used to execute scripts via Microsoft Script Host. The cscript command is available in all versions of Windows. The cscript command is most popularly used to manage printers from the command line using scripts like prncnfg.vbs, prndrvr.vbs, prnmngr.vbs, and others.</td>
</tr>
<tr>
<td>Ctty</td>
<td>The ctty command is used to change the default input and output devices for the system. The ctty command is available in Windows 98 and 95 as well as in MS-DOS. The functions provided by the ctty command were no longer necessary beginning in Windows XP because the command.com interpreter (MS-DOS) is no longer the default command line interpreter.</td>
</tr>
<tr>
<td>Date</td>
<td>The date command is used to show or change the current date. The date command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Dblspace</td>
<td>The dblspace command is used to create or configure DoubleSpace compressed drives. The dblspace command is available in Windows 98 and 95, as well as in MS-DOS. DriveSpace, executed using the drvspace command, is an updated version of DoubleSpace. Windows natively handles compression beginning in Windows XP.</td>
</tr>
<tr>
<td>Debug</td>
<td>The debug command starts Debug, a command line application used to test and edit programs. The debug command is available in MS-DOS as well as in all 32-bit versions of Windows. The debug command is not available in 64-bit versions of Windows.</td>
</tr>
<tr>
<td>Defrag</td>
<td>The defrag command is used to <a href="https://www.lifewire.com/what-is-fragmentation-defragmentation-2625884">defragment</a> a drive you specify. The defrag command is the command line version of Microsoft's Disk Defragmenter. The defrag command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/delete-command-2625859">Del</a></td>
<td>The del command is used to delete one or more files. The del command is available in all versions of Windows, as well as in MS-DOS. The del command is the same as the erase command.</td>
</tr>
<tr>
<td>Deltree</td>
<td>The deltree command is used to delete a directory and all the files and subdirectories within it. The deltree command is available in Windows 98 and 95, as well as in MS-DOS. Beginning in Windows XP, a folder and its files and subfolders can be removed using the /s function of the rmdir command. Deltree was no longer needed with this new rmdir ability so the command was removed.</td>
</tr>
<tr>
<td>Diantz</td>
<td>The diantz command is used to losslessly compress one or more files. The diantz command is sometimes called Cabinet Maker. The diantz command is available in Windows 7, Windows Vista, and Windows XP. The diantz command is the same as the makecab command.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/dir-command-4050018">Dir</a></td>
<td>The dir command is used to display a list of files and folders contained inside the folder that you are currently working in. The dir command also displays other important information like the hard drive's <a href="https://www.lifewire.com/serial-number-2626008">serial number</a>, the total number of files listed, their combined size, the total amount of <a href="https://www.lifewire.com/how-to-check-free-hard-drive-space-in-windows-2619187">free space left on the drive</a>, and more. The dir command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Diskcomp</td>
<td>The diskcomp command is used to compare the contents of two floppy disks. The diskcomp command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Diskcopy</td>
<td>The diskcopy command is used to copy the entire contents of one floppy disk to another. The diskcopy command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Diskpart</td>
<td>The diskpart command is used to create, manage, and delete hard drive partitions. The diskpart command is available in Windows 8, Windows 7, Windows Vista, and Windows XP. The diskpart command replaced the fdisk command beginning in Windows XP.</td>
</tr>
<tr>
<td>Diskperf</td>
<td>The diskperf command is used to manage disk performance counters remotely. The diskperf command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Diskraid</td>
<td>The diskraid command starts the DiskRAID tool which is used to manage and configure RAID arrays. The diskraid command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Dism</td>
<td>The dism command starts the Deployment Image Servicing and Management tool (DISM). The DISM tool is used to manage features in Windows images. The dism command is available in Windows 8 and Windows 7.</td>
</tr>
<tr>
<td>Dispdiag</td>
<td>The dispdiag command is used to output a log of information about the display system. The dispdiag command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Djoin</td>
<td>The djoin command is used to create a new computer account in a domain. The djoin command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Doskey</td>
<td>The doskey command is used to edit command lines, create macros, and recall previously entered commands. The doskey command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Dosshell</td>
<td>The dosshell command starts DOS Shell, a graphical file management tool for MS-DOS. The dosshell command is available in Windows 95 (in MS-DOS mode) and also in MS-DOS version 6.0 and later MS-DOS versions that were upgraded from previous versions that contained the dosshell command. A graphical file manager, Windows Explorer, became an integrated part of the operating system beginning in Windows 95.</td>
</tr>
<tr>
<td>Dosx</td>
<td>The dosx command is used to start DOS Protected Mode Interface (DPMI), a special mode designed to give MS-DOS applications access to more than the normally allowed 640 KB. The dosx command is available in Windows 8, Windows 7, Windows Vista, and Windows XP. The dosx command is not available in 64-bit versions of Windows. The dosx command and DPMI is only available in Windows to support older MS-DOS programs.</td>
</tr>
<tr>
<td>Driverquery</td>
<td>The driverquery command is used to show a list of all installed <a href="https://www.lifewire.com/what-is-a-device-driver-2625796">drivers</a>. The driverquery command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Drvspace</td>
<td>The drvspace command is used to create or configure DriveSpace compressed drives. The drvspace command is available in Windows 98 and 95, as well as in MS-DOS. DriveSpace is an updated version of DoubleSpace, executed using the dblspace command. Windows natively handles compression beginning in Windows XP.</td>
</tr>
<tr>
<td>Echo</td>
<td>The echo command is used to show messages, most commonly from within script or batch files. The echo command can also be used to turn the echoing feature on or off. The echo command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Edit</td>
<td>The edit command starts the MS-DOS Editor tool which is used to create and modify <a href="https://www.lifewire.com/txt-text-file-4150707">text files</a>. The edit command is available in MS-DOS as well as in all 32-bit versions of Windows. The edit command is not available in 64-bit versions of Windows.</td>
</tr>
<tr>
<td>Edlin</td>
<td>The edlin command starts the Edlin tool which is used to create and modify text files from the command line. The edlin command is available in all 32-bit versions of Windows but is not available in 64-bit versions of Windows. In MS-DOS, the edlin command is only available up to MS-DOS 5.0, so unless your later version of MS-DOS was upgraded from 5.0 or prior, you won't see the edlin command.</td>
</tr>
<tr>
<td>Emm386</td>
<td>The emm386 command is used to give MS-DOS access to more than 640 KB of <a href="https://www.lifewire.com/what-is-random-access-memory-ram-2618159">memory</a>. The emm386 command is available in Windows 98 and 95, as well as in MS-DOS. Windows itself has access to extended and expanded memory beginning in Windows 95.</td>
</tr>
<tr>
<td>Endlocal</td>
<td>The endlocal command is used to end the localization of environment changes inside a batch or script file. The endlocal command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Erase</td>
<td>The erase command is used to delete one or more files. The erase command is available in all versions of Windows, as well as in MS-DOS. The erase command is the same as the del command.</td>
</tr>
<tr>
<td>Esentutl</td>
<td>The esentutl command is used to manage Extensible Storage Engine databases. The esentutl command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Eventcreate</td>
<td>The eventcreate command is used to create a custom event in an event log. The eventcreate command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Eventtriggers</td>
<td>The eventtriggers command is used to configure and display event triggers. The eventtriggers command is available in Windows XP. Beginning in Windows Vista, event triggers are created using the Attach Task To This Event feature in Event Viewer, making the eventtriggers command unnecessary.</td>
</tr>
<tr>
<td>Exe2bin</td>
<td>The exe2bin command is used to convert a file of the <a href="https://www.lifewire.com/exe-file-2622732">EXE</a> file type (<a href="https://www.lifewire.com/list-of-executable-file-extensions-2626061">executable file</a>) to a binary file. The exe2bin command is available in 32-bit versions of Windows 8, Windows 7, Windows Vista, and Windows XP. The exe2bin command is not available in any 64-bit version of Windows.</td>
</tr>
<tr>
<td>Exit</td>
<td>The exit command is used to end the cmd.exe (Windows) or command.com (MS-DOS) session that you're currently working in. The exit command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Expand</td>
<td>The expand command is used to extract the files and folders contained in Microsoft Cabinet (<a href="https://www.lifewire.com/cab-file-4144227">CAB</a>) files. The expand command is available in MS-DOS as well as in all versions of Windows. The expand command is not available in the 64-bit version of Windows XP.</td>
</tr>
<tr>
<td>Extrac32</td>
<td>The extrac32 command is used to extract the files and folders contained in Microsoft Cabinet (CAB) files. The extrac32 command is available in all versions of Windows. The extrac32 command is actually a CAB extraction program for use by Internet Explorer but can be used to extract any Microsoft Cabinet file. Use the expand command instead of the extrac32 command if possible.</td>
</tr>
<tr>
<td>Extract</td>
<td>The extract command is used to extract the files and folders contained in Microsoft Cabinet (CAB) files. The extract command is available in Windows 98 and 95. The extract command was replaced by the expand command beginning in Windows XP.</td>
</tr>
<tr>
<td>Fasthelp</td>
<td>The fasthelp command provides more detailed information on any of the other MS-DOS commands. The fasthelp command is only available in MS-DOS. The help command replaced the fasthelp command beginning in Windows 95.</td>
</tr>
<tr>
<td>Fastopen</td>
<td>The fastopen command is used to add a program's hard drive location to a special list stored in memory, potentially improving the program's launch time by removing the need for MS-DOS to locate the application on the drive. The fastopen command is available in MS-DOS as well as in all 32-bit versions of Windows. The fastopen command is not available in 64-bit versions of Windows. Fastopen is only available in Windows 8, 7, Vista, and XP to support older MS-DOS files.</td>
</tr>
<tr>
<td>Fc</td>
<td>The fc command is used to compare two individual or sets of files and then show the differences between them. The fc command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Fdisk</td>
<td>The fdisk command is used to create, manage, and delete hard drive partitions. The fdisk command is available in Windows 98 and 95, as well as in MS-DOS. The fdisk command was replaced by the diskpart command beginning in Windows XP. Partition management is also available from <a href="https://www.lifewire.com/disk-management-2625863">Disk Management</a> in Windows 8, 7, Vista, and XP.</td>
</tr>
<tr>
<td>Find</td>
<td>The find command is used to search for a specified text string in one or more files. The find command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Findstr</td>
<td>The findstr command is used to find text string patterns in one or more files. The findstr command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Finger</td>
<td>The finger command is used to return information about one or more users on a remote computer that's running the Finger <a href="https://www.lifewire.com/what-is-a-service-4107276">service</a>. The finger command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Fltmc</td>
<td>The fltmc command is used to load, unload, list, and otherwise manage Filter drivers. The fltmc command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Fondue</td>
<td>The fondue command, short for Features on Demand User Experience Tool, is used to install any of the several optional Windows features from the command line. The fondue command is available in Windows 8. Optional Windows features can also be installed from the Programs and Features <a href="https://www.lifewire.com/control-panel-applet-2625831">applet</a> in <a href="https://www.lifewire.com/control-panel-2625841">Control Panel</a>.</td>
</tr>
<tr>
<td>For</td>
<td>The for command is used to run a specified command for each file in a set of files. The for command is most often used within a batch or script file. The for command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Forcedos</td>
<td>The forcedos command is used to start the specified program in the MS-DOS subsystem. The forcedos command is only available in 32-bit versions of Windows XP. The forcedos command is only used for MS-DOS programs that are not recognized as such by Windows XP.</td>
</tr>
<tr>
<td>Forfiles</td>
<td>The forfiles command selects one or more files to execute a specified command on. The forfiles command is most often used within a batch or script file. The forfiles command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/format-command-2618091">Format</a></td>
<td>The format command is used to <a href="https://www.lifewire.com/what-does-it-mean-to-format-something-2625882">format</a> a drive in the <a href="https://www.lifewire.com/what-is-a-file-system-2625880">file system</a> that you specify. The format command is available in all versions of Windows, as well as in MS-DOS. Drive formatting is also available from Disk Management in Windows 8, 7, Vista, and XP.</td>
</tr>
<tr>
<td>Fsutil</td>
<td>The fsutil command is used to perform various FAT and NTFS file system tasks like managing reparse points and sparse files, dismounting a volume, and extending a volume. The fsutil command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Ftp</td>
<td>The ftp command can be used to transfer files to and from another computer. The remote computer must be operating as an FTP server. The ftp command is available in all versions of Windows.</td>
</tr>
<tr>
<td>Ftype</td>
<td>The ftype command is used to define a default program to open a specified file type. The ftype command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Getmac</td>
<td>The getmac command is used to display the media access control (MAC) address of all the network controllers on a system. The getmac command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Goto</td>
<td>The goto command is used in a batch or script file to direct the command process to a labeled line in the script. The goto command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Gpresult</td>
<td>The gpresult command is used to display Group Policy settings. The gpresult command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Gpupdate</td>
<td>The gpupdate command is used to update Group Policy settings. The gpupdate command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Graftabl</td>
<td>The graftabl command is used to enable the ability of Windows to display an extended character set in graphics mode. The graftabl command is available in all versions of Windows and in MS-DOS up to version 5.0. The graftabl command is not available in 64-bit versions of Windows.</td>
</tr>
<tr>
<td>Graphics</td>
<td>The graphics command is used to load a program that can print graphics. The graphics command is available in MS-DOS as well as in all 32-bit versions of Windows. The graphics command is not available in 64-bit versions of Windows.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/help-command-2618092">Help</a></td>
<td>The help command provides more detailed information on any of the other Command Prompt or MS-DOS commands. The help command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Hostname</td>
<td>The <a href="https://www.lifewire.com/what-is-a-hostname-2625906">hostname</a> command displays the name of the current host. The hostname command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Hwrcomp</td>
<td>The hwrcomp command is used to compile custom dictionaries for handwriting recognition. The hwrcomp command is available in Windows 8 and Windows 7.</td>
</tr>
<tr>
<td>Hwrreg</td>
<td>The hwrreg command is used to install a previously compiled custom dictionary for handwriting recognition. The hwrreg command is available in Windows 8 and Windows 7.</td>
</tr>
<tr>
<td>Icacls</td>
<td>The icacls command is used to display or change access control lists of files. The icacls command is available in Windows 8, Windows 7, and Windows Vista. The icacls command is an updated version of the cacls command.</td>
</tr>
<tr>
<td>If</td>
<td>The if command is used to perform conditional functions in a batch file. The if command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Interlnk</td>
<td>The interlnk command is used to connect two computers via a serial or parallel connection to share files and printers. The interlnk command is only available in MS-DOS. The ability to directly connect two computers is handled by the networking functions in all versions of Windows.</td>
</tr>
<tr>
<td>Intersvr</td>
<td>The intersvr command is used to start the Interlnk server and to copy Interlnk files from one computer to another. The intersvr command is only available in MS-DOS. The ability to directly connect two computers is handled by the networking functions in all versions of Windows.</td>
</tr>
<tr>
<td>Ipconfig</td>
<td>The ipconfig command is used to display detailed IP information for each network adapter utilizing TCP/IP. The ipconfig command can also be used to release and renew <a href="https://www.lifewire.com/what-is-an-ip-address-2625920">IP addresses</a> on systems configured to receive them via a <a href="https://www.lifewire.com/what-is-dhcp-2625848">DHCP</a> server. The ipconfig command is available in all versions of Windows.</td>
</tr>
<tr>
<td>Ipxroute</td>
<td>The ipxroute command is used to display and change information about IPX routing tables. The ipxroute command is available in Windows XP. Microsoft removed their native NetWare client beginning in Windows Vista, removing the associated ipxroute command as well.</td>
</tr>
<tr>
<td>Irftp</td>
<td>The irftp command is used to transmit files over an infrared link. The irftp command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Iscsicli</td>
<td>The iscsicli command starts the Microsoft iSCSI Initiator, used to manage iSCSI. The iscsicli command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Kb16</td>
<td>The kb16 command is used to support MS-DOS files that need to configure a <a href="https://www.lifewire.com/what-is-a-keyboard-2618153">keyboard</a> for a specific language. The kb16 command is available in Windows 8, Windows 7, Windows Vista, and Windows XP. The kb16 command is not available in 64-bit versions of Windows. The kb16 command replaced the keyb command beginning in Windows XP but only exists to support older MS-DOS files.</td>
</tr>
<tr>
<td>Keyb</td>
<td>The keyb command is used to configure a keyboard for a specific language. The keyb command is available in Windows 98 and 95, as well as in MS-DOS. See the kb16 command for an equivalent command in later versions of Windows. Keyboard language settings are handled by the Region and Language or Regional and Language Options (depending on the version of Windows) Control Panel applets in Windows beginning in Windows XP.</td>
</tr>
<tr>
<td>Klist</td>
<td>The klist command is used to list Kerberos service tickets. The klist command can also be used to purge Kerberos tickets. The klist command is available in Windows 8 and Windows 7.</td>
</tr>
<tr>
<td>Ksetup</td>
<td>The ksetup command is used to configure connections to a Kerberos server. The ksetup command is available in Windows 8 and Windows 7.</td>
</tr>
<tr>
<td>Ktmutil</td>
<td>The ktmutil command starts the Kernel Transaction Manager utility. The ktmutil command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Label</td>
<td>The label command is used to manage the volume label of a disk. The label command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Lh</td>
<td>The lh command is the shorthand version of the loadhigh command. The lh command is available in Windows 98 and 95, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Licensingdiag</td>
<td>The licensingdiag command is a tool used to generate a text-based log and other data files that contain <a href="https://www.lifewire.com/what-is-product-activation-2625971">product activation</a> and other Windows licensing information. The licensingdiag command is available in Windows 8.</td>
</tr>
<tr>
<td>Loadfix</td>
<td>The loadfix command is used to load the specified program in the first 64K of memory and then runs the program. The loadfix command is available in MS-DOS as well as in all 32-bit versions of Windows. The loadfix command is not available in 64-bit versions of Windows.</td>
</tr>
<tr>
<td>Loadhigh</td>
<td>The loadhigh command is used to load a program into high memory and is usually used from within the autoexec.bat file. The loadhigh command is available in Windows 98 and 95, as well as in MS-DOS. Memory usage is handled automatically beginning in Windows XP.</td>
</tr>
<tr>
<td>Lock</td>
<td>The lock command is used to lock a drive, enabling direct disk access for a program. The lock command is only available in Windows 98 and 95. Drive locking is no longer available as of Windows XP.</td>
</tr>
<tr>
<td>Lodctr</td>
<td>The lodctr command is used to update <a href="https://www.lifewire.com/what-is-a-registry-value-2626042">registry values</a> related to performance counters. The lodctr command is available in all versions of Windows.</td>
</tr>
<tr>
<td>Logman</td>
<td>The logman command is used to create and manage Event Trace Session and Performance logs. The logman command also supports many functions of Performance Monitor. The logman command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Logoff</td>
<td>The logoff command is used to terminate a session. The logoff command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Lpq</td>
<td>The lpq command displays the status of a print queue on a computer running Line Printer Daemon (LPD). The lpq command is available in all versions of Windows. The lpq command is not available by default in Windows 8, 7, or Vista, but can be enabled by turning on the LPD Print Service and LPR Port Monitor features from Programs and Features in Control Panel.</td>
</tr>
<tr>
<td>Lpr</td>
<td>The lpr command is used to send a file to a computer running Line Printer Daemon (LPD). The lpr command is available in all versions of Windows. The lpr command is not available by default in Windows 8, 7, or Vista, but can be enabled by turning on the LPD Print Service and LPR Port Monitor features from Programs and Features in Control Panel.</td>
</tr>
<tr>
<td>Makecab</td>
<td>The makecab command is used to losslessly compress one or more files. The makecab command is sometimes called Cabinet Maker. The makecab command is available in Windows 8, Windows 7, Windows Vista, and Windows XP. The makecab command is the same as the diantz command, a command that was removed after Windows 7.</td>
</tr>
<tr>
<td>Manage-bde</td>
<td>The manage-bde command is used to configure BitLocker Drive Encryption from the command line. The manage-bde command is available in Windows 8 and Windows 7. A script by the name of manage-bde.wsf exists in Windows Vista and can be used with the cscript command to perform BitLocker tasks from the command line in that operating system.</td>
</tr>
<tr>
<td>Md</td>
<td>The md command is the shorthand version of the mkdir command. The md command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Mem</td>
<td>The mem command shows information about used and free memory areas and programs that are currently loaded into memory in the MS-DOS subsystem. The mem command is available in MS-DOS as well as in all 32-bit versions of Windows. The mem command is not available in 64-bit versions of Windows.</td>
</tr>
<tr>
<td>Memmaker</td>
<td>The memmaker command is used to start MemMaker, a memory optimization tool. The memaker command is available in Windows 98 and 95, as well as in MS-DOS. Memory usage is automatically optimized beginning in Windows XP.</td>
</tr>
<tr>
<td>Mkdir</td>
<td>The mkdir command is used to create a new folder. The mkdir command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Mklink</td>
<td>The mklink command is used to create a symbolic link. The mklink command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Mode</td>
<td>The mode command is used to configure system devices, most often COM and LPT ports. The mode command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Mofcomp</td>
<td>The mofcomp command properly displays the data within a Managed Object Format (MOF) file. The mofcomp command is available in all versions of Windows.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/more-command-4041467">More</a></td>
<td>The more command is used to display the information contained in a text file. The more command can also be used to paginate the results of any other Command Prompt or MS-DOS command. The more command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Mount</td>
<td>The mount command is used to mount Network File System (NFS) network shares. The mount command is available in Windows 7 and Windows Vista. The mount command is not available by default in Windows Vista or Windows 7 but can be enabled by turning on the Services for NFS Windows feature from Programs and Features in Control Panel. The mount command is not available in Windows 8 because Service for UNIX (SFU) was discontinued.</td>
</tr>
<tr>
<td>Mountvol</td>
<td>The mountvol command is used to display, create, or remove volume mount points. The mountvol command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Move</td>
<td>The move command is used to move one or files from one folder to another. The move command is also used to rename directories. The move command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Mrinfo</td>
<td>The mrinfo command is used to provide information about a <a href="https://www.lifewire.com/what-is-a-router-2618162">router's</a> interfaces and neighbors. The mrinfo command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Msav</td>
<td>The msav command starts Microsoft Antivirus. The msav command is only available in MS-DOS. Microsoft Antivirus was designed for MS-DOS and Windows 3.x only. Microsoft provides an optional virus protection suite called Microsoft Security Essentials for Windows XP and later operating systems, and <a href="https://www.lifewire.com/best-free-antivirus-software-4151895">third party antivirus tools</a> are available for all versions of Windows.</td>
</tr>
<tr>
<td>Msbackup</td>
<td>The msbackup command starts Microsoft Backup, a tool used to back up and restore one or more files. The msbackup command is only available in MS-DOS. The msbackup command was replaced with Microsoft Backup beginning in Windows 95 and then Backup and Restore in later versions of Windows.</td>
</tr>
<tr>
<td>Mscdex</td>
<td>The mscdex command is used to provide <a href="https://www.lifewire.com/what-is-an-optical-disc-drive-2618157">CD-ROM</a> access to MS-DOS. The mscdex command is available in Windows 98 and 95, as well as in MS-DOS. Windows provides access to CD-ROM drives for the MS-DOS subsystem beginning in Windows XP, so the mscdex command is unnecessary in this and later operating systems.</td>
</tr>
<tr>
<td>Msd</td>
<td>The msd command starts Microsoft Diagnostics, a tool used to <a href="https://www.lifewire.com/free-system-information-tools-2625772">display information about your computer</a>. The msd command is only available in MS-DOS. The msd command was replaced with System Information beginning in Windows 95.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/msg-command-2618093">Msg</a></td>
<td>The msg command is used to send a message to a user. The msg command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Msiexec</td>
<td>The msiexec command is used to start Windows Installer, a tool used to install and configure software. The msiexec command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Muiunattend</td>
<td>The muiunattend command starts the Multilanguage User Interface unattended setup process. The muiunattend command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Nbtstat</td>
<td>The nbtstat command is used to show TCP/IP information and other statistical information about a remote computer. The nbtstat command is available in all versions of Windows.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/net-command-2618094">Net</a></td>
<td>The net command is used to display, configure, and correct a wide variety of network settings. The net command is available in all versions of Windows.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/net-command-2618094">Net1</a></td>
<td>The net1 command is used to display, configure, and correct a wide variety of network settings. The net1 command is available in Windows 8, Windows 7, Windows Vista, and Windows XP. The net command should be used instead of the net1 command. The net1 command was made available in Windows NT and Windows 2000 as a temporary fix for a Y2K issue that the net command had, which was corrected before the release of Windows XP. The net1 command remains in later versions of Windows only for compatibility with older programs and scripts that utilized the command.</td>
</tr>
<tr>
<td>Netcfg</td>
<td>The netcfg command is used to install the Windows Preinstallation Environment (WinPE), a lightweight version of Windows used to deploy workstations. The netcfg command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Netsh</td>
<td>The netsh command is used to start Network Shell, a command-line utility used to manage the network configuration of the local, or a remote, computer. The netsh command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/netstat-command-2618098">Netstat</a></td>
<td>The netstat command is most commonly used to display all open network connections and listening ports. The netstat command is available in all versions of Windows.</td>
</tr>
<tr>
<td>Nfsadmin</td>
<td>The nfsadmin command is used to manage Server for NFS or Client for NFS from the command line. The nfsadmin command is available in Windows 7 and Windows Vista. The nfsadmin command is not available by default in Windows Vista or Windows 7 but can be enabled by turning on the Services for NFS Windows feature from Programs and Features in Control Panel. The nfsadmin command is not available in Windows 8 because Service for UNIX (SFU) was discontinued.</td>
</tr>
<tr>
<td>Nlsfunc</td>
<td>The nlsfunc command is used to load information specific to a particular country or region. The nlsfunc command is available in MS-DOS as well as in all 32-bit versions of Windows. The nlsfunc command is not available in 64-bit versions of Windows. Nlsfunc is only available in Windows 8, 7, Vista, and XP to support older MS-DOS files.</td>
</tr>
<tr>
<td>Nltest</td>
<td>The nltest command is used to test secure channels between Windows computers in a domain and between domain controllers that are trusting other domains. The nltest command is available in Windows 8 and Windows 7.</td>
</tr>
<tr>
<td>Nslookup</td>
<td>The nslookup is most commonly used to display the hostname of an entered IP address. The nslookup command queries your configured <a href="https://www.lifewire.com/what-is-a-dns-server-2625854">DNS server</a> to discover the IP address. The nslookup command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Ntbackup</td>
<td>The ntbackup command is used to perform various backup functions from the Command Prompt or from within a batch or script file. The ntbackup command is available in Windows XP. The ntbackup command was replaced with the wbadmin beginning in Windows Vista.</td>
</tr>
<tr>
<td>Ntsd</td>
<td>The ntsd command is used to perform certain command line debugging tasks. The ntsd command is available in Windows XP. The ntsd command was removed beginning in Windows Vista due to the addition of dump file support in <a href="https://www.lifewire.com/task-manager-2626025">Task Manager</a>.</td>
</tr>
<tr>
<td>Ocsetup</td>
<td>The ocsetup command starts the Windows Optional Component Setup tool, used to install additional Windows features. The ocsetup command is available in Windows 8, Windows 7, and Windows Vista. Beginning in Windows 8, Microsoft is depreciating the ocsetup command in favor of the dism command.</td>
</tr>
<tr>
<td>Openfiles</td>
<td>The openfiles command is used to display and disconnect open files and folders on a system. The openfiles command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Path</td>
<td>The path command is used to display or set a specific path available to executable files. The path command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Pathping</td>
<td>The pathping command functions much like the tracert command but will also report information about network latency and loss at each <a href="https://www.lifewire.com/what-are-hops-hop-counts-2625905">hop</a>. The pathping command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Pause</td>
<td>The pause command is used within a batch or script file to pause the processing of the file. When the pause command is used, a "Press any key to continue…" message displays in the command window. The pause command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Pentnt</td>
<td>The pentnt command is used to detect floating point division errors in the Intel Pentium chip. The pentnt command is also used to enable floating point emulation and disable floating point <a href="https://www.lifewire.com/computer-hardware-2625895">hardware</a>. The pentnt command is available in Windows XP. The pentnt command was removed beginning in Windows Vista due to the lack of Intel Pentium <a href="https://www.lifewire.com/what-is-a-cpu-2618150">CPU</a> use at the time of this operating system release.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/ping-command-2618099">Ping</a></td>
<td>The ping command sends an Internet Control Message Protocol (ICMP) Echo Request message to a specified remote computer to verify IP-level connectivity. The ping command is available in all versions of Windows.</td>
</tr>
<tr>
<td>Pkgmgr</td>
<td>The pkgmgr command is used to start the Windows Package Manager from the Command Prompt. Package Manager installs, uninstalls, configures, and updates features and packages for Windows. The pkgmgr command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Pnpunattend</td>
<td>The pnpunattend command is used to automate the installation of hardware device drivers. The pnpunattend command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Pnputil</td>
<td>The pnputil command is used to start the Microsoft PnP Utility, a tool used to install a Plug and Play device from the command line. The pnputil command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Popd</td>
<td>The popd command is used to change the current directory to the one most recently stored by the pushd command. The popd command is most often utilized from within a batch or script file. The popd command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Power</td>
<td>The power command is used to reduce the power consumed by a computer by monitoring software and hardware devices. The power command is available in Windows 98 and 95, as well as in MS-DOS. The power command was replaced by operating system integrated power management functions beginning in Windows XP.</td>
</tr>
<tr>
<td>Powercfg</td>
<td>The powercfg command is used to manage the Windows power management settings from the command line. The powercfg command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Print</td>
<td>The print command is used to print a specified text file to a specified printing device. The print command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Prompt</td>
<td>The prompt command is used to customize the appearance of the prompt text in Command Prompt or MS-DOS. The prompt command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Pushd</td>
<td>The pushd command is used to store a directory for use, most commonly from within a batch or script program. The pushd command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Pwlauncher</td>
<td>The pwlauncher command is used to enable, disable, or show the status of your Windows To Go startup options. The pwlauncher command is available in Windows 8.</td>
</tr>
<tr>
<td>Qappsrv</td>
<td>The qappsrv command is used to display all Remote Desktop Session Host servers available on the network. The qappsrv command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Qbasic</td>
<td>The qbasic command starts QBasic, the MS-DOS based programming environment for the BASIC programming language. The qbasic command is available in Windows 98 and 95, as well as in MS-DOS. The qbasic command is not installed by default with Windows 98 or 95 but is available from the installation disc or disks.</td>
</tr>
<tr>
<td>Qprocess</td>
<td>The qprocess command is used to display information about running processes. The qprocess command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Query</td>
<td>The query command is used to display the status of a specified service. The query command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Quser</td>
<td>The quser command is used to display information about users currently logged on to the system. The quser command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Qwinsta</td>
<td>The qwinsta command is used to display information about open Remote Desktop Sessions. The qwinsta command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Rasautou</td>
<td>The rasautou command is used to manage Remote Access Dialer AutoDial addresses. The rasautou command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Rasdial</td>
<td>The rasdial command is used to start or end a network connection for a Microsoft client. The rasdial command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Rcp</td>
<td>The rcp command is used to copy files between a Windows computer and a system running the rshd daemon. The rcp command is available in Windows 7, Windows Vista, and Windows XP. The rcp command is not available by default in Windows Vista or Windows 7 but can be enabled by turning on the Subsystem for UNIX-based Applications Windows feature from Programs and Features in Control Panel and then installing the Utilities and SDK for UNIX-based Applications available here for Windows Vista and here for Windows 7. The rcp command is not available in Windows 8 because Service for UNIX (SFU) was discontinued.</td>
</tr>
<tr>
<td>Rd</td>
<td>The rd command is the shorthand version of the rmdir command. The rd command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Rdpsign</td>
<td>The rdpsign command is used to sign a Remote Desktop Protocol (RDP) file. The rdpsign command is available in Windows 7.</td>
</tr>
<tr>
<td>Reagentc</td>
<td>The reagentc command is used to configure the Windows Recovery Environment (RE). The reagentc command is available in Windows 8 and Windows 7.</td>
</tr>
<tr>
<td>Recimg</td>
<td>The recimg command is used to create a custom refresh image. The recimg command is available in Windows 8.</td>
</tr>
<tr>
<td>Recover</td>
<td>The recover command is used to recover readable data from a bad or defective disk. The recover command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Reg</td>
<td>The reg command is used to manage the <a href="https://www.lifewire.com/windows-registry-2625992">Windows Registry</a> from the command line. The reg command can perform common registry functions like adding <a href="https://www.lifewire.com/what-is-a-registry-key-2625999">registry keys</a>, <a href="https://www.lifewire.com/how-to-back-up-the-windows-registry-2625146">exporting the registry</a>, etc. The reg command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Regini</td>
<td>The regini command is used to set or change registry permissions and registry values from the command line. The regini command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Register-cimprovider</td>
<td>The register-cimprovider command is used to register a Common Information Model (CIM) Provider in Windows. The register-cimprovider command is available in Windows 8.</td>
</tr>
<tr>
<td>Regsvr32</td>
<td>The regsvr32 command is used to <a href="https://www.lifewire.com/regsvr32-what-it-is-how-to-register-dlls-2623958">register a DLL file</a> as a command component in the Windows Registry. The regsvr32 command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Relog</td>
<td>The relog command is used to create new performance logs from data in existing performance logs. The relog command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Rem</td>
<td>The rem command is used to record comments or remarks in a batch or script file. The rem command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Ren</td>
<td>The ren command is the shorthand version of the rename command. The ren command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Rename</td>
<td>The rename command is used to change the name of the individual file that you specify. The rename command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Repair-bde</td>
<td>The repair-bde command is used to repair or decrypt a damaged drive that's been encrypted using BitLocker. The repair-bde command is available in Windows 8 and Windows 7.</td>
</tr>
<tr>
<td>Replace</td>
<td>The replace command is used to replace one or more files with one or more other files. The replace command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Reset</td>
<td>The reset command, executed as <em>reset session</em>, is used to reset the session subsystem software and hardware to known initial values. The reset command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Restore</td>
<td>The restore command is used to restore files that were backed up using the backup command. The restore command is only available in MS-DOS. The backup command was only available up to MS-DOS 5.00 but the restore command was included by default with later versions of MS-DOS to provide a way to restore files that were backed up in previous versions of MS-DOS.</td>
</tr>
<tr>
<td>Rexec</td>
<td>The rexec command is used to run commands on remote computers running the rexec daemon. The rexec command is available in Windows Vista and Windows XP. The rsh command is not available by default in Windows Vista but can be enabled by turning on the Subsystem for UNIX-based Applications Windows feature from Programs and Features in Control Panel and then installing the Utilities and SDK for UNIX-based Applications available here. The rexec command is not available in Windows 7 but can be executed in Windows XP via Windows XP Mode if need be.</td>
</tr>
<tr>
<td>Rmdir</td>
<td>The rmdir command is used to delete an existing or completely empty folder. The rmdir command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Robocopy</td>
<td>The robocopy command is used to copy files and directories from one location to another. This command is also called Robust File Copy. The robocopy command is available in Windows 8, Windows 7, and Windows Vista. The robocopy command is superior to both the copy command and the xcopy command because robocopy supports many more options.</td>
</tr>
<tr>
<td>Route</td>
<td>The route command is used to manipulate network routing tables. The route command is available in all versions of Windows.</td>
</tr>
<tr>
<td>Rpcinfo</td>
<td>The rpcinfo command makes a remote procedure call (RPC) to an RPC server and reports what it finds. The rpcinfo command is available in Windows 7 and Windows Vista. The rpcinfo command is not available by default in Windows Vista or Windows 7 but can be enabled by turning on the Services for NFS Windows feature from Programs and Features in Control Panel. The rpcinfo command is not available in Windows 8 because Service for UNIX (SFU) was discontinued.</td>
</tr>
<tr>
<td>Rpcping</td>
<td>The rpcping command is used to ping a server using RPC. The rpcping command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Rsh</td>
<td>The rsh command is used to run commands on remote computers running the rsh daemon. The rsh command is available in Windows 7, Windows Vista, and Windows XP. The rsh command is not available by default in Windows Vista or Windows 7 but can be enabled by turning on the Subsystem for UNIX-based Applications Windows feature from Programs and Features in Control Panel and then installing the Utilities and SDK for UNIX-based Applications available here for Windows Vista and here for Windows 7. The rsh command is not available in Windows 8 because Service for UNIX (SFU) was discontinued.</td>
</tr>
<tr>
<td>Rsm</td>
<td>The rsm command is used to manage media resources using Removable Storage. The rsm command is available in Windows Vista and Windows XP. The rsm command was optional in Windows Vista and then removed in Windows 7 due to Removable Storage Manager being removed from the operating system. Search for the rsm command in the C:\Windows\winsxs folder in Windows Vista if you're having trouble executing the command.</td>
</tr>
<tr>
<td>Runas</td>
<td>The runas command is used to execute a program using another user's credentials. The runas command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Rwinsta</td>
<td>The rwinsta command is the shorthand version of the reset session command. The rwinsta command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Sc</td>
<td>The sc command is used to configure information about services. The sc command communicates with the Service Control Manager. The sc command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Scandisk</td>
<td>The scandisk command is used to start Microsoft ScanDisk, a disk repair program. The scandisk command is available in Windows 98 and 95, as well as in MS-DOS. The scandisk command was replaced by the chkdsk command beginning in Windows XP.</td>
</tr>
<tr>
<td>Scanreg</td>
<td>The scanreg command starts Windows Registry Checker, a basic registry repair program and backup utility. The scanreg command is available in Windows 98 and Windows 95. The functions provided by the scanreg command were no longer necessary beginning in Windows XP due to changes in how the Windows Registry functions.</td>
</tr>
<tr>
<td>Schtasks</td>
<td>The schtasks command is used to schedule specified programs or commands to run at certain times. The schtasks command can be used to create, delete, query, change, run, and end scheduled tasks. The schtasks command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.​</td>
</tr>
<tr>
<td>Sdbinst</td>
<td>The sdbinst command is used to deploy customized SDB database files. The sdbinst command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Secedit</td>
<td>The secedit command is used to configure and analyze system security by comparing the current security configuration to a template. The secedit command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Set</td>
<td>The set command is used to display, enable, or disable <a href="https://www.lifewire.com/what-are-environment-variables-2625868">environment variables</a> in MS-DOS or from the Command Prompt. The set command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Setlocal</td>
<td>The setlocal command is used to start the localization of environment changes inside a batch or script file. The setlocal command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Setspn</td>
<td>The setspn command is used to manage the Service Principal Names (SPN) for an Active Directory (AD) service account. The setspn command is available in Windows 8 and Windows 7.</td>
</tr>
<tr>
<td>Setver</td>
<td>The setver command is used to set the MS-DOS version number that MS-DOS reports to a program. The setver command is available in MS-DOS as well as in all 32-bit versions of Windows. The setver command is not available in 64-bit versions of Windows.</td>
</tr>
<tr>
<td>Setx</td>
<td>The setx command is used to create or change environment variables in the user environment or the system environment. The setx command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/sfc-command-system-file-checker-2626020">Sfc</a></td>
<td>The sfc command is used to <a href="https://www.lifewire.com/how-to-use-sfc-scannow-to-repair-windows-system-files-2626161">verify and replace important Windows system files</a>. The sfc command is also referred to as System File Checker or Windows Resource Checker, depending on the operating system. The sfc command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Shadow</td>
<td>The shadow command is used to monitor another Remote Desktop Services session. The shadow command is available in Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Share</td>
<td>The share command is used to install file locking and file sharing functions in MS-DOS. The share command is available in MS-DOS as well as in all 32-bit versions of Windows. The share command is not available in 64-bit versions of Windows. Share is only available in Windows 8, 7, Vista, and XP to support older MS-DOS files.</td>
</tr>
<tr>
<td>Shift</td>
<td>The shift command is used to change the position of replaceable parameters in a batch or script file. The shift command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Showmount</td>
<td>The showmount command is used to display information about NFS mounted file systems. The showmount command is available in Windows 7 and Windows Vista. The showmount command is not available by default in Windows Vista or Windows 7 but can be enabled by turning on the Services for NFS Windows feature from Programs and Features in Control Panel. The showmount command is not available in Windows 8 because Service for UNIX (SFU) was discontinued.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/shutdown-command-2618100">Shutdown</a></td>
<td>The shutdown command can be used to shut down, <a href="https://www.lifewire.com/how-to-reboot-a-computer-2624568">restart</a>, or log off the current system or a remote computer. The shutdown command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Smartdrv</td>
<td>The smartdrv command installs and configures SMARTDrive, a disk caching utility for MS-DOS. The smartdrv command is available in Windows 98 and 95, as well as in MS-DOS. Caching is automatic beginning in Windows XP, making the smartdrv command unnecessary.</td>
</tr>
<tr>
<td>Sort</td>
<td>The sort command is used to read data from a specified input, sort that data, and return the results of that sort to the Command Prompt screen, a file, or another output device. The sort command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Start</td>
<td>The start command is used to open a new command line window to run a specified program or command. The start command can also be used to start an application without creating a new window. The start command is available in all versions of Windows.</td>
</tr>
<tr>
<td>Subst</td>
<td>The subst command is used to associate a local path with a drive letter. The subst command is a lot like the net use command except a local path is used instead of a shared network path. The subst command is available in all versions of Windows, as well as in MS-DOS. The subst command replaced the assign command beginning with MS-DOS 6.0.</td>
</tr>
<tr>
<td>Sxstrace</td>
<td>The sxstrace command is used to start the WinSxs Tracing Utility, a programming diagnostic tool. The sxstrace command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Sys</td>
<td>The sys command is used to copy the MS-DOS system files and command interpreter to a disk. The sys command is available in Windows 98 and 95, as well as in MS-DOS. The sys command is used most often to create a simple bootable disk or hard drive. The necessary system files for Windows are too large to fit on a disk, so the sys command was removed beginning in Windows XP.</td>
</tr>
<tr>
<td>Systeminfo</td>
<td>The systeminfo command is used to display basic Windows configuration information for the local or a remote computer. The systeminfo command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Takeown</td>
<td>The takedown command is used to regain access to a file that that an administrator was denied access to when reassigning ownership of the file. The takeown command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Taskkill</td>
<td>The taskkill command is used to terminate a running task. The taskkill command is the command line equivalent of <a href="https://www.lifewire.com/how-to-force-quit-a-program-in-windows-2625781">ending a process in Task Manager</a> in Windows. The taskkill command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Tasklist</td>
<td>Displays a list of applications, services, and the Process ID (PID) currently running on either a local or a remote computer. The tasklist command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Tcmsetup</td>
<td>The tcmsetup command is used to set up or disable the Telephony Application Programming Interface (TAPI) client. The tcmsetup command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Telnet</td>
<td>The telnet command is used to communicate with remote computers that use the <a href="https://www.lifewire.com/what-is-telnet-2626026">Telnet protocol</a>. The telnet command is available in all versions of Windows. The telnet command is not available by default in Windows 8, 7, or Vista, but can be enabled by turning on the Telnet Client Windows feature from Programs and Features in Control Panel.</td>
</tr>
<tr>
<td>Tftp</td>
<td>The tftp command is used to transfer files to and from a remote computer that's running the Trivial File Transfer Protocol (TFTP) service or daemon. The tftp command is available in Windows 8, Windows 7, Windows Vista, and Windows XP. The tftp command is not available by default in Windows 8, 7, or Vista, but can be enabled by turning on the TFTP Client Windows feature from Programs and Features in Control Panel.</td>
</tr>
<tr>
<td>Time</td>
<td>The time command is used to show or change the current time. The time command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Timeout</td>
<td>The timeout command is typically used in a batch or script file to provide a specified timeout value during a procedure. The timeout command can also be used to ignore keypresses. The timeout command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Title</td>
<td>The title command is used to set the Command Prompt window title. The title command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Tlntadmn</td>
<td>The tlntadmn command is used to administer a local or remote computer running Telnet Server. The tlntadmn command is available in Windows 8, Windows 7, Windows Vista, and Windows XP. The tlntadmn command is not available by default in Windows 8, 7, or Vista, but can be enabled by turning on the Telnet Server Windows feature from Programs and Features in Control Panel.</td>
</tr>
<tr>
<td>Tpmvscmgr</td>
<td>The tpmvscmgr command is used to create and destroy TPM virtual smart cards. The tpmvscmgr command is available in Windows 8.</td>
</tr>
<tr>
<td>Tracerpt</td>
<td>The tracerpt command is used to process event trace logs or real-time data from instrumented event trace providers. The tracerpt command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/tracert-command-2618101">Tracert</a></td>
<td>The tracert command sends Internet Control Message Protocol (ICMP) Echo Request messages to a specified remote computer with increasing Time to Live (TTL) field values and displays the IP address and hostname, if available, of the router interfaces between the source and destination. The tracert command is available in all versions of Windows.</td>
</tr>
<tr>
<td>Tree</td>
<td>The tree command is used to graphically display the folder structure of a specified drive or path. The tree command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Tscon</td>
<td>The tscon command is used to attach a user session to a Remote Desktop session. The tscon command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Tsdiscon</td>
<td>The tsdiscon command is used to disconnect a Remote Desktop session. The tsdiscon command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Tskill</td>
<td>The tskill command is used to end the specified process. The tskill command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Tsshutdn</td>
<td>The tsshutdn command is used to remotely shut down or restart a terminal server. The tsshutdn command is available in Windows XP. The ability to shut down a computer remotely is also available in the more powerful shutdown command, so tsshutdn was removed beginning in Windows Vista.</td>
</tr>
<tr>
<td>Type</td>
<td>The type command is used to display the information contained in a text file. The type command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Typeperf</td>
<td>The typerperf command displays performance data in the Command Prompt window or writes the data to specified log file. The typeperf command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Tzutil</td>
<td>The tzutil command is used to display or configure the current system's time zone. The tzutil command can also be used to enable or disable Daylight Saving Time adjustments. The tzutil command is available in Windows 8 and Windows 7.</td>
</tr>
<tr>
<td>Umount</td>
<td>The umount command is used to remove Network File System (NFS) mounted network shares. The umount command is available in Windows 7 and Windows Vista. The umount command is not available by default in Windows Vista or Windows 7 but can be enabled by turning on the Services for NFS Windows feature from Programs and Features in Control Panel. The umount command is not available in Windows 8 because Service for UNIX (SFU) was discontinued.</td>
</tr>
<tr>
<td>Undelete</td>
<td>The undelete command is used to undo a deletion performed with the MS-DOS delete command. The undelete command is only available in MS-DOS. The undelete command was removed beginning in Windows 95 due to the availability of the Recycle Bin in Windows. Additionally, <a href="https://www.lifewire.com/free-data-recovery-software-tools-2622893">free file recovery programs</a> are available from third-party software makers.</td>
</tr>
<tr>
<td>Unformat</td>
<td>The unformat command is used to undo the formatting on a drive performed by the MS-DOS format command. The unformat command is only available in MS-DOS. The unformat command was removed beginning in Windows 95 due to file system changes.</td>
</tr>
<tr>
<td>Unlock</td>
<td>The unlock command is used to unlock a drive, disabling direct disk access for a program. The unlock command is only available in Windows 98 and 95. Drive locking is no longer available as of Windows XP.</td>
</tr>
<tr>
<td>Unlodctr</td>
<td>The unlodctr command removes Explain text and Performance counter names for a service or device driver from the Windows Registry. The unlodctr command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Vaultcmd</td>
<td>The vaultcmd command is used to create, remove, and show stored credentials. The vaultcmd command is available in Windows 8 and Windows 7.</td>
</tr>
<tr>
<td>Ver</td>
<td>The ver command is used to display the current Windows or MS-DOS <a href="https://www.lifewire.com/version-number-2626043">version number</a>. The ver command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Verify</td>
<td>The verify command is used to enable or disable the ability of Command Prompt, or MS-DOS, to verify that files are written correctly to a disk. The verify command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/vol-command-2618102">Vol</a></td>
<td>The vol command shows the <a href="https://www.lifewire.com/volume-label-2626045">volume label</a> and serial number of a specified disk, assuming this information exists. The vol command is available in all versions of Windows, as well as in MS-DOS.</td>
</tr>
<tr>
<td>Vsafe</td>
<td>The vsafe command is used to start VSafe, a basic virus protection system for MS-DOS. The vsafe command is only available in MS-DOS. VSafe was designed for MS-DOS and Windows 3.x only. Microsoft provides an optional virus protection suite called Microsoft Security Essentials for Windows XP and later operating systems, and third-party antivirus tools are available for all versions of Windows.</td>
</tr>
<tr>
<td>Vssadmin</td>
<td>The vssadmin command starts the Volume Shadow Copy Service administrative command line tool which displays current volume shadow copy backups and all installed shadow copy writers and providers. The vssadmin command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>W32tm</td>
<td>The w32tm command is used to diagnose issues with Windows Time. The w32tm command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Waitfor</td>
<td>The waitfor command is used to send or wait for a signal on a system. The waitfor command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Wbadmin</td>
<td>The wbadmin command is used to start and stop backup jobs, display details about a previous backup, list the items within a backup, and report on the status of a currently running backup. The wbadmin command is available in Windows 8, Windows 7, and Windows Vista. The wbadmin command replaced the ntbackup command beginning in Windows Vista.</td>
</tr>
<tr>
<td>Wecutil</td>
<td>The wecutil command is used to manage subscriptions to events that are forwarded from WS-Management supported computers. The wecutil command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Wevtutil</td>
<td>The wevtutil command starts the Windows Events Command Line Utility which is used to manage event logs and publishers. The wevtutil command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Where</td>
<td>The where command is used to search for files that match a specified pattern. The where command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Whoami</td>
<td>The whoami command is used to retrieve user name and group information on a network. The whoami command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Winmgmt</td>
<td>The winmgmt command starts the command line version of WMI, a scripting tool in Windows. The winmgmt command is available in all versions of Windows.</td>
</tr>
<tr>
<td>Winrm</td>
<td>The winrm command is used to start the command line version of Windows Remote Management, used to manage secure communications with local and remote computers using web services. The winrm command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Winrs</td>
<td>The winrs command is used to open a secure command window with a remote host. The winrs command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Winsat</td>
<td>The winsat command starts the Windows System Assessment Tool, a program that assesses various features, attributes, and capabilities of a computer running Windows. The winsat command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td>Wmic</td>
<td>The wmic command starts the Windows Management Instrumentation Command line (WMIC), a scripting interface that simplifies the use of Windows Management Instrumentation (WMI) and systems managed via WMI. The wmic command is available in Windows 8, Windows 7, Windows Vista, and Windows XP.</td>
</tr>
<tr>
<td>Wsmanhttpconfig</td>
<td>The wsmanhttpconfig command is used to manage aspects of the Windows Remote Management (WinRM) service. The wsmanhttpconfig command is available in Windows 8, Windows 7, and Windows Vista.</td>
</tr>
<tr>
<td><a href="https://www.lifewire.com/xcopy-command-2618103">Xcopy</a></td>
<td>The xcopy command can copy one or more files or directory trees from one location to another. The xcopy command is generally considered a more "powerful" version of the copy command through the robocopy command trumps even xcopy. The xcopy command is available in all versions of Windows, as well as in MS-DOS. A command by the name of xcopy32 existed in Windows 95 and Windows 98. To avoid a long and confusing explanation here, just know that no matter if you executed the xcopy command or the xcopy32 command, you were always executing the most updated version of the command.</td>
</tr>
<tr>
<td>Xwizard</td>
<td>The xwizard command, short for Extensible Wizard, is used to register data in Windows, often from a preconfigured <a href="https://www.lifewire.com/what-is-an-xml-file-2622560">XML</a> file. The xwizard command is available in Windows 8 and Windows 7.</td>
</tr>
</tbody>
</table>

## [DOS-CMDS](https://www.lifewire.com/dos-commands-4070427)

## [21 Command Prompt Tricks and Hacks](https://www.lifewire.com/command-prompt-tricks-and-hacks-2618104)

## Command & Description

<table>
<tr>
<th>S.No</th>
<th style="text-align:center;">Commands &amp; Description</th>
</tr>
<tr>
<td class="ts">1</td>
<td><a href="/batch_script/batch_script_ver.htm">VER</a>
<p>This batch command shows the version of MS-DOS you are using.</p></td>
</tr>
<tr>
<td class="ts">2</td>
<td><a href="/batch_script/batch_script_assoc.htm">ASSOC</a>
<p>This is a batch command that associates an extension with a file type (FTYPE), displays existing associations, or deletes an association.</p></td>
</tr>
<tr>
<td class="ts">3</td>
<td><a href="/batch_script/batch_script_cd.htm">CD</a>
<p>This batch command helps in making changes to a different directory, or displays the current directory.</p></td>
</tr>
<tr>
<td class="ts">4</td>
<td><a href="/batch_script/batch_script_cls.htm">CLS</a>
<p>This batch command clears the screen.</p></td>
</tr>
<tr>
<td class="ts">5</td>
<td><a href="/batch_script/batch_script_copy.htm">COPY</a>
<p>This batch command is used for copying files from one location to the other.</p></td>
</tr>
<tr>
<td class="ts">6</td>
<td><a href="/batch_script/batch_script_del.htm">DEL</a>
<p>This batch command deletes files and not directories.</p></td>
</tr>
<tr>
<td class="ts">7</td>
<td><a href="/batch_script/batch_script_dir.htm">DIR</a>
<p>This batch command lists the contents of a directory.</p></td>
</tr>
<tr>
<td class="ts">8</td>
<td><a href="/batch_script/batch_script_date.htm">DATE</a>
<p>This batch command help to find the system date.</p></td>
</tr>
<tr>
<td class="ts">9</td>
<td><a href="/batch_script/batch_script_echo.htm">ECHO</a>
<p>This batch command displays messages, or turns command echoing on or off.</p></td>
</tr>
<tr>
<td class="ts">10</td>
<td><a href="/batch_script/batch_script_exit.htm">EXIT</a>
<p>This batch command exits the DOS console.</p></td>
</tr>
<tr>
<td class="ts">11</td>
<td><a href="/batch_script/batch_script_md.htm">MD</a>
<p>This batch command creates a new directory in the current location.</p></td>
</tr>
<tr>
<td class="ts">12</td>
<td><a href="/batch_script/batch_script_move.htm">MOVE</a>
<p>This batch command moves files or directories between directories.</p></td>
</tr>
<tr>
<td class="ts">13</td>
<td><a href="/batch_script/batch_script_path.htm">PATH</a>
<p>This batch command displays or sets the path variable.</p></td>
</tr>
<tr>
<td class="ts">14</td>
<td><a href="/batch_script/batch_script_pause.htm">PAUSE</a>
<p>This batch command prompts the user and waits for a line of input to be entered.</p></td>
</tr>
<tr>
<td class="ts">15</td>
<td><a href="/batch_script/batch_script_prompt.htm">PROMPT</a>
<p>This batch command can be used to change or reset the cmd.exe prompt.</p></td>
</tr>
<tr>
<td class="ts">16</td>
<td><a href="/batch_script/batch_script_rd.htm">RD</a>
<p>This batch command removes directories, but the directories need to be empty before they can be removed.</p></td>
</tr>
<tr>
<td class="ts">17</td>
<td><a href="/batch_script/batch_script_ren.htm">REN</a>
<p>Renames files and directories</p></td>
</tr>
<tr>
<td class="ts">18</td>
<td><a href="/batch_script/batch_script_rem.htm">REM</a>
<p>This batch command is used for remarks in batch files, preventing the content of the remark from being executed.</p></td>
</tr>
<tr>
<td class="ts">19</td>
<td><a href="/batch_script/batch_script_start.htm">START</a>
<p>This batch command starts a program in new window, or opens a document.</p></td>
</tr>
<tr>
<td class="ts">20</td>
<td><a href="/batch_script/batch_script_time.htm">TIME</a>
<p>This batch command sets or displays the time.</p></td>
</tr>
<tr>
<td class="ts">21</td>
<td><a href="/batch_script/batch_script_type.htm">TYPE</a>
<p>This batch command prints the content of a file or files to the output.</p></td>
</tr>
<tr>
<td class="ts">22</td>
<td><a href="/batch_script/batch_script_vol.htm">VOL</a>
<p>This batch command displays the volume labels.</p></td>
</tr>
<tr>
<td class="ts">23</td>
<td><a href="/batch_script/batch_script_attrib.htm">ATTRIB</a>
<p>Displays or sets the attributes of the files in the curret directory</p></td>
</tr>
<tr>
<tr>
<td class="ts">24</td>
<td><a href="/batch_script/batch_script_chkdsk.htm">CHKDSK</a>
<p>This batch command checks the disk for any problems.</p></td>
</tr>
<tr>
<td class="ts">25</td>
<td><a href="/batch_script/batch_script_choice.htm">CHOICE</a>
<p>This batch command provides a list of options to the user.</p></td>
</tr>
<tr>
<td class="ts">26</td>
<td><a href="/batch_script/batch_script_cmd.htm">CMD</a>
<p>This batch command invokes another instance of command prompt.</p></td>
</tr>
<tr>
<td class="ts">27</td>
<td><a href="/batch_script/batch_script_comp.htm">COMP</a>
<p>This batch command compares 2 files based on the file size.</p></td>
</tr>
<tr>
<td class="ts">28</td>
<td><a href="/batch_script/batch_script_convert.htm">CONVERT</a>
<p>This batch command converts a volume from FAT16 or FAT32 file system to NTFS file system.</p></td>
</tr>
<tr>
<td class="ts">29</td>
<td><a href="/batch_script/batch_script_driverquery.htm">DRIVERQUERY</a>
<p>This batch command shows all installed device drivers and their properties.</p></td>
</tr>
<tr>
<td class="ts">30</td>
<td><a href="/batch_script/batch_script_expand.htm">EXPAND</a>
<p>This batch command extracts files from compressed .cab cabinet files.</p></td>
</tr>
<tr>
<td class="ts">31</td>
<td><a href="/batch_script/batch_script_find.htm">FIND</a>
<p>This batch command searches for a string in files or input, outputting matching lines.</p></td>
</tr>
<tr>
<td class="ts">32</td>
<td><a href="/batch_script/batch_script_format.htm">FORMAT</a>
<p>This batch command formats a disk to use Windows-supported file system such as FAT, FAT32 or NTFS, thereby overwriting the previous content of the disk.</p></td>
</tr>
<tr>
<td class="ts">33</td>
<td><a href="/batch_script/batch_script_help.htm">HELP</a>
<p>This batch command shows the list of Windows-supplied commands.</p></td>
</tr>
<tr>
<td class="ts">34</td>
<td><a href="/batch_script/batch_script_ipconfig.htm">IPCONFIG</a>
<p>This batch command displays Windows IP Configuration. Shows configuration by connection and the name of that connection.</p></td>
</tr>
<tr>
<td class="ts">35</td>
<td><a href="/batch_script/batch_script_label.htm">LABEL</a>
<p>This batch command adds, sets or removes a disk label.</p></td>
</tr>
<tr>
<td class="ts">36</td>
<td><a href="/batch_script/batch_script_more.htm">MORE</a>
<p>This batch command displays the contents of a file or files, one screen at a time.</p></td>
</tr>
<tr>
<td class="ts">37</td>
<td><a href="/batch_script/batch_script_net.htm">NET</a>
<p>Provides various network services, depending on the command used.</p></td>
</tr>
<tr>
<td class="ts">38</td>
<td><a href="/batch_script/batch_script_ping.htm">PING</a>
<p>This batch command sends ICMP/IP "echo" packets over the network to the designated address.</p></td>
</tr>
<tr>
<td class="ts">39</td>
<td><a href="/batch_script/batch_script_shutdown.htm">SHUTDOWN</a>
<p>This batch command shuts down a computer, or logs off the current user.</p></td>
</tr>
<tr>
<td class="ts">40</td>
<td><a href="/batch_script/batch_script_sort.htm">SORT</a>
<p>This batch command takes the input from a source file and sorts its contents alphabetically, from A to Z or Z to A. It prints the output on the console.</p></td>
</tr>
<tr>
<td class="ts">41</td>
<td><a href="/batch_script/batch_script_subst.htm">SUBST</a>
<p>This batch command assigns a drive letter to a local folder, displays current assignments, or removes an assignment.</p></td>
</tr>
<tr>
<td class="ts">42</td>
<td><a href="/batch_script/batch_script_systeminfo.htm">SYSTEMINFO</a>
<p>This batch command shows configuration of a computer and its operating system.</p></td>
</tr>
<tr>
<td class="ts">43</td>
<td><a href="/batch_script/batch_script_taskkill.htm">TASKKILL</a>
<p>This batch command ends one or more tasks.</p></td>
</tr>
<tr>
<td class="ts">44</td>
<td><a href="/batch_script/batch_script_tasklist.htm">TASKLIST</a>
<p>This batch command lists tasks, including task name and process id (PID).</p></td>
</tr>
<tr>
<td class="ts">45</td>
<td><a href="/batch_script/batch_script_xcopy.htm">XCOPY</a>
<p>This batch command copies files and directories in a more advanced way.</p></td>
</tr>
<tr>
<td class="ts">46</td>
<td><a href="/batch_script/batch_script_tree.htm">TREE</a>
<p>This batch command displays a tree of all subdirectories of the current directory to any level of recursion or depth.</p></td>
</tr>
<tr>
<td class="ts">47</td>
<td><a href="/batch_script/batch_script_fc.htm">FC</a>
<p>This batch command lists the actual differences between two files.</p></td>
</tr>
<tr>
<td class="ts">48</td>
<td><a href="/batch_script/batch_script_diskpart.htm">DISKPART</a>
<p>This batch command shows and configures the properties of disk partitions.</p></td>
</tr>
<tr>
<td class="ts">49</td>
<td><a href="/batch_script/batch_script_title.htm">TITLE</a>
<p>This batch command sets the title displayed in the console window.</p></td>
</tr>
<tr>
<td class="ts">50</td>
<td><a href="/batch_script/batch_script_set.htm">SET</a>
<p>Displays the list of environment variables on the current system.</p></td>
</tr>
