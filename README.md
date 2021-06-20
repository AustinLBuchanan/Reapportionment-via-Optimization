# Reapportionment-via-Optimization
Solving reapportionment problems via MINLP

In US history, several methods have been used for reapportionment. Methods have been proposed by:
 - [Alexander Hamilton](https://github.com/AustinLBuchanan/Reapportionment-via-Optimization/blob/main/Hamilton-Optimization-Toy-Data.ipynb)
 - [Thomas Jefferson](https://github.com/AustinLBuchanan/Reapportionment-via-Optimization/blob/main/Jefferson-Optimization-Toy-Data.ipynb)
 - [John Quincy Adams](https://github.com/AustinLBuchanan/Reapportionment-via-Optimization/blob/main/Adams-Optimization-Toy-Data.ipynb)
 - [Daniel Webster](https://github.com/AustinLBuchanan/Reapportionment-via-Optimization/blob/main/Webster-Optimization-Toy-Data.ipynb)
 - [Huntington and Hill](https://github.com/AustinLBuchanan/Reapportionment-via-Optimization/blob/main/Huntington-Hill-Optimization-Toy-Data.ipynb).

It turns out that each method amounts to solving a mixed integer nonlinear program (MINLP). See Balinski and Young's book _[Fair Representation](https://scholar.google.com/scholar?cluster=13992446900586188509&hl=en&as_sdt=0,37)_ for the details.

The codes solve the associated MINLPs with the MIP solver called Gurobi. Each MINLP is applied to Example 1.1 from the appendix of Balinski and Young's book (1982 edition). 

I also tried applying them to the 2020 Census data, but the resulting instances were too numerically challenging for Gurobi. In several cases, Gurobi would suggest to give one seat to each state (except California) and give California the remaining seats.
