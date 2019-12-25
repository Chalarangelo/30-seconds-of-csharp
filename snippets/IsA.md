---
title: IsA
tags: type,utility,beginner
---

Returns `True` if the given object is of the specified type, `False` otherwise.

Use the `is` operator to check if `obj` is of the given type, `T`.

```csharp
public static partial class _30s 
{
  public static bool IsA<T>(object obj) 
  {
    return obj is T;
  }
}
```

```csharp
string s = "fooBar";

_30s.IsA<string>(s); // True
_30s.IsA<int>(s); // False
```
