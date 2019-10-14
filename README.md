# FlopCalc
This program is designed to calculate the number of flops in a z80 CPU in a ti84+

First a little explanation of my program, I included sources where I got code I did not write. I wrote a program in assembly for the TI84+ calculator. First thing it does is initialize all my registers and variables. Then it starts an 8 Hz clock that ticks from 255. After that it skips to the inner loop and calculates flops using a pseudo-random shift-xor number generator and it adds 1 24-bit flop and subtracts 1 24-bit flop 255 times, 255 times. Then it loads register A with the value from the timer and loads register HL with this value then displays it to the screen. Next it does the same thing but it does not calculate the 24-bit floating point numbers and displays the number 1 line down. To get the number of flops you use these 2 numbers.

time1 = time for the first program to run
time2 = time for second program to run
floptime = time to calculate just 24 bit flops
flops = number of 24 bit flops calculated per second by the cpu
time1 = (255-(firstnumbergenerated))/8
time2 = (255-(secondnumbergenerated))/8
floptime = time1 - time2
flops=(2*255*255)/floptime
