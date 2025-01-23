# Replication-of-Conformance-Checking-of-fuzzy-logs-against-Declerative-temporal-Specification-
is to check whether fuzzy event data conform with declarative temporal rules specified as Declare patterns or, more generally, as formulae of linear temporal logic over finite traces (LTLf ).

# Fuzzy Linear Temporal Logic on Finite traces
The repository implements the Replication of a fast conformance checker for fuzzy logs against temporal specifications in Fuzzy Linear Temporal Logic on finite traces (FLTLf) as described in the paper "Conformance Checking of Fuzzy Logs against Declarative Temporal Specifications".


How we get required Result structured as follows:

A requirements section listing the needed software dependencies.
A running the experiments section explaining how to reproduce the experiments.
A Section with cite the Original Paper.

## Requirements
Implemented with Python 3.8.15, the project requires with the following dependencies:
```
torch==1.13.1
lark==1.1.9
pandas==2.2.3
```
## Running the Experiments
The experiments are stress tests measuring the computational running time of the fuzzy conformance checker by varying the number of events, the number of traces in the log, the complexity of the LTLf formula.

The experiments involving simple LTLf formulas can be executed by running:
python Replicate-Simplerun.py

whereas experiments involving complex LTLf formulas are executed by running:
python Replicate-Declare.py

The results are saved in the results folder.

# Remarks:
A Fast Crisp LTLf Checker
The implementation uses the Zadeh t-norm and co-norm that are the fuzzy counterparts of the AND and OR symbol in propositional logic. Therefore, the code can be used as a fast checker for LTLf where the truth values of the event log are just 0 or 1.



## Reference
```
@inproceedings{donadello2024conformance,
  title={Conformance Checking of Fuzzy Logs Against Declarative Temporal Specifications},
  author={Donadello, Ivan and Felli, Paolo and Innes, Craig and Maggi, Fabrizio Maria and Montali, Marco},
  booktitle={International Conference on Business Process Management},
  pages={39--56},
  year={2024},
  organization={Springer}
}
```
