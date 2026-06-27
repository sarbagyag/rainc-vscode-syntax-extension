---
url: "https://rain-docs.vercel.app/docs/arrays"
title: "Arrays · Rain docs · Rain"
---

Create arrays with `#[ ... ]`. Elements are comma-separated.

Index with `arr[i]`. Call methods with `arr->method()`.

## Literal & index

Literal & index

```
var nums = #[10, 20, 30];
print nums[0];
nums[1] = 99;
print nums[1];
```

output

```
10
99
```

## Array methods

| Symbol | Description | Example |
| --- | --- | --- |
| `->len()` | Element count | `var a = #[1, 2, 3];<br>print a->len();` |
| `->push(x)` | Append; returns array | `var a = #[1];<br>a->push(2);<br>print a;` |
| `->pop()` | Remove last element | `var a = #[1, 2];<br>print a->pop();` |
| `->contains(x)` | Whether value exists | `var a = #[1, 2, 3];<br>print a->contains(2);` |
| `->reverse()` | Reverse in place | `var a = #[1, 2, 3];<br>a->reverse();<br>print a;` |
| `->sort()` | Sort numbers in place | `var a = #[3, 1, 2];<br>a->sort();<br>print a;` |
| `->slice(start, end)` | New array \[start, end) | `var a = #[0, 1, 2, 3];<br>print a->slice(1, 3);` |