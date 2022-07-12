The  _printf() function in C-programming.

_printf  is a  formatted output conversion in C program

_printf is a pseudo-recreation of the printf function.

Description

The _printf() function produces output to the standard output.The function writes how successive arguments are converted for output.

Format of the format string

The format string is a character string that begins and ends in its initial shift state, if any. The format string contains zero or more directives: ordinary characters (not %), which are copied unchanged to the output stream; and conversion specifications, each of which results in fetching zero or more subsequent arguments. Each conversion specification is initialised with the character % and ends with a conversion specifier.

Conversion specifiers

A character that specifies the type of conversion to be applied. The conversion specifiers and their meaning are:

d, i: The int argument should be signed decimal notation, and the resulting number is written.

c: The int argument is converted to a char, and the resulting character is written.

s: The const char * argument is expected to be a pointer to an array of character type (pointer to a string). Characters from the array are written up to (but not including) a terminating null byte ('\0').

%: A '%' is written. No argument is converted. The complete conversion specification is '%%'.

About Functions

int _write(char c)

This function gets a char parameter and writes the parameter to the stdout, the standard output stream.

int _print_a_char (va_list args)

This function gets a variadic arguments list, traverses the list, prints each character of char type and returns the length of the character.

int _print_a_string (va_list args)

This function gets a variadic arguments list, traverses the list, prints each string and returns the length of the string.

int _print_a_integer (va_list args)

This function gets a variadic arguments list, traverses the list, prints each number of int type and returns the length of the integer.

int _print_format (const char *format, va_list args)

This function gets a format to be printed and a variadic arguments list, next to check if the format is valid or invalid and according with the verification the resulting output is written to the standard output stream and returns the format length.

int _print_spec (char format, va_list args):

This function gets a format valid to be printed and a variadic arguments list to find the format in the list and selects the appropriate function to execute and writes the format to the standard output stream and returns the length of the valid format.

int _print_invalid_spec (char prev_format, char format, int count)

This function gets the previous format of the current format, the actual format and the current count of printed characters. Next, the invalid format is written to the standard output stream and returns the length of the invalid format.

void _recursion_integer(int a)

This function gets an integer and prints the last digit of the number as recursion is applied.

int _validate_char(char _type)

Gets a type and checks if the passed parameter is present in a structure of valid conversion specifiers. Next, returns if the parameter is valid or invalid.

Return Value

Upon successful return, the _printf() function return the number of characters printed (excluding the null byte used to end output to strings).

If an output error is encountered, a negative value is returned.

Examples

#include "main.h"

_printf("Hello World"); // the output will be: Hello World

_printf("%c", 'B'); // the output will be: B

_printf("%s", "Hello World"); // the output will be: Hello World

_printf("%!\n"); // the output will be: '%!'

_printf("Complete the sentence: You %s something, Mary White.\n", "know"); // the output will be: Complete the sentence: You know something, Mary White.

_printf("% s", "Hey"); // the output will be: Hey

_printf("% t"); // the output will be: % t

Authors

Byron November (banova18@gmail.com)

Adebimpe Akin-Ademola (adebimpefolayemi1@gmail.com).
