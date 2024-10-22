# Libft Project - README

## Overview

Welcome to my **Libft** project! This repository contains my custom implementation of many standard C library functions, designed according to the specifications of the 42 School's **Libft** project. The goal was to create a robust and reusable library of functions that mimic the behavior of the original ones from the standard library. My implementation includes full protection against **null pointers** and ensures **safe memory management** using `malloc`. 

One key feature is that these functions are designed to never crash, even under edge cases such as bad inputs or memory allocation failures. This makes the library highly reliable, as per the project rules, which state that the program **should never crash**.

## Key Features

- **Safe Memory Management**: All `malloc` calls are checked for success, ensuring that the program handles memory allocation failures gracefully without causing segmentation faults.
- **Null Pointer Protection**: Every function carefully handles null pointers, preventing potential crashes and ensuring safe behavior.
- **Accurate Standard Function Replication**: All functions mirror the behavior of their standard library counterparts, while incorporating additional safety features.
- **Clean Makefile**: The project includes a robust Makefile that compiles the library efficiently. The object files are stored in a dedicated `obj/` directory to keep the repository organized.

## Functions Implemented

Here are some of the key functions I have implemented:

- **String Manipulation**:
  - `ft_strlen`, `ft_strdup`, `ft_strcpy`, `ft_strcat`, `ft_strjoin`, `ft_strtrim`, etc.

- **Memory Functions**:
  - `ft_memset`, `ft_memcpy`, `ft_memmove`, `ft_memchr`, `ft_memcmp`, etc.

- **Character Checks and Conversions**:
  - `ft_isalpha`, `ft_isdigit`, `ft_isalnum`, `ft_isascii`, `ft_isprint`, `ft_tolower`, `ft_toupper`, etc.

- **List Manipulation**:
  - `ft_lstnew`, `ft_lstadd_front`, `ft_lstadd_back`, `ft_lstdelone`, `ft_lstclear`, `ft_lstiter`, `ft_lstmap`, etc.

- **Additional Utility Functions**:
  - `ft_atoi`, `ft_itoa`, `ft_split`, `ft_substr`, etc.

## Project Structure

```bash
.
├── Makefile         # Handles compilation and organization of object files
├── libft.h          # Header file
├── obj/             # Directory for object files after compilation
├── *.c              # Source code implementing the functions
├── README.md        # This readme file
```

### Makefile Targets

- `make`: Compiles the library and generates `libft.a`.
- `make clean`: Removes all object files in the `obj/` directory.
- `make fclean`: Removes object files and the compiled `libft.a`.
- `make re`: Recompiles everything from scratch by running `fclean` and `make`.

## Installation and Usage

1. Clone the repository:

```bash
git clone https://github.com/ivotints/Libft.git
cd Libft
```

2. Compile the library:

```bash
make
```

This will create the `libft.a` static library.

3. To use the library in your project, include `libft.h` and link the library when compiling:

```c
#include "libft.h"
```

Then, compile your project with `libft.a`:

```bash
gcc your_file.c -L. -lft -o your_program
```

## Conclusion

This **Libft** implementation was crafted with an emphasis on reliability and code safety. With thorough protections against null pointers and failed memory allocations, the functions in this library aim to be crash-proof and maintain the expected behavior of the standard C library functions.

Feel free to explore the code, use it in your own projects, and suggest improvements!

---
