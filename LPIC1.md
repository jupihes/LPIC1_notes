#linux #os #scheduling


# LPIC 1 class

## Session 1

GNU/Linux $\to$ OS
Linux $\rightarrow$ Core or Kernel


40 years ago architecture $\rightarrow$ Multiuser Single server

![[Pasted image 20240828142536.png]]


OS = Kernel + tools
GNU/Linux = Linux + GNU

File system: store and recovery of files in system
- Format
- Block size

#####  Multiuser Single server Architecture 
Users with Terminal (IU and OU)

| CPU        |     | ALU |     |     |
| ---------- | --- | --- | --- | --- |
|            |     |     |     |     |
| Input Unit |     | CU  |     | OU  |
|            |     |     |     |     |
|            |     | MU  |     |     |
#####  Client server Architecture 


Every OS needs to work with special Filesystems

Linux native file system: EXT4, btrfs
Non-native: NTFS, XFS, APFS, ZFS, SWAP
Cross-platform FS: FAT8, 16, 32, CDFS, ISO

```shell
mk 
```

GCC = GNU C Compiler

Enterprise Environments
 - Big scale, scalable, multilocation, multiservice, complex
 - high con-current users, 24/7
 - zero down time = high availability
 - separability of internal / external parts
 - Income, 



My ubuntu details:
<!--
```yaml

```
-->

- share folder : `D:\Hesam\Linux_shared`

