# ft_printf – Custom Implementation of printf in C

Welcome to my implementation of **ft_printf**, a **recreation of the standard C `printf` function**. This project is part of the **42 Network Common Core curriculum** and was developed using only allowed functions and features, focusing on **low-level C programming**, **variadic functions**, and **format parsing**.

---

## 📚 Project Description

The goal of the **ft_printf project** is to understand how formatted output works under the hood. I created a fully functional version of `printf` in C that handles **various format specifiers**, **flags**, **precision**, and **width modifiers**, using only a limited set of standard C functions.

This project strengthens skills in:
- **String and character manipulation**
- **Pointer arithmetic**
- **Memory management**
- **Function pointers**
- **Variadic functions (`stdarg.h`)**
- Writing **modular and reusable code**

---

## 🛠️ Skills Learned

- Mastery of **C programming**
- Implementing **variadic functions**
- Parsing **format specifiers**
- Handling **different data types and conversions**
- Writing code with **clean architecture**
- Respecting **Norminette** standards and constraints

---

## ✅ Features and Supported Specifiers

The following conversions are supported by `ft_printf`:

| Specifier | Description                            |
|-----------|----------------------------------------|
| `%c`      | Character                              |
| `%s`      | String                                 |
| `%p`      | Pointer address                        |
| `%d`      | Signed decimal integer                 |
| `%i`      | Signed decimal integer (same as `%d`)  |
| `%u`      | Unsigned decimal integer               |
| `%x`      | Unsigned hexadecimal (lowercase)       |
| `%X`      | Unsigned hexadecimal (uppercase)       |
| `%%`      | Literal percent sign                   |

All handled with **precision**, **width**, and **flag** support where applicable.

---

## 🔧 How It Works

Under the hood:
- `ft_printf` uses `va_list`, `va_start`, `va_arg`, and `va_end` from `stdarg.h` to handle an unknown number of arguments.
- The format string is parsed **character by character**.
- For each `%` format specifier, a handler function is called to format and print the value accordingly.
- The total number of printed characters is returned, matching `printf`’s behavior.

---

## 🧩 Project Structure

```bash
.
├── ft_printf.h       # Header file with prototypes and includes
├── ft_printf.c       # Main parsing and controller function
├── ft_utils.c        # Utility functions (e.g., strlen, itoa)
├── ft_convert.c      # Conversion logic for different specifiers
├── ft_hex_utils.c    # Functions for hexadecimal conversions
├── ft_putchar.c      # Output functions
├── Makefile
└── README.md
```

---

## HOW TO USE
#### 1 - Clone the repository
```git
https://github.com/na7li/ft_printf
```

#### 2 - Enter the project folder and run `make`
```bash
cd ft_printf/ft_printf
make
```

#### 3 - To use in your code, include the header
```c
#include "ft_printf.h"
```

#### 4 - Example
```bash
ft_printf("Hello %s! You have %d new messages.\n", "Mohamed", 5);
```

#### 5 - Expected Output:
```bash
Hello Mohamed! You have 5 new messages.
```

#### MAKEFILE RULES

`make` or `make all` - Compile ft_printf files.

`make clean` - Delete all .o (object files) files.

`make fclean` - Delete all .o (object files) and .a (executable) files.

`make re` - Use rules `fclean` + `all`.

---
## 🤝 Credits
Developed by Mohamed, student at 42 Network, as part of the Common Core projects.
