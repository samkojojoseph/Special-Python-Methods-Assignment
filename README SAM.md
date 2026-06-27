# Python Special Methods


## What's Inside

| Method | Does What | Example |
|--------|-----------|---------|
| `__init__` | Constructor | `Bird` with name and wingspan |
| `__str__` | Pretty print | `Album` title and artist |
| `__repr__` | Debug info | Recreate the `Album` |
| `__len__` | Length | `Toolbox` tool count |
| `__eq__` | Equal check | `Member` by ID |
| `__add__` | Addition | `Matrix` addition |
| `__sub__` | Subtraction | `Matrix` subtraction |
| `__mul__` | Multiply | `Matrix` scaling |
| `__getitem__` | Index access | `Queue` items |
| `__setitem__` | Index update | Edit `Queue` |
| `__contains__` | Check `in` | `Cupboard` contents |
| `__call__` | Call like function | `Converter` currency |
| `__iter__` | Loop with `for` | `Stepper` sequence |
| `__next__` | Next item | Continue stepper |
| `__bool__` | True/False | `Vault` has gold? |
| `__del__` | Cleanup hint | `TempLog` |

## Run It

```bash
pip install notebook
jupyter notebook Python_Special_Methods_B.ipynb
```

## Quick Example

```python
class Matrix:
    def __init__(self, a, b, c, d):
        self.a, self.b, self.c, self.d = a, b, c, d

    def __add__(self, other):
        return Matrix(
            self.a + other.a, self.b + other.b,
            self.c + other.c, self.d + other.d
        )

    def __str__(self):
        return f"[{self.a} {self.b}; {self.c} {self.d}]"

m1 = Matrix(1, 2, 3, 4)
m2 = Matrix(5, 6, 7, 8)
print(m1 + m2)  # [6 8; 10 12]
```


## License

MIT
