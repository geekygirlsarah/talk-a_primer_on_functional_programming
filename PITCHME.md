---
@title[0 - Welcome]

# A Primer on Functional Programming

Sarah Withee
@geekygirlsarah

Slides:  geekygirlsarah.com/primer-fp

---
@title[0 - Welcome]

## Who has heard of functional programming?

---
@title[0 - Welcome]

## Who has done some form of functional programming?

---
@title[0 - Welcome]

## Who IS a functional prgrammer?

---
@title[0 - Welcome]

## Who has wanted to learn but never had time or good resources?

---
@title[0 - Welcome]

## Intro

1. Functional Programming Concepts
2. Why Use Functional Programming?
3. Brief Glance at Functional Programming Languages

---
@title[0 - Sarah]

# Hello!

*I am Sarah Withee*

I am a software engineer at Arcadia.io
I'm on social media as @geekygirlsarah

(Yes, you can tweet all the things)

---
@title[1 - Functional Programming Concepts]

# 1. Functional Programming Concepts

---
@title[1 - Functional Programming Concepts]

### Background

It's not new!

(Languages and ideas have been around since 1950s)

---
@title[1 - Functional Programming Concepts]

### Background

Built on ideas of lambda calculus developed in the 1930s

(I promise, we're not discussing this today)

---
@title[1 - Functional Programming Concepts]

# Pure Functions

Function that, given a certain input, _*always*_ produces the same output.

---

### Functional Programming Concepts

Pure functions don't have side effects

---

### Functional Programming Concepts

Side effects include:
- Time
- File access
- Database access
- Network access
- Previous function calls

---

### Functional Programming Concepts

User input is never pure.

(duh)

---

### Functional Programming Concepts

Call by reference is never pure


---

### Functional Programming Concepts

Basically inpossible to write software using 100% pure functions

---

### Functional Programming Concepts

`sin(x)`

`abs(x)`

`sqrt(x)`

These always returns same values for x

---

### Functional Programming Concepts

`str.length()`

`str.isEmpty()`

`str.concat(str)`

Always returns same values for the string `str` (and `str2`)

---

### Functional Programming Concepts

`getAccountNumberFromDB(acctOwner)`

Kidding...  definitely not pure

---

### Review - Pure Functions

- Pure functions, given certain input, always produce same output
- No side effects
- User input is never pure
- Call by reference is never pure
- Impossible to write software in 100% pure functions

---
@title[1 - ]

# Referential Transparency

Any expression that can replace a function with its return value with no behavior changes

---

### Functional Programming Concepts

Example:
If x = 3...

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;x + 5 = 8

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3 + 5 = 8

---

### Functional Programming Concepts

(note: sin 30° = 0.5 and cos 60° = 0.5)

`x = 30`

`y = sin(x) + cos(x * 2)       # y = 1`

`y = sin(30) + cos (30 * 2)`

`y =    0.5  +   0.5           # y - 1`

---

### Functional Programming Concepts

Pure functions _always_ have referential transparency

---

### Functional Programming Concepts

In mathematics, all functions are transparent.

In programming, this is NOT true.

---

### Functional Programming Concepts

Assignments are NOT transparent

`x = x + 1`

---

### Functional Programming Concepts

Referencially transparent assignment:

```
def addOne (int num):
   return num + 1; 

y = addOne(x)
```

---

### Functional Programming Concepts

More languages are starting to have immutable variables by default

---

### Functional Programming Concepts

Lambda function (or anonymous function):

A function without a name

---

### Functional Programming Concepts

Why lambdas?

- For building up higher-level functions
- To pass arguments to another function
- Used once to a few times

---

### Functional Programming Concepts

Lambda's can't be recursive*

`*` otherwise they need a name or some way to maintain state

`**` which is possible but outside of the scope of this talk

---

### Functional Programming Concepts

[lambda example here]

```
f = lambda x: x * x
print f(5)
```

```
> 25
```

---

### Functional Programming Concepts

Functions ARE values

Can be passed into other functions

---

### Functional Programming Concepts

```
define divide(x, y):
    return x / y

def divisor(d):
    return lambda r: divide (r, d)

half = divisor(2)

print(half(32))
```

---

### Functional Programming Concepts

Who has heard of map/filter/reduce?

---

### Functional Programming Concepts

Who has _used_ map/filter/reduce?

---

### Functional Programming Concepts

map - apply a function to all terms in a list

usage:

`map (function, list)`

---

### Functional Programming Concepts

```
items = [1, 2, 3, 4, 5]

squared = map (lambda x: x ** 2, items)

# same as:
squared = []
for i in items:
    squared.append (i ** 2)
```

---

### Functional Programming Concepts

filter - creates a list of all items matching a filter (a function that returns true)

usage:

`filter (function, list)`

---

### Functional Programming Concepts

```
items = [1, 2, 3, 4, 5, 6, 7, 8]

under_5 = filter (lambda x: x < 5, items)

# same as:
under_5 = []
for i in items:
    if (i < 5):
        under_5.append(i)
```

