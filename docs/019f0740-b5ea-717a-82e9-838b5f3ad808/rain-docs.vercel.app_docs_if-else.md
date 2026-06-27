---
url: "https://rain-docs.vercel.app/docs/if-else"
title: "If / else · Rain docs · Rain"
---

Conditions go in parentheses after `if`. The body can be a single statement or a `{ ... }` block.

`else` attaches to the nearest `if`. Only `false` and `nil` are falsy.

rain

```
var score = 85;

if (score >= 90) {
  print "A";
} else if (score >= 80) {
  print "B";
} else {
  print "Keep going";
}
```

output

```
B
```

## Truthy / falsy

Truthy / falsy

```
if (nil) print "no";
if (0) print "zero is truthy";
if ("") print "empty string is truthy";
```

output

```
zero is truthy
empty string is truthy
```