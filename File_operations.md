#### cd ~ :
To move to home directory.

#### ls : 
This lists the contents of the current directory.

#### cat : 
It is used to read content of file after `ls` command. syntax: `cat a.txt`  
 
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
To create multi line file content.

#### sed -i '2s/.*/Line 3 text/' myfile.txt :
To update specific line with othe line. 
sed : is a text editor, -i : interactive, 2 : line number 2, s/.*/Line3/ : substitute entire line with 'Line3 text'. 

#### touch filename.extention : 
to make a new file.

#### mkdir DirectoryName :
create a new folder.

#### cp : 
to copy source file to destination. If destination file does not exist. It is created and if already exists. It is overwritten without any warning. 

syntax:`cp a.txt b.txt`. Here contents of a.txt is copied and a new file b.txt is created with same contents. If b.txt pre-existed, operation will ask for confirmation to overwrite b.txt or might fail.

syntax: `cp Src_file1 Src_file2 Src_file3 Dest_directory` . Here, all source files copied to a destination directory.

syntax: `cp -R Src_directory Dest_directory` copying directories.

syntax: `cp -f [Source_file] [Destination_file]` force copy. If is used if used lacks permission to write in destination file/Directory. This deletes the destination 
file/Directory if needed.

syntax: `cp -b a.txt b.txt` .Cretes backup of the destination file with different name.


#### mv : 
Can be used for both moving and renaming. 
`mv old_folder_name new_folder_name`. To rename to new filename. `mv -f old_folder_name new_folder_name` to forcefully overwrite if a file with same new filename already exists. 

`mv [source_file_name(s)] [Destination_path]`. To move file(s) into a destination path.

`mv [source_directory_name(s)] [Destination_directory_name]`: To move directory(s) into a destination directory.

`mv -i [source_file/directory_name(s)] [Destination_file/directory_name/path]`: with -i ,it asks before overwriting the existing file.  


#### `rm` : 
This removes files,directories. syntax: `rm a.txt b.txt`

`rm -f a.txt`: force delete

`rm -i a.txt`: to ask before deleting

`rm -r foldername`: To delete directory and the onsode directories recursively.

#### find: 
`find . -name "*.txt"` : To find files with name having `.txt` init recursively (all the child folders)
to find onlt in same folder: `ls *.txt`  `ls *'practice'*`

#### Download files from url: 
Goto file and run : `wget -p "url"`

#### hidden files :  Change permissions:
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
   
#### zip:
 `zip -r file.zip file.txt` : To zip a file,  `zip -r folderName.zip FolderName` : To Zip Folder,  `zip -r Foldername.zip /path/to/Folder` : To Zip specified folders.
 
#### unzip:
 To extract the ziped file. same commands like zip 

#### sort:
`ls -l`: Sort by name,  `ls -lS`: Sort by name,  `ls -lt` : by time, ls -ltr: by time in reverse.
`sort filename` : To sort lines inside file.
To sort files in alphabetical order.

#### grep:

