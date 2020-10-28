PrintF Project

This is a project in which we will work on the skills to work in a group as well as our knowledge.

Members:

@adrian-blip @Sebasssssss7

Links:

Proyect:https://intranet.hbtn.io/projects/228

secrets of printf:https://www.cypress.com/file/54761/download

Compilation

Your code will be compiled this way:

$ gcc -Wall -Werror -Wextra -pedantic *.c

As a consequence, be careful not to push any c file containing a main function in the root directory of your project (you could have a test folder containing all your tests

files including main functions)

Our main files will include your main header file (holberton.h): #include holberton.h

You might want to look at the gcc flag -Wno-format when testing with your _printf and the standard printf. Example of test file that you could use:

alex@ubuntu:~/c/printf$ cat main.c 

#include <limits.h>

#include <stdio.h>

#include "holberton.h"

/**
 * main - Entry point
 *
 * Return: Always 0
 */
int main(void)
{
    int len;
    int len2;
    unsigned int ui;
    void *addr;

    len = _printf("Let's try to printf a simple sentence.\n");
    
    len2 = printf("Let's try to printf a simple sentence.\n");
    
    ui = (unsigned int)INT_MAX + 1024;
    
    addr = (void *)0x7ffe637541f0;
    
    _printf("Length:[%d, %i]\n", len, len);
    
    printf("Length:[%d, %i]\n", len2, len2);
    
    _printf("Negative:[%d]\n", -762534);
    
    printf("Negative:[%d]\n", -762534);
    
    _printf("Unsigned:[%u]\n", ui);
    
    printf("Unsigned:[%u]\n", ui);
    
    _printf("Unsigned octal:[%o]\n", ui);
    
    printf("Unsigned octal:[%o]\n", ui);
    
    _printf("Unsigned hexadecimal:[%x, %X]\n", ui, ui);
    
    printf("Unsigned hexadecimal:[%x, %X]\n", ui, ui);
    
    _printf("Character:[%c]\n", 'H');
    
    printf("Character:[%c]\n", 'H');
    _printf("String:[%s]\n", "I am a string !");
    printf("String:[%s]\n", "I am a string !");
    _printf("Address:[%p]\n", addr);
    printf("Address:[%p]\n", addr);
    len = _printf("Percent:[%%]\n");
    len2 = printf("Percent:[%%]\n");
    _printf("Len:[%d]\n", len);
    printf("Len:[%d]\n", len2);
    _printf("Unknown:[%r]\n");
    printf("Unknown:[%r]\n");
    return (0);
}
alex@ubuntu:~/c/printf$ gcc -Wall -Wextra -Werror -pedantic -Wno-format *.c
alex@ubuntu:~/c/printf$ ./printf
Let's try to printf a simple sentence.
Let's try to printf a simple sentence.
Length:[39, 39]
Length:[39, 39]
Negative:[-762534]
Negative:[-762534]
Unsigned:[2147484671]
Unsigned:[2147484671]
Unsigned octal:[20000001777]
Unsigned octal:[20000001777]
Unsigned hexadecimal:[800003ff, 800003FF]
Unsigned hexadecimal:[800003ff, 800003FF]
Character:[H]
Character:[H]
String:[I am a string !]
String:[I am a string !]
Address:[0x7ffe637541f0]
Address:[0x7ffe637541f0]
Percent:[%]
Percent:[%]
Len:[12]
Len:[12]
Unknown:[%r]
Unknown:[%r]
alex@ubuntu:~/c/printf$
We strongly encourage you to work all together on a set of tests
If the task does not specify what to do with an edge case, do the same as printf
Tasks

0. I'm not going anywhere. You can print that wherever you want to. I'm here and I'm a Spur for life mandatory
Write a function that produces output according to a format.

Prototype: int _printf(const char *format, ...);
Returns: the number of characters printed (excluding the null byte used to end output to strings)
write output to stdout, the standard output stream
format is a character string. The format string is composed of zero or more directives. See man 3 printf for more detail. You need to handle the following conversion specifiers:
c
s
%
You don’t have to reproduce the buffer handling of the C library printf function
You don’t have to handle the flag characters
You don’t have to handle field width
You don’t have to handle precision
You don’t have to handle the length modifiers
Repo:

GitHub repository: printf

1. Education is when you read the fine print. Experience is what you get if you don't mandatory
Handle the following conversion specifiers:

d
i
You don’t have to handle the flag characters
You don’t have to handle field width
You don’t have to handle precision
You don’t have to handle the length modifiers
Repo:

GitHub repository: printf

2. Just because it's in print doesn't mean it's the gospel mandatory
Create a man page for your function.

Repo:

GitHub repository: printf
File: man_3_printf
