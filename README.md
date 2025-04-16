# Cobra

**Cobra** is a lightweight extension of C that adopts Python-style syntax—using indentation, colons, and optional semicolons—to streamline and modernize low-level programming. Cobra code compiles down to standard C, enabling compatibility with existing toolchains while making C easier to read and write.

---

## Why Cobra?

C was designed for machines. Cobra is designed for humans who still want the power of C, minus the boilerplate.

**Advantages over regular C:**
- **No braces `{}`:** Block structure is defined by **indentation**, like Python.
- **Colons `:` instead of `{`:** Clear, intuitive block openers.
- **Semicolons optional:** Trailing semicolons are no longer required for most statements.
- **Cleaner syntax:** Reduces visual clutter and cognitive load.
- **Faster prototyping:** Focus on logic, not syntax scaffolding.
- **Zero runtime cost:** Cobra transpiles to C—no VM, no interpreter.

---

## Examples

### Regular C

```c
#include <stdio.h>

int main() {
    int i = 0;
    while (i < 5) {
        printf("%d\n", i);
        i++;
    }
    return 0;
}
```

### 🐍 Cobra

```cobra
import <stdio.h>

fn main():
    i = 0
    while i < 5:
        printf("%d\n", i)
        i += 1
    return 0
```

---

## Usage

```sh
cobra <input.ic> [-o <outputfile.extension>] [--keep-c]
```

- `<input.ic>`: Your Cobra source file.
- `-o <outputfile>`: Optional. Specify the output C or executable filename.
- `--keep-c`: Retain the generated `.c` file for inspection.

### Examples

Compile a Cobra file to an executable:
```sh
cobra hello.ic -o hello
```

Generate only the C file:
```sh
cobra hello.ic --keep-c
```

---

## 🛠️ Setup

To use `cobra` as a CLI command, follow the instructions in [SETUP.md](SETUP.md).

---

## Status

Cobra supports:
- Functions
- Conditionals (`if`, `else if`, `else`)
- Loops (`while`, `for`)
- Structs (basic)
- Pointers (basic)
- Imports (`import <stdio.h>`)

Planned:
- Better error handling
- IDE/linter support
- Advanced type checking

---
