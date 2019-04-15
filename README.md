# C-buffer-overflow
# What You Need

A 32 bit Unix/linux Machine real or virtual .
Purpose
To develop a Vulnerable program.
To develop buffer overflow exploit in linux.

# ASLR
Address Space Layout Randomization is a defense feature to make buffer overflows more difficult, most of the Unix/Linux machine uses it by default.
# To disable ASLR : 
sudo sysctl -w kernel.randomize_va_space=0

# Run the python file redirect the output of that file into some other file.
# Execute the program with this command this will disable the stack protection.
# >> gcc -m32 -ggdb -g -z execstack -no-pie -fno-stack-protector -o out filename.c
# Take this output as input of the c program:
#  >> ./cfile $(cat out) or any other method if you have.
