---
layout: default
title: The MAX-3SAT Example
permalink: /data/maxSat/
---
# The MAX-3SAT Example

Here we use the *optimizationBenchmarking* framework to investigate the results of some simple algorithms applied to the [MAX-3SAT](http://en.wikipedia.org/wiki/MAX-3SAT) problem.

## 1. Example Structure

This example is structured as follows

1. The archive [`benchmarks.zip`](benchmarks.zip) contains some benchmark instances for the MAX-3SAT problem from the popular [SATLIB](http://www.cs.ubc.ca/~hoos/SATLIB/benchm.html) benchmark instance set.
2. The archive [`sources.zip`](sources.zip) contains some simple `Java` "solvers" to solve these MAX-3SAT instances. These "solvers" (notice the quotes) are not an attempt to actually solve the problems well - they are quite stupid and primitive. But they are easy to understand, which is the goal of the example. They also illustrate how data can be gathered in log files which can later be loaded into the evaluator.
3. The archive [`results.zip`](results.zip) contains the results of these algorithms. 

## 2. The MAX-3SAT Problem

[MAX-3SAT](http://en.wikipedia.org/wiki/MAX-3SAT) is an optimization problem where we want to find a way to satisfy a Boolean function of a specific structure. "Satisfy" means to find a setting for its (Boolean) input values so that its (Boolean) output becomes `true`. If there is no such setting, well, at least we want to make as many of its components ("clauses") to become `true`. The Boolean functions considered here are in [conjunctive normal form](http://en.wikipedia.org/wiki/3-CNF), meaning they are an `and` combination of several smaller `or`s. Moreover, each of these `or`s has exactly three inputs, which come from the inputs or negated inputs of the overall formula. In particular, such a formula `f(x1, x2, x3, x4)` could look like

    f(x1, x2, x3, x4) = (x1 or x2 or (not x3)) and (x2 or (not x3) or x4) and ((not x1) or x2 or (not x4))

This formula has four variables (`x1`, `x2`, `x3`, and `x4`) and three clauses. If can become `true` if
`x2` is `true` (as it appears in each `or` without negation), in which case the other variables don't matter. For problems more variables and clauses, it becomes much harder to find a solution or to find the variable setting making the most clauses become `true`. Matter of fact, MAX-3SAT is [NP-hard](http://en.wikipedia.org/wiki/NP-hard).

As benchmark problems for our Maximum 3 Satisfiability example, we use some instances from the well-known [SATLib](http://www.satlib.org/) obtained from [http://www.cs.ubc.ca/~hoos/SATLIB/benchm.html](http://www.cs.ubc.ca/~hoos/SATLIB/benchm.html) [1], as we describe in the `README.md` file in the `benchmark` folder.


## 3. Benchmark Problems for the MAX-3SAT Example

As benchmark problems for our Maximum 3 Satisfiability example, we use some instances from the well-known [SATLib](http://www.satlib.org/) obtained from [http://www.cs.ubc.ca/~hoos/SATLIB/benchm.html](http://www.cs.ubc.ca/~hoos/SATLIB/benchm.html) [1].

### 3.1. Selected Instances
In particular, we pick the first ten instances of each of the following [uniform random 3-SAT](http://www.cs.ubc.ca/~hoos/SATLIB/Benchmarks/SAT/RND3SAT/descr.html) benchmark sets:

1. [`uf20-91`](http://www.cs.ubc.ca/~hoos/SATLIB/Benchmarks/SAT/RND3SAT/uf20-91.tar.gz): 20 variables, 91 clauses - first 10 of 1000 instances, all satisfiable, all MAX 3-SAT
2. [`uf50-218`](http://www.cs.ubc.ca/~hoos/SATLIB/Benchmarks/SAT/RND3SAT/uf50-218.tar.gz): 50 variables, 218 clauses - first 10 of 1000 instances, all satisfiable, all MAX 3-SAT
3. [`uf75-325`](http://www.cs.ubc.ca/~hoos/SATLIB/Benchmarks/SAT/RND3SAT/uf75-325.tar.gz): 75 variables, 325 clauses - first 10 of 100 instances, all satisfiable
4. [`uf100-430`](http://www.cs.ubc.ca/~hoos/SATLIB/Benchmarks/SAT/RND3SAT/uf100-430.tar.gz): 75 variables, 325 clauses - first 10 of 100 instances, all satisfiable, all MAX 3-SAT
5. [`uf125-538`](http://www.cs.ubc.ca/~hoos/SATLIB/Benchmarks/SAT/RND3SAT/uf125-538.tar.gz): 100 variables, 430 clauses - first 10 of 1000 instances, all satisfiable, all MAX 3-SAT
6. [`uf150-645`](http://www.cs.ubc.ca/~hoos/SATLIB/Benchmarks/SAT/RND3SAT/uf150-645.tar.gz): 150 variables, 645 clauses - first 10 of 100 instances, all satisfiable, all MAX 3-SAT
7. [`uf175-753`](http://www.cs.ubc.ca/~hoos/SATLIB/Benchmarks/SAT/RND3SAT/uf175-753.tar.gz) 175 variables, 753 clauses - first 10 of 100 instances, all satisfiable, all MAX 3-SAT
8. [`uf200-860`](http://www.cs.ubc.ca/~hoos/SATLIB/Benchmarks/SAT/RND3SAT/uf200-860.tar.gz): 200 variables, 860 clauses - first 10 of 100 instances, all satisfiable, all MAX 3-SAT
9. [`uf225-960`](http://www.cs.ubc.ca/~hoos/SATLIB/Benchmarks/SAT/RND3SAT/uf225-960.tar.gz): 225 variables, 960 clauses - first 10 of 100 instances, all satisfiable, all MAX 3-SAT
10. [`uf250-1065`](http://www.cs.ubc.ca/~hoos/SATLIB/Benchmarks/SAT/RND3SAT/uf250-1065.tar.gz): 250 variables, 1065 clauses - first 10 of 100 instances, all satisfiable, all MAX 3-SAT

### 3.2. Instance Features
Our instances have two features:

1. The number of variables
2. The number of clauses (which here is a function of the number of variables)


## References
1. Holger H. Hoos and Thomas Stützle: SATLIB: An Online Resource for Research on SAT. In: Ian P.Gent, Hans van Maaren, and Tobi Walsh, editors, SAT 2000, pp.283-292, Amsterdam, The Netherlands: IOS Press, 2000. SATLIB is available online at [www.satlib.org](http://www.satlib.org/).
