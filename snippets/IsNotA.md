---
title: IsNotA
tags: utility,type,beginner
---

Returns `True` if the given object is not of the specified type, `False` otherwise.

Use the `is` operator to check if `obj` is not of the given type, `T`.

```csharp
public static partial class _30s 
{
  public static bool IsNotA<T>(object obj) 
  {
    return !(obj is T);
  }
}
```

```csharp
string s = "fooBar";

_30s.IsNotA<string>(s); // False
_30s.IsNotA<int>(s); // True
```
