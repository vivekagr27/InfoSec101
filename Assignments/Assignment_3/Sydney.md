# Microcorruption Writeup

Challenge Page: [Sydney](https://microcorruption.com/cpu/debugger)

## Walkthrough
First I read the main function, there I could find that access is granted if value in r15 register is not zero. I then saw the Check password function. I could see that it was comparing a certain 2 bytes hexadeimal value(0x3f55 in my case) with first 2 characters of password and similarly further 6 bytes. So I proceeded by providing password as `3f55` in hexadecimal format as the password and set the breakpoint at the jump instruction. For the first 2 bytes of password to be correct it shoud have skipped the jump instruction but it didnot happen. Now I read about the MSP430 microcontroller and found that it was little-endian, that is it read bytes from less significant to more, therefore I provided `55f3` as the password which successfully skipped the jump instruction. I similarly provided the other pairs of bytes in reverse order and the door got unlocked. Password is provided in hexadecimal format.

## Password
`553f5a6e69752e6f`