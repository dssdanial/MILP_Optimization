# Train scheduling documentation

## 1- Train dispatching approaches

An effective Decision Support System (DSS) must be able to provide the dispatcher with a conflict-free disposition schedule, which assigns a travel path and a start time to each train movement inside the
considered time horizon and, additionally, minimizes the delays (and possibly the main broken connections) that could occur in the network. The main pre-requisite of a good DSS is the ability to deal with actual traffic conditions and safety rules for practical networks. In other words, the solution provided by a DSS must be feasible in practice, since the human
dispatcher may have not enough time to check and eventually adjust the schedule suggested by the DSS.

A recognized approach to represent the feasibility of a railway schedule is provided by the **blocking time theory**, which represents a safe corridor for the train movements in the railway network with the so-called blocking time stairways.
A set of individually feasible blocking time stairways (one foreach train) is globally feasible if no two blocking time stairways overlap.


One of the most successful attempt in the literature to incorporate the blocking time theory in an optimization model is based on the **alternative graph model**. However, an alternative graph formulation can
be easily translated into a mixed integer program (MIP), and then solved with a commercial software.




## 2- MILP formulations
<img src="https://github.com/dssdanial/MILP_Optimization/assets/32397445/36e1aa01-2faa-4f56-9166-b8b5b33efe3c"  />






source: https://www.dia.uniroma3.it/~sezione/wordpress/wp-content/uploads/2015/02/2013-207.pdf
Real-time train scheduling:from theory to practice
