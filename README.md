# Implement the Algorithm Simulated Annealing 
# Documentation & Sample Sources
https://vuonghienuit.wordpress.com/2012/05/13/simulated-annealing-thuat-toan-mo-phong-luyen-kim/
https://www.codeproject.com/Articles/13789/Simulated-Annealing-Example-in-C
## Simulated Annealing Algorithm (For minimization case)
```
Select an initial temperature 𝑇>0;  (Initially a high number)
Select a temperature reduction function α;

Select a (initial) candidate solution 𝑠_0; 
Best  𝑠_0;
Repeat  (Cooling loop)
      Repeat (Search move loop)
           Randomly select  s∈𝑁(𝑠_0);   (Tweck: Incumbent solution)
           δ=𝑓(𝑠)−𝑓(𝑠_0)";"
           If δ<0                            (Improving move)        
              then 𝑠_0  𝑠;
           Else                                 (Non-improving move)  
              if U(0,1)< exp(−δ/𝑘𝑇) then 𝑠_0  𝑠;
           If 𝑓(𝑠_0 )<𝑓(𝐵𝑒𝑠𝑡)", "then Best"  " 𝑠_0 ";"
      Until 𝐼𝑡𝑒𝑟𝑎𝑡𝑖𝑜𝑛_𝑐𝑜𝑢𝑛𝑡= # of replications
      Set 𝑇=α(𝑇);
Until stopping condition = true.

```
