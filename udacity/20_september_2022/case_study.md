# Case Study

Math is really useful when writing an algorithm. They can help with:

1. Formalize what you are doing
2. Analize correctness
3. Analize efficiency

Efficiency standards are based on a particular variable or specification, it could be time, memory allocation, or electrical power efficiency.

**Example**

```py
def naive(a, b):
  x = a; y = b
  z = 0
  while x > 0:
    z += y
    x -= 1
  return z
```

What that code does?

A. Does it takes `max(a, b)`?

B. Does it calculates `a - b`?

C. Does it calculates `b - a`?

D. Does it calculates `a + b`?

E. Does it calculates `a * b`?

The answer is E, because `Y` is added, as many times as `X`

## Correctness of naive(a, b) = ab

*claim: Before or after "while" loop,*

![first eq](./case_study_img/first_eq.png)

**Proof**

*In Base Case: First Time Through,*

![second eq](./case_study_img/second_eq.png)

*Based in claim:*

![third eq](./case_study_img/third_eq.png)

*Inductive step*

![ind header](./case_study_img/inductive_step_header.png)

Given that the loop goes while `x > 0` that means that when `x = 0` the loop will terminate, so 

![fourth eqs](./case_study_img/fourth_eqs.png)

## Running time of naive(a,b)

The larger the inputs, the longer the execution time.

If you make a graph, which plots the computational time, against the number being calculated, the graph will look like this:

![case study 1](./case_study1.png)

The x-axis represents numbers in the order of billions, and the y-axis is time in seconds.

How does running time `t` relate to input `n`?

![final opts](./case_study_img/final_opts.png)

The answer is C.