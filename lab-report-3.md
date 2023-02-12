# **Researching Commands**
I am using find command as one command to invest in to show more uses of it. 

The first one I am using is `find . -type f -name file`. This search in the current directory and its subdirectories to find a file named file. 
`.` means the current directory, `-type f` refers to look for file. I will be using in the Abernathy directory.

For reference of 4 command I am showing, visite [this](https://linuxhandbook.com/find-command-examples/)

Example 1: 
```
find . -type f -name ch3.txt
./ch3.txt
```
Example 2:
```
find -type f -name ch9.txt
./ch9.txt
```
We can see that the whether or not a exists under the the current directory, and we're sure that it is a file, and not a directory.

The second one I am showing is find . `-type f -iname SEARCH_NAME`. By default, the find command is case sensitive. 
We can run a case-insensitive search with the given name by using `-iname` instead of `-name`.

Example 1: (In Abernathy directory)
```
find -type f -iname CH3.txt
./ch3.txt
```
Example 2: (In Abernathy directory)
```
find -type f -iname CH9.txt
./ch9.txt
```
You can see that even I capitaliza both c and h for both example, but I am still able to find the file that I am looking for, this could be really helpful.

The third one I am showing is `find . -type f -name "*.java" -o -name "*.txt"`. The `-o` stand for the logical OR. This help search multiple files with multiple extensions.

Example 1: (In Abernathy directory)
```
find . -type f -name "*.java" -o -name "*.txt"
./ch1.txt
./ch14.txt
./ch15.txt
./ch2.txt
./ch3.txt
./ch6.txt
./ch7.txt
./ch8.txt
./ch9.txt
```
Example 2:
```
cd ../Berk/
305$ cd ../Berk/
[cs15lwi23abj@ieng6-203]:Berk:306$ find . -type f -name "*.java" -o -name "*.txt"
./CH4.txt
./ch1.txt
./ch2.txt
./ch7.txt
```
Since we only have text files contains in those directories, so we only get the list of all the text files in current directory. But in other case where we have multiple file extensions,
then it will be useful to use this to find multiple files at once. 

The last one I am showing is `find . -size -50k`. This looks for files in current directory that is less than 50 kilobyte. We can also change - to +, k to G, and more.

Example 1: (In Abernathy directory)
```
-size -50k
.
./ch1.txt
./ch14.txt
./ch15.txt
./ch2.txt
./ch3.txt
./ch6.txt
./ch7.txt
./ch9.txt
```
Example 2:
```
find . -size +50k
./ch8.txt
```
We can see that only ch8 is greater than 50kb, and is the biggest file in this directory. This can be useful because you can check if certain files are taking up too much
memories and you might want to delete or modify it.

And that is 4 alternative ways to use find command, it is really useful at finding for the specific stuff. 
