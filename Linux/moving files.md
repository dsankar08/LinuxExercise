# Problem 

## Do in Linux

- a. Create a compressed archive named mariyam.tar.gz of the /data/mariyam directory.

- b. Transfer the archive to the /home directory on the Storage Server.

## Solution

 `tar -cf mariyam.tar mariyam/` - archiving folder
 check it by listing - `ls`
 `tar -vcf mariyam.tar` - listing files inside archived folder
 `gzip mariyam.tar` - g zipping tar file
 `mv /data/mariyam.tar.gz /home/` - move file
 
