---
title: Chunk
tags: list,lambda,advanced
---

Chunks an array into smaller arrays of a specified size.

Use `Enumerable.Select()` to convert the given list to index-value pairs.
Use `Enumerable.GroupBy()` to split elements into groups based on their index.
Use `Enumerable.Select()` a seconds time to map each group's elements to their values and `Enumerable.ToList()` to convert the result to a list.
Finally, use `Enumerable.ToList()` on the result to convert everything to a list and return it.
If the original list can't be split evenly, the final chunk will contain the remaining elements.

```csharp
using System.Collections.Generic;
using System.Linq;

public static partial class _30s 
{
  public static List<List<T>> Chunk<T>(List<T> list, int size)
  {
    return list
      .Select((x, i) => new { Index = i, Value = x })
      .GroupBy(x => x.Index / size)
      .Select(x => x.Select(v => v.Value).ToList())
      .ToList();
  }
}
```

```csharp
List<int> nums =  new List<int>(){  1,  2,  3,  4,  5  };

_30s.Chunk(nums, 2); // { {1, 2}, {3, 4}, {5} }
```
