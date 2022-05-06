# MathCase

## Tips for good names

Since names are the smallest building block of code, they should follow some rules to be good.

- Use intention-revealing names
- Avoid disinformation
- Make meaningful distinctions
- Use pronounceable names
- Use searchable names
- Avoid encondings
- Avoid mental mapping

But, when we are talking about math formulas, some of these rules are difficult to follow. For example, take a look at this code:

```python
for i in range(n):
    for j in range(m):
        for k in range(l):
            temp_value = X[i][j][k] * 12.5
            new_array[i][j][k] = temp_value + 150
```

If you were trying to modify or debug this code, you'd be at a loss unless you could read the author's mind. Even if you were the author, a few days after writing this code you might not remember what it does because of the unhelpful variable names and use of _magic numbers_.


