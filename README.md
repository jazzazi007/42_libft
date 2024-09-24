# 42_libft
42_libft gradded 100%
Overview
Libft is a custom implementation of standard C library functions along with additional utilities that are designed to be reused across various C projects. It serves as a foundational project aimed at understanding core functions in C and creating a useful library for future assignments.

Table of Contents
Introduction
Compilation and Setup
Mandatory Functions
Additional Functions
Technical Considerations
Testing
Introduction
Libft is a C library that replicates several essential standard library functions (such as string manipulation, memory management, etc.) and extends them with additional utility functions. These functions will serve as tools for future projects, where using the C standard library might not be allowed or available.

Compilation and Setup
To compile the library, execute the following steps:

Clone the repository:
bash
Copy code
git clone https://github.com/jazzazi007/42_libft.git
cd libft
Run the Makefile to generate the libft.a static library:
bash
Copy code
make
This will create the libft.a file that contains all implemented functions.
You can use the following additional Makefile commands:

Clean build files:
bash
Copy code
make clean
Remove all compiled files and the library:
bash
Copy code
make fclean
Rebuild the library from scratch:
bash
Copy code
make re
Mandatory Functions
Libc Functions
The following functions are re-implemented to behave like their standard C library counterparts, with each function prefixed with ft_:

Character Checks: ft_isalpha, ft_isdigit, ft_isalnum, ft_isascii, ft_isprint
String Operations: ft_strlen, ft_strlcpy, ft_strlcat
Memory Operations: ft_memset, ft_bzero, ft_memcpy, ft_memmove, ft_memchr, ft_memcmp
String Search: ft_strchr, ft_strrchr, ft_strncmp, ft_strnstr
Conversion Functions: ft_atoi
Character Conversion: ft_toupper, ft_tolower
Memory Allocation: ft_calloc, ft_strdup
Function Descriptions
ft_strlen: Returns the length of a string.
ft_memset: Fills a block of memory with a specified byte.
ft_strchr: Locates a character in a string.
ft_atoi: Converts a string to an integer.
All functions are designed to behave identically to their standard C counterparts, except they are prefixed with ft_.

Additional Functions
The following functions extend the basic functionality and provide additional utilities:

ft_substr: Creates a substring from a given string.
ft_strjoin: Joins two strings into a new string.
ft_strtrim: Removes specified characters from the beginning and end of a string.
ft_split: Splits a string into an array of strings based on a delimiter.
ft_itoa: Converts an integer into a string.
ft_strmapi: Applies a function to each character of a string to create a new string.
ft_striteri: Applies a function to each character of a string by reference.
File Descriptor Output Functions:
ft_putchar_fd: Outputs a character to a specified file descriptor.
ft_putstr_fd: Outputs a string to a specified file descriptor.
ft_putendl_fd: Outputs a string followed by a newline to a specified file descriptor.
ft_putnbr_fd: Outputs an integer to a specified file descriptor.
These additional functions make the library more versatile and useful in various programming scenarios.

Technical Considerations
Memory Management: All dynamically allocated memory must be freed to avoid memory leaks. Proper memory management is essential to ensure no memory is left allocated after the program finishes.
Global Variables: Global variables are not allowed. Any required variables should be passed as arguments or declared locally within functions.
Static Helper Functions: If a function is only used within a specific .c file, it should be declared as static to limit its scope to that file.
Makefile: The Makefile must compile the project using the flags -Wall -Wextra -Werror and must include the standard rules: all, clean, fclean, re.
Testing
Testing your functions is crucial to ensure they behave as expected. Although testing is not required for submission, it is highly recommended to create a set of test programs to validate the functionality of each function. This will also help during the peer-evaluation process.
