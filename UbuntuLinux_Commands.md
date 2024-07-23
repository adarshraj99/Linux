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
- 
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




 
