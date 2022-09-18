# Algorithms are fun

The idea behind making an algorithm is that it first solves a problem, i.e. it is correct. The algorithm must be fast or efficient enough. So creating an algorithm is an algorithm itself.

```py
def algorithm_development(problem_spec):
  correct = False
  while not correct or not fast_enough(running_time):
    algorithm = devise_algorithm(problem_spec)
    correct = analyze_correctness(algorithm)
    running_time = analize_efficiency(algorithm)
  return algorithm
```

