---
title: ordinal
tags: string,intermediate
---

Adds an ordinal suffix to an integer.

- Use list indexing to get the ordinal suffix of the integer.
- Clamp the maximum index to 3 using `min()` since all digits after 4 use the same ordinal suffix.
- Exception for numbers ending with 11, 12 or 13 as their ordinal suffix is always "th".

```py
def ordinal(n):
  suffix = ('st', 'nd', 'rd', 'th')[min(n % 10 - 1, 3)]
  if (n % 100) in range(11, 14):
    suffix = 'th'
  return str(n) + suffix
```

```py
ordinal(42) # 42nd
```