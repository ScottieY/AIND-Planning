## STRIPS

STRIPS stands for Stanford Research Institute Problem Solver. It is an automated planner that works by executing a domain and problem to find a final goal. With STRIPS, the world is described by objects, actions, preconditions and effects. A problem would have an inital state and a goal condition. STRIPS would search through all possible states from the inital state, executing various valid actions that satisfying the preconditions, and eventually reach the goal.



A cooman language for writing STRIPS domain and problems sets is the Planning Domain Definition Language(PDDL) as we used to described the Air Cargo Problem.



STRIPS allows computer make plan and reach goals by just knowing the initial states and actions.



## General Problem Solver

General Problem Solver(GPS) was a computer program created in 1959 by Herbert A.Simon, J.C.Shaw, and Allen Newell intended to work as a universal problem solver machine. Any problem that can be expressed as a set of well-formed formulas (WFFs) or Horn clauses, and that constitute a directed graph with one or more sources (viz., axioms) and sinks (viz., desired conclusions), can be solved, in principle, by GPS. Proofs in the predicate logic and Euclidean geometry problem spaces are prime examples of the domain the applicability of GPS.



While GPS solved simple problems such as the Towers of Hanoi that could be sufficiently formalized, it could not solve any real-world problems because search was easily lost in the combinatorial explosion. Later on, alpha-beta pruning and min-max algorithm were developed to address this explosion issue.



## Heuristic Problem Solving

In their Turing Award acceptance speech, Allen Newell and Herbert A. Simon discuss the heuristic search hypothesis: a physical symbol system will repeatedly generate and modify known symbol structures until the created structure matches the solution structure. Each successive iteration depends upon the step before it, thus the heuristic search learns what avenues to pursue and which ones to disregard by measuring how close the current iteration is to the solution. Therefore, some possibilities will never be generated as they are measured to be less likely to complete the solution.



A heuristic method can accomplish its task by using search trees. However, instead of generating all possible solution branches, a heuristic selects branches more likely to produce outcomes than other branches. It is selective at each decision point, picking branches that are more likely to produce solutions.



The heuristic function is a way to inform the search about the direction to a goal. It only uses the existing information about the state. 

### Sources:

http://www.primaryobjects.com/2015/11/06/artificial-intelligence-planning-with-strips-a-gentle-introduction/

https://en.wikipedia.org/wiki/General_Problem_Solver

https://en.wikipedia.org/wiki/Heuristic_(computer_science)

http://artint.info/html/ArtInt_56.html