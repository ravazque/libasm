*This project has been created as part of the 42 curriculum by ravazque.*

---

## Description

libasm is an introduction to **x86-64 assembly** (Intel syntax, compiled with NASM): a static library, `libasm.a`, that re-implements standard C library functions with behavior identical to the originals — including `errno` handling.

The mandatory functions are:

| Function | Equivalent | Notes |
|---|---|---|
| `ft_strlen` | `strlen(3)` | string length |
| `ft_strcpy` | `strcpy(3)` | string copy |
| `ft_strcmp` | `strcmp(3)` | string comparison |
| `ft_write` | `write(2)` | syscall wrapper, sets `errno` on error |
| `ft_read` | `read(2)` | syscall wrapper, sets `errno` on error |
| `ft_strdup` | `strdup(3)` | allocates with `malloc` |

The real subject of the project is the **System V AMD64 calling convention** (argument registers, return value, callee-saved registers), Linux **syscalls**, and how assembly links against C in a PIE world (`wrt ..plt` calls, 16-byte stack alignment, `__errno_location`).

The bonus part adds `ft_atoi_base` and a set of linked-list functions (`ft_list_push_front`, `ft_list_size`, `ft_list_sort`, `ft_list_remove_if`).
