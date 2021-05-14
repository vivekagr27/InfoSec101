# Bandit Level 8 to 9 Writeup

Author: [Vivek Agrawal](https://github.com/vivekagr27) 

Problem Page: [bandit8](https://overthewire.org/wargames/bandit/bandit9.html) 

## List of Commands Used
```
ls - list files in a directory
cat - concatenate files and print on the standard output
sort - sort lines of text files
uniq - report or omit repeated lines
```

## Walkthrough
For this level, it was given on the Bandit8 page to pick the line of text from data.txt file which occurs only once. I firstly opened the file. There were many lines of text and I needed the line which occured only once. Now I read about the commands given on the Bandit8 page.Out of these, only grep,sort,uniq was related to lines of text. grep command also didin't work as it is to be used when we know about the text in the passsword line.I used uniq -u command but got many lines printed. Then I read and again and got to know that it compares adjacent lines that whether they are same or not. Therefore to bring all lines with same text I used sort command first and then uniq command.

## Password
`UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR`

## Bash/Python script to automate the process
```
#!/bin/sh

sort ./data.txt | uniq -u
```

## Suggested modifications [Optional]
What can you do to make this level more difficult. The inherent idea should be similar.
