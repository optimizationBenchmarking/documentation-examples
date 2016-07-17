---
layout: default
title: The TSP Suite Example
permalink: /data/tspSuite/
---
# The TSP Suite Example

Here we provide an example data set from several algorithms solving the Traveling Salesman Problem ([TSP](https://en.wikipedia.org/wiki/Travelling_salesman_problem)) gathered with the [TSP Suite](https://github.com/optimizationBenchmarking/tspSuite). The TSP&nbsp;Suite&nbsp;[<a href="#ref1">1</a>] is the direct predecessor of the  {{ site.projectNameStyled }} framework. Here we conduct experiments based on the 68 smallest-scale symmetric benchmark instances from the [TSPLib](www.iwr.uni-heidelberg.de/groups/comopt/software/TSPLIB95/) benchmark set&nbsp;[2].

## 1. Example Structure

This example is structured as follows

1. The archive [`results.zip`](results.zip) contains the results of eleven algorithms setups with different operators and restart policies on the selected TSP problem [instances](benchmarks.zip).
3. The file [`evaluation.xml`](evaluation.xml) contains an example evaluation definition. We apply a set of different modules and configurations.
4. The file [`configForIEEEEtran.xml`](configForIEEEEtran.xml) is a configuration that applies [`evaluation.xml`](evaluation.xml) to the [results](results.zip) and renders the output as LaTeX document styled according to `IEEEtran.cls` into a folder named `reports/LaTeX/IEEEtran/`. 
6. The file [`configForLNCS.xml`](configForLNCS.xml) is a configuration that applies [`evaluation.xml`](evaluation.xml) to the [results](results.zip) and renders the output as LaTeX document styled according to `LLNCS.cls` into a folder named `reports/LaTeX/LNCS/`.
6. The file [`configForSigAlternate.xml`](configForSigAlternate.xml) is a configuration that applies [`evaluation.xml`](evaluation.xml) to the [results](results.zip) and renders the output as LaTeX document styled according to `sig-alternate.cls` into a folder named `reports/LaTeX/SigAlternate/`.
6. The file [`configForXHTML.xml`](configForXHTML.xml) is a configuration that applies [`evaluation.xml`](evaluation.xml) to the [results](results.zip) and renders the output as XHTML document into a folder named `reports/XHTML/`.
6. The file [`configForExport.xml`](configForExport.xml) is a configuration that applies [`evaluation.xml`](evaluation.xml) to the [results](results.zip) and renders the output as text (for import into other tools) into a folder named `reports/export/`.
3. The archive [`benchmarks.zip`](benchmarks.zip) contains the some symmetric benchmark instances for the TSP from the popular [TSPLib](www.iwr.uni-heidelberg.de/groups/comopt/software/TSPLIB95/) benchmark instance set. This is just for information, you don't need that for the automatic evaluation of the experiments.
 

## 2. The Traveling Salesman Problem

The [TSP](https://en.wikipedia.org/wiki/Travelling_salesman_problem) is maybe the oldest and most well-known combinatorial optimization problem. Given are *n* cities. A salesman starts at one of these cities. He wants to visit all other cities (each exactly once) and then return to his origin. The question for the shortest tour that he can take to realize this travel is [NP-hard](https://en.wikipedia.org/wiki/NP-hard) and the best exact algorithms for solving this problem need a runtime exponential in *n* to find the best-possible solution in the worst case.


## 3. Benchmark Problems for the TSP Suite Example

As benchmark problems for our TSP example, we use some instances from the well-known [TSPLib](www.iwr.uni-heidelberg.de/groups/comopt/software/TSPLIB95/)&nbsp;[2]. We pick the 68 smallest-scale instances from 110 symmetric instances to run out experiments.

## 4. Investigated Algorithms

Here we investigate twelve *anytime optimization* methods for the TSP, i.e., algorithms that can step-wise improve their best guess of the solution. They can provide an approximate solution at any time. Among the tested algorithms, you can find 11 [metaheuristics](https://en.wikipedia.org/wiki/Metaheuristic) and one [branch and bound](https://en.wikipedia.org/wiki/Branch_and_bound) algorithm.

1. `ea2048+4096e`. An evolutionary algorithm with (2048+4096) population strategy using edge crossover, as investigated in&nbsp;[3].
2. `hillClimber`. A hill-climbing algorithm, as investigated in&nbsp;[1].
3. `ma16+64mns`. A memetic algorithm with a (16+64) population as investigated in&nbsp;[1], applying edge crossover at a crossover rate of 100%. The local search MNS&nbsp;[1] is applied to each generated solution. The first population is initialized with various constructive heuristics.
3. `ma16+64ts`. A memetic algorithm with a (16+64) population as investigated in&nbsp;[4], applying edge crossover at a crossover rate of 100%. The local search Tabu search is applied to each generated solution. The first population is initialized with various constructive heuristics.
4. `ma128+256lk-mns-lkx` a memetic algorithm with a (128+256) population using a hybrid LK-MNS local search to refine each generated solution, as investigated in&nbsp;[5]. This algorithm applies the new Lin-Kernighan crossover operator. The first population is initialized with various constructive heuristics.
5. `mns`, the multi-neighborhood search, a local search algorithm introduced in&nbsp;[1].
6. `paco3,10lk10mns`, a hybrid population-based ant colony optimization algorithm with population size 3 and sample size 10, using a hybrid LK-MNS local search to refine each generated solution, as investigated in&nbsp;[5].
7. `paco3,10mns`, a hybrid population-based ant colony optimization algorithm with population size 3 and sample size 10, using an MNS local search to refine each generated solution, as investigated in&nbsp;[1].
8. `paco3,10ts`, a hybrid population-based ant colony optimization algorithm with population size 3 and sample size 10, using a Tabu search to refine each generated solution, as investigated in&nbsp;[4].
9. `paco3,10fsm`, a hybrid population-based ant colony optimization algorithm with population size 3 and sample size 10, using a the ejection chain method FSM** to refine each generated solution, as investigated in&nbsp;[6].
10. `tbb`, truncated branch-and-bound.
11. `ts`, Tabu search, as investigated in&nbsp;[4].

## References
<span id="ref1">1</span>. Thomas Weise, Raymond Chiong, Ke Tang, Jörg Lässig, Shigeyoshi Tsutsui, Wenxiang Chen, Zbigniew Michalewicz, and Xin Yao. Benchmarking Optimization Algorithms: An Open Source Framework for the Traveling Salesman Problem. *IEEE Computational Intelligence Magazine (CIM)*. 9(3):40-52. August 2014. Piscataway, NJ, USA: IEEE Computational Intelligence Society. [pdf](http://www.it-weise.de/research/publications/WCTLTCMY2014BOAAOSFFTTSP/WCTLTCMY2014BOAAOSFFTTSP.pdf), doi:[10.1109/MCI.2014.2326101](http://dx.doi.org/10.1109/MCI.2014.2326101). Featured article and selected paper at the website of the IEEE Computational Intelligence Society (http://cis.ieee.org/).
2. Gerhard Reinelt. TSPLIB - A Traveling Salesman Problem Library. *ORSA Journal on Computing*. 3(4):376-384. 1991. Operations Research Society of America (ORSA). doi:[10.1287/ijoc.3.4.376](10.1287/ijoc.3.4.376)
3. Thomas Weise, Yuezhong Wu, Raymond Chiong, Ke Tang, and Jörg Lässig. Global versus Local Search: The Impact of Population Sizes on Evolutionary Algorithm Performance. *Journal of Global Optimization*. accepted 12&nbsp;February, 2016, published first online: 23&nbsp;February, 2016. [pdf](http://www.it-weise.de/research/publications/WWCTL2016GVLSTIOPSOEAP/WWCTL2016GVLSTIOPSOEAP.pdf), doi:[10.1007/s10898-016-0417-5](http://dx.doi.org/10.1007/s10898-016-0417-5).
4. Dan Xu, Thomas Weise, Yuezhong Wu, Jörg Lässig, and Raymond Chiong. An Investigation of Hybrid Tabu Search for the Traveling Salesman Problem. In *Proceedings of the 10th International Conference on Bio-Inspired Computing – Theories and Applications (BIC-TA'15)*, Maoguo Gong, Linqiang Pan, Tao Song, Ke Tang, and Xingyi Zhang, editors, September&nbsp;25–28, 2015, Hefei, Anhui, China, volume 562 of Communications in Computer and Information Science. Berlin/Heidelberg: Springer-Verlag, pages&nbsp;523–537, ISBN 978-3-662-49013-6. [pdf](http://www.it-weise.de/research/publications/XWWLC2015AIOHTSFTTSP/XWWLC2015AIOHTSFTTSP.pdf), doi:[10.1007/978-3-662-49014-3\_47](http://www.dx.doi.org/10.1007/978-3-662-49014-3_47)) ">10.1007/978-3-662-49014-3_47</a>
5. Yuezhong Wu, Thomas Weise, and Weichen Liu. Hybridizing Different Local Search Algorithms with Each Other and Evolutionary Computation: Better Performance on the Traveling Salesman Problem. In *Proceedings of the 18th Genetic and Evolutionary Computation Conference (GECCO'16)*, Denver, Colorado, USA, July&nbsp;20–24,&nbsp;2016, New York, NY, USA: Association for Computing Machinery (ACM). accepted for publication
6. Weichen Liu, Thomas Weise, Yuezhong Wu, and Raymond Chiong. Hybrid Ejection Chain Methods for the Traveling Salesman Problem. In *Proceedings of the 10th International Conference on Bio-Inspired Computing – Theories and Applications (BIC-TA'15)*, Maoguo Gong, Linqiang Pan, Tao Song, Ke Tang, and Xingyi Zhang, editors, September&nbsp;25–28, 2015, Hefei, Anhui, China, volume 562 of Communications in Computer and Information Science. Berlin/Heidelberg: Springer-Verlag, pages&nbsp;268–282, ISBN 978-3-662-49013-6. [pdf](http://www.it-weise.de/research/publications/LWWC2015HECMFTTSP/LWWC2015HECMFTTSP.pdf), doi:[10.1007/978-3-662-49014-3_25](http://dx.doi.org/10.1007/978-3-662-49014-3_25)