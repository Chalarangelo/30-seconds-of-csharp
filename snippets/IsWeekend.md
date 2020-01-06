---
title: IsWeekend
tags: date,utility,beginner
---

Returns `True` if the given `DateTime` is a not weekday, `False` otherwise.

Use `DateTime.DayOfWeek` to check if the given `DateTime` is a Saturday or Sunday.

```csharp
public static partial class _30s 
{
  public static bool IsWeekend(DateTime date) 
  {
    return date.DayOfWeek == DayOfWeek.Saturday || date.DayOfWeek == DayOfWeek.Sunday;
  }
}
```

```csharp
_30s.IsWeekend(new DateTime(2020, 1, 15)); // False
_30s.IsWeekend(new DateTime(2020, 1, 19)); // True
```
