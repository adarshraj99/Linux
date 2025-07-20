#### | : 
To mix many commands. Multiple pipes are possible.

#### traceroute -4 'google.com': 
To get the nodes connection in between the connection

#### ping 'web_link':
To check connectivity

#### nano : 
A text editor

#### curl 'web_link':
to communicate with website, to send data to url

#### wget: 
to communicate with heavy data and get more data. To download files.

Linux is case sensitive. Linux donot have recyclebin.

#### chown:
Change file owner or group

#### man: 
To get more informations about command.

#### top: Task manager of Linux.
To get the most resource consuming processes currently. Type `k` to get kill mode. Type PID to kill. 
To force kill type `9` or `KILL`

#### ps: 
To list all the processes.

#### ps -a: 
To list all the background processes. 

#### kill 'processID': 
To stop the working processes(running softwares). Can get the working processID by 'top' command.  `CTRL+C` to escape.

#### Kill -9 'processID': 
To kill all the processes with this PID.

#### ls: 
for getting all children files and folders inside the present directory. 

#### ls -R: 
Listing all the sub-directories and files 'Recursively'. 

#### ls -la : 
Too get more file informations.

#### ls -lart: 
Gives list of files timesorted. l: long list, a: include hidden files, r: reverse order, t:Sort by time. 

#### ls -l:  
![git](https://github.com/adarshraj99/Linux/assets/122180050/8a3e898c-b2a5-4f0b-897d-db8f774d7b8f)
Gives permission details of users, groups, others respectively. Here, 1.txt, 2.txt are file names. -rw_: is user access (read,write,no execute). r_ _: is for group (read only) and same read only is for others also.
'Harry2' is file name and second 'harryname' is group name . __

#### diffrence between cd bin and cd /bin :
'/bin' is absolute path and 'bin' is relative path. In absolute path, it can be traversed from root or other folder and relative path is for current file or folder.

#### cd .. : 
One folder back. 

#### sed , awk : both are text editors

#### scp: 
To copy from one machine to other machine. 

#### winscp : 
To copy paste from one window to other window. 

#### ssh: 
secure shell connection. Used to make the connections from windows to mac ,linux or any vice versa. after getting the authority.

#### q! : To unsave and go outside of vim. 

#### history: 
Gives all the previous commands provided by users.  (BEWARE OF USING PASSWORD OR SENSITIVE INFO AS COMMAND AS OTHER USERS MAY SEE)

#### sudo apt install softwareName: 
To install softwares with name 'softwareName'. `apt` is package manager here. 

#### Users system: 
There are 2 users inside a system : Regular user(sudo user) and Super user(root user).
Regular user donot have access each other filesystrem access unless someone give it's filesystem access or someone is root user. 
After getting access use 'sudo {command_here}' to make changes. 

#### $ and #: 
$ sign means a regular user and # means root user.

#### sudo :
A normal user can write 'sudo' before any command to work as a superuser. with regular user creds only. limited access than root. More secure.
uses: Change file access, install/uninstall apps, system

#### root: 
all accesses .Have root password ,used rarely. Very high risk.
uses: Sesurity management, BIOS change.

#### apt:
To install and update software. It is linux package manager like pip. ex: `sudo apt install zip`.

#### sudo apt-get update: 
To update the list of softwares available in system. Just for downloading not installing.

#### sudo apt-get upgrade:
To install the list of system softwares. 1st update then, upgrade.

#### sudo su: 
After getting the other user's access. If starting any command with 'sudo su', system assumes you are superuser and gives all types of access. It can be dangerous as all can delete important files.

#### chmod 'number' 'filename': 
To update the user, group, others access. 
Number: Get 'number' from https://chmodcommand.com/ by providing different access and accrodingly 'fileName' access will change.
Here ,'Number' is coming from Binary to Integer format. checked is 1 and unchecked is 0. So, if owner is read, write ,noExecute. it is 110. 

## vim: (a text editor): 
Used to update the texts of a file by commandline. 

#### vim 'fileName.txt':  
To open the command line text Editor.
After opening vim editor click 'i' then can write. 

#### q :
To directly quit without saving in Vim.  

#### wq : 
Save changes and quit. 

To save and exit. Can use 'escape',':','wq'.


#### scp: To send file from one to other servers:

#### How to check linux version and other software versions:
linux version: `apt ubuntu --version`
software version: `apt list --installed`

#### uname -a: 
system info
