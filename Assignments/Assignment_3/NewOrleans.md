# Microcorruption Writeup

Challenge Page: [New Oreans](https://microcorruption.com/cpu/debugger/)

## Walkthrough
First I read the main function, there I could find that access is granted if value in r15 register is not zero. I then saw the Create Password function and then Check password function. I could see that it was comparing every character of password by the character at the address 0x2400(r14), similar to a loop. Also after comparing first 8 characters it puts value 1 in r15 and returns to main function where access gets granted. Thus the password is first 8 characters stored at address 0x2400.

## Password
`QR"W32j`
