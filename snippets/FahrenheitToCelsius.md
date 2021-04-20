---
title: fahrenheitToCelsius
tags: math,beginner
---

Converts Fahrenheit to Celsius

- Follow the conversion formula C = (F - 32) * 5/9.

```csharp
public static partial class _30s 
{
  public static float fahrenheitToCelsius(float degrees)
  {
    return (degrees - 32) * 5 / 9;
  }
}
```

```csharp
_30s.fahrenheitToCelsius(30); // -1.11
```
