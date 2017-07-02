# Research Review

Many experts say that we are currently experiencing an *Ai Renaissance* 
with a lot of monay and focus in many business are trying to harness the power of 
computing in new and more intelegent ways. 

Large planning problems are a common challenge for business and a key area where Ai practitionars 
have made significant progress.
The following are three big advances in *classical planning* which I have selected to highlight from the 
book *Artificial Intelligence: A Modern Approach* by Norvig and Russell.

### Defining the Problem
Modeling or definging the problem is the very first and key step that needs
to be completed before a planning problem can be solved by Ai. The deficulty arrises when 
we try to take the real world with all of its compleixty and try to boil in down to 
logical statments which can be used in algorythms to interate over what is called that state space.

According to Norvig and Russell, STRIPS was the very first major planning system which 
used a representation language and set the stage for what is now __PDDL__. 

>*Problem Domain Description Language or PDDL (Ghallab et al., 1998), 
was introduced as a computer-parsable, standardized synatx for rpresenting
planning problems and has been used s the standard language for the 
International Planning Competition since 1998. - Norvig and Russell. - Artificial Intelligence: A Modern Approach*

PDDL made modleing the problems simpler by employing two key concepts:
* __Database Semantic:__ assumes if it is not mentioned than it is considered false
* __Action Schemas:__ gives a structured way to define the preconditions and effents of actions.

### A Better Way to Search For a Plan - HSP
Probubly the biggiest hurtl to overcome in solving planning problems is the complexity of the search
which leads to large time and space requriements which ultimatly render many solutions impractical.
Early on, this difficulty drove a loss in interest in state-space planning. Interst was revitalized by the introduction
of __Hueristic Search Plnannung (HSP)__. 

> *"Bont and Geffner's Hueristic Search Planning (HSP) and its later derivatives
 (Bont and Geffner, 1999; Haslum et al., 2005; Haslum, 2006) were the first to make 
 state-space search practical for large planning problems." - Norvig and Russell. - Artificial Intelligence: A Modern Approach*


Unfortunatily, derving good hueristics for the problem is key for HSP to be succesful and was soon
discovered that there are some limitiations with deriving good heuristics. 

> *Hoffmann et al. (2006) shows some limiations of abstraction for classivcal planning problems. - 
Norvig and Russell. - Artificial Intelligence: A Modern Approach*

### A Better Way to Build a Heuristic - GRAPHPLAN
Even though there was promissing results comming out of the HSP implimentations of search,
there were deficulty in determining good hueristics for different types of planning problems.
This was the case until Avrim Blum and Marerric Furst introduced the idea of __GRAPHPLAN__. 

> *"Avrim Blum and Maerrick Furst (1995,1997) revitalized the field 
of planning with thier GRAPHPLAN system, which was orders 
of magnitude faster than the partial order planning" - Artificial Intelligence: A Modern Approach*

Many different derived works of the GRAPHPLAN help derive heuristics used to 
guide search in many large plroblems.

### Conclusion
Without advances in defining the problem, improving the speed of the search and finally the advances in 
hardware performance, much of the work in classical planning would be purly academic with no practical use. 
It was these three breakthroughs in combination others not mentioned here 
that added to much of what we are now seeing in the *Ai Renaissance* of today.

