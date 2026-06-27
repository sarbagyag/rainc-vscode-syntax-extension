---
url: "https://rain-docs.vercel.app/docs/types"
title: "Types & literals · Rain docs · Rain"
---

Rain is dynamically typed. Values know their type at runtime; you don't declare types on variables.

Numbers are IEEE doubles. Whole numbers print without a trailing `.0`.

`nil` is the absence of a value. Only `false` and `nil` are falsy in conditions.

Arrays are first-class values created with `#[ ... ]`.

rain

```
print 42;
print 3.14;
print "hello";
print true;
print false;
print nil;
print #[1, 2, 3];
```

output

```
42
3.14
hello
true
false
nil
[1, 2, 3]
```

## String + number

String + number

```
print "value: " + 42;
```

output

```
value: 42
```