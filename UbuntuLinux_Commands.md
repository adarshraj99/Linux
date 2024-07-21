#### `ls`: 
This lists the contents of the current directory.

#### `cat`: 
It is used to read content of file after `ls` command. syntax: `cat a.txt`  

#### `cd`: 
Change directories. Use cd .. to go up one level and provide the directory name to enter a specific folder (e.g., cd documents).

#### `pwd`: 
Present working directory.

#### `mkdir`: 
To make a new directory.

#### `touch`: 
to make a new file.

#### `cp`: 
to copy source file to destination. If destination file does not exist. It is created and if already exists. It is overwritten without any warning. 

syntax:`cp a.txt b.txt`. Here content of c.txt is overwritten with content of a.txt

syntax: `cp Src_file1 Src_file2 Src_file3 Dest_directory` . Here, all source files copied to a destination directory.

syntax: `cp -R Src_directory Dest_directory` copying directories.

syntax: `cp -f [Source_file] [Destination_file]` force copy. If is used if used lacks permission to write in destination file/Directory. This deletes the destination 
file/Directory if needed.

syntax: `cp -b a.txt b.txt` .Cretes backup of the destination file with different name.

#### `mv`: 
`mv [source_file_name(s)] [Destination_path]`. To move file(s) into a destination path.
`mv [source_directory_name(s)] [Destination_directory_name]`: To move directory(s) into a destination directory.
`mv -i [source_file/directory_name(s)] [Destination_file/directory_name/path]`: with -i ,it asks before overwriting the existing file.  

#### `rm`: rm: 
This removes files/directories. syntax: `rm a.txt b.txt`
`rm -f a.txt`: force delete
`rm -i a.txt`: to ask before deleting

#### `whoami`: 
tells current username 

#### `uname -a`:
tells info about system kernel version.

#### `df`:
shows how much disk space is used and available.

#### `sudo`:
To run command with admin privileges.

#### `apt-get`:
This is package manager of Ubuntu. For install, update ,un-install softwares.

#### `man <command name>`: 
To get all details of the provided command.

#### `clear`: 
To clear terminal

#### `IP`:
uses: 
- To see IPconfiguration. Can see Internal and External IP addresses. Can assign, remove hardware IP connections.
`ip addr show`: get list of all network interfaces, their IP addresses, etc.
`ip addr add <IP_address>/<subnet_mask> dev <interface_name>`: ex: ip addr add 192.168.1.100/255.255.255.0 dev eth0.
`ip addr del <IP_address>/<subnet_mask> dev <interface_name>`: To remove IP address.
``

 #### `PS`: Prosess Status:
 By Default it shows basic listing of proceses: PID(ProcessID), TIME(CPU time used by process), CMD(Command that launched the process).
 `PS -A`: List all processes ,not just those with currrent user.
 `PS -f`: Full format listing, providing details like user, parent process ID, start time, and more.
 `PS -e`: Show all processes.
 `ps -ef`: Full format listing. Provide details like CPU and Memory usage for each process. 
 `ps -e | grep ": not tty"`:  Filters for processes without a controlling terminal (daemons).
 `ps aux`: Lists all processes with detailed information.
 `PS -u <username>`: Filter processes by username.
 `PS -x`:  Display processes not associated with a terminal.
 `PS grep`: By combining PS with grep command can filter output to find specific processes and monitor status. ex: `ps -ef | grep sshd` to check if ssh deamon is running.
 `PS grep ": not tty"`: Filters output using grep for processes with "not tty" in the TTY (terminal) column.

 Can combine different processes to run together. ex: `PS -Af` to get more informations.
 
 #### killall: 
 `killall firefix`: To kill all the firefox instances.
 `killall -e firefox`: (exact match) Kill all instances of firefox but insure exact name match.
 `sudo killall -u john`: (user) kill all instances started by john. # requires root previliges. 
 `killall -I firefox`: (Ignorecase) makes the processname match case sensitive. 
 `killall -i firefox`: (Interactive) asks for processname before killing each process.
 `killall -l`: (listall) To list all available signals.
 `killall -v`: (verbose) TO provide more detailed info of the output processes. 
 
 #### Pkill: 
 It is similar to killall command and uses same commands. But, it provides flexiblity of pattern matching. Killall is simpler to use.

 #### Top: 
 To know the heavy resource processes.

 #### unzip {options} {filename}: 
 To extract the ziped file.

 #### sort {filename}: 
 To sort files in alphabetical order.

 #### tar {options} {action} {filename} : Options is optional here. 


 #### hidden files : 
 - To hide a file .Rename it with `.` at start ex: `.mytextfile` or use `touch .myfilename`
 - To un-hide  file: Same way do remove the `.` to unhide a file. Use `ls -a` to view all the files including the hidden ones.  
 - `chmod` : To hide, can modify file permissions also to make it non-view ,non-edit.
   `chmod ugo-rwx filename`: u(user/owner) ,g(group) ,o(others). 
   to hide file from everyone for read, write ,execute including me.  Can use `ls -l` to see it. This restriction cannot undo. But, to be re-set premissions.
   `chmod u=rw,g=r,o-r filename`: to user(owner) to get read&write access, group and others will get read only access.
   `chmod a=r filename`: Everyone can read only.
 - Encryption:
   Can encrypt file to make it un-readable without a  key.
   `gpg`: Naavigate to directory while have file to encrypt .generate key-pair with `gpg --gen-key`. Then encrypt with : `gpg -c recipient_email filename`.
   `recipient_email` is the email address of the recipient who has the corresponding public key to decrypt the file.
   
