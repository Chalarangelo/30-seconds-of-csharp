---
title: DistinctValues
tags: array,beginner
---

Returns all distinct values in an array.

Use `Enumerable.Distinct()` to get the distinct values in the given array.
Use `Enumerable.ToArray()` to convert the result to an array and return it.

```csharp
using System.Linq;

public static partial class _30s 
{
  public static T[] DistinctValues<T>(T[] arr) 
  {
    return arr.Distinct().ToArray();
  }
}
```

```csharp
int[] nums =  { 1, 2, 1, 3, 3, 4, 5 };

_30s.DistinctValues(nums); // { 1, 2, 3, 4, 5 }
```
