# Microcorruption Writeup

Challenge Page: [Reykjavik](https://microcorruption.com/cpu/debugger)

## Walkthrough
First I read the main function, It is different from the previous levels where some unlock door function was available. There are two function calls enc and #0x2400. It set breakpoint at function call to 0x2400 to see where the password is taken. Till now no password is taken therefore it should be taken and further compared in instructions from address 0x2400. These instructions are disassembled and therefore non-human readable, so now I will see each command step wise in the current instruction window. Now i remove the breakpoints. I put some random password and saw each step there-on. After some steps I could see some cmp instruction in current instruction window, comparing a value(b985) with the value stored at location -0x24(r4). This location is the place where the random password which i gave stored. Now noting down this value which is compared, I saw the next instruction as jmp. So I think 85b9 is the password in hex as the microcontroller is little-endian. Giving this as hex-encoded input door is unlocked.

## Password
`85b9`