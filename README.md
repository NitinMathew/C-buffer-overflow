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

# Creating a vulnerable C program:
#include <string.h>
#include <stdio.h>
void main(int argc, char *argv[]) {
	copier(argv[1]);
	printf("Done!\n");
}
int copier(char *str) {
	char buffer[100];
	strcpy(buffer, str);
}
