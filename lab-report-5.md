# **Researching more Commands**
Last time, I did the exploration for find command, and this time, I am going to do some exploration on cp command. 
This command is used to copy files or group of files or directory. It creates an exact image of a file on a disk with different file name.

For reference visit [this](https://www.geeksforgeeks.org/cp-command-linux-examples/)

First one is cp with one or more arguments. `cp Src_file1 Src_file2 Src_file3 Dest_directory`. This allow us to copy all files to the Dest_directory. 
Example 1: (newDirectory is initially empty)
```
$ ls
a.txt  b.txt  newDirectory
$ cp a.txt b.txt newDirectory
$ ls newDirectory
a.txt  b.txt
```
Example 2: (newDirectory is have same files, these files will be overwritten)
```
$ cd newDirectory
$ ls
a.txt  b.txt
$ cd ..
$ ls
a.txt  b.txt  newDirectory
$ cp a.txt b.txt newDirectory
$ ls newDirectory
a.txt  b.txt
```
Copying multiple files to a directory is really useful when it comes to organizing datas, and we can also just overwritten the older version of files. 

Second one is using cp with two directory. This will need to use `-R` to recursively copy directories. `cp -R Src_directory Dest_directory`.
Example 1: (newDirectory is empty)
```
$ ls directory
a.txt  b.txt
$ cp -R directory newDirectory
$ ls newDirectory
a.txt b.txt
```
Example 2: (newDirectory already contains both text files and will be overwritten)
```
$ ls directory
a.txt  b.txt
$ ls newDirectory
a.txt  b.txt
$ cp -R directory newDirectory
$ ls newDirectory
a.txt b.txt
```
This is a sample way to transfer files over to a new directory, and it can also be use to updating the data in dest-directory. 

Third one is using `-i` behind cp for interactive copying, that way it will ask you to overwrite certain files or not. `cp -i a.txt b.txt`.
Example 1: (b.txt is being overwritten)
```
$ cp -i a.txt b.txt
cp: overwrite 'b.txt'? y
```
Example 2: (b.txt is empty)
```
$ cp -i a.txt b.txt
```
This helps preventing from overwriting data without acknowledge it, which can be really useful. 

Fourth one is to use -b to creates the backup of the destination file in the same folder with the different name and in different format. `cp -b a.txt b.txt`.
Example 1: (b.txt is not being overwritten)
```
$ ls
a.txt  b.txt
$ cp -b a.txt b.txt
$ ls
a.txt  b.txt  b.txt~
```
Example 2: (use --backup)
```
$ ls
a.txt  b.txt
$ cp --backup a.txt b.txt
$ ls
a.txt  b.txt  b.txt~
```
Creating back up file is always necessary if there is problems with the newer version of the file, This is the easy way to create a back up file. 
So that's some useful ways to use cp command, it could be handy when working with a lot of files and data.
