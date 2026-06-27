---
url: "https://rain-docs.vercel.app/docs/variables"
title: "Variables · Rain docs · Rain"
---

Use `var` to create a variable. You can omit the initializer — it defaults to `nil`.

Assign later with `=`. Reassignment works for locals and instance fields.

rain

```
var name = "Rain";
var count = 0;
print name;
print count;
```

output

```
Rain
0
```

## Reassign

Reassign

```
var n = 1;
n = n + 1;
print n;
```

output

```
2
```

## Block scope

Block scope

```
var x = "outer";
{
  var x = "inner";
  print x;
}
print x;
```

output

```
inner
inner
```

## Notes