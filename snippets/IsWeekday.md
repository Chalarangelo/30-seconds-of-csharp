---
title: IsWeekday
tags: date,utility,beginner
---

Returns `True` if the given `DateTime` is a weekday, `False` otherwise.

Use `DateTime.DayOfWeek` to check if the given `DateTime` is not a Saturday or Sunday.

```csharp
public static partial class _30s 
{
  public static bool IsWeekday(DateTime date) 
  {
    return date.DayOfWeek != DayOfWeek.Saturday && date.DayOfWeek != DayOfWeek.Sunday;
    }
}
```

```csharp
_30s.IsWeekday(new DateTime(2020, 1, 15)); // True
_30s.IsWeekday(new DateTime(2020, 1, 19)); // False
```
