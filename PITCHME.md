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

## Functional Programming Concepts

User input is never pure.

(duh)

---

## Functional Programming Concepts

Call by reference is never pure


---

## Functional Programming Concepts

Basically inpossible to write software using 100% pure functions

---

## Functional Programming Concepts

`sin(x)`

`abs(x)`

`sqrt(x)`

These always returns same values for x

---

## Functional Programming Concepts

`str.length()`

`str.isEmpty()`

`str.concat(str)`

Always returns same values for the string `str` (and `str2`)

---

## Functional Programming Concepts

`getAccountNumberFromDB(acctOwner)`

Kidding...  definitely not pure