[Anisa ftp](http://ftp.anisa.co.ir/)
[http://ftp.anisa.co.ir/OVA/RockyLinux_9_Minimal.ova](http://ftp.anisa.co.ir/OVA/RockyLinux_9_Minimal.ova) 
[http://ftp.anisa.co.ir/ISO/Rocky-9.0-x86_64-dvd.iso](http://ftp.anisa.co.ir/ISO/Rocky-9.0-x86_64-dvd.iso)
[Alireza's at share folder](\\mtnirancell\marketing\Marketing\Public\Alireza.h)
#### 
Client / Server old 
$\rightarrow$ 2-layer $\rightarrow$ 3-layer $\rightarrow$ N-tier

middle-tier

IPC - ICP (**Internal Communication Protocol**)


| Administration           | DevOps | Developer |
| ------------------------ | ------ | --------- |
|                          |        |           |
| LPICs                    |        |           |
|                          |        |           |
| LPIC-3                   |        |           |
| 300 Mix Env. (SMB, LDAP) |        |           |
| 303 Security             |        |           |
| 305 Virtualization       |        |           |



Linux
1.  Debian based
2.  Redhat based



 - LPIC 3
    - SMB protocol - CIFS protocol for connecting Windows - Samba (Windows mask on Linux)
    - LDAP protocol  - LDAP servers implementation by providers 
	    - (Active directory Windows, Oracle Internet directory, Linux: several like OPEN LDAP)
	    - 

- Security Enhanced Linux: for Application limitation (like firewall)


[Anisa FTP with files for download](http://ftp.anisa.co.ir/) 

$\rightarrow$
$\rightarrow$

## Session 2

? to review
part 2

1. `root`: as super user
2. `root`: `filesystem root` highest position in hierarchy - `/`
3. `root`: `root` a root's  home directory - `/root/`   دارکتوری هم نام یوزر
4. `root`: `root` a group - `/root/`
5. `root`: `root` as a access level

tilde  $\textasciitilde$    current user home directory

when login $\rightarrow$ go to home of user
- `whoami`
- `pwd` - `cd`


- root account identifier at shell: `#` 
- rest of user: `$`
- switch to `root` user

	1. Run `sudo <command>` and type in your login password, if prompted, to run only that instance of the command as root. Next time you run another or the same command without the `sudo` prefix, you will not have root access.
	    
	2. Run `sudo -i`. This will give you an interactive root shell. Note that the `$` at the end of your prompt has changed to a `#`, indicating that you have root access. But you fall in the root home directory (`/root/`). From here you can run any sequence of commands as root, or run the command `exit` to leave the root shell.
	    
	3. Use the `su` (substitute user) command to get a root shell. This is effectively the same as using `sudo -i`. Note that when you use this command it will ask for the root password and not your login password. These are not the same. You may have to set or change the root password by running `sudo passwd root` first.
	    
	4. Run `sudo -s`. This gives you root access, but maintains your current SHELL. Shell specific settings, including your current directory, are preserved. For instance if you use `bash` (Ubuntu's default shell), aliases (and any other settings from `~/.bashrc`) are kept when you switch to the root user. To leave the root access, type `exit` as in the cases above.
## Session 3
have 6 text mode and one graphical mode 



![](./images/linux/Linux_modes.png)


right Ctrl + 
Ctrl+alt+ F + $\{1, ...,  7\}$ 
- there exist `system` and `service/application` related users
	- like `ftp service`, `mail server service` , etct
	- We can check them in `config` file [later](in cource)
         check whole users $\rightarrow$ check config file
shutdown $\rightarrow$ `init 0`

< i see till min 41:03>  exercises at <-48:00>

| shutdown | `init 0` |
| -------- | -------- |
| reboot   | `init 6` |

`whoami`
`pwd`
`dir` or `ls`    `ls <address>`    `ls /Var>`
useradd  with privilages of `root`

control + F2
`useradd`      $\rightarrow$ `passwd` to set password

`hostname`    `<computername>.<domain name>`

```shell
echo "server1.lpic.org" > /etc/hostname
init 6
```
- reboot to be possible to see the file


`ps` ? 
- Zoom in or out in `Ctrl+Shift`    `Ctrl`
- clear screen `clear`
- `R Ctrl+l`   hostkey
- `L Ctrl+ C`
- `ls -l` long list with details
- `cat`
```shell
ls /boot

boot loader# grub2
initrd #
# kernel linux file which contains version

```

- `-l` (long listing), `-a` (show hidden dot files), and `-t` options (list by time)
- Sometimes, an `argument` is associated with an `option`. 
- argument must immediately follow the option. 
	- single-letter options, the argument typically follows after a space.  
	- full-word options, the argument often follows an equal sign (=).
```shell
ls ?
ls --hide=Desktop
```

1. دسترسی‌ها permission access
2. hard link

3. مالک
4. گروه مالک group owner

5. size (Byte)
6. modify time (mtime)
7.  filename


- `ls -l -h` `<switch> <option`> option does not work stand alone 
- `ls -a `all  provide all which add things start with `.`
- `.`  and `..`
	- absolute address vs relative addressing
	- `ls .` folder im am in 
	- `ls./..` = `ls ..`
- 1993 - 1994 FHS Filesystem Hierarchy Standard $\to$ LSB (Linux Standard Base)
- Long Term Support LTS     
- [check distro differences](distrowatch.com)
- Linux features LSB,  LTS


- `\` : ریشه فایل سیستم و شروع آدرس دهی از این دایرکتوری
- `/boot`: برخی فایل های اصلی در این قرار دارند از جمله  
- `/`:
- `/`:
- `/bin`: فایل اجرایی دستورات عمومی سیستم که توسط همه کاربران قابل اجرا هستند در این مسیر قرار می گیرد. اصطلابه این دستورات user commands  یا  general commands می گویند
- `/sbin`: فایل اجرایی دستورات عمومی سیستم که توسط همه کاربران قابل اجرا هستند در این مسیر قرار می گیرد. اصطلابه این دستورات system commands  یا  administration commands می گویند
- `/lib`: فایل اجرایی دستورات عمومی سیستم که توسط همه کاربران قابل اجرا هستند در این مسیر قرار می گیرد. اصطلابه این دستورات user commands  یا  general commands می گویند
- `/opt`: `<optinal>` third-party applications



تکالیف

- Window
	- client
	- server

- Linux
	- client: N/A
	- server: 
		1. Server (core)  $\to$ ubuntu server, RHEL, OEL, 
		2. desktop   ==$\to$ ubuntu server, RHEL, OEL,== 



- `ls /bin/ | more` : only go done, `q` for quit
-  `ls /bin/ | less` :  $\uparrow$ $\downarrow$ work 
	- less or more pagination
- `|` : pipe operator : to side of operator should be command
- `cat`:
- `cat <filename> | ws -l` or `ws -l <filename>`: 
- `less <filename>`
- `nl <filename>
- `cat file | nl | more`

- `4700 PB` = $4700 \times 1000^{5} Byte$ =  $4700\times1000^{4} \times 1000 Byte$ = 4.7e+15 KB
- `4700 PB` = $4700 \times 1000^{5} Byte$ =  $4700 \times 1000^{7} \times \frac{1}{1000^{2}} ZB$ = 0.0047 ZB

- `4700 TB` = $4700 \times 1000^{4} Byte$ =  $4700 \times 1000^{3} \times 1000 Byte$ = 4.7e+12 KB
- `4700 TB` = $4700 \times 1000^{4} Byte$ =  $4700 \times 1000^{7} \times \frac{1}{1000^{3}} ZB$ = 4.7e-6 ZB


[linux-directory-structure](https://www.geeksforgeeks.org/linux-directory-structure/)   
### **These are the common top-level directories associated with the root directory:**


![tree](https://media.geeksforgeeks.org/wp-content/uploads/20210501124411/dir.png)

| Directories | Description                                          |
| ----------- | ---------------------------------------------------- |
| **/bin**    | binary or executable programs.                       |
| **/etc**    | system configuration files.                          |
| **/home**   | home directory. It is the default current directory. |
| **/opt**    | optional or third-party software.                    |
| **/tmp**    | temporary space, typically cleared on reboot.        |
| **/usr**    | User related programs.                               |
|             |                                                      |
|**/var**|log files.|


### Some other directories in the Linux system:

| Directories     | Description                                                                                                                         |
| --------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| **/**           |                                                                                                                                     |
| **/boot**       | It contains all the boot-related information files and folders such as conf, grub, etc.                                             |
| **/dev**        | It is the location of the device files such as dev/sda1, dev/sda2, etc.                                                             |
| **/lib**        | It contains kernel modules and a shared library.                                                                                    |
| **/lost+found** | It is used to find recovered bits of corrupted files.                                                                               |
| **/media**      | It contains subdirectories where removal media devices are inserted.                                                                |
| **/mnt**        | It contains temporary mount directories for mounting the file system.                                                               |
| **/proc**       | It is a virtual and pseudo-file system to contains info about the running processes with a specific process ID or PID.              |
| **/run**        | It stores volatile runtime data.                                                                                                    |
| **/sbin**       | binary executable programs for an administrator.                                                                                    |
| **/srv**        | It contains server-specific and server-related files.                                                                               |
| **/sys**        | It is a virtual file system for modern Linux distributions to store and allows modification of the devices connected to the system. |

#### Log Files:

| Log Files             | Descriptions                                        |
| --------------------- | --------------------------------------------------- |
| **/var/log/lastlog**  | It stores user’s last login info.                   |
| **/var/log/messages** | It has all the global system messages               |
| **/var/log/wtmp**     | It keeps a history of login and logout information. |


#### System Configuration Files:

|Configuration Files|Description|
|---|---|
|**/etc/bashrc**|It is used by bash shell that contains system defaults and aliases.|
|**/etc/crontab**|A shell script to run specified commands on a predefined time interval.|
|**/etc/exports**|It contains information on the file system available on the network.|
|**/etc/fstab**|Information of the Disk Drive and their mount point.|
|**/etc/group**|It is a text file to define Information of Security Group.|
|**/etc/grub.conf**|It is the grub bootloader configuration file.|
|**/etc/init.d**|Service startup Script.|
|**/etc/lilo.conf**|It contains lilo bootloader configuration file.|
|**/etc/hosts**|Information of IP and corresponding hostnames|
|**/etc/hosts.allow**|It contains a list of hosts allowed accessing services on the local machine.|
|**/etc/host.deny**|List of hosts denied accessing services on the local machine.|
|**/etc/inittab**|INIT process and their interaction at the various run levels.|
|**/etc/issue**|Allows editing the pre-login message.|
|**/etc/modules.conf**|It contains the configuration files for the system modules.|
|**/etc/motd**|It contains the message of the day.|
|**/etc/mtab**|Currently mounted blocks information.|
|**/etc/passwd**|It contains username, password of the system, users in a shadow file.|
|**/etc/printcap**|It contains printer Information.|
|**/etc/profile**|Bash shell defaults.|
|**/etc/profile.d**|It contains other scripts like application scripts, executed after login.|
|**/etc/rc.d**|It avoids script duplication.|
|**/etc/rc.d/init.d**|Run Level Initialisation Script.|
|**/etc/resolv.conf**|DNS being used by System.|
|**/etc/security**|It contains the name of terminals where root login is possible.|
|**/etc/skel**|Script that initiates new user home directory.|
|**/etc/termcap**|An ASCII file that defines the behavior of different types of the terminal.|
|**/etc/X11**|Directory tree contains all the conf files for the X-window System.|



#### Virtual and Pseudo Process Related Files:

| Virtual and Pseudo Process Related Files | Descriptions                                                              |
| ---------------------------------------- | ------------------------------------------------------------------------- |
| **/proc/cpuinfo**                        | CPU Information                                                           |
| **/proc/filesystems**                    | It keeps useful info about the processes that are currently running.      |
| **/proc/interrupts**                     | it keeps the information about the number of interrupts per IRQ.          |
| **/proc/ioports**                        | Contains all the Input and Output addresses used by devices on the server |
| **/proc/meminfo**                        | It reports the memory usage information.                                  |
| **/proc/modules**                        | Currently using kernel module.                                            |
| **/proc/mount**                          | Mounted File-system Information.                                          |
| **/proc/stat**                           | It displays the detailed statistics of the current system.                |
| **/proc/swaps**                          | It contains swap file information.                                        |

## Session 4

- Programs
	- complier - binary file 
		- system related `/sbin`
		- person related `/bin`
	 - interpereter
		 - python, shell, perl - text file (script) - `~`? 


- executable file
	- windows
	- Linux
		- executable file
		- use permission to use `rwx` 
			- whatever get `x` permission

- ` wc -l` line count
- `cat localrepo | nl`
- `ls /boo -a -l -h`  arguments
	- 0 referencing
	- `ls -l -h -a /boot` more Linux
	- similar arguments can be mixed `ls -alh  /boot`
	- switches without values can be merged 
		- `command -a <value> -b <value>`
	- `ls -lhtr` ? ?????

- unix style: `ls -a`, `rpm -i   ...` , `ps -a -u -x` or `ps -aux`
- GNU style`ls --all`, `rpm --install   ...`
- BSD style`ps aux`, `rpm --install   ...`

- `user manual` or `manual`
    - `man ls`: `man <name>`
    1. user command - default user - `/bin` 
    8.  system command   - `/sbin`

![](./images/linux/Ls_man.png)
- search `/`   
	- `n` : next match
	- `N` : previous match
	- `q`: quit


- `echo $?`
- `touch`
	- `touch .f4` `touch ./.f5` `touch ....f4`
	- `~` home directory of root user
	- `rm -i <filename>` : i = `interactive`
		- in `redhat` and `centos` and??? : as these are for servers to prevent deleting files
			- `rm -f` - `force`
	- `cd -` : last address
	- `history`
		- `!number`

- `cd ~` or `cd ../../../root` or  `cd ./../../../root` `cd $HOME` `cd/root` or simply `cd`

- absolute vs relative address
	- absolute: not important where we are: only address `destination` start with `/`
		- `.` currnet directory
		- `..` currnet directory
	- relative

![](./images/linux/addressing.png)


- `mkdir /root/1403/mehr/11/linux/class/`
	- `mkdir/root/1403`                                             `cd ~
	- `mkdir/root/1403/mehr`                                  `mkdir ./1403 cd ~
	- ...
	- missed for few minutes
	- `rm f?`
	- `mkdir - p `

- `auto completion`: to character
- `echo`
	 1. print argument:  
		 - `echo  salam              baxs` 
		 - `echo  "salam              baxs"` 
	2. see `variable` value
		 - V1=500  : in RAM -= memory
		 - `echo V1` `echo $V1`
		 - `echo $?`    : `?` [exit code](https://www.cyberciti.biz/faq/linux-bash-exit-status-set-exit-statusin-bash/ )  = 0 correct else not correct


- `echo  $PATH`
- `which mkdir` the one is nearest
- `which -a mkdir`
- `whereis mkdir`

### File Types
 - `-`  regular files (data $\to$ txt, jpg, pdf, mp3)
 - `d` directory
 - `l` symbolic link (shortcut)
 - `c` special device,  character
 - `b` special device, block
 - `p` pipe: interfacing 2 file 
 - `s` socket: 2 applications


- `file <filename>`
- `ls -l zero`
- `ls -l cdrom`  $\to$ `ls - sr0`
- `ls -l sd*`

- `touch f4.mp4`
- `reset`
- `cd /dev` and  `cd /etc` and check file types

- `pwd > f1`
- command  `>` file: to write to file    (making file method 2)
- command `>>` file : to append        (making file method 3)

*exercise 1*
```shell # 3 method
cd 
echo Hesam > myinfo.mp3
echo MH >> myinfo.mp3
echo 09350000 >> myinfo.mp3

cd /root/1043/mehr/11/Linux/calss  
  
echo "Hesam 
MH  
09350000" > myinfo.mp3

echo Hesam > myinfo.mp3
echo MH >> myinfo.mp3
echo 09350000 >> myinfo.mp3
```


###### Find file python - check version
 - python - check version
```shell
ls /usr/bin/python*
which systemctl

python3 --version
```
## Session 5
exercises of session 4: i missed

- copy file: `cp <source file> <destination>` 
	1. make new copy in same place with new name: `cp myinfo m1`
	2. make new copy in other place with same name: `cp ./myinfo ./root/hes/`
	3. make new copy in other place with new name: `cp ./myinfo ./root/moz.txt
		1. `cp ./myinfo ../../hes_info.txt


- move file: `mv <source file> <destination>` 
	1. rename file in same place : `mv myinfo m1`
	2. move = cut and past : `mv ./myinfo ./root/hes/`
	3. move + rename:  `mv ./myinfo ./root/moz.txt
		1. `mv ./myinfo ../../moz.txt

- 
```shell
echo "1403/07/18" >>moz.txt 

date >> moz.txt
```


**Exercise:** 
1. make following path `/root/1403/mehr/18/linux/class/mydir
    - since does not have `/` at end, it is file and should be made by touch
```shell
mkdir /root/1403/mehr/18/linux/class/mydir

mkdir /root/1403
cd ./1403/
mkdir /root/1403
cd ./1403/

## or 
mkdir -p /root/1403/mehr/18/linux/class
cd /root/1403/mehr/18/linux/class
touch mydir

# or
touch /root/1403/mehr/18/linux/class/mydir
```

 2. remove file `mydir`
 3. move file `myinfor` `11/class` to `18/class`

```shell
mv ./root/1403/mehr/11/myinfo ./root/1403/mehr/18/myinfo 
```

4. `myinfo.mp3`
```shell
date >> myinfo.mp3
cp ./myinfo.mp3 ./opt/myinfo.mp3 
```

5. `myinfo.mp3`
```shell
cd ./opt
cp ./myinfo.mp3 hajiz.pdf 
```

6. `myinfo.txt`
```shell
cp ./root/hes/myinfo.txt  ./root/hes/1403/ 
mv ./root/hes/myinfo.txt ./root/hes/test47

```

**Exercise:** 
```shell
dmesg > 
```

- `dmesg`: command for getting ????
- copy directory: ?
	- read `man cp` `-r` `--recursively` = with all details within
	- `cp -r 1403 1404`
- `tree` command
- `rmdir 1404` # not empty folders
- `rm 1404`
- `rm -r 1404` 
	- `rm -rf 1404` :  `force` so that not to ask for each cleaning 
- `;`: `: pwd; date; ls/boooot; hostname`
    - `mkdir anisa; cd anisa`
- define `alias`:  `alias pk='cp /var/log/messages /root/1403/mehr/18/m1.txt
    - `alias`
    - `unalias`:  `unalias ll
    - alias are session based unless we write it in related file to be permeant  `
    - `alias hmh='pwd; ls'`

`ll` = `ls -l` 


- alias has priority over `$PATH`
- `/bin/rm f1`

- `timedatectl`
- `ping`
- `ifconfig`
- `systemctl restart network`
- `yum install -y <package name>`


- `sudo` ???????
#### session 5 - part 2
- `ls -l <names>`
- `ls -l <wildcard on names>`
	- `ls -l m*`: `*` nothing or something with any length

###### wildcards
- on file names 
- meta characters: 
	- `*` 


```shell
cd /dev
ls -l sd*
ls -l sd?             # 3 chars
ls -l sd??            # 4 chars
ls -l sd[abcdek]            # 
ls -l sd[a-ek]            # 
ls -l sd[!aekrt]            # 
ls -l sd{a,b,c,d,e,k}            # 
ls -l sd{a,b1,cdefg123}            # 
```


**Exercise:** on `anisa sample`
```bash
cd /anisa
ls -l
ls -l man* 
ls -l man? 
ls -l ???? 
ls -l man??


ls -l *i
ls -l [s-S]* 
rm -f {s,S}*; rm -f [sS]* ; rm -f s* S* 
touch majid, karim; touch /root/anisa/majid /root/anisa/karim; 
ls -l *i*
ls -l ??i*
clear; pwd; cd ./var/log/
mkdir /opt/test
mv /root/anisa/??[0-9]* ./opt/test/

```

- 4th way to make file: use text editor
   - nano, emacs
   - gedit, kedit, nedit, xed,
   - vi, vitiny

###### vi

- mode of operations
	- command mode   $\longleftrightarrow{\text{unten i for Insert}}{\text{oben Esc}}$	- insert (edit) mode
- `vi /opt/f1`, `/opt/f1`
- `vi f1 f2, f3`

```shell
cd ~
ls
vi batman.rrr
h j k l
i
Hesam
Esc.
:w   \n = Enter
:q   \n = Enter

:wq

vi batman.rrr
Mohammad Hosseini
099352002331
:wq

```
- command
- `i h j k l `
- `:`

```shell
cd ~
dmesg > f1
vi f1

:set nu # set number
:185    # go to line 185
:       # movment in 
# <--h j k^ l-->
:       # movment in  <--h 4j 2k^ 8l-->
#w word forward   6w
#b word backward  2b

#H  head line screan
#L  Last line screan

#gg = :1 last line of file

#G last line of file
ctrl+f 1 page forward (down)
ctrl+b 1 page backward (up)
:55
i 8 space
Esc.
---> ^ caret start of line
     0 start of line
     $ end of line
     
:       # movment in  <--h j k^ l-->
::
```



```shell
ls - lhtr #?
```

###### regular expression
- More capable for working on contents file


## Session 6
- on using `vi`
```bash
demsg >f1
vi f1

:99
----> go to middle of line
### deletion from text
x 8x # delete from right of cursur
X 9X # delete from left of cursur


s Xi # delete 1 character from right and go to Insert mode  
6s =
S  3S + insert mode # delete line and go to insert mode 
### cut from text
d6w   # d + number + dirction
d9l
d7w
d5j
d$ --> D
dG
...
dd # cut one line
5dd
...
cd6w   # c + number + dirction + go to Insert mode
c9l
c7w
c5j
c$ --> C
cG
....
cc  # cut one line + go to Insert mode
5cc # cut one 5 line + go to Insert mode
### copy from text
Yank = copy
y6w   # y + number + dirction
y9l
y7w
y5j
y$ --> Y
yG
....
yy # copy one line
5yy


p # paste right of  - 6p 
P # paste left of 

u # (undo)
ctrl+r # (redo)
. # redo the last command 

#### searcing in manual
/word + enter # go from location downward
?word + enter # go from location upward and from start to location
n # next match in direction
N # next match in anti direction

i # switch to Insert mode +  start add from location to the right 
a # switch to Insert mode + start add from location to the left  
I # switch to Insert mode + cursur go to start of line
A # switch to Insert mode + cursur go to end of line
o # switch to Insert mode + **open** (add) new line after cursur
O # switch to Insert mode + **open** (add) new line before cursur
r # switch to Insert mode + replace 1 character + switch to command mode
R # switch to Insert mode + replace Mode
Insert or Ins. # Switch between Insert mode and replace mode
#### : File / host command mode
:w + Enter  # save file if name is given 
:w + name and address file  # save file  
vi f1 f2 f3 f4 
:n # go to next file
:e + name and address file # open new file 
:r + name and address file # copy other file inside what you are in 
:q # quit vi if you saved
:wq # to save and exit
:q! # to force ignoring changes

:n! # 
:e!
:w! # save for file you are not owner

:wq! # not correct # not needed to force
:wq = :x = ZZ # save and exit
:w!q #  correct

#### work on sample @ 39:00
:set nu # line number 
:180
y3l
6p


/pci # serach downward 
     # n next, N the one before
     
?PCI # search in last driection we worked 
     # n , N switch drection 

vi numbers myinfo

:w # save file 
# save as continue in old file in Linux # unlike Windows

```

if we close `vi` and open new `vi`, what we copy or cut will not be accessible any more. 
  	 - old process of `vi`
	- new process of `vi` 
	- open 2 files if we know in advance
	- `:e`  to open other files and do what we need like past
		- decide on action on newly opened like paste and move on
	- `:r` 
- `ubuntu` and `Mint` - copied in `common RAM` part

- open temporary `subshell`
```bash
:! command # to do bash command  in vi

           # Enter to go back
```

###### processes and Subshell

Working with few machines in a queue

`SSH` or `TELNET` connecting to next Machines
- what happens if we exit from last?
- what happens if network connection somewhere disconnect? Machine before that
<svg version="1.1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1315.416488647461 241.47888310726557" width="1315.416488647461" height="241.47888310726557">
  <!-- svg-source:excalidraw -->
  
  <defs>
    <style class="style-fonts">
      @font-face {
        font-family: "Virgil";
        src: url("https://excalidraw.com/Virgil.woff2");
      }
      @font-face {
        font-family: "Cascadia";
        src: url("https://excalidraw.com/Cascadia.woff2");
      }
    </style>
    
  </defs>
  <rect x="0" y="0" width="1315.416488647461" height="241.47888310726557" fill="#ffffff"></rect><g stroke-linecap="round"><g transform="translate(158.58724947680025 74.67017298953397) rotate(0 66.128906462976 0.05212976518623691)"><path d="M-0.4 -1.02 C21.37 -1.16, 108.62 -0.26, 130.5 0.02 M1.59 1.06 C23.73 0.98, 111.3 1, 132.66 1.14" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g><g transform="translate(158.58724947680025 74.67017298953397) rotate(0 66.128906462976 0.05212976518623691)"><path d="M102.74 9.58 C111.24 7.34, 120.51 6.48, 133.32 3.13 M104.01 10.74 C113.15 7.77, 121.96 3.99, 133.06 0.17" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g><g transform="translate(158.58724947680025 74.67017298953397) rotate(0 66.128906462976 0.05212976518623691)"><path d="M102.8 -10.95 C111.43 -7.22, 120.68 -2.11, 133.32 3.13 M104.07 -9.78 C113.3 -6.14, 122.09 -3.3, 133.06 0.17" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g></g><mask></mask><g stroke-linecap="round" transform="translate(10 10) rotate(0 70.27765909830735 64.72230275471975)"><path d="M7.86 8.16 C7.86 8.16, 7.86 8.16, 7.86 8.16 M7.86 8.16 C7.86 8.16, 7.86 8.16, 7.86 8.16 M3.66 19.09 C5.3 14.29, 10.32 9.37, 18.1 2.48 M3.66 19.09 C9.12 13.9, 15.05 6.2, 18.1 2.48 M2.75 26.24 C8.17 20.69, 16.37 11.53, 24.4 1.33 M2.75 26.24 C10.87 17.37, 19.61 8.17, 24.4 1.33 M2.48 32.64 C9.58 22.05, 17.84 14.72, 30.7 0.18 M2.48 32.64 C10.15 23.52, 18.04 15.46, 30.7 0.18 M2.88 38.28 C14.3 27.87, 23.63 15.82, 34.37 2.05 M2.88 38.28 C12.49 28.39, 20.45 17.35, 34.37 2.05 M2.62 44.68 C13.39 32.3, 26.69 17.21, 39.36 2.41 M2.62 44.68 C15.38 29.08, 28.67 14.02, 39.36 2.41 M2.36 51.07 C19.08 33.4, 34.73 13.06, 45 2.02 M2.36 51.07 C19.22 32.6, 35.3 13.35, 45 2.02 M2.75 56.72 C20.66 36.11, 39.28 16.69, 49.99 2.38 M2.75 56.72 C17.27 41.77, 30.67 25.35, 49.99 2.38 M2.49 63.11 C18.42 44.54, 32.03 28.96, 55.63 1.98 M2.49 63.11 C18.87 43.97, 34.41 26.06, 55.63 1.98 M2.88 68.76 C16.5 52.77, 26.48 40.11, 60.62 2.34 M2.88 68.76 C25.11 43.9, 45.76 19.84, 60.62 2.34 M2.62 75.16 C28.09 48.45, 52.34 18.83, 66.26 1.95 M2.62 75.16 C17.25 57.47, 32.05 41.16, 66.26 1.95 M2.36 81.55 C18.58 65.92, 34.19 47.47, 71.25 2.31 M2.36 81.55 C25.83 55.96, 48.16 28.85, 71.25 2.31 M2.76 87.2 C17.45 68.01, 36.6 49.09, 76.23 2.67 M2.76 87.2 C27.43 59.2, 53.12 29.46, 76.23 2.67 M2.49 93.59 C30.54 60.09, 60.29 28.02, 81.88 2.27 M2.49 93.59 C32.98 59.8, 62.18 25.91, 81.88 2.27 M2.89 99.24 C31.2 63.73, 62.84 33.09, 86.86 2.63 M2.89 99.24 C30.35 67.06, 56.61 37.96, 86.86 2.63 M1.97 106.39 C22.6 80.03, 46.64 55.34, 92.51 2.24 M1.97 106.39 C34.29 68, 65.66 31.23, 92.51 2.24 M3.68 110.52 C33.94 74.91, 69.76 35.97, 97.49 2.6 M3.68 110.52 C22.73 86.14, 44.62 62.48, 97.49 2.6 M4.73 115.41 C25.49 90.03, 46.64 66.35, 103.14 2.21 M4.73 115.41 C24.88 92.86, 44.49 70.4, 103.14 2.21 M7.09 118.79 C37.74 80.38, 72.86 43.77, 108.12 2.57 M7.09 118.79 C33.46 88.95, 58.57 60.36, 108.12 2.57 M9.45 122.17 C36.31 91.78, 62.01 61.64, 113.77 2.17 M9.45 122.17 C35.33 92.83, 62.76 61.28, 113.77 2.17 M12.47 124.79 C37.58 95.49, 65.99 64.6, 118.76 2.53 M12.47 124.79 C56.04 76.66, 97.38 27.76, 118.76 2.53 M15.49 127.42 C51.32 85.65, 89.19 41.27, 123.74 2.89 M15.49 127.42 C51.93 86.54, 89 44.97, 123.74 2.89 M19.82 128.53 C48.78 96.92, 71.52 70.17, 127.42 4.76 M19.82 128.53 C56.54 85.14, 95.44 41.12, 127.42 4.76 M24.81 128.89 C48.83 100.46, 68.21 75.92, 130.44 7.39 M24.81 128.89 C56.36 92.26, 88.69 54.66, 130.44 7.39 M29.8 129.25 C57.54 94.91, 86.24 63.83, 134.11 9.25 M29.8 129.25 C71.52 83.34, 113.53 35.29, 134.11 9.25 M35.44 128.86 C59.91 97.12, 84.82 69.28, 136.47 12.63 M35.44 128.86 C65.29 94.52, 95.72 61.72, 136.47 12.63 M40.43 129.22 C63.55 100.72, 87.82 72.11, 138.18 16.77 M40.43 129.22 C73.61 90.43, 107.57 51.1, 138.18 16.77 M46.07 128.82 C68.35 104.13, 90.22 77.79, 140.54 20.15 M46.07 128.82 C70.43 99.71, 95.1 71.89, 140.54 20.15 M51.06 129.18 C79.31 95.34, 111.02 62.45, 141.59 25.03 M51.06 129.18 C86.44 89.15, 120.29 49.59, 141.59 25.03 M56.04 129.54 C77.75 105.66, 101.46 81.41, 140.68 32.19 M56.04 129.54 C77.33 104.76, 99.61 78.77, 140.68 32.19 M61.69 129.15 C89.96 94.02, 120.57 60.15, 140.41 38.58 M61.69 129.15 C78.56 110.5, 96.48 89.59, 140.41 38.58 M66.67 129.51 C91.87 102.27, 113.85 73.44, 140.81 44.23 M66.67 129.51 C91.92 98.95, 117.3 70.8, 140.81 44.23 M72.32 129.12 C86.14 114.05, 101.59 93.49, 140.55 50.63 M72.32 129.12 C95.83 99.54, 121.33 72.92, 140.55 50.63 M77.3 129.48 C99.03 104.47, 122.22 74.03, 140.29 57.02 M77.3 129.48 C92.66 110.16, 109.56 92.25, 140.29 57.02 M82.95 129.08 C100.75 109.48, 114.94 90.91, 140.68 62.67 M82.95 129.08 C95.58 113.79, 109.2 100.69, 140.68 62.67 M87.93 129.44 C104.17 111.05, 122.58 90.64, 140.42 69.06 M87.93 129.44 C108.27 105.08, 129.13 82.05, 140.42 69.06 M92.92 129.8 C110.09 109.01, 126.28 90.02, 140.16 75.46 M92.92 129.8 C101.84 119.95, 111.38 108.53, 140.16 75.46 M98.56 129.41 C114.75 111.24, 129.35 95.8, 140.55 81.11 M98.56 129.41 C114.08 111.76, 130.1 93.1, 140.55 81.11 M103.55 129.77 C113.56 116.45, 127.61 102.3, 140.29 87.5 M103.55 129.77 C111.92 119.62, 122.75 109.61, 140.29 87.5 M109.19 129.37 C120.82 116.54, 133.11 100.6, 140.03 93.9 M109.19 129.37 C118.53 117.89, 130.06 107.1, 140.03 93.9 M114.84 128.98 C120.77 120.06, 128.4 110.45, 140.42 99.54 M114.84 128.98 C121.83 122.27, 126.97 114.72, 140.42 99.54 M121.14 127.83 C127.29 119.16, 136.31 111.4, 140.82 105.19 M121.14 127.83 C127.57 119.21, 134.72 111.52, 140.82 105.19 M124.81 129.7 C129.76 122.01, 136.54 118.21, 139.9 112.34 M124.81 129.7 C127.9 125.12, 132.36 120.94, 139.9 112.34" stroke="#a5d8ff" stroke-width="0.5" fill="none"></path><path d="M32 0 M32 0 C48.65 1.77, 65.71 2.01, 108.56 0 M32 0 C53.88 0.61, 74.38 -0.12, 108.56 0 M108.56 0 C129.58 -0.81, 138.89 12.07, 140.56 32 M108.56 0 C132.13 -1.1, 139.95 8.71, 140.56 32 M140.56 32 C140.96 53.62, 139.47 71.21, 140.56 97.44 M140.56 32 C141.62 46.33, 140.67 60.42, 140.56 97.44 M140.56 97.44 C138.77 119.25, 131.68 127.53, 108.56 129.44 M140.56 97.44 C139.37 118.89, 130.24 128.23, 108.56 129.44 M108.56 129.44 C79.92 129.73, 48.92 131.31, 32 129.44 M108.56 129.44 C86.5 128.61, 62.39 129.22, 32 129.44 M32 129.44 C11.91 128.97, -1.27 119.95, 0 97.44 M32 129.44 C10.1 128.42, -1.37 117.49, 0 97.44 M0 97.44 C-1.4 79.48, -1.21 67.14, 0 32 M0 97.44 C-0.54 73.26, 1.06 48.79, 0 32 M0 32 C-0.19 12.46, 10.05 -1.77, 32 0 M0 32 C-0.78 12.28, 9.16 0.94, 32 0" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g><g transform="translate(57.222137451171875 61.111310323079124) rotate(0 18.665992736816406 22.5)"><text x="0" y="0" font-family="Virgil, Segoe UI Emoji" font-size="36px" fill="#1e1e1e" text-anchor="start" style="white-space: pre;" direction="ltr" dominant-baseline="text-before-edge">M1</text></g><g stroke-linecap="round" transform="translate(298.87699368293784 10) rotate(0 70.27765909830735 64.72230275471975)"><path d="M7.86 8.16 C7.86 8.16, 7.86 8.16, 7.86 8.16 M7.86 8.16 C7.86 8.16, 7.86 8.16, 7.86 8.16 M3.66 19.09 C8.81 14.11, 9.38 11.52, 18.1 2.48 M3.66 19.09 C9.06 12.72, 14.77 6.27, 18.1 2.48 M2.75 26.24 C9.41 19.39, 15.84 12.97, 24.4 1.33 M2.75 26.24 C7.39 21.78, 11.73 14.93, 24.4 1.33 M2.48 32.64 C9.45 25.42, 16.95 15.05, 30.7 0.18 M2.48 32.64 C7.64 26.05, 14.31 19.3, 30.7 0.18 M2.88 38.28 C9.45 28.61, 20.38 19.37, 34.37 2.05 M2.88 38.28 C15.23 23.96, 26.18 10.2, 34.37 2.05 M2.62 44.68 C13.5 32.02, 24.08 18.27, 39.36 2.41 M2.62 44.68 C14.98 30.97, 27.1 15.63, 39.36 2.41 M2.36 51.07 C21.29 30.15, 35.5 11.34, 45 2.02 M2.36 51.07 C17.87 32.28, 35.08 13.38, 45 2.02 M2.75 56.72 C19.42 40.7, 34.82 23.17, 49.99 2.38 M2.75 56.72 C17.91 38.13, 34.99 19.99, 49.99 2.38 M2.49 63.11 C21.19 43.9, 37.59 23.04, 55.63 1.98 M2.49 63.11 C21.85 39.42, 42.34 17.23, 55.63 1.98 M2.88 68.76 C25.24 43.34, 46.22 14.32, 60.62 2.34 M2.88 68.76 C19.49 49.39, 35.65 31.38, 60.62 2.34 M2.62 75.16 C24.41 48.53, 50.58 23.46, 66.26 1.95 M2.62 75.16 C19.88 54.08, 37.36 34.04, 66.26 1.95 M2.36 81.55 C25.23 57.52, 48.16 32.04, 71.25 2.31 M2.36 81.55 C24.2 56.99, 47.49 30.39, 71.25 2.31 M2.76 87.2 C19.38 66.19, 37.99 46.25, 76.23 2.67 M2.76 87.2 C23.89 63.08, 43.67 39.58, 76.23 2.67 M2.49 93.59 C28.16 63.18, 57.14 30.96, 81.88 2.27 M2.49 93.59 C31.65 61.07, 59.66 26.44, 81.88 2.27 M2.89 99.24 C28.5 71.16, 53.63 39.07, 86.86 2.63 M2.89 99.24 C26.15 70.87, 49.43 44.5, 86.86 2.63 M1.97 106.39 C37.28 66.25, 70.03 28.77, 92.51 2.24 M1.97 106.39 C32.95 70.81, 63.62 34.67, 92.51 2.24 M3.68 110.52 C29.78 78.93, 57.18 47.7, 97.49 2.6 M3.68 110.52 C25.8 84.21, 47.22 58.79, 97.49 2.6 M4.73 115.41 C36.02 78.08, 68.87 39.83, 103.14 2.21 M4.73 115.41 C39.41 75.66, 72.4 38.09, 103.14 2.21 M7.09 118.79 C45.73 72.74, 87.54 28.24, 108.12 2.57 M7.09 118.79 C32.6 87.37, 60.9 56.56, 108.12 2.57 M9.45 122.17 C28.68 96.23, 52.82 71.46, 113.77 2.17 M9.45 122.17 C40.92 88, 69.88 55.43, 113.77 2.17 M12.47 124.79 C37.77 97.13, 63.05 66.84, 118.76 2.53 M12.47 124.79 C47.37 86.52, 81.03 46.88, 118.76 2.53 M15.49 127.42 C46.58 93.32, 77.74 56.2, 123.74 2.89 M15.49 127.42 C42.47 97.8, 69.33 67.33, 123.74 2.89 M19.82 128.53 C59.22 80.77, 100.5 32.62, 127.42 4.76 M19.82 128.53 C52.44 91.52, 85.55 53.04, 127.42 4.76 M24.81 128.89 C51.65 97.82, 73.53 67.87, 130.44 7.39 M24.81 128.89 C62.77 83.62, 102.59 38.67, 130.44 7.39 M29.8 129.25 C64.05 90.19, 94.17 52.26, 134.11 9.25 M29.8 129.25 C66.95 87.93, 105.64 44.39, 134.11 9.25 M35.44 128.86 C61.09 98.98, 85.21 73.66, 136.47 12.63 M35.44 128.86 C66.28 93.04, 96.6 57.77, 136.47 12.63 M40.43 129.22 C71.97 92.09, 102.77 57.64, 138.18 16.77 M40.43 129.22 C79.63 83.64, 117.93 39.98, 138.18 16.77 M46.07 128.82 C74.48 92.96, 104.52 62.02, 140.54 20.15 M46.07 128.82 C83.96 87.01, 121.66 42.65, 140.54 20.15 M51.06 129.18 C84.41 89.93, 121.53 46.82, 141.59 25.03 M51.06 129.18 C80.56 95.69, 111.42 60.64, 141.59 25.03 M56.04 129.54 C83.89 97.11, 107.65 68.74, 140.68 32.19 M56.04 129.54 C78.86 101.97, 102.84 72.72, 140.68 32.19 M61.69 129.15 C84.22 99.62, 109.79 75.05, 140.41 38.58 M61.69 129.15 C84.08 103.61, 107.43 79.05, 140.41 38.58 M66.67 129.51 C92.64 98.67, 117.35 68.37, 140.81 44.23 M66.67 129.51 C89.75 103.31, 112.85 78.36, 140.81 44.23 M72.32 129.12 C96.14 100.12, 122.11 71.62, 140.55 50.63 M72.32 129.12 C96.47 100.4, 120.74 72.09, 140.55 50.63 M77.3 129.48 C103.53 99.65, 126.95 73.39, 140.29 57.02 M77.3 129.48 C95.86 108.79, 115.08 87.13, 140.29 57.02 M82.95 129.08 C98.39 111.48, 115.06 90.37, 140.68 62.67 M82.95 129.08 C99.83 111.21, 114.55 92.78, 140.68 62.67 M87.93 129.44 C103.86 112.44, 118.38 95.42, 140.42 69.06 M87.93 129.44 C108.12 106.95, 128.61 81.9, 140.42 69.06 M92.92 129.8 C103.8 117.81, 114.26 104.76, 140.16 75.46 M92.92 129.8 C108.65 110.74, 124.28 93.67, 140.16 75.46 M98.56 129.41 C108.44 114.59, 120.78 103.72, 140.55 81.11 M98.56 129.41 C106.94 119.05, 115.77 108.66, 140.55 81.11 M103.55 129.77 C112.11 121.52, 119.66 109.82, 140.29 87.5 M103.55 129.77 C112.14 120.07, 120.15 110.92, 140.29 87.5 M109.19 129.37 C119.3 118.45, 129.97 106.21, 140.03 93.9 M109.19 129.37 C117.67 118.97, 126.61 108.56, 140.03 93.9 M114.84 128.98 C123.65 117.5, 134.51 105.76, 140.42 99.54 M114.84 128.98 C121.41 121.69, 129.23 112.86, 140.42 99.54 M121.14 127.83 C129.42 117.16, 135.11 108.64, 140.82 105.19 M121.14 127.83 C126.21 122.79, 130.22 116.61, 140.82 105.19 M124.81 129.7 C130.66 122.5, 136.11 114.18, 139.9 112.34 M124.81 129.7 C129.33 123.78, 135 117.74, 139.9 112.34" stroke="#a5d8ff" stroke-width="0.5" fill="none"></path><path d="M32 0 M32 0 C55.83 0.96, 80.07 -0.33, 108.56 0 M32 0 C61.55 -0.3, 93.07 -0.1, 108.56 0 M108.56 0 C129.75 -1.51, 138.85 12.37, 140.56 32 M108.56 0 C131.56 1.38, 140.4 11.82, 140.56 32 M140.56 32 C138.71 51.92, 141.72 72.58, 140.56 97.44 M140.56 32 C139.15 50.48, 139.81 69.68, 140.56 97.44 M140.56 97.44 C140.16 119.06, 128.23 131.08, 108.56 129.44 M140.56 97.44 C141.78 119.09, 129.22 127.49, 108.56 129.44 M108.56 129.44 C80.56 128.79, 52.56 131.15, 32 129.44 M108.56 129.44 C90.37 129.58, 74.76 129.03, 32 129.44 M32 129.44 C9.81 127.58, -1.92 116.84, 0 97.44 M32 129.44 C9.29 128.07, 1.08 118.42, 0 97.44 M0 97.44 C1.58 73.32, 0.37 51.33, 0 32 M0 97.44 C0.9 81.19, 0.69 65.03, 0 32 M0 32 C-0.84 10.22, 10.86 -1.82, 32 0 M0 32 C-1.17 8.43, 8.39 -1.33, 32 0" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g><g transform="translate(346.0991311341097 61.11131032308003) rotate(0 26.603988647460938 22.5)"><text x="0" y="0" font-family="Virgil, Segoe UI Emoji" font-size="36px" fill="#1e1e1e" text-anchor="start" style="white-space: pre;" direction="ltr" dominant-baseline="text-before-edge">M2</text></g><g stroke-linecap="round"><g transform="translate(737.1013846357641 74.818329134554) rotate(0 65.45691308102221 -0.09602637983425666)"><path d="M-1.03 0.19 C20.83 0.1, 110 -0.49, 131.94 -0.36 M0.63 -0.75 C22.29 -0.77, 109.13 0.03, 131.21 0.56" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g><g transform="translate(737.1013846357641 74.818329134554) rotate(0 65.45691308102221 -0.09602637983425666)"><path d="M103.18 11.06 C111.29 5.52, 123.96 4.17, 129.51 0.12 M102.65 10.9 C114.6 7.01, 123.8 3.14, 131.08 1.3" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g><g transform="translate(737.1013846357641 74.818329134554) rotate(0 65.45691308102221 -0.09602637983425666)"><path d="M103.5 -9.46 C111.53 -7.47, 124.08 -1.28, 129.51 0.12 M102.96 -9.61 C114.61 -5.71, 123.7 -1.78, 131.08 1.3" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g></g><mask></mask><g stroke-linecap="round" transform="translate(587.8853106388527 10) rotate(0 70.27765909830737 64.72230275471975)"><path d="M7.86 8.16 C7.86 8.16, 7.86 8.16, 7.86 8.16 M7.86 8.16 C7.86 8.16, 7.86 8.16, 7.86 8.16 M3.66 19.09 C9.62 12.49, 16.27 4.94, 18.1 2.48 M3.66 19.09 C6.76 15.21, 10.86 12.43, 18.1 2.48 M2.75 26.24 C7.09 21.12, 13.65 13.99, 24.4 1.33 M2.75 26.24 C11.54 16.18, 18.68 7.67, 24.4 1.33 M2.48 32.64 C13.59 18.97, 23.49 9, 30.7 0.18 M2.48 32.64 C13.79 19.29, 25.35 5.95, 30.7 0.18 M2.88 38.28 C16.35 23.44, 29.44 9.96, 34.37 2.05 M2.88 38.28 C13.21 27.69, 21.31 17.59, 34.37 2.05 M2.62 44.68 C12.65 33.77, 19.35 25.92, 39.36 2.41 M2.62 44.68 C12.44 33.96, 21.29 22.64, 39.36 2.41 M2.36 51.07 C13.91 39.7, 23.27 24.25, 45 2.02 M2.36 51.07 C12.39 38.95, 22.93 26.88, 45 2.02 M2.75 56.72 C16.88 39.73, 29.84 24.31, 49.99 2.38 M2.75 56.72 C16.77 40.25, 29.18 24.98, 49.99 2.38 M2.49 63.11 C20.24 44.94, 36.65 24.25, 55.63 1.98 M2.49 63.11 C20.99 41, 40.13 21.03, 55.63 1.98 M2.88 68.76 C19.4 50.04, 32.82 33.48, 60.62 2.34 M2.88 68.76 C21.27 45.32, 42.58 23.92, 60.62 2.34 M2.62 75.16 C27.32 48.06, 49.83 22.7, 66.26 1.95 M2.62 75.16 C15.38 58.8, 30.74 42.83, 66.26 1.95 M2.36 81.55 C21.49 61.9, 35.61 43.71, 71.25 2.31 M2.36 81.55 C16.84 66.01, 31.59 47.36, 71.25 2.31 M2.76 87.2 C21.42 63.29, 43.97 40.28, 76.23 2.67 M2.76 87.2 C24.7 62.26, 48.16 36.39, 76.23 2.67 M2.49 93.59 C32.84 59.39, 61.82 26.84, 81.88 2.27 M2.49 93.59 C22.39 72.28, 43.78 47.65, 81.88 2.27 M2.89 99.24 C25.45 71.92, 50.08 47.34, 86.86 2.63 M2.89 99.24 C27.87 70.39, 52.63 42.39, 86.86 2.63 M1.97 106.39 C32.1 72.9, 60.26 38.47, 92.51 2.24 M1.97 106.39 C32.35 70.81, 64.6 35.2, 92.51 2.24 M3.68 110.52 C38.13 67.9, 74.6 28.85, 97.49 2.6 M3.68 110.52 C35.84 75.97, 67.08 38.27, 97.49 2.6 M4.73 115.41 C28.59 91.4, 50.36 63.65, 103.14 2.21 M4.73 115.41 C40.25 73.63, 76.86 33.13, 103.14 2.21 M7.09 118.79 C30.33 95, 53.42 68.42, 108.12 2.57 M7.09 118.79 C31.92 91.05, 57.79 62.19, 108.12 2.57 M9.45 122.17 C44.44 80.72, 84.33 37.71, 113.77 2.17 M9.45 122.17 C40.44 86.76, 72.28 50.51, 113.77 2.17 M12.47 124.79 C38.3 96.71, 62.02 67.76, 118.76 2.53 M12.47 124.79 C41.95 89.92, 70.68 56.8, 118.76 2.53 M15.49 127.42 C38.59 98.46, 64.9 68.84, 123.74 2.89 M15.49 127.42 C50.72 86.56, 86.34 45.78, 123.74 2.89 M19.82 128.53 C44.32 97.67, 69.79 70.51, 127.42 4.76 M19.82 128.53 C55.9 86.47, 93 44.28, 127.42 4.76 M24.81 128.89 C59.2 90.42, 93.27 50.49, 130.44 7.39 M24.81 128.89 C61.92 88.09, 97.96 45.77, 130.44 7.39 M29.8 129.25 C53.57 100.67, 78.29 74.36, 134.11 9.25 M29.8 129.25 C50.25 104.14, 70.64 80.73, 134.11 9.25 M35.44 128.86 C71.85 87.55, 109.99 42.17, 136.47 12.63 M35.44 128.86 C58.84 101.94, 81.08 75.95, 136.47 12.63 M40.43 129.22 C64.79 100.17, 92.65 70.6, 138.18 16.77 M40.43 129.22 C68.16 97.78, 95.16 66.15, 138.18 16.77 M46.07 128.82 C84.84 84.97, 123.11 42.14, 140.54 20.15 M46.07 128.82 C81.95 86.46, 118.78 44.02, 140.54 20.15 M51.06 129.18 C76.91 96.92, 107.75 67.35, 141.59 25.03 M51.06 129.18 C72.65 103.3, 95.19 78.11, 141.59 25.03 M56.04 129.54 C85.2 96.1, 115.43 60.45, 140.68 32.19 M56.04 129.54 C73.64 108.78, 92.11 89.8, 140.68 32.19 M61.69 129.15 C94.28 94.9, 123.12 57.15, 140.41 38.58 M61.69 129.15 C78.43 109.06, 95.24 89.62, 140.41 38.58 M66.67 129.51 C84.74 110.72, 104.23 88.01, 140.81 44.23 M66.67 129.51 C82.08 112.65, 97.77 95.25, 140.81 44.23 M72.32 129.12 C95.46 104.17, 115.25 77.55, 140.55 50.63 M72.32 129.12 C97.92 98.41, 123.89 70.13, 140.55 50.63 M77.3 129.48 C89.23 114.64, 106.81 97.18, 140.29 57.02 M77.3 129.48 C93.22 110.84, 109.79 93.27, 140.29 57.02 M82.95 129.08 C98.2 111.79, 114.86 91.69, 140.68 62.67 M82.95 129.08 C103.71 106.53, 124.06 82.88, 140.68 62.67 M87.93 129.44 C104.82 108.83, 120.05 89.8, 140.42 69.06 M87.93 129.44 C97.86 117.46, 108.99 103.81, 140.42 69.06 M92.92 129.8 C105.99 111.71, 122.72 95.98, 140.16 75.46 M92.92 129.8 C103.16 117.2, 113.7 103.87, 140.16 75.46 M98.56 129.41 C109.64 120.17, 116.65 107.98, 140.55 81.11 M98.56 129.41 C107.18 118.2, 117.03 108.63, 140.55 81.11 M103.55 129.77 C117.4 116.64, 128.6 99.62, 140.29 87.5 M103.55 129.77 C116.17 115.52, 128.07 100.73, 140.29 87.5 M109.19 129.37 C122.69 113.93, 133.68 103.67, 140.03 93.9 M109.19 129.37 C117.02 120.33, 123.67 111.99, 140.03 93.9 M114.84 128.98 C119.89 123.72, 127.9 116.37, 140.42 99.54 M114.84 128.98 C122.88 121.34, 129.81 111.84, 140.42 99.54 M121.14 127.83 C127.8 121.65, 135.08 114.44, 140.82 105.19 M121.14 127.83 C129.6 119.11, 136.05 110.28, 140.82 105.19 M124.81 129.7 C128.46 124.85, 136.03 119.43, 139.9 112.34 M124.81 129.7 C128.44 124.86, 133.6 118.68, 139.9 112.34" stroke="#a5d8ff" stroke-width="0.5" fill="none"></path><path d="M32 0 M32 0 C47.83 0.49, 64.2 0.18, 108.56 0 M32 0 C53.16 -0.58, 72.36 0.33, 108.56 0 M108.56 0 C128.72 1.23, 141.74 10.49, 140.56 32 M108.56 0 C131.02 -2.01, 138.55 10.01, 140.56 32 M140.56 32 C138.59 47.61, 141.08 60.69, 140.56 97.44 M140.56 32 C140.16 48.68, 140.42 64.45, 140.56 97.44 M140.56 97.44 C139.11 118.62, 129.33 131.06, 108.56 129.44 M140.56 97.44 C140.48 117.17, 130.8 128.12, 108.56 129.44 M108.56 129.44 C80.18 128.69, 50.48 128.19, 32 129.44 M108.56 129.44 C87.1 130.96, 65.3 129.47, 32 129.44 M32 129.44 C10.69 130.16, 1.1 117.7, 0 97.44 M32 129.44 C9.94 127.47, -0.69 117.41, 0 97.44 M0 97.44 C-1.94 82.03, -1.86 70.6, 0 32 M0 97.44 C-0.05 74.1, -0.35 49.45, 0 32 M0 32 C0.32 10.3, 11.23 1.57, 32 0 M0 32 C1.55 11.53, 8.6 0.04, 32 0" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g><g transform="translate(635.1074480900246 61.111310323078214) rotate(0 26.045989990234375 22.5)"><text x="0" y="0" font-family="Virgil, Segoe UI Emoji" font-size="36px" fill="#1e1e1e" text-anchor="start" style="white-space: pre;" direction="ltr" dominant-baseline="text-before-edge">M3</text></g><g stroke-linecap="round" transform="translate(876.6759665981052 10) rotate(0 70.27765909830737 64.72230275471975)"><path d="M7.86 8.16 C7.86 8.16, 7.86 8.16, 7.86 8.16 M7.86 8.16 C7.86 8.16, 7.86 8.16, 7.86 8.16 M3.66 19.09 C6.36 15.11, 10.08 9.2, 18.1 2.48 M3.66 19.09 C7.37 14.51, 12.41 8.73, 18.1 2.48 M2.75 26.24 C12.6 16.88, 18.73 8.42, 24.4 1.33 M2.75 26.24 C8.94 20.87, 12.99 14.34, 24.4 1.33 M2.48 32.64 C10.13 25.2, 14.53 19.29, 30.7 0.18 M2.48 32.64 C10.7 25.08, 16.3 16.55, 30.7 0.18 M2.88 38.28 C10.82 28.01, 18.46 20.84, 34.37 2.05 M2.88 38.28 C11.94 26.28, 21.2 16.57, 34.37 2.05 M2.62 44.68 C11.66 31.57, 21.15 22.6, 39.36 2.41 M2.62 44.68 C12.31 34.4, 21.99 22.43, 39.36 2.41 M2.36 51.07 C17.07 32.73, 34.62 14.81, 45 2.02 M2.36 51.07 C13.59 38.57, 25.47 25.42, 45 2.02 M2.75 56.72 C14.64 43.37, 27.69 30.26, 49.99 2.38 M2.75 56.72 C14.01 44.59, 25.54 32.63, 49.99 2.38 M2.49 63.11 C21.7 40.05, 38.96 19.16, 55.63 1.98 M2.49 63.11 C13.13 50.56, 24.85 38.21, 55.63 1.98 M2.88 68.76 C20.18 52.02, 34.01 30, 60.62 2.34 M2.88 68.76 C14.65 54.83, 25.68 42.49, 60.62 2.34 M2.62 75.16 C19.24 55.42, 37.5 31.21, 66.26 1.95 M2.62 75.16 C16.49 57.79, 32.78 42.2, 66.26 1.95 M2.36 81.55 C23.19 56.95, 45.26 30.43, 71.25 2.31 M2.36 81.55 C29.45 49.89, 56.38 17.96, 71.25 2.31 M2.76 87.2 C20.19 67.11, 36.53 46.48, 76.23 2.67 M2.76 87.2 C25.87 61.35, 47.53 34.68, 76.23 2.67 M2.49 93.59 C23.02 67.22, 43.88 42.3, 81.88 2.27 M2.49 93.59 C32.35 58.09, 64.68 22.62, 81.88 2.27 M2.89 99.24 C24.13 71.32, 48.31 47.1, 86.86 2.63 M2.89 99.24 C25.69 72.5, 49.39 47.19, 86.86 2.63 M1.97 106.39 C31.67 74.77, 57.71 39.1, 92.51 2.24 M1.97 106.39 C30.37 73.52, 57.92 41.75, 92.51 2.24 M3.68 110.52 C25.7 84.34, 44.88 61.19, 97.49 2.6 M3.68 110.52 C38.83 69.65, 74.71 29.71, 97.49 2.6 M4.73 115.41 C38.84 77.57, 69.92 38.37, 103.14 2.21 M4.73 115.41 C24.58 91.85, 45.55 68.29, 103.14 2.21 M7.09 118.79 C43.41 72.67, 83.11 28.8, 108.12 2.57 M7.09 118.79 C43.76 75.76, 80.22 32.87, 108.12 2.57 M9.45 122.17 C41 86.39, 72.12 47.63, 113.77 2.17 M9.45 122.17 C44.27 80.83, 81.03 40.36, 113.77 2.17 M12.47 124.79 C51.81 78.36, 92.66 33.41, 118.76 2.53 M12.47 124.79 C34.09 100.56, 56.91 73.96, 118.76 2.53 M15.49 127.42 C50.38 89.72, 83.72 50.57, 123.74 2.89 M15.49 127.42 C43.33 93.03, 74.52 58.8, 123.74 2.89 M19.82 128.53 C48.88 96.38, 76.63 64.05, 127.42 4.76 M19.82 128.53 C56.15 86.54, 91.5 44.5, 127.42 4.76 M24.81 128.89 C59.64 88.59, 90.91 50.8, 130.44 7.39 M24.81 128.89 C61.87 85.98, 98.94 43.6, 130.44 7.39 M29.8 129.25 C57.32 96.02, 88.97 62.25, 134.11 9.25 M29.8 129.25 C57.12 99.6, 82.55 69.44, 134.11 9.25 M35.44 128.86 C73.36 84, 114.39 39.46, 136.47 12.63 M35.44 128.86 C60.11 99.65, 85.37 70.82, 136.47 12.63 M40.43 129.22 C65.61 98.06, 92.47 68.44, 138.18 16.77 M40.43 129.22 C68.31 98.76, 94.83 69.1, 138.18 16.77 M46.07 128.82 C75.4 96.79, 100.21 62.23, 140.54 20.15 M46.07 128.82 C67.14 106.2, 88.07 81.88, 140.54 20.15 M51.06 129.18 C74.91 98.51, 101.66 68.08, 141.59 25.03 M51.06 129.18 C69.62 107.83, 87.9 86.91, 141.59 25.03 M56.04 129.54 C80.21 100.03, 108.5 70.11, 140.68 32.19 M56.04 129.54 C76.96 104.29, 97.42 81.56, 140.68 32.19 M61.69 129.15 C88.13 99.14, 119.37 66.32, 140.41 38.58 M61.69 129.15 C83.76 103.45, 106.65 76.4, 140.41 38.58 M66.67 129.51 C91.78 96.53, 120.05 65.3, 140.81 44.23 M66.67 129.51 C87.75 104.21, 109.83 80.95, 140.81 44.23 M72.32 129.12 C95.44 106.06, 117.04 81.23, 140.55 50.63 M72.32 129.12 C86.99 111.07, 103.14 91.08, 140.55 50.63 M77.3 129.48 C98.44 101.63, 119.94 75.61, 140.29 57.02 M77.3 129.48 C92.69 112.4, 108.22 94.03, 140.29 57.02 M82.95 129.08 C106.55 102.17, 127.58 77.54, 140.68 62.67 M82.95 129.08 C105.06 103.01, 126.7 78.23, 140.68 62.67 M87.93 129.44 C97.23 116.18, 111.65 102.77, 140.42 69.06 M87.93 129.44 C106.78 108.96, 125.52 86.71, 140.42 69.06 M92.92 129.8 C100.73 119.81, 113.64 106.92, 140.16 75.46 M92.92 129.8 C108.62 112.31, 124.73 94.15, 140.16 75.46 M98.56 129.41 C113.04 111.71, 130.62 91.89, 140.55 81.11 M98.56 129.41 C109.05 118.6, 119.29 106.72, 140.55 81.11 M103.55 129.77 C118.89 112.89, 133.84 96.4, 140.29 87.5 M103.55 129.77 C118.25 114.05, 130.17 99.52, 140.29 87.5 M109.19 129.37 C114.76 122.63, 120.71 114.5, 140.03 93.9 M109.19 129.37 C116.67 120.29, 124.47 110.74, 140.03 93.9 M114.84 128.98 C123.76 118.31, 132.58 108.77, 140.42 99.54 M114.84 128.98 C124.39 117.53, 134.61 107.42, 140.42 99.54 M121.14 127.83 C129.77 119.27, 137 113.13, 140.82 105.19 M121.14 127.83 C127.73 121.64, 133.72 112.94, 140.82 105.19 M124.81 129.7 C129.87 123.19, 133.68 115.78, 139.9 112.34 M124.81 129.7 C128.89 124.36, 135.39 118.16, 139.9 112.34" stroke="#a5d8ff" stroke-width="0.5" fill="none"></path><path d="M32 0 M32 0 C58.73 1.42, 87.92 1.33, 108.56 0 M32 0 C53.14 0.05, 76.05 -0.65, 108.56 0 M108.56 0 C130.87 -1.75, 138.81 10.1, 140.56 32 M108.56 0 C128.35 -2.2, 142.4 9.13, 140.56 32 M140.56 32 C139.9 53.28, 141.82 72.49, 140.56 97.44 M140.56 32 C139.64 54.32, 140.08 77.59, 140.56 97.44 M140.56 97.44 C140.49 117.38, 130.68 128.29, 108.56 129.44 M140.56 97.44 C142.56 117.4, 131.78 130.89, 108.56 129.44 M108.56 129.44 C90.54 129.85, 74.82 128.97, 32 129.44 M108.56 129.44 C78.63 129.36, 49.23 128.46, 32 129.44 M32 129.44 C10.04 127.73, -0.6 117.59, 0 97.44 M32 129.44 C8.53 131.25, 1.2 117.13, 0 97.44 M0 97.44 C1.77 82.99, -0.87 69.63, 0 32 M0 97.44 C0.58 73.49, 0.7 50.68, 0 32 M0 32 C1.35 11.42, 8.87 0.04, 32 0 M0 32 C0.48 10.65, 9.66 0.81, 32 0" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g><g transform="translate(923.8981040492771 61.11131032308003) rotate(0 25.30799102783203 22.5)"><text x="0" y="0" font-family="Virgil, Segoe UI Emoji" font-size="36px" fill="#1e1e1e" text-anchor="start" style="white-space: pre;" direction="ltr" dominant-baseline="text-before-edge">M4</text></g><g stroke-linecap="round" transform="translate(1164.8611704508462 10) rotate(0 70.27765909830737 64.72230275471975)"><path d="M7.86 8.16 C7.86 8.16, 7.86 8.16, 7.86 8.16 M7.86 8.16 C7.86 8.16, 7.86 8.16, 7.86 8.16 M3.66 19.09 C10.61 11.15, 16.13 4.23, 18.1 2.48 M3.66 19.09 C7.76 15.2, 11.61 9.03, 18.1 2.48 M2.75 26.24 C8.1 17.99, 13.98 10.52, 24.4 1.33 M2.75 26.24 C8.7 19.36, 12.47 13.41, 24.4 1.33 M2.48 32.64 C9.82 21.9, 21.25 11.1, 30.7 0.18 M2.48 32.64 C11.04 23.89, 19.76 13.91, 30.7 0.18 M2.88 38.28 C9.48 29.72, 16.82 22.46, 34.37 2.05 M2.88 38.28 C12.05 28.94, 20.13 17.48, 34.37 2.05 M2.62 44.68 C18.02 28.64, 29.93 15.45, 39.36 2.41 M2.62 44.68 C10.39 35, 19.17 24.06, 39.36 2.41 M2.36 51.07 C17.45 35.5, 31.8 17.66, 45 2.02 M2.36 51.07 C19.87 32.87, 35.66 13.63, 45 2.02 M2.75 56.72 C14.6 43.57, 25.67 33.97, 49.99 2.38 M2.75 56.72 C13.66 42.44, 24.71 29.66, 49.99 2.38 M2.49 63.11 C24.75 39.65, 44.26 16.84, 55.63 1.98 M2.49 63.11 C17.84 43.4, 35.55 25.06, 55.63 1.98 M2.88 68.76 C21.35 44.49, 41.59 26, 60.62 2.34 M2.88 68.76 C15.92 53.95, 28.57 38.22, 60.62 2.34 M2.62 75.16 C14.04 60.07, 27.4 44.4, 66.26 1.95 M2.62 75.16 C22.37 50.72, 43.01 27.75, 66.26 1.95 M2.36 81.55 C26.97 52.25, 53.83 22.3, 71.25 2.31 M2.36 81.55 C18.75 62.32, 33.32 45.39, 71.25 2.31 M2.76 87.2 C23.83 58.7, 47.25 33.95, 76.23 2.67 M2.76 87.2 C26.94 59.23, 51.68 32.93, 76.23 2.67 M2.49 93.59 C31.88 59.66, 62.55 23.74, 81.88 2.27 M2.49 93.59 C21.81 71.33, 40.57 49.15, 81.88 2.27 M2.89 99.24 C34.56 63.71, 62.54 29.63, 86.86 2.63 M2.89 99.24 C26.46 73.93, 48.67 46.17, 86.86 2.63 M1.97 106.39 C25.42 81.72, 42.55 56.9, 92.51 2.24 M1.97 106.39 C23.45 82.33, 46.22 56.01, 92.51 2.24 M3.68 110.52 C24.65 86.72, 48.55 59.75, 97.49 2.6 M3.68 110.52 C38.15 70.27, 73.56 30.22, 97.49 2.6 M4.73 115.41 C34.86 79.39, 68.82 41.4, 103.14 2.21 M4.73 115.41 C39.11 77.86, 70.32 38.75, 103.14 2.21 M7.09 118.79 C45.76 75, 84.36 29.28, 108.12 2.57 M7.09 118.79 C35.32 83.67, 64.38 50.68, 108.12 2.57 M9.45 122.17 C44.51 79.22, 83.23 37.67, 113.77 2.17 M9.45 122.17 C49.81 76.99, 87.86 32.57, 113.77 2.17 M12.47 124.79 C47.63 85.82, 79.46 46.91, 118.76 2.53 M12.47 124.79 C49.07 83.11, 83.22 43.3, 118.76 2.53 M15.49 127.42 C49.54 88.93, 80.43 49.78, 123.74 2.89 M15.49 127.42 C57.12 80.33, 98.47 32.2, 123.74 2.89 M19.82 128.53 C46.91 95, 76.29 62.34, 127.42 4.76 M19.82 128.53 C48.86 94.39, 79.2 62.09, 127.42 4.76 M24.81 128.89 C52.99 91.99, 86.93 56.07, 130.44 7.39 M24.81 128.89 C61.12 88.75, 95.27 48.5, 130.44 7.39 M29.8 129.25 C61.83 93.71, 94.78 55.57, 134.11 9.25 M29.8 129.25 C64.61 88.77, 98.4 50.91, 134.11 9.25 M35.44 128.86 C62.1 97.13, 91.74 67.01, 136.47 12.63 M35.44 128.86 C68.13 90.13, 102.88 51.08, 136.47 12.63 M40.43 129.22 C66.43 97.71, 95.04 65.93, 138.18 16.77 M40.43 129.22 C76.9 86.12, 113.71 45.61, 138.18 16.77 M46.07 128.82 C79.06 91.38, 108.54 52.43, 140.54 20.15 M46.07 128.82 C71.38 97.7, 96.29 69.52, 140.54 20.15 M51.06 129.18 C74.3 103.78, 96.22 75.16, 141.59 25.03 M51.06 129.18 C80.67 94.51, 111.16 60.29, 141.59 25.03 M56.04 129.54 C80.37 104.49, 102.11 76.55, 140.68 32.19 M56.04 129.54 C87.05 92.64, 119.87 55.98, 140.68 32.19 M61.69 129.15 C84.87 102.43, 105.7 76.8, 140.41 38.58 M61.69 129.15 C91.77 94.57, 123.7 58.46, 140.41 38.58 M66.67 129.51 C93.42 100.24, 116.89 73.8, 140.81 44.23 M66.67 129.51 C81.95 110.9, 99.64 92.7, 140.81 44.23 M72.32 129.12 C88.15 114.08, 101.86 95.96, 140.55 50.63 M72.32 129.12 C98.83 97.63, 124.41 67.08, 140.55 50.63 M77.3 129.48 C96.7 106.12, 114.25 83.11, 140.29 57.02 M77.3 129.48 C99.43 104.02, 120.38 77.76, 140.29 57.02 M82.95 129.08 C99.94 111.32, 114.22 92.47, 140.68 62.67 M82.95 129.08 C105.12 103.25, 129.22 76.33, 140.68 62.67 M87.93 129.44 C100.67 113.01, 115.29 99.16, 140.42 69.06 M87.93 129.44 C100.74 113.73, 114.21 99.58, 140.42 69.06 M92.92 129.8 C109.31 110.09, 126.55 92.84, 140.16 75.46 M92.92 129.8 C109.71 110.45, 126.66 90.5, 140.16 75.46 M98.56 129.41 C112.76 111.15, 128.59 93.46, 140.55 81.11 M98.56 129.41 C113.42 112.89, 127.76 96.33, 140.55 81.11 M103.55 129.77 C110.34 120.07, 120.15 107.91, 140.29 87.5 M103.55 129.77 C113.76 117.96, 124.89 107.42, 140.29 87.5 M109.19 129.37 C119.69 121.04, 125.18 107.99, 140.03 93.9 M109.19 129.37 C118.28 119.84, 124.68 110.68, 140.03 93.9 M114.84 128.98 C126.01 115.53, 133.34 105.57, 140.42 99.54 M114.84 128.98 C125.28 117.39, 134.59 105.12, 140.42 99.54 M121.14 127.83 C127.6 120.96, 134.61 111.08, 140.82 105.19 M121.14 127.83 C127.4 119.9, 134.04 113.18, 140.82 105.19 M124.81 129.7 C129.73 127.22, 131.65 122.49, 139.9 112.34 M124.81 129.7 C130.25 123.63, 137.25 116.77, 139.9 112.34" stroke="#a5d8ff" stroke-width="0.5" fill="none"></path><path d="M32 0 M32 0 C52.95 -0.25, 70.43 -0.22, 108.56 0 M32 0 C48.95 -0.32, 66.42 -0.72, 108.56 0 M108.56 0 C128.03 -0.96, 141.57 8.88, 140.56 32 M108.56 0 C129.69 1.05, 140.68 9.28, 140.56 32 M140.56 32 C138.66 52.31, 140.54 75.72, 140.56 97.44 M140.56 32 C140.71 57.77, 140.69 81.38, 140.56 97.44 M140.56 97.44 C141.91 120.22, 128.83 128.78, 108.56 129.44 M140.56 97.44 C140.33 118.45, 130.69 130.44, 108.56 129.44 M108.56 129.44 C83.3 130.07, 56.76 130.45, 32 129.44 M108.56 129.44 C90.85 129.95, 73.34 128.48, 32 129.44 M32 129.44 C11.93 130.83, 1.62 119.9, 0 97.44 M32 129.44 C10.09 131.01, 2.29 120.9, 0 97.44 M0 97.44 C0.27 76.48, 0.97 59.82, 0 32 M0 97.44 C-1.44 80.72, -0.35 62.87, 0 32 M0 32 C1.76 9.28, 11.41 -1.16, 32 0 M0 32 C0.89 10.94, 8.82 -1.26, 32 0" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g><g transform="translate(1212.083307902018 61.111310323078214) rotate(0 24.9119873046875 22.5)"><text x="0" y="0" font-family="Virgil, Segoe UI Emoji" font-size="36px" fill="#1e1e1e" text-anchor="start" style="white-space: pre;" direction="ltr" dominant-baseline="text-before-edge">M5</text></g><g stroke-linecap="round"><g transform="translate(448.85564332742865 74.71205041713347) rotate(0 64.80316793177394 0.010252337586734939)"><path d="M-0.22 -1.19 C21.75 -1.15, 109.31 -0.3, 131.4 0.07 M-1.79 0.8 C20.05 0.99, 108.09 0.94, 130.38 1.21" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g><g transform="translate(448.85564332742865 74.71205041713347) rotate(0 64.80316793177394 0.010252337586734939)"><path d="M100.16 11.09 C108.34 9.96, 117.35 7.36, 129.23 2.16 M101.23 11.78 C108.92 8.74, 114.36 7.08, 130.41 0.39" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g><g transform="translate(448.85564332742865 74.71205041713347) rotate(0 64.80316793177394 0.010252337586734939)"><path d="M100.26 -9.43 C108.4 -5.15, 117.37 -2.33, 129.23 2.16 M101.33 -8.74 C109.1 -7.38, 114.51 -4.66, 130.41 0.39" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g></g><mask></mask><g stroke-linecap="round"><g transform="translate(1025.3010401904444 74.35037689856381) rotate(0 65.74518743233875 0.37192585615639473)"><path d="M0.67 -1.09 C22.58 -0.89, 110.08 0.01, 131.93 0.44 M-0.44 0.95 C21.31 1.38, 109.26 2.02, 131.19 1.78" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g><g transform="translate(1025.3010401904444 74.35037689856381) rotate(0 65.74518743233875 0.37192585615639473)"><path d="M101.18 12.69 C111.95 8.77, 123.28 3.48, 129.85 2.48 M102.11 11.2 C111.09 8.77, 117.86 7.76, 131.05 1.62" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g><g transform="translate(1025.3010401904444 74.35037689856381) rotate(0 65.74518743233875 0.37192585615639473)"><path d="M101.18 -7.83 C111.83 -4.82, 123.15 -3.18, 129.85 2.48 M102.11 -9.32 C111.23 -6.33, 118 -1.92, 131.05 1.62" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g></g><mask></mask><g stroke-linecap="round"><g transform="translate(535.5555216471354 23.847293217977494) rotate(0 -39.07079118713736 63.384118265955294)"><path d="M0.33 0.06 C-12.58 21.49, -65.41 106.78, -78.47 127.72 M-0.95 -0.95 C-13.38 20.23, -63.12 104.91, -76.13 126.15" stroke="#e03131" stroke-width="1" fill="none"></path></g></g><mask></mask><g stroke-linecap="round"><g transform="translate(471.11114501953125 23.847293217977494) rotate(0 33.54061588000815 65.77923307788114)"><path d="M0.44 0.65 C11.36 22.5, 54.62 109.83, 65.68 131.62 M-0.79 -0.06 C10.49 21.39, 56.73 107.61, 67.88 129.76" stroke="#e03131" stroke-width="1" fill="none"></path></g></g><mask></mask><g stroke-linecap="round"><g transform="translate(1160.0001017252603 150.06958325703908) rotate(0 -70.34697142037089 29.833639633967778)"><path d="M-0.17 -0.63 C-11.86 9.48, -46.44 60.48, -69.72 60.45 C-93 60.43, -128.03 9.45, -139.84 -0.79 M-1.72 1.65 C-13.07 11.42, -44.31 58.83, -67.44 58.57 C-90.57 58.31, -128.32 9.95, -140.52 0.12" stroke="#f08c00" stroke-width="1" fill="none"></path></g><g transform="translate(1160.0001017252603 150.06958325703908) rotate(0 -70.34697142037089 29.833639633967778)"><path d="M-114.43 11.51 C-121.69 8.84, -132.85 3.3, -142.17 0.93 M-113.21 12.02 C-119.73 10.31, -127.47 5.82, -139.59 -0.03" stroke="#f08c00" stroke-width="1" fill="none"></path></g><g transform="translate(1160.0001017252603 150.06958325703908) rotate(0 -70.34697142037089 29.833639633967778)"><path d="M-128.99 25.97 C-131.34 18.48, -137.63 8.09, -142.17 0.93 M-127.77 26.48 C-130.49 21.02, -134.47 12.8, -139.59 -0.03" stroke="#f08c00" stroke-width="1" fill="none"></path></g></g><mask></mask><g stroke-linecap="round"><g transform="translate(865.9022896169854 170.68042197593786) rotate(0 -70.1646959640085 29.73714597252956)"><path d="M0.39 -0.18 C-11.12 9.76, -45.23 60.75, -68.75 60.8 C-92.27 60.85, -128.85 10.14, -140.72 0.1 M-0.86 -1.32 C-12.54 8.79, -46.73 58.63, -69.62 59.1 C-92.51 59.56, -126.53 11.61, -138.21 1.48" stroke="#f08c00" stroke-width="1" fill="none"></path></g><g transform="translate(865.9022896169854 170.68042197593786) rotate(0 -70.1646959640085 29.73714597252956)"><path d="M-111.87 15.52 C-119.05 9.67, -128.88 6.43, -137.25 3.29 M-111.8 14.96 C-120.39 10.8, -127.95 6.78, -137.45 1.09" stroke="#f08c00" stroke-width="1" fill="none"></path></g><g transform="translate(865.9022896169854 170.68042197593786) rotate(0 -70.1646959640085 29.73714597252956)"><path d="M-126.98 29.41 C-129.36 18.99, -134.28 11.23, -137.25 3.29 M-126.91 28.85 C-131.17 20.54, -134.28 12.42, -137.45 1.09" stroke="#f08c00" stroke-width="1" fill="none"></path></g></g><mask></mask></svg>
```bash
bash
	--- ls YES
	     --- cp ? NO
	          # while copy in progress: no place to do this
	          # wait until task done and shell allow us
	           --- pwd ? 
	     
ps # show processes
```
- is it possible to run `bash` inside `bash`? Yes
```bash
bash
   |___ bash # subshell of above 
            --- pwd
            --- zsh
                   --- csh
                          --- ksh
                                 --- pwd
                                 --- bash 
                                 # if exit, go 1 step back
                                 # if KILLED, to patternt of where it was
    
```

```bash
ps # show 
```
- `process ID` = `PID` of `ps` changes every time as `ps` task is 2 print exiting processes and terminate
- `PID` of `bash` is same. Interactive processes are like this = endless life time processes. 
![](ps_processes.png)
- `exit` or `Ctrl+D` (left Ctrl)

```bash
bash
   |___ vi
            --- :! pwd # temporary subshell is opended
            --- :! --- bash # if more than 1 line bash command is needed
                            # line of commands    
```

###### 7 notes

**LPIC 1 concepts** 
1. `Linux` assign a number to each `file`, called `inode#`
2. `Linux` assign a number to each `user` , called `UID` = `User Identity`
3. `Linux` assign a number to each `Group`, called `GID` = `Group Identity`
4. `Linux` assign a number to each `Process`, called `PID` = `Process Identity`

**LPIC 2 concepts**
1. `mail server` by default at any `Linux`. For internal email between users of this `Linux`
2. `router` by default (software) . routing table . Off by default
	- command to start
3. `firewall`: Kernel itself handle this functionality.
	- Interfaces for configuring firewall = to write rules : `firewalld`, `ufw`, `ipchains`,`iptables`, etc 


###### **LPIC 1 concepts details** 
1. `inode#`
```bash
ls -i # to watch inode,
      # random number allocation to same file
ls -li
```

- `inode table` when disk/partition is formatted
	- contains more columns [more on inode](https://docs.rackspace.com/docs/what-are-inodes-in-linux) 

| inode#      | filename                |
| ----------- | ----------------------- |
| 1           |                         |
| 2           | write related file name |
|             |                         |
| 200_000_000 |                         |
![inode ](https://premaseem.wordpress.com/wp-content/uploads/2016/02/linux_inode_diagram.gif)
- number of `inode` is function of 
	1. `partition size` 
	2. type of `file system`

- What is the maximum number of files? = number of `inode`s
	- if small size files and `inode` finished, no other file can be made even if half of hard is empty. Like Car plate `پلاک`
	- block size is something else
	- delete file $\to$ make `inode` free
	
```
inode      size     address
35324      10G     /root/1403/aba/02/linux/class/myinfo    
53297547   2K     /opt/f1    
```

- how commands work in backend
	- `cp` - make a new file at same folder or other folder
		- 2 different file at the end of copy process
	- `rm` remove file - 
		- in graphical interface - only pointer to file is deleted 
			- pointer to file deleted
			- finename  in table will be deleted
			- summary of changes write in temp [recyclebin??]
			- Hard is not cleaned and space is not freed - `restore` in `trash`
		![file_deletion](file_deletion_process.png)
		- `rm` in `command mode`
		     - pointer to file deleted
			- finename  in table related row will be deleted
			- no information be stored
			- invalid marker on file in Harddisk $\to$ space free up  
				- recovery from backup - depends on your actions on partition
				- recovery tool capabilities: `testdick`
		- `mv` 
		     - filename in table be updated
			- no physically change on file  
			- `mv` to `/boot`  $\to$` inode` will be changed, why?
				- since partition is changed: *each partition has its own inode table* 

```bash
cd /dev
ls -l sd* # try to understand

ls -l sda*

df -h
```
- disk partition
![disk partition](disk_partition.png)

- logical vs physical partition understanding
![](disk_partition1.png)

- `mount point` -   2:20:00
    - a directory in logical domain (addressing domain) which is connected to partition in physical domain is called a `mount point`.
    - connecting is called mounting. disconnecting = unmounting 
    - hard with `n` partition needs `n` `mount point `
		- `mount` command - make connection
		- `umount` first and then do action like 

    - only these could be moved 	`/boot, /root, /home, /opt, /temp, /var` 
    - `/bin, /etc, /sbin, /lib` should not be 
	    - if `/var` moved, services might be affected

###### On Hard-disk and partitioning 
- magnetic disk $\to$ track $\to$ sector $\to$ bit (magnetic bipolar stuff which can store 1 bit of data)
- how to use a new hard? stranded partitioning = fixed size 
	1. cable connection (data) + power
	2. partitioning                                                            $\to$ `fdisk`
	3. choose filesystem
	4. format                                                                     $\to$ `mkfs`
	    - (example: ext4 $\to$ Block size (4KB)) 
	    - at the end of format we have `inode table`  
	1. mount: make a directory and point it to partition   $\to$ `mount != umount`
	2. to view                                                                      $\to$ `df -hT`

- hard devices type
	- IDE (PATA =Parallel ATA) - 2 cable each with 2 free port = 4 port. 
	 IDE cables - connectors (primary, secondary) - 
	 power cable
	 jumpers to mention which hard to be - or based on sequence of connecting to slots
		- `/dev/hda` 
		      `hdb`
			  `hdc`
			  `hdd`
	- SCSI  $\to$ card on motherboard - port # 8-1=7   or 16 -1= 15
	    - `/dev/sda` 
		      `sdb`, `sdc`, `sdd`,   ...
	- SATA = Serial ATA
		    - `/dev/sda` 
		      `sdb`, `sdc`, `sdd`,   ...
	-
	- cool disk = cool memory = pen memory = memory stick = flash memory
	 USB connected, plug&play 
		    - `/dev/sda` 
		      `sdb`, `sdc`, `sdd`,   ...
 - If system has SCSI, SATA and cool disk, first SCSI labeled and then SATA and finally cool disk.
    - SSD hard
     1. SATA - technologically is SATA
     	   - `/dev/sda` 
		    `sdb`
     2. NVMe
     	  - `/dev/nvme0n1` 
		    `nvme1n1`
		    `nvme2n1`
    - SD cards: mini/micro SD
      - `/dev/mmcblk0`
           `mmcblk1`, `...`

###### Why we partition?
- segregate `system data` from `user/services/projects data`
	- encrypt on partition
	- make read-only for backup
- speed in recovery
- access management - DB admin to only access his related partition (part)
- differentiation between services
- different file system on partition per service needs

- back up
	- data
	- block $\to$ whole partition blocks to be copied
- Low-level backup = `image` 

- LVM = Logical volume ?????????????  **3:27:00**
- dual-boot capability 


## Session 7  

```bash
root@hes:~# df -h
Filesystem                         Size  Used Avail Use% Mounted on
tmpfs                              197M  1.2M  196M   1% /run
/dev/mapper/ubuntu--vg-ubuntu--lv  8.1G  7.2G  448M  95% /
tmpfs                              985M     0  985M   0% /dev/shm
tmpfs                              5.0M     0  5.0M   0% /run/lock
/dev/sda2                          1.7G   94M  1.5G   6% /boot
tmpfs                              197M   12K  197M   1% /run/user/0
Linux_shared                       327G  312G   15G  96% /media/sf_Linux_shared
root@hes:~# ls -l sd
ls: cannot access 'sd': No such file or directory
root@hes:~# ls -l
total 8
-rw------- 1 root root  391 Oct 28 15:24 50-cloud-initbackup.yaml
drwx------ 3 root root 4096 Oct 30 06:48 snap
root@hes:~# find /  -name "sd*"



root@hes:~# cd /dev
root@hes:/dev# ls -l s*
brw-rw---- 1 root disk   8,   0 Oct 30 06:48 sda
brw-rw---- 1 root disk   8,   1 Oct 30 06:48 sda1
brw-rw---- 1 root disk   8,   2 Oct 30 06:48 sda2
brw-rw---- 1 root disk   8,   3 Oct 30 06:48 sda3
crw-rw---- 1 root cdrom 21,   0 Oct 30 06:48 sg0
crw-rw---- 1 root disk  21,   1 Oct 30 06:48 sg1
crw------- 1 root root  10, 231 Oct 30 06:48 snapshot
brw-rw---- 1 root cdrom 11,   0 Oct 30 06:48 sr0
lrwxrwxrwx 1 root root       15 Oct 30 06:04 stderr -> /proc/self/fd/2
lrwxrwxrwx 1 root root       15 Oct 30 06:04 stdin -> /proc/self/fd/0
lrwxrwxrwx 1 root root       15 Oct 30 06:04 stdout -> /proc/self/fd/1

shm:
total 0

snd:
total 0
drwxr-xr-x 2 root root       60 Oct 30 06:05 by-path
crw-rw---- 1 root audio 116,  5 Oct 30 06:48 controlC0
crw-rw---- 1 root audio 116,  3 Oct 30 06:48 pcmC0D0c
crw-rw---- 1 root audio 116,  2 Oct 30 06:48 pcmC0D0p
crw-rw---- 1 root audio 116,  4 Oct 30 06:48 pcmC0D1c
crw-rw---- 1 root audio 116,  1 Oct 30 06:05 seq
crw-rw---- 1 root audio 116, 33 Oct 30 06:48 timer
```

#### Methods of partitioning

- `MBR scheme`: master boot record = first 512 byte of Disk, ( other names `MSDOS style, MSDOS, DOS`) 
	- only 4 primary is possible 
		- extended to 16 then 64
	- size limited for each to 2 TB
- `GPT scheme` :  GUID partition Table
	- 128 partition
	- larger size till 9.5 ZB

Both limited, but differences:
1. 4 partition vs 128 primary partition
	 change 1 extended to logical     ==min12:00==

2. ????

###### `MBR scheme`
- Extended Partition will be used to make Logical partitions

| Primary Partition | Extended Partition | Logical Partition |
| :---------------: | :----------------: | :---------------: |
|       Max 4       |        n/a         |        n/a        |
|       Max 3       |       Max 1        |      Max 60       |
- example: What is partition name connected to Secondary Master $\to$ IDE
   - `hdc`
	![](partition_1.png)
- partition name on this hard
	- add number to partition name - `hdc1`, `hdc2`, .... 
![](partition_2.png)

- example: we have 3 IDE, 2 SCSI, 1 SATA and 1 flash. What is flash name?
   SCSI, SATA and flash: `sd#`
    - we have 4 then name is `sdd`
 - 1 P $\to$ `sdd1`
 - can we make Disk as 1 primary partition? Yes
 - can we make Disk as 1 extended partition? Yes. One primary was needed to be possible to be booted from 30 years ago. if it was 2nd hard.
 - partition identified by sector or cylinder number. start or end is not important
 - SAS hard on enterprise servers. 
	 - SATA with  10000 rpm ??
- is this possible? Yes
	- what happened to end of Disk? wasted - unallocated = free space
	- maximum count limit reached (one dimension of limitation) - max Disk space not met

![](partition_3.png)
	- What we can do to use unallocated space
		- format all and reparation again $\to$ ==whole data will be lost ????==
		- if allowed to miss part of data
			- sample possibilities
![](partition_4.png)
			- noting wasted: use last partition

- example: 6th SCSI hard. what is name? `sdf`
	- can label not starting from 1.
	- Normal admin will not do such.
		- start from start of Disk 
		- name starting from 1 as partition number
![](partition_5.png)
- example:
	- logical inside `extended`
	- the first logical should be `5` and  should be name in order
	- last logical number = 64
	- first `Logical` on `Extended` labeled 5
    - then we can have till 64 -  on `sdc` hard for example `sdc64`
	 ![](partition_6.png)



---

```bash
root@hes:/dev# ls -l /dev/sd*
brw-rw---- 1 root disk 8, 0 Oct 30 06:48 /dev/sda
brw-rw---- 1 root disk 8, 1 Oct 30 06:48 /dev/sda1
brw-rw---- 1 root disk 8, 2 Oct 30 06:48 /dev/sda2
brw-rw---- 1 root disk 8, 3 Oct 30 06:48 /dev/sda3
root@hes:/dev# ^C
root@hes:/dev# ls -l cdrom
lrwxrwxrwx 1 root root 3 Oct 30 06:05 cdrom -> sr0
```

---
##### filesystems

![](filesystem1.png)
- small partition $\le 2 TB \lt$  large partition

the extended filesystem $\to$  `extfs` $\to$ `ext`

- `ext` 	- linux native - 1992
	- with coming of `ext2` in few months, in early 1993, deprecated.
	- max partition size: 2GB - max single file size : 2GB
- `ext2 
	- linux native - 1993. similar to first generation with main distinction. 
	- not have `journal` functionality. hence, if `crashed`, `recovery` is slow and mostly not successful.
	- max partition size: 32TB - max single file size : 2TB

- `ext3`
	- linux native - 1999. similar to `ext2` with only adding `journal` functionality. 
	- hence, if `crashed`, `recovery` is slow and mostly not successful.
    - max partition size: 32TB - max single file size : 2TB

- what is `journal`? 
	- metadata gathered from not closed and files in use are called.  
	- application of `journal`: is for `recovery` after `crash`. This metadata is store with different method in different filesystems. 
	- save and decide / store unsaved things 
	- `crash` : edited, open changed not saved, ... like electricity : clean vs dirty. consistent vs not consistent.
	- if `crashed`, `recovery` is slow and mostly is successful.

- `ext4`
	- Linux native - 2006. similar to older generation, but have diverse changes with enhancement. enhanced for huge size. 
	- max partition size: 1 EB = 1,000,000 TB - max single file size : 16 TB
-
- Use `ext4` for personal and enterprise 

- `butterfs`
	- advanced Linux native by Oracle- 2007. similar to XFS and ext4, good for huge size partitions on very huge Disk.
	- `time shifting` functionality
	- max partition size: 16 EB = 16,000 PB - max single file size : 16 EB
		- Oracle concept: `table space`: logical -> 1 or some file
		- big table space


- `reiserfs`
	- Linux native by German guy called Reiser- 2001. similar to XFS and ext4, good for huge size. journal functionality.
	- million small files of like 1 KB
	- max partition size: 16 TB  - max single file size : 8 TB
	- versions



- `vFAT` virtual **File Allocation Table** (**FAT**)
	- Linux knows them as Virtual FAT, including FAT12, FAT16, FAT32, etc. 
	- FAT12: max partition size: 32 MB- max single file size : 32 MB
	- FAT16: max partition size: 4 GB  - max single file size : 2 GB
	-  FAT32: max partition size: 8 TB  - max single file size : 4 GB


- rest of cross-platform like `iso9660, CDFS (joliet)`
	- All are fine for using in CD, DVD, etc. Almost similar and have minor differentiation. 

-  `swap`
	- part of Linux hard file system, considered as different partition with `swap` file system.  useful in systems where RAM might become limited. 
	- whole programs stays on RAM for working. 
		- IF RAM become limited, `swap` become temporary location 

- `NFS` network file system
	- sometime in our system `mountpoint` which seems to be local but data are store on other Linux hard in network stored. 
	- NFS refer to 3 things:
		- name of service  network file sharing
		- file system of NFS 
		- NFS protocol
    - NFS service on other location and make mount point for it in local Disk.
 

- How Windows do this?
	- file sharing protocol `CIFS` old $\to$ `SMB`
	- `SIMBA` to connect Windows to Linux  

- `proc` 
	- semi filesystem with storing footprints of kernel in filesystem
	- where to see them?
		- `/proc` and `/sys`

- What is definition of `FILE SYSTEM`?
	- A `file system` is a `system`, parts which are working together, which `manage`
		- `storing` and `recovery` of files in disk. 
	

[Comparison_of_file_systems](https://en.wikipedia.org/wiki/Comparison_of_file_systems)
![](fs_comparision.png)
- practical numbers may differ
	- per need and use case we have to investigate and decide


- Mounting logic explanation - start session 2 - continue example
  ![](mount_example1.png) 
  - under `/mnt/disk2` 
  - add `SATA`
	  - `VMDK` (Virtual Machine Disk) and `dynamically allocated` - `sdb`


```shell
ls -l /dev/sd* # to get list sd? on /dev/
fdisk /dev/sdb # provide fdisk possibilities
               # n new
		              # Partition type: p primary, e extended 
		              # Partiotion number (1-4, defaulat 1)
		              # First sector (2048 - 4194303 , default 2048):
		              # Last sector , +sectors or +size{K, M, G} (2048 - 4194303 ,                                                               default 4194303):
		              # MiBi Byte - hardware 1000, software 1024
		              # Id 83 =  native Linux file system
               # p print  
               # d delete 
               # w write table to disk and exit
        # if it can not write in filesystem MBR, ask for reboot   
init 6 # reboot is needed
mkfs -t ext2 /dev/sdb1 # -t type selection
                       # -t ext2
```
- review what reported at the end 
![](mkfs_sample1.png)
- notes
	- software vs hardware size difference
	- 5%  of storage reserved for supper user
	- `df` only show `mounted` items
	- Till now, it is made but not mounted to address so that to be accessible
	- unmount `umount` physical or logical address
		- we need to be out of place to unmount!

```bash
cd /mnt #
ls
mkdir /mnt/disk2 # empty forlder 
cd disk2/
cd ..  # during mount and umount time, we should not be in folder
mount /dev/sdb1 -t ext2  /mnt/disk2/
echo $? # check what returned? 0 = done
df -h # or check 
pwd
cd dick2/
ls # not empty any more
   # lost+found dirctory
vi primary.txt # -> 1403/08/09\nThis is my PRIMARY partition. 
cat primary.txt
# history command 
```
- do same in my machine as sample
	- note the order of steps and switches

- unmounting 
```bash
umount  <> # Physical address or Logical address (Mounted on)
           # if in location: target is busy
```

- get Type of file system in `df` - `T` = `Type` column added
```bash
root@hes:~# df -hT
Filesystem                        Type    Size  Used Avail Use% Mounted on
tmpfs                             tmpfs   197M  1.1M  196M   1% /run
/dev/mapper/ubuntu--vg-ubuntu--lv ext4    8.1G  7.6G   33M 100% /
tmpfs                             tmpfs   985M     0  985M   0% /dev/shm
tmpfs                             tmpfs   5.0M     0  5.0M   0% /run/lock
/dev/sda2                         ext4    1.7G   94M  1.5G   6% /boot
Linux_shared                      vboxsf  327G  299G   28G  92% /media/sf_Linux_shared
tmpfs                             tmpfs   197M   12K  197M   1% /run/user/0
```
###### Linux books
Folder address : `D:\Hesam\Data Science\Linux` 
-  Wiley Linux.Bible.9th.Edition.pdf
- Wiley Linux Command Line and Shell.Scripting.Bible.3rd.Edition.pdf
##### What is `$?` in Bash?

- `$?` is a special parameter in Bash that holds the `exit status of the most recently executed foreground pipeline`.
- It expands to the decimal exit status of the last executed command.
- An exit status of `0` indicates success, while non-zero values indicate various types of errors or failures.

###### Key Points

- $? is typically used immediately after running a command to check its exit status.
- It can be used in conditional statements like if() { } to check if a command succeeded or failed.
- The exit status is usually a small integer value, often 0 for success and 1-255 for various error conditions.
- $? is reset to 0 after each successful command execution.
---
- **Exercise for next time:** 
we know that with `df -hT` for mounted. How we get similar information for unmounted items?

```shell
root@hes:~# df -hT
Filesystem                        Type    Size  Used Avail Use% Mounted on
tmpfs                             tmpfs   197M  1.1M  196M   1% /run
/dev/mapper/ubuntu--vg-ubuntu--lv ext4    8.1G  7.2G  444M  95% /
tmpfs                             tmpfs   985M     0  985M   0% /dev/shm
tmpfs                             tmpfs   5.0M     0  5.0M   0% /run/lock
/dev/sda2                         ext4    1.7G   94M  1.5G   6% /boot
Linux_shared                      vboxsf  327G  313G   14G  96% /media/sf_Linux_shared
tmpfs                             tmpfs   197M   12K  197M   1% /run/user/0
```
   - solution [reference](https://vitux.com/display-drives-on-linux/):
   The drives on any system can either be mounted or unmounted. The mounted drives are the ones that are ready to be accessed at any time whereas the data residing on the unmounted drives can only be accessed after these drives are mounted. 
   
	 1. `sudo fdisk -l`
	
```bash
root@hes:~# fdisk -l
Disk /dev/loop0: 4 KiB, 4096 bytes, 8 sectors
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/loop1: 73.88 MiB, 77463552 bytes, 151296 sectors
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/loop2: 272.11 MiB, 285323264 bytes, 557272 sectors
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/loop3: 505.09 MiB, 529625088 bytes, 1034424 sectors
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/loop4: 91.69 MiB, 96141312 bytes, 187776 sectors
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/loop5: 38.83 MiB, 40714240 bytes, 79520 sectors
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/sda: 10 GiB, 10737418240 bytes, 20971520 sectors
Disk model: VBOX HARDDISK
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disklabel type: gpt
Disk identifier: 8BDAD3B2-0B2C-4563-9AAB-442A602539CC

Device       Start      End  Sectors  Size Type
/dev/sda1     2048     4095     2048    1M BIOS boot
/dev/sda2     4096  3674111  3670016  1.8G Linux filesystem
/dev/sda3  3674112 20969471 17295360  8.2G Linux filesystem


Disk /dev/sdb: 1 GiB, 1073741824 bytes, 2097152 sectors
Disk model: VBOX HARDDISK
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/mapper/ubuntu--vg-ubuntu--lv: 8.25 GiB, 8854175744 bytes, 17293312 sectors
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
```

	 2. `sudo blkid`

```Shell
root@hes:~# sudo blkid
/dev/sr0: BLOCK_SIZE="2048" UUID="2024-01-11-12-47-49-66" LABEL="VBox_GAs_6.1.50" TYPE="iso9660"
/dev/mapper/ubuntu--vg-ubuntu--lv: UUID="bbe08565-5d30-42a8-bb84-2aecebbee7eb" BLOCK_SIZE="4096" TYPE="ext4"
/dev/sda2: UUID="ecb84121-5aa7-4b01-8a6d-b4433dc5e7c4" BLOCK_SIZE="4096" TYPE="ext4" PARTUUID="bfba3ee8-d758-44f6-99a8-a532f81561a7"
/dev/sda3: UUID="VEA5dH-S9Ou-ndm8-tBsu-f3bx-NefO-jA2z2Z" TYPE="LVM2_member" PARTUUID="467a3377-c857-4a25-9709-281a7bf51da9"
/dev/loop1: BLOCK_SIZE="131072" TYPE="squashfs"
/dev/loop6: BLOCK_SIZE="131072" TYPE="squashfs"
/dev/loop4: BLOCK_SIZE="131072" TYPE="squashfs"
/dev/loop2: BLOCK_SIZE="131072" TYPE="squashfs"
/dev/loop0: BLOCK_SIZE="131072" TYPE="squashfs"
/dev/sda1: PARTUUID="ca0a7439-c349-4cee-9dbf-7598c4b48a4f"
/dev/loop5: BLOCK_SIZE="131072" TYPE="squashfs"
/dev/loop3: BLOCK_SIZE="131072" TYPE="squashfs"
```

     3. `lsblk`

```shell
root@hes:~# lsblk
NAME                      MAJ:MIN RM   SIZE RO TYPE MOUNTPOINTS
loop0                       7:0    0     4K  1 loop /snap/bare/5
loop1                       7:1    0  73.9M  1 loop /snap/core22/1663
loop2                       7:2    0 272.1M  1 loop /snap/firefox/5134
loop3                       7:3    0 505.1M  1 loop /snap/gnome-42-2204/176
loop4                       7:4    0  91.7M  1 loop /snap/gtk-common-themes/1535
loop5                       7:5    0  38.8M  1 loop /snap/snapd/21759
loop6                       7:6    0 273.6M  1 loop /snap/firefox/5187
sda                         8:0    0    10G  0 disk
├─sda1                      8:1    0     1M  0 part
├─sda2                      8:2    0   1.8G  0 part /boot
└─sda3                      8:3    0   8.2G  0 part
  └─ubuntu--vg-ubuntu--lv 252:0    0   8.2G  0 lvm  /
sdb                         8:16   0     1G  0 disk
sr0                        11:0    1  61.1M  0 rom
```

	4. `sudo parted -l`

```bash 
(base) [root@ ~]# parted -l
Model: VMware Virtual disk (scsi)
Disk /dev/sda: 85.9GB
Sector size (logical/physical): 512B/512B
Partition Table: msdos
Disk Flags:

Number  Start   End     Size    Type     File system  Flags
 1      1049kB  1075MB  1074MB  primary  xfs          boot
 2      1075MB  85.9GB  84.8GB  primary               lvm


Error: /dev/sdb: unrecognised disk label
Model: VMware Virtual disk (scsi)
Disk /dev/sdb: 429GB
Sector size (logical/physical): 512B/512B
Partition Table: unknown
Disk Flags:

Error: /dev/sdc: unrecognised disk label
Model: VMware Virtual disk (scsi)
Disk /dev/sdc: 268GB
Sector size (logical/physical): 512B/512B
Partition Table: unknown
Disk Flags:

Model: Linux device-mapper (linear) (dm)
Disk /dev/mapper/centos-home: 26.8GB
Sector size (logical/physical): 512B/512B
Partition Table: loop
Disk Flags:

Number  Start  End     Size    File system  Flags
 1      0.00B  26.8GB  26.8GB  xfs


Model: Linux device-mapper (linear) (dm)
:Disk /dev/mapper/centos-swap: 4295MB
Sector size (logical/physical): 512B/512B
Partition Table: loop
Disk Flags:

Number  Start  End     Size    File system     Flags
 1      0.00B  4295MB  4295MB  linux-swap(v1)


Model: Linux device-mapper (linear) (dm)
Disk /dev/mapper/centos-root: 478GB
Sector size (logical/physical): 512B/512B
Partition Table: loop
Disk Flags:

Number  Start  End    Size   File system  Flags
 1      0.00B  478GB  478GB  xfs
```
---
- **تمرین** : روی هارد دوم خود یک پارتیشن logical به سایز 200M بسازید که ext3 فرمت شود و از مسیر  `/root/alaki/` در دسترس باشد.

2:59:50 
**Mounting Steps for reference:** 
1.  [x] cable connection (data) + power: not needed as it already exited disk
2. partitioning                                                            $\to$ `fdisk`
	 need to make an `extended` first as `Logical` could be added there
	 make 1 `extended` larger than `200 MB`
	 not work with `extended` - only to make it possible to `Logical`
		 `boot, format` not possible on `extended` 
1. choose filesystem
2. format                                                                     $\to$ `mkfs`
	- (example: ext4 $\to$ Block size (4KB)) 
	- at the end of format we have `inode table`  
3. mount: make a directory and point it to partition   $\to$ `mount != umount`
4. to view                                                                      $\to$ `df -hT`

```bash
fdisk Command (m for help): m

Help:

  DOS (MBR)
   a   toggle a bootable flag
   b   edit nested BSD disklabel
   c   toggle the dos compatibility flag

  Generic
   d   delete a partition
   F   list free unpartitioned space
   l   list known partition types
   n   add a new partition
   p   print the partition table
   t   change a partition type
   v   verify the partition table
   i   print information about a partition

  Misc
   m   print this menu
   u   change display/entry units
   x   extra functionality (experts only)

  Script
   I   load disk layout from sfdisk script file
   O   dump disk layout to sfdisk script file

  Save & Exit
   w   write table to disk and exit
   q   quit without saving changes

  Create a new label
   g   create a new empty GPT partition table
   G   create a new empty SGI (IRIX) partition table
   o   create a new empty MBR (DOS) partition table
   s   create a new empty Sun partition table


Command (m for help): p
Disk /dev/sdb: 1 GiB, 1073741824 bytes, 2097152 sectors
Disk model: VBOX HARDDISK
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disklabel type: dos
Disk identifier: 0xbbe4b1b0

Device     Boot   Start     End Sectors  Size Id Type
/dev/sdb1          2048 1048576 1046529  511M 83 Linux
/dev/sdb2       1050624 1071103   20480   10M  5 Extended
```


```bash
ls -l /dev/sd*
fdisk /dev/sdb
      p   # p   print the partition table
      n   # n new
      e
      2 # default = Enter for defualt 
      Last Sector +1G
      
 
Command (m for help): n
Partition type
   p   primary (1 primary, 1 extended, 2 free) # 
   l   logical (numbered from 5)

Select (default p): l

Adding logical partition 5
First sector (1052672-1071103, default 1052672):
Last sector, +/-sectors or +/-size{K,M,G,T,P} (1052672-1071103, default 1071103): +2M

Created a new partition 5 of type 'Linux' and of size 2 MiB.

Device     Boot   Start     End Sectors  Size Id Type
/dev/sdb1          2048 1048576 1046529  511M 83 Linux
/dev/sdb2       1050624 1071103   20480   10M  5 Extended
/dev/sdb5       1052672 1056767    4096    2M 83 Linux


Command (m for help): w
The partition table has been altered.
Calling ioctl() to re-read partition table.
Syncing disks.


root@hes:~# df -hT
Filesystem                        Type    Size  Used Avail Use% Mounted on
tmpfs                             tmpfs   197M  1.1M  196M   1% /run
/dev/mapper/ubuntu--vg-ubuntu--lv ext4    8.1G  7.6G   33M 100% /
tmpfs                             tmpfs   985M     0  985M   0% /dev/shm
tmpfs                             tmpfs   5.0M     0  5.0M   0% /run/lock
/dev/sda2                         ext4    1.7G   94M  1.5G   6% /boot
Linux_shared                      vboxsf  327G  299G   28G  92% /media/sf_Linux_shared
tmpfs                             tmpfs   197M   12K  197M   1% /run/user/0

# reboot message
init 6
ls -l /dev/sd* # root@hes:~# ls -l /dev/sd*
brw-rw---- 1 root disk 8,  0 Dec 30 15:59 /dev/sda
brw-rw---- 1 root disk 8,  1 Dec 30 15:59 /dev/sda1
brw-rw---- 1 root disk 8,  2 Dec 30 15:59 /dev/sda2
brw-rw---- 1 root disk 8,  3 Dec 30 15:59 /dev/sda3
brw-rw---- 1 root disk 8, 16 Dec 30 15:59 /dev/sdb
brw-rw---- 1 root disk 8, 17 Dec 30 15:59 /dev/sdb1
brw-rw---- 1 root disk 8, 18 Dec 30 15:59 /dev/sdb2
brw-rw---- 1 root disk 8, 21 Dec 30 15:59 /dev/sdb5

mkfs -t ext3 /dev/sdb5 # equivalent 
mkfs.ext3 /dev/sdb5
### why???
root@hes:~# mksf -t ext3 /dev/sdb5
-bash: mksf: command not found

pwd # ensure to be on /root 
mkdir /root/alaki
df -h
mount /dev/sdb5 -t ext3  /root/alaki/
mount /dev/sdb5 /root/alaki/ # format not needed. it infer itself
df -h
cd /alaki
echo "1403/08/09
This is my LOGICAL partition." > logical.txt
cat logical.txt
```


```bash
root@hes:~# mkfs.
mkfs.bfs     mkfs.btrfs   mkfs.cramfs  mkfs.ext2    mkfs.ext3    mkfs.ext4    mkfs.minix   mkfs.xfs

# not working in my Linux
```

- With `reboot`, partitions are not there any more
	- system does not know to were connect what
	- stored in RAM $\to$ we need to `persist`
	- `config` file store this located at `/etc`
		- `fstab` = file system table
		- need a row per partition

```bash
vi /etx/fstab
root@hes:~# vi /etc/fstab
# /etc/fstab: static file system information.
#
# Use 'blkid' to print the universally unique identifier for a
# device; this may be used with UUID= as a more robust way to name devices
# that works even if disks are added and removed. See fstab(5).
#
# <file system> <mount point>   <type>  <options>       <dump>  <pass>
# / was on /dev/ubuntu-vg/ubuntu-lv during curtin installation
/dev/disk/by-id/dm-uuid-LVM-cm7KMhr6LDVL7GVxYSJRkfXEtZfykJkwD4OUp0fwK0bRwpPPRjvoTor5GkNQatMU / ext4 defaults 0 1
# /boot was on /dev/sda2 during curtin installation
/dev/disk/by-uuid/ecb84121-5aa7-4b01-8a6d-b4433dc5e7c4 /boot ext4 defaults 0 1
/swap.img       none    swap    sw      0       0
~
```
###### fstab file structure 
		- 6 item with 1 space between

![](fstab.png)

|        col1         |    col2     |      col3       |    col4    |    col5     |                      col6                       |
| :-----------------: | :---------: | :-------------: | :--------: | :---------: | :---------------------------------------------: |
| Physical address or | mount pount | filesystem tipe |   option   | dump backup |                file system check                |
|       UUID or       |             |                 | example:ro |    0 no     | 0 no, 1 earliest (==only for `/`==, 2 then rest |
|        label        |             |                 |            |    1 yes    |                                                 |
###### filesystem check types 
1. `automatic`  $\to$ `/etc/fstab` 
   will be read at after reboot - if 1 or 2 $\to$  check first and then mount 
3. `manual`   $\to$ manual by admin
			`unmount ...` unmount to not corrupt data
			`fsck ....` file system check
			`mount ....` mount again
- file we write at `/etc/fstab` will be considered at next `reboot`
- how to do without reboot?
     - `mount -a` = All

--- 
- **Exercise**: how to find `Universal UniqID` of partitions in Linux? 
**Universally Unique Identifier** (**UUID**) is a [128-bit](https://en.wikipedia.org/wiki/128-bit "128-bit") 
Here are the key methods to find the UUID of partitions in Linux:
1. `tune2fs -l <partition>`
    `tune2fs -l /dev/sdb1 | grep UUID`
    `tune2fs -l /dev/sdb1 | grep UUID >> /etc/fstab  
2. `blkid`
3.  `lsblk -f` # shows UUIDs along with other partition information.
4. `ls -l /dev/disk/by-uuid`
5. `findmnt -n -o UUID /`

>  Key Points:
- These methods work for both local and remote systems
- No need for root access in most cases
- UUIDs remain consistent even if device names change
- Useful for scripting and automating system configurations
> Best Practices:
- Use UUIDs instead of device names (/dev/sdX) in fstab for reliability
- Combine with other commands like `df` or `mount` for more context
- Be aware of potential caching issues with `blkid`

By using these methods, you can reliably retrieve UUIDs for partitions in Linux, which is essential for many system administration and scripting tasks.

--- 

## Session 8
 
- get details on partition - `tune2fs -l /mnt/disk2/`
```bash
ls -l /dev/sd*
root@hes:~# tune2fs -l /dev/sdb1
tune2fs 1.47.0 (5-Feb-2023)
Filesystem volume name:   <none>
Last mounted on:          <not available>
Filesystem UUID:          a09ebe4a-f52d-47ed-b1c9-cf52175f5fe8
Filesystem magic number:  0xEF53
Filesystem revision #:    1 (dynamic)
Filesystem features:      ext_attr resize_inode dir_index filetype sparse_super large_file
Filesystem flags:         signed_directory_hash
Default mount options:    user_xattr acl
Filesystem state:         clean
Errors behavior:          Continue
Filesystem OS type:       Linux
Inode count:              130816
Block count:              130816
Reserved block count:     6540
Overhead clusters:        8283
Free blocks:              122527
Free inodes:              130805
First block:              0
Block size:               4096
Fragment size:            4096
Reserved GDT blocks:      31
Blocks per group:         32768
Fragments per group:      32768
Inodes per group:         32704
Inode blocks per group:   2044
Filesystem created:       Mon Dec 30 12:25:34 2024
Last mount time:          Mon Dec 30 12:25:43 2024
Last write time:          Mon Dec 30 12:58:18 2024
Mount count:              1
Maximum mount count:      -1
Last checked:             Mon Dec 30 12:25:34 2024
Check interval:           0 (<none>)
Lifetime writes:          12 kB
Reserved blocks uid:      0 (user root) # root
Reserved blocks gid:      0 (group root) # Group root
First inode:              11
Inode size:               256
Required extra isize:     32
Desired extra isize:      32
Default directory hash:   half_md4
Directory Hash Seed:      b9e8bb37-7c99-43dc-bc33-b9fd067ced3a
```

- Label partition : `mkfs3 -L "name" /dev/sdb5`
	- name - 1 word, unique and not a reserved Linux keywords

```bash
mkfs3 -L "backup" /dev/sdb5`
mount /dev/sdb5  /root/alaki
mount -Lbackup /root/alaki
```

- How to revise `/etc/fstab` file?
	- `UUID=`
	- `LABEL=`
- Disk usage = ` du -csh /var/ # c cummulative, h human readable, s summarize
```bash
 du -csh /var/ /bin /usr/
1.9G    /var/
0       /bin
2.0G    /usr/
3.9G    total
```
readable 
- `df -hT # h human readable, T type of file system 
--- 
**Exercise**: We can get details for mounted partitions with`df -hT`. How we can get similar details for unmounted partitions?
???

---
- `df -i` details per `inode`
```bash
root@hes:~# df -i
Filesystem                        Inodes   IUsed   IFree IUse% Mounted on
tmpfs                             251932     960  250972    1% /run
/dev/mapper/ubuntu--vg-ubuntu--lv 540672  138928  401744   26% /
tmpfs                             251932       1  251931    1% /dev/shm
tmpfs                             251932       3  251929    1% /run/lock
/dev/sda2                         114688     317  114371    1% /boot
tmpfs                              50386      33   50353    1% /run/user/0
Linux_shared                        1000 -999000 1000000     - /media/sf_Linux_shared
```

- count `inode` depends on 
	- `partition size` 
	- `format` type
- `device` does not have number - `partitions` on device got numbers
- How to identify `logical` partitions on devices?
	- start from 5 in partition numbers
- how to understand count `extended` partitions?
	- maximum possible extended is 1. It is either 0 or 1.
		- when we have `logical`, we have to have `extended` $\to$ therefore:  1 `extended`
		- at most 4 `primary` is possible
		- numbers `1, 2, 3, 4` are for `primary` or 3 `p` and 1 `e`
	- which one is `extended`?
		- each one could be
			- `fdisk -l`   # provide details for all disks
			- `fdisk -l  /dev/sdb` 
![](partition_q.png)

- `#block` * `block_size` =  Size
- How to check count logical?
	- `fdisk -l < >` 
- Check `Disk label style`, 
	- `MBR = dos`
	- `GPT` till 128 primary partition is possible
		- we do not have `logical` 
- we can change format   `fdisk  <>` then `g`
     `g   create a new empty GPT partition table`
- last possible logical is 64. If there exists number $\gt 64$ then we can ensure it is `GPT`  
- change format to `dos - MBR` again
	 `o   create a new empty MBR (DOS) partition table` 
	 partitions will be deleted and information will be lost.

- after we have done configuration, only steps are 
	- 0. cable connection
	- 4. mount 
		- not needed in graphical case

- new flash disk
	- under `/media/` # portable devices
	- `/mnt` on old devices
	- some system has both of above
	- `umount` or eject flash
- other tools for partitioning
	- `parted` # partition editor
		- `parted -l`
		- `gparted` - Gnome
- what `unmount` do
	- synch data
	- power off


- Minimum partition required for a Linux? 1
	- mount point of this = `/` 
- minimum practical = 2
	- mount points : `/` and `swap` with `swap` file system + if RAM become limited

- real memory = physical memory = RAM != virtual memory
- virtual memory
	1. page file (Windows)
	2. swap
- Least Recently Use (LRU) algorithm
![](swap.png)

- who use swap? Kernel
-  what is `mount point` of swap? Kernel does not required as it knows where it writes.
- what is reasonable / logical size of `swap`?
	- not logical to have huge as addressing of it have overhead for Kernel
	- 1.5 RAM $\le$ swap $\le$  3.5 RAM 
	- 

- RAM : 2TB, swap size? 5TB ? no ~~5TB~~
	- per use case: 8 GB at most
	- how to understand `swap` allocated volume is low or high?
- What can be done if we understand `swap` part is not enough?
![](swap_1.png)
	- `/boot` can not be `LVM` partition
	- if we have `LVM` partitions, part(s) from each can be catch and added to `swap`
		- what is `LVM`
	- if we have free space at the end of Hard, add
	- no need neighbor partition, delete and add
	- have money, buy new hard and put `swap` there
		- limited place on other hard to be added. formatted `swap` to be added
		- `swap` size issue solve, performance downgraded as `Kernel` need to manage 2 `swap` parts resources and decide
	- command to check `swap` - `free -h` 
```bash
free -h
               total        used        free      shared  buff/cache   available
Mem:           1.9Gi       322Mi       649Mi       1.1Mi       1.1Gi       1.6Gi
Swap:          1.6Gi          0B       1.6Gi
```
- `swap` with 2 other 
![](swap_3part.png)
- where is the partition`swap` located?
	- does not have mount point - not visible with `df -h` 
```bash
/dev/sda
     sda1  # --> /
     sda2  # --> /root

parted -l 
root@hes:/# lsblk
NAME                      MAJ:MIN RM   SIZE RO TYPE MOUNTPOINTS
loop0                       7:0    0     4K  1 loop /snap/bare/5
loop1                       7:1    0  73.9M  1 loop /snap/core22/1663
loop3                       7:3    0  73.9M  1 loop /snap/core22/1722
loop4                       7:4    0 273.6M  1 loop /snap/firefox/5187
loop5                       7:5    0 505.1M  1 loop /snap/gnome-42-2204/176
loop6                       7:6    0  91.7M  1 loop /snap/gtk-common-themes/1535
loop7                       7:7    0  38.8M  1 loop /snap/snapd/21759
loop8                       7:8    0  44.3M  1 loop /snap/snapd/23258
loop9                       7:9    0 273.7M  1 loop /snap/firefox/5437
sda                         8:0    0    10G  0 disk
├─sda1                      8:1    0     1M  0 part
├─sda2                      8:2    0   1.8G  0 part /boot
└─sda3                      8:3    0   8.2G  0 part  # LVM 
  └─ubuntu--vg-ubuntu--lv 252:0    0   8.2G  0 lvm  /
sdb                         8:16   0     1G  0 disk
├─sdb1                      8:17   0   511M  0 part
├─sdb2                      8:18   0     1K  0 part
└─sdb5                      8:21   0     2M  0 part
sr0  
```
- `swap` is under `LVM` part

![](partition_swap.png)
###### steps for adding to `swap` 
Almost steps of default partitioning with few differences
0. cable connection
1. partitioning                                     `fdisk`
2. file system selection 
We need to change `Id system` Linux, = `83`, to `swap` = `82`
```bash
fdisk Command (m for help): m

   l   list known partition types
   t   change a partition type
```

3. format                                             `mkswap  <>`
4. no `mount point`
5. add to system `swap`                      `swapon` and `swapoff`
6. to view                                             `free -h`


- what if still `swap` size is low?
	- make a file of 500 MB inside partition
```bash 
touch f1
echo "......." > f2 # 500 M characte is needed as each 1 char is one Byte
echo "......." >> f3 # append
# use file zero @ /dev/zero
dd if=/dev/zero  of=/root/myswap  bs=500M count=1 status=progress 
    # block size, count 
    # other usage -> low level backup

ls -lh
mkswap  /root/myswap
free -h
swapon /root/myswap
free -h
```
	- change to `swap` type
![](partition_swap_inside.png)


![](swap_dd.png)

- in operational environments, at least 3 partition is needed
	- `Kernel` not load from `LVM` partitions   # to check
	
- `kernel` write footprints at `/proc`
```bash
root@hes:~# cat /proc/swaps
Filename                                Type            Size            Used            Priority
/swap.img                               file            1640444         0               -2
```
- partition better than file
- one location is better than some locations 
- make permanent by write `/etc/fstab`
	- how to write `mount point` of `swap`
	- just something is needed to fill between spaces: `swap, /swap, none
		- `sw` instead of `defaults`
		- reboot to added to `swap` - file reeded to add
			- how to add without reboot?
				- `swapon -a`

- `kernel` has details of stuff available at `/proc`
    - `cat /proc/meminfo 
```bash
root@hes:~# cat  /proc/meminfo
MemTotal:        2015460 kB
MemFree:          446128 kB
MemAvailable:    1630164 kB
Buffers:           75848 kB
Cached:          1165844 kB
...
```
- `cat /proc/cpuinfo`
```bash
root@hes:~# cat  /proc/cpuinfo
processor       : 0
vendor_id       : GenuineIntel
cpu family      : 6
model           : 154
model name      : 12th Gen Intel(R) Core(TM) i5-1235U
stepping        : 4
cpu MHz         : 2495.976
...
```
- `cat /proc/version`  - 
```bash
cat  /proc/version
Linux version 6.8.0-45-generic (buildd@lcy02-amd64-115) (x86_64-linux-gnu-gcc-13 (Ubuntu 13.2.0-23ubuntu4) 13.2.0, GNU ld (GNU Binutils for Ubuntu) 2.42) #45-Ubuntu SMP PREEMPT_DYNAMIC Fri Aug 30 12:02:04 UTC 2024
```

###### Permissions in Linux
- how to see file permission: `ls -l`
```bash
root@hes:/# ls -l
total 1640536
lrwxrwxrwx   1 root root          7 Apr 22  2024 bin -> usr/bin
drwxr-xr-x   2 root root       4096 Feb 26  2024 bin.usr-is-merged
drwxr-xr-x   4 root root       4096 Oct  1 14:12 boot
dr-xr-xr-x   2 root root       4096 Apr 23  2024 cdrom
drwxr-xr-x  19 root root       4220 Jan  1 11:21 dev
drwxr-xr-x   2 root root       4096 Dec 30 12:01 disk2
drwxr-xr-x  98 root root       4096 Dec 30 16:23 etc
drwxr-xr-x   3 root root       4096 Oct  1 14:24 home
lrwxrwxrwx   1 root root          7 Apr 22  2024 lib -> usr/lib
drwxr-xr-x   2 root root       4096 Feb 26  2024 lib.usr-is-merged
lrwxrwxrwx   1 root root          9 Apr 22  2024 lib64 -> usr/lib64
drwx------   2 root root      16384 Oct  1 14:08 lost+found
drwxr-xr-x   3 root root       4096 Oct 26 07:29 media

```

  - 10 `-` each with meaning as
	- File type: `-`, `d`, ...
	- Permission settings:  9 items`rw-r--r--`
	- Extended attributes: dot (`.`)

| File Type         | Command to create the File | Located in           | The file type using “ls -l” is denoted using | FILE command output                               |
| ----------------- | -------------------------- | -------------------- | -------------------------------------------- | ------------------------------------------------- |
| Regular FIle      | `touch`                    | Any directory/Folder | –                                            | PNG Image data, ASCII Text, RAR archive data, etc |
| Directory File    | `mkdir`                    | It is a directory    | d                                            | Directory                                         |
| Block Files       | `fdisk`                    | /dev                 | b                                            | Block special                                     |
| Character Files   | `mknod`                    | /dev                 | c                                            | Character special                                 |
| Pipe Files        | `mkfifo`                   | /dev                 | p                                            | FIFO                                              |
| Symbol Link Files | `ln`                       | /dev                 | l                                            | Symbol link to <linkname>                         |
| Socket Files      | `socket() system call`     | /dev                 | s                                            | Socket                                            |
![](file_perm1.png)
Permissions

- User owner:  owner of file - sample `root`
- Group owner:  sample `edari`
- Others: not file owner and not in Group owner
![](file_perm2.png)
what type of permission `Ali` have? wrong as permissions are per file
- `r` (read): 4 
- `w` (write): 2
- `x` (execute): 1 - if executable file
`rwxrw-r--`
what permissions `ali` has?
- mention all he has and has not 
	- Ali on `myfile1`
		- have all permissions = all `r, w, e`
	- Sara on `myfile1`
		- only have `read` and `write`, can not `execute`

Permission of file : In the `permission value`, the first digit corresponds to the `user`, the second digit to the `group`, and the third digit to `others`.
- 3 digit number : 764 for `myfile1`
	- in real 3 other same logic is there - `sst` 
		- they may affect only if the relevant part in `user`, `group`, or `others` is `x` # @3:15:15 ???
		- s: SUID
		- s: SGID
		- t: Sticky
	-  File permission value conversion
		 - `r-xr---w-` $\to$ 542
		 - 316 (0316) $\to$ `--x--xrw-`  
			 - 2316 $\to$ `--x--srw-`  2nd `x` converted to `s`
- 4 digit number for `myfile1`: 0764
	- Owner: `rwx` = 4+2+1 = 7
	- Group: `rw-` = 4+0+0 = 4
	- Others: `r--` = 4+0+0 = 4


```bash
chmod 401 <file name> # `r-------x`
chmod 123 <file name> # `--x-w--wx`
chmod 435 <file name> # `r---wxr-x`
ls -l
```

- admin job responsibilities 
	- disk space management

## Session 9
 



missed

==My location on **2:27:32 ??? **==
## Session 10
 

==My location on **2:27:32 ??? **==

## Session 11 <!-- 1403-09-07-->
14:07 joined


exercise
2. write a line of command to - part 2 -
Part on `processes` finished


#### User and group management

```shell
useradd peter
```

1. check user is not already taken
2. assign the first existing `UID`
3. make a `GID`
4. add him to this group
	1. `opensuse` : group `users`
5. make directry of 
6. ownership and access of this dirctory to be assigned to user
7. `/etc` ?????
8. `/var/spool/mail/peter` file which stores emails related to this user
9. etcetera
10. in `/etc/passwd` = `Linux password file` make one record for this user
	1. take a look at this file: 7 columns
11. `passwd peter` 
	1. `shadowing feature` is active to make passwords invisible
	2. passwords stored at `/etc/shadow` - `SHA512`


```shel
guseradd edari
```


1. check user is not already taken
2. assign the first existing `UID`
3. make a `GID`
4. etc
5. a record for this group added to `/etc/group`
6. `gpasswd edari` 
7. `/etc/gpasswd`


```shell
useradd peter
```


difference between `ubuntu` and `centos`

exercise at class
```
groupadd it
groupadd IT
groupadd research
groupadd developers
groupadd managers
yum install - yz zsh
which zsh
which -a zsh
useradd -d /my_HHH_dir ??????????????


cat /etc/


# dar group asli esm fard are naanvested 

groups smith
groups

id peter
id  # currnet ligind user information
```


- add smith to research group
	- `vi /etc/group`
	- `usermod -G research peter`
- `groups smith`
- `usermod -Ga managers smith` # wrong
- `usermod -aG managers smith` 
- Lock/Unlock the user
	- `usermod -L smith` 
	- `usermod -U smith` 
	- `passwd -l smith` 
	- `passwd -u smith` 


- `cat /etc/passwd | grep smith`

- `usermod -s /bin/bash smith`
- `chsh` # change shell

- what are differences of `/sbin/nologin` and  `/bin/false`?
`UID` and `GID` user root: 0



in 2:55
	`redhat` based: 500 `UID` and `GID`, (from 0 to 499)
	`debian` based: 1000 `UID` and GID, from 0 to 999) 
are reserved for services.
This and other defualts are stored at `logins.def` at ???
and can be modified


```shell
su - peter
- whoami
- ls
- ls -a
- cd /etc/skel/
```


15:02 - 15:07 missed - min 1118
non-login mode  ~/ .bashrc environment


```shell
su  # means switch to root
su - zahra
```

- when files at `~/.bash_profile` runs?
	- when login
129 min
- when files at `~/.bashrs` runs?
	- when kernel ? 

```shell
.bash_logout
.bach_profile  ~./ bash_login  ???
```


```shell
ll filename # ll f1


newgrp 
```



@ min 157

#### user management
administrative like acivity in Linux:   4 person to do admin tasks
 
 - change their `UID-GID` to `0`: not proper way
 - `sudoers` - listen carefully
	 - make group : myadmin
		 - add persons to this group
		 - limit on set of commands
 - 

```shell
history 
$HISTSIZE
$HISTFILE
echo $HISTTIMEFORMAT # ???
```


- We can assign `uid` to user
home directory
- `userdel`
   - ` -r` 
- `groupdel`

I need `Windows` `bash` script to - monitor battery level continuously and make beep when power is less than 6%. - monitor battery level continuously and make beep when power is above than 96%.

##### Shadowing feature
`pwconf`

table 

##### what happens between starting up till ?


runlevels
 - BIOS (Basic Input/Output System)  $\to$ Firmware
 - hardware clock $\to$ CMOS battery
 - software clock
 -
- CHS (cylinder/head/sector)
- LBA(Logical Block Addressing)


- EFI (Extensible Firmware Interface)
- UEFI (Universal Extensible Firmware Interface) $\to$ 2005
	- 35 to 100 MB  - EFI boot partition


- MBR (Master Boot Record) 
   512 first Byte 
- 446 B (boot loader information)
- 64 B  (boot l?
- 2 B - parity check of file

Bootloaders:

| Name                                   | abb name | address               |                         |
| -------------------------------------- | -------- | --------------------- | ----------------------- |
| LILO                                   | lilo     | `/etc/lilo.conf`      |                         |
| Grand unified Bootloader (GRUB legacy) | grub     | `/boot/grub/menu.lst` | `/boot/grub/grub.conf`  |
| GRUB2                                  |          | `/boot/grub/grub.cfg` | `/boot/grub2/grub.cfg`  |



- Sample Grub file
	- General section
	- Private section(s)






Kernel ring bugger
- `dmesg` @ `/var/log/dmesg`
- 






## Session 12  <!-- 14 Azar -->
 
Missed 10 min of start

```shell
runlevel # show current and preivous runlevels
> N 5 # 5  Full multi user + graphical

# change runlevel
init 
telinit
```

- `rc` directories

```shell
init 2 # change to run level2 



startx # add graphical service
```



| service (server) |  application   | daemon (service) |
| :--------------: | :------------: | :--------------: |
|       WEB        |     apache     |      httpd       |
|       SSH        | openssh-server |       sshd       |
|       DNS        |      bind      |      named       |
|     database     |     Mysql      |      mysqld      |
|                  |                |                  |
|   cache/proxy    |     squid      |      squid       |
|                  |                | network-manager  |
- `cd /etc/init.d`


```shell
fuser 22/tcp # if provide responce
/etc/init.d/ sshd status
netstats -ntulp  | grep :22
netstats -ntulp  | grep ssh
/etc/init.d/ sshd stop
/etc/init.d/ sshd start # new process with new pid
/etc/init.d/ sshd restart
/etc/init.d/ sshd reload # send reload signal = 1 = SIGHUP to ?
kill 1 
kill -s SIGHUP 4053
```



Symbolic Link (SL)

```shell
/etc/init.d/sshd     status|stop|reload|start|restart|
            httpd
            mysqld


each service has one SL on each rc
```


SL    Snnsshd $\to$ start
SL    Knnsshd $\to$ kill


```shell
/etc/rc0.d/Knnssd
/etc/rc1.d/Knnssd
/etc/rc2.d/Knnssd
/etc/rc3.d/Knnssd
/etc/rc4.d/Knnssd
/etc/rc5.d/Knnssd
/etc/rc6.d/Knnssd
```

```shell
K\d{1,2}name  # priority with highest = 00
# sample Network is more important than SSH
```


##### commands to manage ?

difference between `redhat` vs `debian`- base
- Redhat  base
 ```shell
 1. LSB  /etc/init.d/sshd staus
 2. service sshd status
 3. chkconfig # command to manage things
	 1. chkconfig --list crond
	 2. chkconfig crond off
	 3. chkconfig crond on
	 4. chkconfig --level 135 crond on
 ----
 4. systemctl 

```

- Debian
 ```shell
 1. LSB  /etc/init.d/sshd staus
 2. service sshd status|... # recently added
 3. update-rc.d # command to manage things
	 1. update-rc.d crond defaults
	 2. update-rc.d -f dovcot remove # mailserver
	 3. update-rc.d -f dovcot stop 24 2 3 4 5 # /etc/rc[2-5].d/K24dovcot
	 4. ?
 ----
 4. systemctl 
```





##### Service managment methods

- `system V (Sysvinit)` $\to$ init (CentOS 5, older) (Ubuntu 6.06, older)
	 `service sshd stop`
- `upstart` $\to$ init (CentOS 6) (Ubuntu 6.10 to 14.10)
```shell
initctl stop sshd
chkconfig or  update-rc.d
init 0
```
- `systemd` $\to$ init (CentOS 7 onward) (Ubuntu 15.04, newer)
```shell
   systemctl stop sshd.service   # در لحظه
   systemctl stop sshd   # در لحظه
   systemctl start sshd  #  در لحظه
   systemctl enable sshd # in next boot and always
   systemctl disable sshd  # in next boot and always
   systemctl poweroff    # = init 0
```


```shell
BIOS                                   BIOS 
MBR                                    MBR 
B.L.                                   B.L.
Kernel                                 Kernel 
init                                   systemd
runlevel --> service                   target unit --> service unit
```


```shell

CentOS 5:  cat  /etc/inittab |grep initdefault
min 97?

```


write [unit] to make service up

##### systemd 
types of units
1. service          sshd.service = sshd
2. socket
3. target           multi-user.target = multi-user
4. timer
5. mount
6. path
7. slice

`/etc/systemd/system`
`/lib/systemd/system`

```shell
systemctl status sshd
journalctl -xe # to check those which have issues
systemctl --failed

systemctl -list-uinit  --type=service
```

```shell
shutdown 
-h (halt, shutdown)
-r (reboot)
-c (cancel)
-f (fast boot -> NO file system check)
-F (force filesystem check -> YES file system check )
```

##### package management

- default 
1) Redhat Base   `rpm`    *.rpm*  redhat package management
2) Debian Base   `dpkg`    *.deb  debian package management


a-b.c.d-e.f.rpm
a = package name
b = version
c = major release (major  revision)
d = minor release (minor  revision)
e = build number
f = arch


```shell
rpm
-i install
-u (update)
-U (install/update)
   -v (verbose)
   -h (hash)
-e  (erase)
-q  (query)
   -a  (list all package names installed on this system)
   -f (file)
   -l (list of all package files)
   -c (list of all package config  files)





uname -r
rpm -qa | grep ssh # 
which ssh
rpm -qf /usr/bin/ssh

rpm -qa | grep chmod
rpm -qa | grep -i chmod
which chmod
rpm -qf ???


rpm -qc openssh-clients
rpm -ql openssh-server

rpm -qlzsh | wc -l

```

exercise image

```shell
rpm -i zsh
rpm -ivh zsh
rpm -Uvh zsh


wget <address to download>


cd /media/
mkdir DVD_DRIVE

```

exercise image 

- issue with `rpm`
	- `not installing dependencies`

- Wrapper based installation to cover above shortcomings

wrapper:
```shell
1.  yum/dnf       (Redhat Base) # Yellowdog Updater Modified
/etc/yum.conf 
yum update | install | remove
2. apt           (Debian Base) # Advanced Package Tools
   apt-get update
   apt-get update 
   apt-get update
   apt-get update
   apt-get update
   apt-get update
```

- Graphical
- sandbox
	- snap - flatpack


###### How to install from local
min 205
```shell
cd /etc/yum.repos.d/
# make local 


[LocalRepo]
name=
```




## Session 13   <!-- 1403/10/05 -->

joined at 6:50
-  use `alias` for few line repetitive commands
##### Scripting 

- shell scripting
	- bash scripting

```bash
bash myscript
!rm # last use of rm will be repeated
chown root:it myscript
chmod +x myscrpit  = chmod a+x myscrpit

myscript # will not run, why?
         # command not found, currnet dircty is not part of Linux PATH
echo $PATH


```
1. put file in one of addresses in PATH list
2. `PATH=$PATH+`
3. `PATH=; .` # do not use
4.  provide path `./root/class/myclass or ./myscript

```bash
#! /bin/bash      # shebang 
ls /boot > /root/class/list1
cp /root/class/list1  /root/class/list2
#cp /root/class/list1  /root/class/list2 #
```

Good script should have
 1. `x`permission
 2. `.sh` extension
 3. `shebang` line `#!`
##### How to write a new C or `?` program
1. `apt-get update / yum update
2. `apt ` gcc, g++, ...
3. `gcc <filename> -o myapp`


```c
#include<studio.h>

int main():
{
    printf("Hi there!");
    return 0
}
```


```bash
which python3 # identify where python3 
              # for `shebang` line: #! /user/bin/python3
/usr/bin/python3

which python3.12
/usr/bin/python3.12 #! /usr/bin/python3.12

which perl
/usr/bin/perl # #! /usr/bin/perl
```
###### `bash` scripting
```bash
expr 7+8 # 7+8
expr 7 + 8 # 15
date
sleep 4 # second
echo salam # print
echo $HOME
seq 1 10 # with steps 
v1=3
v2=5
expr $v1 + $v2
v3 = `expr $v1 + $v2` # ` = $()

read age

ls - l /bin/top
which top
ls -l `which top`
ls -l $(which top)
```

```bash
#!  /bin/bash
echo "Start time is: `date`"
sleep 8
echo "End time is: `date`"
```
- read `date` command details
```bash
date +%R
date 
```

```bash
#!  /bin/bash
echo "Start time is: `date   ???? `"
sleep 8
echo "End time is: $(date ?? )"
```

```bash
#!  /bin/bash
echo "your 1st number is: $1"
echo "your 2st number is: $2"
total=`expr $1 + $2`
echo "your total is: $total"
```

`./myscript.sh 7 + 8`

```bash
#!  /bin/bash
echo -n "please enter your age: "
read age
total=`expr $age \* 365` # \ is scape character
echo "your age in days is : $total"
```

**Exercise** 
get 2 numbers from user and print sum of them
```bash
#!  /bin/bash
echo -n "please enter number 1: "
read number1
echo -n "please enter number 2: "
read number2
total=`expr $number1 \+ $number1 ` # \ is scape character
echo "sum of ? and ? is : $total"
```

```bash
#!  /bin/bash
if [ $USER = root]
    then echo "You are allowed :)"
    else echo "You are not allowed :("
fi
```

67:40

```bash # for loop
#!  /bin/bash
for i in 1 2 3 4 5
   do
      echo "your room number is: #$i " 
  done


for i in `seq 1 500`
   do
      echo "your room number is: #$i " 
      touch test$i.txt # make file
  done
```

```bash
man touch

find / -mtime -2  # 2 days
```


exercise 2 min 75:00
rewrite exercise 5000 karbar with `bash`
get 2 numbers from user and print sum of them

```bash


paste -d "@" users domain > mailing.list
 | split -200
```

min 80:00
```bash
#!  /bin/bash
`date +%F_%T`.bck



```


###### `cron`

```bash
- crond^
crontab -l --> list
crontab -r --> remove
crontab -e --> edit

```

MIN    HRS    DOM    MOY    DOW    COM
15        8        *            *           *           /rrot/class/myscript 
15        *        *            *           *           /rrot/class/myscript # every hour at 15'
*        *        *            *           *           /rrot/class/myscript # every minutes
15       17-20        *            *           *           /rrot/class/myscript # 17 till 20
15       17,20        *            *           *           /rrot/class/myscript # 17 and 20
                          0 sun    
                          1 mon
                          2 tue
                          3 wed
                          4 thu
                          5 fri    
                          6 sat
                          7 sun
                          

read from end to start to understand


`anacron`     `cron` for desktops

- every 7 minutes or every 7 hours?
exercise 3 
    how to run script with `cron` every 30second
    how to run script with `cron` every 15 min ?
    how to run script with `cron` every 5 min ?
    how to run script with `cron` every 7 min ?
    how to run script with `cron` every 3 hour ?
    how to run script with `cron` every 9 min ?

exercise 4 
memorize dictation of month and days 

##### Networking
what is computer network?
2 device connect in a medium with same protocol

OSI layers
All people seem to need data processing
Please do not Throw sausages Pizza Away

client                      Server
Application               A
Presentation             P
Session                     S
Transport                  T
Network                   N
Data Link                  D
Physical                     P
    
     ----------------


Network Interface Card (NIC)   کارت شبکه
1. Ethernet   -> eth0 `# has priority`
2. Wireless    -> wlan0 

`eht0, eth1, ...` and `wh0, .... `

###### naming approaches
1. Hostname
	- Hostname = computer_name.domain_name
		 www.google.com 
		 mail.yahoo.com
		 kashani.lpir.org
	                 TLD (top level domain)  
	                     - General TLD
	                     com, net, org, gov, edu
	                     - CC TLD
	                     .ir, fr, ca, ...
	                    SLD (Second level domain)
	                    Sub-Domain Name
	
2. Physical address - MAC address Burned, Hardware addr
3. IP Address

![parts of address](https://forum.huawei.com/enterprise/api/file/v1/small/thread/689589783975825408.png?appid=esc_en)

```bash
hostname
hostname test.lpir.org # changed temporary

# CentOS /etc/sysconfig/network
HOSTNAME= 
# CentOS7 /etc/hostname

```

####### Physical address - MAC address Burned, Hardware addr
Hexadecimal
manufacturer number   part number

```bash
yum install net-tools  --> ifconfig, rout, ...
          iproute     --> ip

ifconfig # check
         # not possible to change MAC address phusically

```

loopback IP address  147:51

####### IP address
1. IPv4 : 32 bit  -> $2^{32} = 4,294,967,296$  
![ipv4](https://upload.wikimedia.org/wikipedia/commons/6/66/IPv4_address_structure_and_writing_systems-en.svg)
`0.0.0.0` to `255.255.255.255`

2. IPv6 : 128 bit  -> $2^{128} =$ huge numbers  
![ipv6](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/IPv6_address_terminology-en.svg/720px-IPv6_address_terminology-en.svg.png)



- switch vs router (gateway)

NAT server = router with change IP functionality 
default gateway = internet

image

IP
- static 
	- servers
	- clients if less than 11
- dynamic (DHCP)     
	- `Windows` `ipconfig/release ipconfig/renew`
	- `linux` dhclient (IP, gateway, dns)
- 
```bash
ifconfig eth0 192.168.10.11 
ifconfig eth0 192.168.10.11 netmask 255.255.255.0 # (Classfull model) neteer to write netmask
ifconfig eth0 192.168.10.11/24  (CIDR Model)

                         # /24 prefix
```

- netmask
	- differentiate `netid(network)` from `hostid(host)`   # min 178

	- IP (host id) = $2^8$ = 256
	
	192.168.10.0 -> network interface
	192.168.10.255 -> broadcast 
	
	- host count = 256 - 2 

```bash
ifconfig eth0 192.168.10.11/28 # 16 subnets each with 16 hostids
                               # we need to make rout to connect these 
```

==at minute 194 =  ???==

- Debian based
 `/etc/network/interfaces`
```bash
auto enp0s3
iface enp03 inet dhcp

auto enp0s3
   iface enp03 inet static
   address 192.168.10.11
   netmask 2555.255.255.0
   gateway   192.168.10.1
   dns-nameservers   192.168.10.2


```


- Redhat based
 `/etc/network/interfaces` ????????????????
```bash
auto enp0s3
iface enp03 inet dhcp

auto enp0s3
   iface enp03 inet static
   address 192.168.10.11
   netmask 2555.255.255.0
   gateway   192.168.10.1
   dns-nameservers   192.168.10.2


```


```bash
route -n # numeric
route add defualt ????
```

###### DNS
`/etc/hosts`
`192.168.10.11   oradb.lpir.org    oradb`
`192.168.10.12   appsrv.lpir.org    appsrv`


```shell
/etc/resolve.conf
nameserver 192.168.10.1
nameserver 192.168.10.2 # go to this if upper is not proving answer
                        #
nameserver 8.8.8.8
nameserver 4.2.2.4
```


###### port
- port count $2^{16}$ = 65536 
- 0 to 1023 = privileged - well-known ports
   - page 425 426 book
- ping protocol = [Internet_Control_Message_Protocol - ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol)


```bash
wget http://www.google.com
```

###### summarizer - hash 
- hash algorithm 
```bash
cksum myfile1
md5sum myfile1
sha1sum myfile1
sha224sum myfile1
sha256sum myfile1
sha384sum myfile1
sha512sum myfile1
sha1024sum myfile1
sha32048sum myfile1
```


```bash
service network stop
systemctl stop network
ifconfig eth0 down = ifdown eth0
ifconfig eth0 up = ifup eth0


ifconfig

ip
ip address show
ip a show
ip a s
ip a

route -n # roting table
ip rout show
ip r s
ip s

# link means network card


/etc/sysconfig/network-scripts/
# in Rocky Linux 9
nmcli connection migrate

/etc/NetworkManager/sysyem-connections/


change file
systemctl restart 
```


To change network setting
- GUI :  via menu
- TUI (Text based User Interface) : `nmtui`, `ntsysv`, `nt`, `nc`, `mc` = like `nc` in Window
- CLI : `nmcli`
	
make up and down

picture

###### SSH 
- port 22

- `opensssh-client`     `openssh-server` server_A
                        `opensssh-client`                 `openssh-server` server_B

1. remote console
```bash
ssh 
```

2. secure copy
```bash
scp username_A@IP_A:/path  username_B@IP_B:/path
# similar to cp 
```


- Exam next week =  @ 13:00
