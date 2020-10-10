---
title: WordsInText
tags: utility,regex,beginner
---

Returns an enumerable with all the words in the text.

- Uses Regex to find sequence of characters between 'a' through 'z' (insensitive)
- Converts the matches into an enumerable containing the matched values

```csharp
using System.Collections.Generic;
using System.Linq;
using System.Text.RegularExpressions;

public static partial class _30s
{
  public static IEnumerable<string> WordsInText(string text)
  {
    var matches = Regex.Matches(text, @"\b[a-z]+\b", RegexOptions.IgnoreCase);

    return
      matches
        .Cast<Match>()
        .Select(m => m.Value)
        .ToList();
  }
}
```

```csharp
_30s.WordsInText("The quick brown fox jumps over the lazy dog");
// { "The", "quick", "brown", "fox", "jumps", "over", "the", "lazy", "dog" }

_30s.WordsInText("Alice 123blah sends 123 a 789 message");
// { "Alica", "sends", "a", "message" }

_30s.WordsInText("Bob,receives,a 1234 message");
// { "Bob", "receives", "a", "message" }
```
