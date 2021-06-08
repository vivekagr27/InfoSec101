# PicoGym Web Exploitation Writeup

Author: [Vivek Agrawal](https://github.com/vivekagr27)

Challenge Page: [login](https://login.mars.picoctf.net/)

## Walkthrough
How did you solve this level? Include the complete thought process, even stuff that didn't work. Give explanations wherever necessary.
I firstly inspected the page. There in the index.js file I found a statement  written "The flag is atob(t.p)" and t.p string was also given in the file. I googled about atob function and got to know that it decodes a base64 encoded string, therefore I decoded it and got the flag.   

## Flag
`picoCTF{53rv3r_53rv3r_53rv3r_53rv3r_53rv3r}`

## Useful resources (if any)

## Suggested modifications [Optional]
What can you do to make this level more difficult. The inherent idea should be similar.