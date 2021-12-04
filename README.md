# replicating_portfolio

This repository tries to present a framework to predict hedging errors when hedging any contigent claim without making any assumptions under the strategy to be used. The main use of this repository in the moment is to replicate results from reserch papers.

-/stable_tools/misc.py -> miscellaneous methods;

-/stable_tools/replicating_fixed_time.py -> base class for replicating fixed time strategies declaration;

-/test_tools/. -> scripts used to test some features of numba and to test some design choices made;

-/option_class.py -> implementation of some methods using the base class to test some results form Yet Another Note on the Leland’s OptionHedging Strategy with Transaction CostsValeri I. Zakamouline

-/main.py -> usage of the methods implemented in option_class.py 

Setup:
- install miniconda/anaconda python distribution;
-To setup an enviorment for this repository use open command line in the repository folder and:
conda env create -f environment.yml

Usage:
- To activate the enviorment and use the scripts:
  - conda activate Master_Thesis_ENV
  - python3 main.py

To do list:
- (important) fix bug that makes the results slightly off when comparing to the results from the paper (even when using large samples and considering the confidence intervals over the obtained results);
- add a method in the base class to allow "delta" to have access to previous computed deltas (to test Emmanuel Lépinette. Modified Leland’s Strategy).
- add a method in order to return, in combination with the hedging error, the final stock price at expire date (to test Yet Another Note on the Leland’s OptionHedging Strategy with Transaction CostsValeri I. Zakamouline table 3).
- generalize the risk-return test function;
- create a new class to test moved-based hedging strategies (intead of fixed interval ones);


  
