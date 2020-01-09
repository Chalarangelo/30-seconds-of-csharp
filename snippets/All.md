---
title: All
tags: array,lambda,overload,intermediate
---

Returns `true` if the provided predicate function returns `true` for all elements in a collection, `false` otherwise.

Use `Array.TrueForAll()` to test if all elements in the collection return `true` based on the predicate function, `match`.
Omit the predicate function, `match`, to use the overload that checks if each value is different from `null` by default.

```csharp
public static partial class _30s 
{
  public static bool All<T>(T[] arr, Predicate<T> match) 
  {
    return Array.TrueForAll(arr, match);
  }
  public static bool All<T>(T[] arr) 
  {
    return Array.TrueForAll(arr, val => val != null);
  }
}
```

```csharp
int[] nums = { 4, 2, 3 };

_30s.All(nums, x => x > 1); // true
_30s.All(nums); // true
```
