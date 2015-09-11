#Genetic Algorithm Package

Contains a generalizable genetic algorithm written in Python.


##Genetic Algorithm
#####(`GeneticAlgorithm/genalg.py`)

class `Population`: Given problem specifications, create and run through a population of possible individual solutions until either the fitness goal or the generation limit is reached.

class `Individual`: Given problem specifications, randomly create a possible solution individual.


##Example Usage
#####(`examples/function-maximizer.py`)

```python
from GeneticAlgorithm import genalg

def func_to_optimize(inputs):
  x, y, z = inputs
  return x ** y / z

if __name__ == "__main__":
  p = genalg.Population(popsize = 100, nchrom = 3, chromset = range(1, 20))
  best = p.run(eval_fn = func_to_optimize, fitness_goal = float("Inf"), generations = 300, verbose = True)
```


##To Do:

* Add optional flag to only mutate if new fitness is greater than old?
