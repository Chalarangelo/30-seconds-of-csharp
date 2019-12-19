---
title: IsEven
tags: math,beginner
---

Returns `True` if the given number is even, `False` otherwise.

Check whether a number is odd or even using the modulo (`%`) operator. 
Return `True` if the number is even, `False` if the number is odd.

```csharp
public static partial class _30s 
{
  public static bool IsEven(int n) 
  {
    return n % 2 == 0;
  }
}
```

```csharp
_30s.IsEven(2); // True
_30s.IsEven(3); // False
```
