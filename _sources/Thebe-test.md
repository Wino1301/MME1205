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

<!-- Configure and load Thebe !-->
<script type="text/x-thebe-config">
  {
    requestKernel: true,
    binderOptions: {
      repo: "Wino1301/MME1205",
    },
    codemirror_mode: {theme: "blackboard"},
  }
</script>
<script src="https://unpkg.com/thebe@latest/lib/index.js"></script>

+++

<button id="activateButton"  style="width: 150px; height: 45px; font-size: 1.5em;">Activate</button>
<script>
var bootstrapThebe = function() {
    thebelab.bootstrap();
}

document.querySelector("#activateButton").addEventListener('click', bootstrapThebe)
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

+++ {"tags": ["thebe-init"]}

<pre data-executable="true" data-language="python">
#Your code here
5**10
</pre>

+++ {"tags": ["thebe-init"]}

{toggle}
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

+++ {"tags": ["thebe-init", "hide-input"]}


:class: dropdown 
<pre data-executable="true" data-language="python" hidden>
{admonition} Click the button to reveal!
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
</pre>

+++ {"tags": ["thebe-init", "remove-input"]}

:tags: [remove-input]
<pre data-executable="true" data-language="python">
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
</pre>

```{code-cell} ipython3
# No thebe-init tag

from datetime import datetime
datetime.now()
```

```{code-cell} ipython3

```
