---
title: None
tags: array,lambda,overload,intermediate
---

Returns `True` if the provided predicate function returns `False` for all elements in a collection, `False` otherwise.

Use `Array.Exists()` to test if all elements in the collection return `False` based on the predicate function, `match`.
Omit the predicate function, `match`, to use the overload that checks if each value is `null` by default.

```csharp
public static partial class _30s 
{
  public static bool None<T>(T[] arr, Predicate<T> match) 
  {
    return !Array.Exists(arr, match);
  }
  public static bool None<T>(T[] arr) 
  {
    return Array.Exists(arr, val => val == null);
  }
}
```

```csharp
int[] nums = { 4, 2, 3 };

_30s.None(nums, x => x < 0); // True
_30s.None(nums); // False
```
