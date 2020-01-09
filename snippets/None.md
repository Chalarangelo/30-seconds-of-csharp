---
title: None
tags: array,lambda,overload,intermediate
---

Returns `true` if the provided predicate function returns `false` for all elements in a collection, `false` otherwise.

Use `Array.Exists()` to test if all elements in the collection return `false` based on the predicate function, `match`.
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

_30s.None(nums, x => x < 0); // true
_30s.None(nums); // false
```
