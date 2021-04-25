# pdo_bio_opt
<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=default"></script>


## Executive Summary

The consistent creation of peniciliin is critical modern life. Increasing demand for antibiotics is driving the annual growth of this part of the pharmaceutical industry and predictable fermentation is key(Lee).  Peniciilin V is converted into amoxicillin and amicillin. 

Multi-objective otimization

## Background
### Penicillin Production Model
This is a model of Penicilln V prodcued by the fermentation of the fungus *Penicillium chrysogenum*. The mathemtical model of fermentation used here accounts for production  in 3 celluar types in the fungus. 
### CSTR Model
Continiously Stirred-Tank Reactor are an alternative to the 
-This model assumes perfect mixing & a uniform concentration profile

## Formulation

##### System of Equations
The system of equations used can be found in the paper by Binjade. It is a modification of the fermentation model found in the Lee paper for a feed barch penicillin production set-up. To apply that model to the CSTR process, the equations were made time-independent. This assumption is possible because of the ideal CSTR model where there is perfect missing and a uniform concentration profile (Bush, FluidFlo).

|Constant|Value|Units| Meaning|
|---|---|---| ---|
|$\alpha_{csl}$||| |
|||| |

#### Objective Functions
$Penicillin Concentration = C_{pen}$  
$R = \hat V \times C_{pen}$  
$ P = S_{pen} \times n \times C_{pen} \times \hat V \times (1-f) - C_{opt} $  
$ Y = \frac{\displaystyle C_{pen}}{\displaystyle In_{glu} \times \alpha_{csl} \times In_{cls}}$ 


### Processs Control Variables
These design varaibles would be manipulated to controll the managed the fermentation process.  

| Symb. | Meaning | Units | Lower Bound| Upper Bound|   
|---|---|-----|---|---|
| $ \hat V $ | Volumetric flow into reactor | $L* hr^-1$ |0| 5,000 |
| $ Vol $ | Volumn of Reactor | L | 0 | 5,000,000|  
| $In_{glu}$ |Glucose concentration input into the  reactor | $$ gm*L^-1 $$ |0|909|
| $In_{cls}$ |CSL concentration input into reactor | $$ gm*L^-1 $$ |0|909|
| $ X $ |Biomass concentration inside reactor | $$ gm*L^-1 $$ | 0 | 40 |  

### Reactor Condition Varaibles
These design variables are needed to solve the system of equation defined above. 

| Symb. | Meaning | Units | Lower Bound| Upper Bound|   
|---|---|---|---|---|
|$Z_a$|Apical cells|~|0|1|
|$Z_s$|Subapical cells|~|0|1|
|$Z_h$|Hyphal cells|~|0|1|
| $C_{glu}$ |Glucose concentration inside reactor |  $$ gm*L^-1 $$ |0|909 
| $C_{cls}$ |CSL concentration inside reactor |  $$ gm*L^-1 $$ |0|909|
| $C_{pen}$ | Penicillin Concentration|  $$ gm*L^-1 $$ | 0 | 100

#### Constraints
$$ SSE \leq 1^-25 $$ 
$$ yield < 1$$ 
$$ C_{pen} \leq 100 $$
$$ Vol \leq 5,000,000 $$ 
$$ \dfrac{Vol}{\hat V} \leq 1000 $$
$$ C_{glu} \leq 1^-25 $$
$$ C_{cls} \leq 1^-25 $$
$$ Z_a + Z_s + Z_h = 1 $$

### Results
### Conclusion

### References

---

- Bush, Derek B., and Dila Banjade. "Optimization of Penicillin V Production Using a Continuous Reactor." (2015).

- Lee, Fook Choon, Gade Pandu Rangaiah, and Ajay Kumar Ray. "Multi‐objective optimization of an industrial penicillin V bioreactor train using non‐dominated sorting genetic algorithm." Biotechnology and bioengineering 98.3 (2007): 586-598.

- Zangirolami, Teresa C., et al. "Simulation of penicillin production in fed‐batch cultivations using a morphologically structured model." Biotechnology and bioengineering 56.6 (1997): 593-604.

- FluidFlo, director. Three Main Ideal Reactors (Batch, PFR, MFR/CSTR). YouTube, YouTube, 8 Feb. 2015, www.youtube.com/watch?v=XyLUVSfHL0Y. 
