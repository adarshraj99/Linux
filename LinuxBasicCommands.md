#### | : 
To mix many commands. Multiple pipes are possible.

#### traceroute -4 'google.com': 
To get the nodes connection in between the connection

#### ping 'web_link':
To check connectivity

#### zip: and unzip: 

#### nano : A text editor

#### top: 

#### curl 'web_link':
to communicate with website, to send data to url

#### wget: 
to communicate with heavy data and get more data.

Linux is case sensitive. Linux donot have recyclebin.

#### chown: 
Change file owner or group

#### man: 
To get more informations about command.

#### ctrl Shift ++ : 
Zoom-in

#### top: Task manager of Linux.
To get the most resource consuming processes currently.

#### f9: 
To kill and process.

#### ps: 
To list all the processes.

#### ps -a: 
To list all the background processes. 

#### kill 'processID': 
To stop the working processes(running softwares). Can get the working processID by 'top' command.

#### Kill -9 'processID': 
To kill all the processes with this PID.

#### dif:
system disc usage

#### du: 



## File system: 

#### ls: 
for getting all children files and folders inside the present directory. 

#### ls -R: 
Listing all the sub-directories and files 'Recursively'. 

#### cd /:
'cd' takes to a directory and '/' is the root node. 

#### pwd: 
print working directory. 

#### diffrence between cd bin and cd /bin :
'/bin' is absolute path and 'bin' is relative path. Absolute path means it is starting with '/' the full path and with relative path we can only goto next file or folder.

#### cd.. : 
One folder back. 

#### mkdir 'foldername': 
making directory in pwd.

#### touch 'fileName.txt' : 
makes files with given filename.

#### mv 'fileName.txt' 'FolderName'/
mv is for moving. Here, moving fileName.txt file inside folder FolderName. 

#### cp 'fileName.txt' 'FolderName':
cp is for copy. Here, copying fileName.txt in 'FolderName' 

#### cp '/filePath' 'Folderpath': 
copying from full file and folder path.

#### touch .fileName:
To make a new hidden file named 'fileName'. It cannot be found by 'ls'.

#### ls -a : 
To see the hidden files and normal files together.

#### -c:
To count.

#### sed:

#### awk: 

To get find ,replace web data.

#### scp: 
To copy from one machine to other machine. 

#### winscp : 
To copy paste from one window to other window. 

#### ssh: 
secure shell connection. Used to make the connections from windows to mac ,linux or any vice versa. after getting the authority.



#### ls -la : 
Too get more file informations.

#### ls -lart: 
Gives list of files timesorted. l: long list, a: include hidden files, r: reverse order, t:Sort by time. 

#### cat: 
copy and see

#### less: 

#### tail: 
To see the end of the file.

#### head: 
To see the start of the file

#### rm -r foldername
Delete folder even it have files. 

#### rm -rf 'filename' or rm -rf *'fiername' : 
remove file with force. 

#### find: 
#### q! : To unsave and go outside of vim. 

#### history: 
Gives all the previous commands provided by users.  (BEWARE OF USING PASSWORD OR SENSITIVE INFO AS COMMAND AS OTHER USERS MAY SEE)

#### echo and printf: 
for printing. eg: echo printThis   ,    printf "printThis\n" (will print in nextline).

#### sudo apt install softwareName: 
To install softwares with name 'softwareName'. `apt` is package manager here. 

#### Users system: 
There are 2 users inside a system : Regular user and Super user(root user).
Regular user donot have access each other filesystrem access unless someone give it's filesystem access or someone is root user. 
After getting access use 'sudo {command_here}' to make changes. 

#### $ and #: 
$ sign means a regular user and # means root user.

#### sudo :
A normal user can write 'sudo' before any command to work as a superuser. 

#### apt:
To install and update software. It is linux package manager like pip. ex: sudo apt install zip.

#### sudo apt-get update: 
To update the list of softwares available in system. Just for downloading not installing.

#### sudo apt-get upgrade:
To install the list of system softwares. 

#### sudo su: 
After getting the other user's access. If starting any command with 'sudo su', system assumes you are superuser and gives all types of access. It can be dangerous as all can delete important files.

#### ls -l:  
![git](https://github.com/adarshraj99/Linux/assets/122180050/8a3e898c-b2a5-4f0b-897d-db8f774d7b8f)
Gives permission details of users, groups, others respectively. Here, 1.txt, 2.txt are file names. -rw_: is user access (read,write,no execute). r_ _: is for group (read only) and same read only is for others also.
'Harry2' is file name and second 'harryname' is group name . __

#### chmod 'number' 'filename': 
To update the the user,group,others access. 
Number: Get 'number' from https://chmodcommand.com/ by providing different access and accrodingly 'fileName' access will change.
Here ,'Number' is coming from Binary to Integer format. checked is 1 and unchecked is 0. So, if owner is read, write ,noExecute. it is 110.

#### chgrp: 

#### chown: 
To change groups.


## vim: (a text editor): 
Used to update the texts of a file by commandline. 

#### vim 'fileName.txt':  
To open the command line text Editor.
After opening vim editor click 'i' then can write. 

#### q :
To directly exit without saving.
#### wq : 

To save and exit. Can use 'escape',':','wq'.

#### How to search and areplace, 

#### scp:To send file from one to other servers:

#### How to check linux version and other software versions

#### grep: 
To find patterns ....................many optins are in geeksforgeeks. 

#### uname -a: 
system info

#### copy paste, find and replace ,regex search, pattern match, 
