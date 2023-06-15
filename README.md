# MatSurv_ITS

This repo contains the R markdown code used for the segmented regression analyses of the MatSurvey study.

The analysis code is made available under an MIT license - please refer to the license file in this repository for full details.

EID requires authors to not include equations and describe the model equations in words. While this makes the methods section more accessible to less mathematically inclined readers, it can leave the actual model details ambiguous.
To avoid this, we provide here the model equations for the segmented regression models we used:

Mathematically, our modelling framework can be written as:

$$
\log(E[Y|t1,t2]) = b_0 + b_1\cdot t + b_2\cdot I(t-t_1) + b_3\cdot (t-t_1)_{+} + b_4\cdot I(t-t_2) + b_5\cdot (t-t_2)_{+}
$$

where $Y$ is the response variable, $I(x) = 0$ if $x \leq 0$ and 1 if $x>0$ and $(x)_{+} = 0$ if $x \leq 0$ and x if $x>0$, $Y|t_1,t_2$ follows a negative binomial distribution and $b_1, b_2, b_3, b_4, b_5$ are regression coefficients to be estimated. 
