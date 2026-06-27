---
url: "https://rain-docs.vercel.app/docs/operators"
title: "Operators · Rain docs · Rain"
---

`+` adds numbers or concatenates if either side is a string.

Comparisons (`<`, `<=`, `>`, `>=`) require numbers. `==` and `!=` work on any values.

`and` / `or` short-circuit. `!` negates truthiness.

## Arithmetic

Arithmetic

```
print 10 + 3;
print 10 - 3;
print 10 * 3;
print 10 / 3;
```

output

```
13
7
30
3.3333333333333335
```

## Comparison & logic

Comparison & logic

```
print 5 > 3;
print 5 == 5;
print !false;
print true and false;
print true or false;
```

output

```
true
true
true
false
true
```

## Operator reference

| Symbol | Description |
| --- | --- |
| `+ - * /` | Arithmetic (numbers) |
| `+` | Also string concatenation |
| `== != < <= > >=` | Comparisons |
| `and or` | Logical (short-circuit) |
| `!` | Logical not |
| `=` | Assignment |