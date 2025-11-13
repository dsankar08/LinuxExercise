# Problem 

## Do in Linux

- a. Delete all lines containing word code and save results in /home/BSD_DELETE.txt file. (Please be aware of case sensitivity)

- b. Replace all occurrence of word the to their and save results in /home/BSD_REPLACE.txt file.

## Solution

- identify the word count of `the` in file
- `grep -we "the" /home/BSD.txt | wc -l`
- to delete `sed "s/\bthe\b//g" /home/BSD.txt > /home/BSD_DELETE.txt`
- check the count
- to replace `sed "s/the/their/g" /home/BSD.txt > /home/BSD_REPLACE.txt`
- check the count and replacement.
