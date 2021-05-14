# Bandit Level 10 to 11 Writeup

Author: [Vivek Agrawal](https://github.com/vivekagr27) 

Problem Page: [bandit10](https://overthewire.org/wargames/bandit/bandit11.html)

## List of Commands Used
```
ls - list files in a directory
cat - concatenate files and print on the standard output
base64 - base64 encode/decode data and print to standard output
```

## Walkthrough
It was given on the Bandit10 page that the file contained base64 command so I started with reading about base64 command in the man page and I could easily find the command to decode the file.

## Password
`IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR`

## Bash/Python script to automate the process
```
#!/bin/bash

base64 -d ./data.txt  
```

## Suggested modifications [Optional]
What can you do to make this level more difficult. The inherent idea should be similar.
