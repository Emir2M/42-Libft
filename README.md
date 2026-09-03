*This project has been created as part of the 42 curriculum by emirhyil.*

# Libft

## Description

Libft is the first library project in the 42 curriculum. The goal of the project is to build a personal C library by reimplementing commonly used functions from the C standard library and developing additional utility functions.

The project is designed to provide a deeper understanding of how fundamental C functions work internally instead of simply relying on existing library implementations.

While developing Libft, I worked with important C concepts such as:

- Memory management
- Dynamic memory allocation
- Pointers
- String manipulation
- Memory manipulation
- File descriptors
- Function pointers
- Structures
- Linked lists
- Static libraries

The final result of the project is a static library called `libft.a`, which can be reused in future C projects.

---

## Library Overview

The library is divided into three main parts.

### Part 1 - Libc Functions

The first part consists of reimplementations of standard C library functions.

These functions reproduce the behavior of their original counterparts while using the `ft_` prefix.

#### Character checks and conversions

- `ft_isalpha`
- `ft_isdigit`
- `ft_isalnum`
- `ft_isascii`
- `ft_isprint`
- `ft_toupper`
- `ft_tolower`

#### String functions

- `ft_strlen`
- `ft_strlcpy`
- `ft_strlcat`
- `ft_strchr`
- `ft_strrchr`
- `ft_strncmp`
- `ft_strnstr`
- `ft_strdup`

#### Memory functions

- `ft_memset`
- `ft_bzero`
- `ft_memcpy`
- `ft_memmove`
- `ft_memchr`
- `ft_memcmp`
- `ft_calloc`

#### Conversion

- `ft_atoi`

---

### Part 2 - Additional Functions

The second part contains utility functions that are either not available in the standard C library or exist there in a different form.

These functions introduce more dynamic memory allocation, string processing, function pointers, and file descriptor operations.

#### String creation and manipulation

- `ft_substr`
- `ft_strjoin`
- `ft_strtrim`
- `ft_split`
- `ft_itoa`

#### String iteration

- `ft_strmapi`
- `ft_striteri`

#### File descriptor output

- `ft_putchar_fd`
- `ft_putstr_fd`
- `ft_putendl_fd`
- `ft_putnbr_fd`

---

### Part 3 - Linked Lists

The third part introduces singly linked lists using the following structure:

```c
typedef struct s_list
{
    void            *content;
    struct s_list   *next;
}   t_list;
```

The `content` pointer allows each node to store data of any type, while `next` points to the next node in the list.

The following functions provide operations for creating, traversing, modifying, deleting, and transforming linked lists:

- `ft_lstnew`
- `ft_lstadd_front`
- `ft_lstsize`
- `ft_lstlast`
- `ft_lstadd_back`
- `ft_lstdelone`
- `ft_lstclear`
- `ft_lstiter`
- `ft_lstmap`

This part of the project provides practical experience with structures, pointers to pointers, dynamic allocation, function pointers, and memory management.

---

## Instructions

### Compilation

The project includes a `Makefile` that compiles the source files and creates the static library:

```bash
make
```

After successful compilation, the following library is generated at the root of the repository:

```text
libft.a
```

The project is compiled using:

```text
cc -Wall -Wextra -Werror
```

The static library is created using the `ar` command.

### Makefile Rules

The available rules are:

```bash
make
```

Compiles the source files and creates `libft.a`.

```bash
make clean
```

Removes the generated object files.

```bash
make fclean
```

Removes the object files and the `libft.a` library.

```bash
make re
```

Performs a full recompilation by running `fclean` followed by `all`.

---

## Using Libft

Include the Libft header in your C source file:

```c
#include "libft.h"
```

For example:

```c
#include "libft.h"
#include <stdio.h>

int main(void)
{
    char *str;

    str = ft_strdup("Hello, Libft!");
    if (!str)
        return (1);
    printf("%s\n", str);
    free(str);
    return (0);
}
```

Compile the program together with the library:

```bash
cc main.c libft.a -o program
```

Then run it:

```bash
./program
```

---

## Resources

The main resources used during the development of this project were:

- The official 42 Libft subject
- Unix/Linux manual pages (`man`)
- Peer learning and discussions with other 42 students
- Internet research and technical references
- AI tools as a supplementary learning resource

For the standard library functions, manual pages were especially useful for understanding function prototypes, expected behavior, return values, and edge cases.

Peer learning was also an important part of the development process. Discussing problems and different approaches with other students helped me understand alternative ways of solving problems rather than simply finding a working implementation.

---

## AI Usage

AI was used as a learning and reasoning aid, not as a replacement for implementing the project.

My general workflow was to first read the relevant manual pages to understand the prototype, expected behavior, return values, and documented edge cases of a function. I then used AI when necessary to explore the boundaries and behavior of the function in greater depth before starting the implementation.

During implementation, when I encountered a problem that I could not solve on my own, I first discussed it with my peers. If the issue was still unclear, I researched it using internet resources and search engines.

AI was used after these steps when additional guidance was necessary. Instead of requesting the direct solution or complete implementation, I asked for simpler exercises, examples, or explanations related to the same concept. I then used those smaller problems to understand the underlying logic and return to the original problem with my own solution.

This approach allowed AI to support the learning process while keeping the reasoning, implementation, debugging, and understanding of the final code my own.