# mata-sim-eval
Evaluation enviroment for simulation algorithm implemented in libmata (https://github.com/VeriFIT/mata)

The simulation algorithm can be found at https://link.springer.com/chapter/10.1007/978-3-540-27812-2_11

# Installation
Firstly, benchmarks need to be compiled:
```
cd src
make
```

# How to evaluate
We are using pycobench to evaluate the algortihm.
To evaluate speed:
```
./pycobench -c input/bench-simulation.yaml -m "iny" -o results/output.out < input/single-automata.input
```
To evaluate correctness: (This should always pass)
```
./pycobench -c input/test-simulation.yaml -o results/output.out < input/single-automata.input
```

# How to parse the output
Pycobench output may not be in optimal format. Parsing the output:
```
cd results
../pyco_proc --csv output.out > result.csv
```

# Visualising the output
Note that the result.csv must be in the results folder
```
cd visual
python3 graph.py
```
