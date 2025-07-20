#### /mnt/d
Goto from default(root directory) linux path to drive

#### cd ~ :
To move to home directory. typically it is /home/username or /root if in root. 

#### cd /:
'cd' takes to root directory. This is top most level containing directories like: bin, mnt, home.

#### ls : 
This lists the contents of the current directory.

#### cat : 
It is used to read content of file after `ls` command. syntax: `cat a.txt`  

#### less:
To read big file lines like cat. But, it dosen't load all the texts at once like cat. Here, scroll to see more

#### tail: 
To see the endlines of the file. 

#### head: 
To see the startlines of the file

#### cd : 
Change directories. Use cd .. to go up one level and provide the directory name to enter a specific folder (e.g., cd documents).

#### pwd : 
Present working directory.

#### mkdir : 
To make a new directory.

#### echo "file contents" > filename.txt :
overwrite a file texts.

#### echo "file contents" >> filename.txt :
append to the existing file content

#### cat > filename.txt :
Then, 
line1
line2
To create multi line file content. This overwrites previous one. Save with CTRL+D
`cat -n filename.txt` : To see line numbers with outputs


#### To update specific line with othe line.
`sed -i '2s/.*/Line 3 text/' myfile.txt` :
 
sed : is a text editor, -i : interactive, 2 : line number 2, s/.*/Line3/ : substitute entire line with 'Line3 text'. 

#### Search and replace: 
`find . -type f -name "*.txt" -exec sed -i 's/old_word/new_word/g' {} \;`:
find . -type f -name "*.txt":   This command locates all files with the .txt extension recursively.
i : interactive, g: global replacement flag(not just the first one),  {}: Placeholder for each word found by find, \ : Marks the end of the -exec command, 

#### touch filename.extention : 
to make a new file.

#### mkdir DirectoryName :
create a new folder.

#### cp : 
to copy source file to destination. If destination file does not exist. It is created and if already exists. It is overwritten without any warning. 

syntax:`cp a.txt b.txt`. Here contents of a.txt is copied and a new file b.txt is created with same contents. If b.txt pre-existed, operation will ask for confirmation to overwrite b.txt or might fail.

syntax: `cp Src_file1 Src_file2 Src_file3 Dest_directory` . Here, all source files copied to a destination directory. ex: `cp file.txt /mnt/foldername/folder`

syntax: `cp -R Src_directory Dest_directory` copying directories. 

syntax: `cp -f [Source_file] [Destination_file]` force copy. If is used if used lacks permission to write in destination file/Directory. This deletes the destination 
file/Directory if needed.

syntax: `cp -b a.txt b.txt` .Cretes backup of the destination file with different name.


#### mv : 
Can be used for both moving and renaming. 

`mv old_folder_name new_folder_name`. To rename to new filename. 

`mv -f old_folder_name new_folder_name` to forcefully overwrite if a file with same new filename already exists. 

`mv [source_file_name(s)] [Destination_path]` or `mv filename.txt ../previous_directory`:  To move file(s) into a destination path.

`mv [source_directory_name(s)] [Destination_directory_name]`: To move directory(s) into a destination directory.

`mv -i [source_file/directory_name(s)] [Destination_file/directory_name/path]`: with -i ,it asks before overwriting the existing file.  


#### `rm` : 
This removes files, directories. syntax: `rm a.txt b.txt`

`rm -f a.txt`: force delete

`rm -i a.txt`: to ask before deleting

`rm -r foldername`: To delete directory and the onsode directories recursively.

