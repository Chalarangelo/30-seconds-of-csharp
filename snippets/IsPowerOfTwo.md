---
title: IsPowerOfTwo
tags: math,intermediate
---

Returns `True` if the given number is a power of `2`, `False` otherwise.

Use the bitwise binary AND operator (`&`) to determine if `n` is a power of `2`.
Additionally, check that `n` is different from `0`.

```csharp
public static partial class _30s 
{
  public static bool IsPowerOfTwo(ulong n) 
  {
    return (n != 0) && ((n & (n - 1)) == 0);
  }
}
```

```csharp
_30s.IsPowerOfTwo(0); // False
_30s.IsPowerOfTwo(1); // True
_30s.IsPowerOfTwo(8); // True
```
