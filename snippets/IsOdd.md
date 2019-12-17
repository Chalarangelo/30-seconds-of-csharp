---
title: IsOdd
tags: math,beginner
---

Returns `True` if the given number is odd, `False` otherwise.

Check whether a number is odd or even using the modulo (`%`) operator. 
Return `True` if the number is odd, `False` if the number is even.

```csharp
public static partial class _30s 
{
  public static bool IsOdd(int n) 
  {
    return n % 2 != 0;
  }
}
```

```csharp
_30s.IsOdd(3); // True
_30s.IsOdd(4); // False
```