`rm -rf 'filename' or rm -rf *'fiername' : remove file with force.


#### find: 
`find . -name "*.txt"` : To find files with name having `.txt` init recursively (all the child folders)
to find onlt in same folder: `ls *.txt`  `ls *'practice'*`

#### Download files from url: 
Goto file and run : `wget -p "url"`

#### hidden files :  Change permissions:
 - To hide a file .Rename it with `.` at start ex: `.mytextfile` or use `touch .myfilename`
   
 - To un-hide  file: Same way do remove the `.` to unhide a file. Use `ls -a` to view all the files including the hidden ones.

 - `ls -a` : To see all the hidden files. 
   
 - `chmod` : To hide, can modify file permissions also to make it non-view ,non-edit.
   
   `chmod ugo-rwx filename`: u(user/owner) ,g(group) ,o(others).
   to hide file from everyone for read, write ,execute including me.  Can use `ls -l` to see it. This restriction cannot undo. But, to be re-set premissions.
   
   `chmod u=rw,g=r,o-r filename`: to user(owner) to get read&write access, group and others will get read only access.
   
   `chmod a=r filename`: Everyone can read only.

 - Encryption:
   Can encrypt file to make it un-readable without a  key.
   
   `gpg`: Naavigate to directory while have file to encrypt .generate key-pair with `gpg --gen-key`. Then encrypt with : `gpg -c recipient_email filename`.
   
   `recipient_email` is the email address of the recipient who has the corresponding public key to decrypt the file.
   
#### zip:
 `zip -r file.zip file.txt` : To zip a file,  `zip -r folderName.zip FolderName` : To Zip Folder,  `zip -r Foldername.zip /path/to/Folder` : To Zip specified folders.
 
#### unzip:
 To extract the ziped file. same commands like zip 

#### sort:
`ls -l`: Sort by name,  `ls -lS`: Sort by name,  `ls -lt` : by time, ls -ltr: by time in reverse.
`sort filename` : To sort lines inside file.
To sort files in alphabetical order.

#### grep: 
To search data by patterns, search text.
`grep -n 'error:' file1.txt file2.txt file3.txt` : To search lines which contains text 'error:' .
`grep "pattern" *` : Search all files in pwd.

`-n`: gives line number.
`-i`: ignore case.
`-w`: match only whole word.
`-r`: Recursively searches files in all subdirectories.
`-c`: Gives count of matching lines. 
`-v`: Gives lines that donot contain required pattern.
`-F`: Given Patterns is searched as full string, not regular expression.

`grep "^start_string" filename.txt` : `^` Mathes the begining of line.
`grep "end_string$" filename.txt` : `$` matches at line end.
`grep -E "pattern1|pattern2" filename.txt` : `-E` enables Extended match with either "pattern1" or "pattern2".
`grep "[0-9]" logfile.txt` : Find lines containing any digit.
`grep "U.e" logfile.txt` : Find "U" followed by any character, then "e"
`grep "\d{4}" logfile.txt` : Find lines with a 4-digit number (like a year)
`grep "Service \D" logfile.txt` : Find lines with "Service" not followed by a digit
`grep "logged in\s" logfile.txt` : Find "logged in" followed by a space.
`grep "User '\S+'" logfile.txt` : Find "User '" followed by non-whitespace characters
`grep "User '\w+'" logfile.txt` : Find "User '" followed by word characters
`grep "disk\W" logfile.txt` : Find "disk" followed by a non-word character

`grep "WARNING.*low" logfile.txt`: Match WARNING followed by any characters until "low"
`grep "[0-9]+" logfile.txt` : Find numbers with one or more digits
`grep "colou?r" file_with_color.txt` : Match "color" or "colour" (the "u" is optional)
`grep "\d{4}" logfile.txt` : Find lines with exactly four digits 
`grep "\d{2}:\d{2}:\d{2,}" logfile.txt` : Match lines containing a timestamp like "10:30:05"
`grep "\.[a-z]{2,5}" logfile.txt` : Find lines with . followed by 2 to 5 lowercase letters

`grep -P "\bUser\b" logfile.txt` : Find the whole word "User" (not "Users" or "Superuser") 
`grep -P "\Bser\B" logfile.txt` : Find "ser" that is not a whole word (e.g., part of "User") 
`grep "Disk (space|usage)" logfile.txt` : Find "Disk" followed by "space" or "usage"
`grep -E "ERROR|CRITICAL" logfile.txt` : Find lines containing either "ERROR" or "CRITICAL" 



#### chgrp:
To change the group ownership of files.


#### chown: 
To change the owner/group owner of files.

#### #### `diff file1.txt file2.txt`:
To get diffrence between files.
