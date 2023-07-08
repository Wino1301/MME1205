---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.14.7
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---

<script type="text/javascript" src="https://unpkg.com/thebe@rc/lib/index.js"></script>
<link rel="stylesheet" href="https://unpkg.com/thebe@thebe@rc/lib/thebe.css" />

+++

<script type="text/x-thebe-config">
  {
      useBinder: true,
      binderSettings: {
          repo: "Wino1301/MME1205"
      },
      mountActivateWidget: true,
      mountStatusWidget: true,
  }
</script>

+++

# Example of Live Feedback In Class

+++

This page serves as an exmaple to use Thebe in live class 
---
- Thebe allows live code edits and runs using BinderHub 
- Thebe allows hide-input so students does not have acces to cell contents

--- 
- This will aid in the learnes feedback for in class excersises / labs
---
- Exam / Quizzes should be done entierly on colab or locally

+++

## Exercise 1

Return the value of raising 5 to the power of 10

```{code-cell} ipython3
:tags: [thebe-init]

#Your code here
5**10
```

```{code-cell} ipython3
:tags: [thebe-init]

# Only thebe-init tag

# Run hidden tests using assert statements
q1 = 0
try: 
    assert _ == 9765625
except: 
    q1 += 1
    print("That is not the correct answer")
    
try:
    assert isinstance(_, int)
except: 
    q1 += 1
    print("Result is not int")

print("Hidden Tests Completed")
if q1 != 0:
    print("Try again!")
else: 
    print("All good!")
```

```{code-cell} ipython3
:tags: [thebe-init, hide-input]

# thebe-init + hide-input

# Run hidden tests using assert statements
q1 = 0
try: 
    assert _ == 9765625
except: 
    q1 += 1
    print("That is not the correct answer")
    
try:
    assert isinstance(_, int)
except: 
    q1 += 1
    print("Result is not int")

print("Hidden Tests Completed")
if q1 != 0:
    print("Try again!")
else: 
    print("All good!")
```

```{code-cell} ipython3
:tags: [thebe-init, remove-input]

#thebe-init + remove-input

# Run hidden tests using assert statements
q1 = 0
try: 
    assert _ == 9765625
except: 
    q1 += 1
    print("That is not the correct answer")
    
try:
    assert isinstance(_, int)
except: 
    q1 += 1
    print("Result is not int")

print("Hidden Tests Completed")
if q1 != 0:
    print("Try again!")
else: 
    print("All good!")
```

```{code-cell} ipython3
# No thebe-init tag

from datetime import datetime
datetime.now()
```

```{code-cell} ipython3

```
