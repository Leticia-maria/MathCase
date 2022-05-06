# MathCase

A new convention for naming variables taken from math formulas.

## Tips for Creating Good Names for Variables

Since names are the smallest building block of code, they should follow some rules to be good.

- **Use intention-revealing names**
- **Avoid disinformation**
- **Make meaningful distinctions**
- **Use pronounceable names**
- **Use searchable names**
- **Avoid encondings**
- **Avoid mental mapping**

But, when we are talking about math formulas, some of these rules are difficult to follow. For example, take a look at this code:

```python
for i in range(n):
    for j in range(m):
        for k in range(l):
            temp_value = X[i][j][k] * 12.5
            new_array[i][j][k] = temp_value + 150
```

If you were trying to modify or debug this code, you'd be at a loss unless you could read the author's mind. Even if you were the author, a few days after writing this code you might not remember what it does because of the unhelpful variable names and use of _magic numbers_.

Looking at scientific programming codes, it is often to see examples like above (or worse): code with variable names such as `X`, `y`, `xs`, `x1`, `x2`, `tp`, `tm`, `cif`, `reg`, `xi`, `yi`, `ii` and numerous unnamed constant values.

## What Makes a Bad Variable Name?

Summarizing that, most problems with naming variables stem from:

- **A desire to keep variable names short**
- **A direct translation of formulas into code**

On this first point, while languages like Fortran did limit the length of variable names (to six characters), modern programming languages have no restrictions so don't feel forced to use contrived abbreviations. But it is not recommended to use long variable names (always thinking about _readability_).

Let's see an example that makes both mistakes. Say we have a polynomial equation for finding the price of a house from a model. You may be tempted to write the mathematical formula directly in code.

![y = m_1 * x_1 + m_2 * x_2^2 + b](https://latex.codecogs.com/svg.latex?&space;y=m_1*x_1+m_2*x_2^2+b) 

```python
temp = m1 * x1 + m2 * (x2 ** 2)
final = temp + b
```
This code looks like it was written by a machine for a machine. While a computer will ultimately run your code, it'll be read by humans, so write code intended for humans. To do this, we need to think not about the formula itself (_the how_) and consider the real-world objects being modeled (_the what_). Then, rewriting the last example:

```python
house_price = price_per_room * rooms + \ price_per_floor_squared  * (floors ** 2) 
house_price = house_price + expected_mean_house_price
```
