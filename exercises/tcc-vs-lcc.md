# TCC *vs* LCC

Explain under which circumstances *Tight Class Cohesion* (TCC) and *Loose Class Cohesion* (LCC) metrics produce the same value for a given Java class. Build an example of such as class and include the code below or find one example in an open-source project from Github and include the link to the class below. Could LCC be lower than TCC for any given class? Explain.

## Answer

### TCC vs LCC 

TCC is the normalized ratio between the number of methods directly connected with other methods through an instance variable and the total number of possible connections between methods.

LCC is the normalized ratio between the number of methods directly or indirectly connected with other methods through an instance variable and the total number of possible connections between methods.


TCC = LCC = 1 is a maximally cohesive class: all methods are connected.
When TCC and LCC are equal, this mean that the class is too cohesive.


