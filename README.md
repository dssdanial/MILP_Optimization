# MILP_Optimization
Mixed Integer Linear Programming for train timetable optimization problem.

## Main steps of any linear optimization problem
<p align="center">
<img src="https://github.com/dssdanial/MILP_Optimization/assets/32397445/d95506f7-802b-4af3-8170-01747dcee901" width="350" height="300" />


## Solvers
In Python, there are different libraries for linear programming such as the multi-purposed SciPy, the beginner-friendly PuLP, the exhaustive Pyomo, and many others.
We are going to use Google OR-Tools. OR-Tools is an open source software suite for optimization, tuned for tackling the world's toughest problems in vehicle routing, flows, integer and linear programming, and constraint programming.
After modeling your problem in the programming language of your choice, you can use any of a half dozen solvers to solve it: commercial solvers such as Gurobi or CPLEX, or open-source solvers such as SCIP, GLPK, or Google's GLOP and award-winning CP-SAT.

```bash
!python -m pip install --upgrade --user -q ortools
```
<p align="center">
<img src="https://github.com/dssdanial/MILP_Optimization/assets/32397445/2cdb155a-ea17-4fb9-844e-5fa6ac53af9f" width="350" height="300" />

All these libraries have a hidden benefit: they act as interfaces to use the same model with different solvers. Solvers like Gurobi, Cplex, or SCIP have their own APIs, but the models they create are tied to a specific solver.
OR-Tools allows us to use an abstract (and quite pythonic) way of modeling our problems. We can then choose one or several solvers to find an optimal solution. The model we built is thus highly reusable!
OR-Tools comes with its own linear programming solver, called GLOP (Google Linear Optimization Package). It is an open-source project created by Google’s Operations Research Team and written in C++.
Other solvers are available such as SCIP, an excellent non-commercial solver created in 2005 and updated and maintained to this day. We could also use popular commercial options like Gurobi and Cplex. However, we would need to install them on top of OR-Tools and get the appropriate licenses (which can be quite costly).



## Linear programing VS Machine Learning 
- Linear programming can produce an optimal solution in an undetermined amount of time (it can take years), while machine learning can approximate complex functions in no time.
- There is no training in LP, but an expert is required to build a mathematical model. Machine learning needs data, but the models can be used as black boxes to solve a problem.
- As a rule of thumb, problems that do not have a particular time constraint and/or are not extremely complex can be advantageously solved with linear programming.
<p align="center">
<img src="https://github.com/dssdanial/MILP_Optimization/assets/32397445/1c2f6f60-c5a4-4504-bac0-30690dcd5cef" width="350" height="300" />



## Constraint programing
Constraint Programming is a technique to find every solution that respects a set of predefined constraints.

It is an invaluable tool for data scientists to solve a huge variety of problems, such as scheduling, timetabling, sequencing, etc. In this article, we’ll see how to use CP in two different ways:
-Satisfiability: the goal is to find one or multiple feasible solutions (i.e., solutions that respect our constraints) by narrowing down a large set of potential solutions;
-Optimization: the goal is to find the best feasible solution according to an objective function, just like Linear Programming (LP).


Unlike Linear Programming, we don’t have to define an objective function here.
The reason is simple: there is nothing to optimize! We just want to find a feasible solution that satisfies our constraints, but there is no “good” or “bad” answers. This is a key feature of Constraint Programming.

<p align="center">
<img src="https://github.com/dssdanial/MILP_Optimization/assets/32397445/0c448764-f79e-42b4-bd4c-3ba6f332fdbf" width="350" height="300" />









#### Sources:
https://developers.google.com/optimization
https://mlabonne.github.io/blog/posts/2022-03-02-Linear_Programming.html
