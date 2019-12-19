---
title: IsDouble
tags: math,beginner
---

Returns `True` if the given string can be parsed into a double, `False` otherwise.

Return the result of calling `Double.TryParse()` with `NymberStyles.Float` for the given `num` string.

```csharp
using System.Globalization;

public static partial class _30s 
{
  public static bool IsDouble(string num) 
  {
    Double _ = 0.0;
    return Double.TryParse(num, NumberStyles.Float, NumberFormatInfo.CurrentInfo, out _);
  }
}
```

```csharp
_30s.IsDouble("2"); // True
_30s.IsDouble("hi"); // False
```
