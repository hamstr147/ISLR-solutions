ISLR Chapter 7 Solutions - conceptual
================

## Exercise 1

**It was mentioned in the chapter that a cubic regression spline with
one knot at ![\\xi](https://latex.codecogs.com/png.latex?%5Cxi "\\xi")
can be obtained using a basis of the form
![x](https://latex.codecogs.com/png.latex?x "x"),
![x^2](https://latex.codecogs.com/png.latex?x%5E2 "x^2"),
![x^3](https://latex.codecogs.com/png.latex?x%5E3 "x^3"),
![(x-\\xi)^3\_+](https://latex.codecogs.com/png.latex?%28x-%5Cxi%29%5E3_%2B
"(x-\\xi)^3_+"), where
![(x-\\xi)^3\_+=(x-\\xi)^3](https://latex.codecogs.com/png.latex?%28x-%5Cxi%29%5E3_%2B%3D%28x-%5Cxi%29%5E3
"(x-\\xi)^3_+=(x-\\xi)^3") if
![x\>\\xi](https://latex.codecogs.com/png.latex?x%3E%5Cxi "x\>\\xi") and
equals ![0](https://latex.codecogs.com/png.latex?0 "0") otherwise. We
will now show that a function of the form   
![&#10;f(x)=\\beta\_0+\\beta\_1x+\\beta\_2x^2+\\beta\_3x^3+\\beta\_4(x-\\xi)^3\_+&#10;](https://latex.codecogs.com/png.latex?%0Af%28x%29%3D%5Cbeta_0%2B%5Cbeta_1x%2B%5Cbeta_2x%5E2%2B%5Cbeta_3x%5E3%2B%5Cbeta_4%28x-%5Cxi%29%5E3_%2B%0A
"
f(x)=\\beta_0+\\beta_1x+\\beta_2x^2+\\beta_3x^3+\\beta_4(x-\\xi)^3_+
")  
is indeed a cubic regression spline, regardless of the values of
![\\beta\_0](https://latex.codecogs.com/png.latex?%5Cbeta_0 "\\beta_0"),
![\\beta\_1](https://latex.codecogs.com/png.latex?%5Cbeta_1 "\\beta_1"),
![\\beta\_2](https://latex.codecogs.com/png.latex?%5Cbeta_2 "\\beta_2"),
![\\beta\_3](https://latex.codecogs.com/png.latex?%5Cbeta_3 "\\beta_3"),
![\\beta\_4](https://latex.codecogs.com/png.latex?%5Cbeta_4
"\\beta_4").**

**(a) Find a cubic polynomial   
![&#10;f\_1(x)=a\_1+b\_1x+c\_1x^2+d\_1x^3&#10;](https://latex.codecogs.com/png.latex?%0Af_1%28x%29%3Da_1%2Bb_1x%2Bc_1x%5E2%2Bd_1x%5E3%0A
"
f_1(x)=a_1+b_1x+c_1x^2+d_1x^3
")  
such that
![f(x)=f\_1(x)](https://latex.codecogs.com/png.latex?f%28x%29%3Df_1%28x%29
"f(x)=f_1(x)") for all
![x\\leq\\xi](https://latex.codecogs.com/png.latex?x%5Cleq%5Cxi
"x\\leq\\xi"). Express ![a\_1](https://latex.codecogs.com/png.latex?a_1
"a_1"), ![b\_1](https://latex.codecogs.com/png.latex?b_1 "b_1"),
![c\_1](https://latex.codecogs.com/png.latex?c_1 "c_1"),
![d\_1](https://latex.codecogs.com/png.latex?d_1 "d_1") in terms of
![\\beta\_0](https://latex.codecogs.com/png.latex?%5Cbeta_0 "\\beta_0"),
![\\beta\_1](https://latex.codecogs.com/png.latex?%5Cbeta_1 "\\beta_1"),
![\\beta\_2](https://latex.codecogs.com/png.latex?%5Cbeta_2 "\\beta_2"),
![\\beta\_3](https://latex.codecogs.com/png.latex?%5Cbeta_3 "\\beta_3"),
![\\beta\_4](https://latex.codecogs.com/png.latex?%5Cbeta_4
"\\beta_4").**

A cubic polynomial that satisfies these requirements is   
![&#10;f\_1(x)=\\beta\_0+\\beta\_1x+\\beta\_2x^2+\\beta\_3x^3&#10;](https://latex.codecogs.com/png.latex?%0Af_1%28x%29%3D%5Cbeta_0%2B%5Cbeta_1x%2B%5Cbeta_2x%5E2%2B%5Cbeta_3x%5E3%0A
"
f_1(x)=\\beta_0+\\beta_1x+\\beta_2x^2+\\beta_3x^3
")  

**(b) Find a cubic polynomial   
![&#10;f\_2(x)=a\_2+b\_2x+c\_2x^2+d\_2x^3&#10;](https://latex.codecogs.com/png.latex?%0Af_2%28x%29%3Da_2%2Bb_2x%2Bc_2x%5E2%2Bd_2x%5E3%0A
"
f_2(x)=a_2+b_2x+c_2x^2+d_2x^3
")  
such that
![f(x)=f\_2(x)](https://latex.codecogs.com/png.latex?f%28x%29%3Df_2%28x%29
"f(x)=f_2(x)") for all
![x\>\\xi](https://latex.codecogs.com/png.latex?x%3E%5Cxi "x\>\\xi").
Express ![a\_2](https://latex.codecogs.com/png.latex?a_2 "a_2"),
![b\_2](https://latex.codecogs.com/png.latex?b_2 "b_2"),
![c\_2](https://latex.codecogs.com/png.latex?c_2 "c_2"),
![d\_2](https://latex.codecogs.com/png.latex?d_2 "d_2") in terms of
![\\beta\_0](https://latex.codecogs.com/png.latex?%5Cbeta_0 "\\beta_0"),
![\\beta\_1](https://latex.codecogs.com/png.latex?%5Cbeta_1 "\\beta_1"),
![\\beta\_2](https://latex.codecogs.com/png.latex?%5Cbeta_2 "\\beta_2"),
![\\beta\_3](https://latex.codecogs.com/png.latex?%5Cbeta_3 "\\beta_3"),
![\\beta\_4](https://latex.codecogs.com/png.latex?%5Cbeta_4
"\\beta_4").**

We can derive a cubic polynomial that satisfies these requirements:   
![&#10;f\_2(x)=\\beta\_0+\\beta\_1x+\\beta\_2x^2+\\beta\_3x^3+\\beta\_4(x-\\xi)^3\\\\&#10;=\\beta\_0+\\beta\_1x+\\beta\_2x^2+\\beta\_3x^3+\\beta\_4(x-\\xi)(x^2-2x\\xi+\\xi^2)\\\\&#10;=\\beta\_0+\\beta\_1x+\\beta\_2x^2+\\beta\_3x^3+\\beta\_4(x^3-3x^2\\xi+3x\\xi^2-\\xi^3)\\\\&#10;=\\beta\_0+\\beta\_1x+\\beta\_2x^2+\\beta\_3x^3+\\beta\_4x^3-3\\beta\_4x^2\\xi+3\\beta\_4x\\xi^2-\\beta\_4\\xi^3\\\\&#10;=(\\beta\_0-\\beta\_4\\xi^3)+(\\beta\_1+3\\beta\_4\\xi^2)x+(\\beta\_2-3\\beta\_4\\xi)x^2+(\\beta\_3+\\beta\_4)x^3\\\\&#10;](https://latex.codecogs.com/png.latex?%0Af_2%28x%29%3D%5Cbeta_0%2B%5Cbeta_1x%2B%5Cbeta_2x%5E2%2B%5Cbeta_3x%5E3%2B%5Cbeta_4%28x-%5Cxi%29%5E3%5C%5C%0A%3D%5Cbeta_0%2B%5Cbeta_1x%2B%5Cbeta_2x%5E2%2B%5Cbeta_3x%5E3%2B%5Cbeta_4%28x-%5Cxi%29%28x%5E2-2x%5Cxi%2B%5Cxi%5E2%29%5C%5C%0A%3D%5Cbeta_0%2B%5Cbeta_1x%2B%5Cbeta_2x%5E2%2B%5Cbeta_3x%5E3%2B%5Cbeta_4%28x%5E3-3x%5E2%5Cxi%2B3x%5Cxi%5E2-%5Cxi%5E3%29%5C%5C%0A%3D%5Cbeta_0%2B%5Cbeta_1x%2B%5Cbeta_2x%5E2%2B%5Cbeta_3x%5E3%2B%5Cbeta_4x%5E3-3%5Cbeta_4x%5E2%5Cxi%2B3%5Cbeta_4x%5Cxi%5E2-%5Cbeta_4%5Cxi%5E3%5C%5C%0A%3D%28%5Cbeta_0-%5Cbeta_4%5Cxi%5E3%29%2B%28%5Cbeta_1%2B3%5Cbeta_4%5Cxi%5E2%29x%2B%28%5Cbeta_2-3%5Cbeta_4%5Cxi%29x%5E2%2B%28%5Cbeta_3%2B%5Cbeta_4%29x%5E3%5C%5C%0A
"
f_2(x)=\\beta_0+\\beta_1x+\\beta_2x^2+\\beta_3x^3+\\beta_4(x-\\xi)^3\\\\
=\\beta_0+\\beta_1x+\\beta_2x^2+\\beta_3x^3+\\beta_4(x-\\xi)(x^2-2x\\xi+\\xi^2)\\\\
=\\beta_0+\\beta_1x+\\beta_2x^2+\\beta_3x^3+\\beta_4(x^3-3x^2\\xi+3x\\xi^2-\\xi^3)\\\\
=\\beta_0+\\beta_1x+\\beta_2x^2+\\beta_3x^3+\\beta_4x^3-3\\beta_4x^2\\xi+3\\beta_4x\\xi^2-\\beta_4\\xi^3\\\\
=(\\beta_0-\\beta_4\\xi^3)+(\\beta_1+3\\beta_4\\xi^2)x+(\\beta_2-3\\beta_4\\xi)x^2+(\\beta_3+\\beta_4)x^3\\\\
")  
Therefore we can express
![a\_2](https://latex.codecogs.com/png.latex?a_2 "a_2"),
![b\_2](https://latex.codecogs.com/png.latex?b_2 "b_2"),
![c\_2](https://latex.codecogs.com/png.latex?c_2 "c_2"),
![d\_2](https://latex.codecogs.com/png.latex?d_2 "d_2") in terms of
![\\beta\_0](https://latex.codecogs.com/png.latex?%5Cbeta_0 "\\beta_0"),
![\\beta\_1](https://latex.codecogs.com/png.latex?%5Cbeta_1 "\\beta_1"),
![\\beta\_2](https://latex.codecogs.com/png.latex?%5Cbeta_2 "\\beta_2"),
![\\beta\_3](https://latex.codecogs.com/png.latex?%5Cbeta_3 "\\beta_3"),
![\\beta\_4](https://latex.codecogs.com/png.latex?%5Cbeta_4 "\\beta_4")
as follows:   
![&#10;a\_2=\\beta\_0-\\beta\_4\\xi^3\\\\&#10;b\_2=\\beta\_1+3\\beta\_4\\xi^2\\\\&#10;c\_2=\\beta\_2-3\\beta\_4\\xi\\\\&#10;d\_2=\\beta\_3+\\beta\_4\\\\&#10;](https://latex.codecogs.com/png.latex?%0Aa_2%3D%5Cbeta_0-%5Cbeta_4%5Cxi%5E3%5C%5C%0Ab_2%3D%5Cbeta_1%2B3%5Cbeta_4%5Cxi%5E2%5C%5C%0Ac_2%3D%5Cbeta_2-3%5Cbeta_4%5Cxi%5C%5C%0Ad_2%3D%5Cbeta_3%2B%5Cbeta_4%5C%5C%0A
"
a_2=\\beta_0-\\beta_4\\xi^3\\\\
b_2=\\beta_1+3\\beta_4\\xi^2\\\\
c_2=\\beta_2-3\\beta_4\\xi\\\\
d_2=\\beta_3+\\beta_4\\\\
")  

**(c) Show that
![f\_1(\\xi)=f\_2(\\xi)](https://latex.codecogs.com/png.latex?f_1%28%5Cxi%29%3Df_2%28%5Cxi%29
"f_1(\\xi)=f_2(\\xi)"). That is,
![f(x)](https://latex.codecogs.com/png.latex?f%28x%29 "f(x)") is
continuous at ![\\xi](https://latex.codecogs.com/png.latex?%5Cxi
"\\xi").**

We can show that
![f\_2(\\xi)](https://latex.codecogs.com/png.latex?f_2%28%5Cxi%29
"f_2(\\xi)") is equivalent to
![f\_1(\\xi)](https://latex.codecogs.com/png.latex?f_1%28%5Cxi%29
"f_1(\\xi)"):   
![&#10;f\_2(\\xi)=(\\beta\_0-\\beta\_4\\xi^3)+(\\beta\_1+3\\beta\_4\\xi^2)\\xi+(\\beta\_2-3\\beta\_4\\xi)\\xi^2+(\\beta\_3+\\beta\_4)\\xi^3\\\\&#10;=\\beta\_0-\\beta\_4\\xi^3+\\beta\_1\\xi+3\\beta\_4\\xi^3+\\beta\_2\\xi^2-3\\beta\_4\\xi^3+\\beta\_3\\xi^3+\\beta\_4\\xi^3\\\\&#10;=\\beta\_0+\\beta\_1\\xi+\\beta\_2\\xi^2+\\beta\_3\\xi^3\\\\&#10;=f\_1(\\xi)&#10;](https://latex.codecogs.com/png.latex?%0Af_2%28%5Cxi%29%3D%28%5Cbeta_0-%5Cbeta_4%5Cxi%5E3%29%2B%28%5Cbeta_1%2B3%5Cbeta_4%5Cxi%5E2%29%5Cxi%2B%28%5Cbeta_2-3%5Cbeta_4%5Cxi%29%5Cxi%5E2%2B%28%5Cbeta_3%2B%5Cbeta_4%29%5Cxi%5E3%5C%5C%0A%3D%5Cbeta_0-%5Cbeta_4%5Cxi%5E3%2B%5Cbeta_1%5Cxi%2B3%5Cbeta_4%5Cxi%5E3%2B%5Cbeta_2%5Cxi%5E2-3%5Cbeta_4%5Cxi%5E3%2B%5Cbeta_3%5Cxi%5E3%2B%5Cbeta_4%5Cxi%5E3%5C%5C%0A%3D%5Cbeta_0%2B%5Cbeta_1%5Cxi%2B%5Cbeta_2%5Cxi%5E2%2B%5Cbeta_3%5Cxi%5E3%5C%5C%0A%3Df_1%28%5Cxi%29%0A
"
f_2(\\xi)=(\\beta_0-\\beta_4\\xi^3)+(\\beta_1+3\\beta_4\\xi^2)\\xi+(\\beta_2-3\\beta_4\\xi)\\xi^2+(\\beta_3+\\beta_4)\\xi^3\\\\
=\\beta_0-\\beta_4\\xi^3+\\beta_1\\xi+3\\beta_4\\xi^3+\\beta_2\\xi^2-3\\beta_4\\xi^3+\\beta_3\\xi^3+\\beta_4\\xi^3\\\\
=\\beta_0+\\beta_1\\xi+\\beta_2\\xi^2+\\beta_3\\xi^3\\\\
=f_1(\\xi)
")  

**(d) Show that
![f'\_1(\\xi)=f'\_2(\\xi)](https://latex.codecogs.com/png.latex?f%27_1%28%5Cxi%29%3Df%27_2%28%5Cxi%29
"f'_1(\\xi)=f'_2(\\xi)"). That is,
![f'(x)](https://latex.codecogs.com/png.latex?f%27%28x%29 "f'(x)") is
continuous at ![\\xi](https://latex.codecogs.com/png.latex?%5Cxi
"\\xi").**

First differentiating both
![f\_1(x)](https://latex.codecogs.com/png.latex?f_1%28x%29 "f_1(x)") and
![f\_2(x)](https://latex.codecogs.com/png.latex?f_2%28x%29 "f_2(x)"):   
![&#10;f'\_1(x)=\\beta\_1+2\\beta\_2x+3\\beta\_3x^2\\\\&#10;f'\_2(x)=\\beta\_1+3\\beta\_4\\xi^2+2x(\\beta\_2-3\\beta\_4\\xi)+3x^2(\\beta\_3+\\beta\_4)&#10;](https://latex.codecogs.com/png.latex?%0Af%27_1%28x%29%3D%5Cbeta_1%2B2%5Cbeta_2x%2B3%5Cbeta_3x%5E2%5C%5C%0Af%27_2%28x%29%3D%5Cbeta_1%2B3%5Cbeta_4%5Cxi%5E2%2B2x%28%5Cbeta_2-3%5Cbeta_4%5Cxi%29%2B3x%5E2%28%5Cbeta_3%2B%5Cbeta_4%29%0A
"
f'_1(x)=\\beta_1+2\\beta_2x+3\\beta_3x^2\\\\
f'_2(x)=\\beta_1+3\\beta_4\\xi^2+2x(\\beta_2-3\\beta_4\\xi)+3x^2(\\beta_3+\\beta_4)
")  
We can show that
![f'\_2(\\xi)](https://latex.codecogs.com/png.latex?f%27_2%28%5Cxi%29
"f'_2(\\xi)") is equivalent to
![f'\_1(\\xi)](https://latex.codecogs.com/png.latex?f%27_1%28%5Cxi%29
"f'_1(\\xi)"):   
![&#10;f'\_2(\\xi)=\\beta\_1+\\beta\_43\\xi^2+2\\xi(\\beta\_2-\\beta\_43\\xi)+3\\xi^2(\\beta\_3+\\beta\_4)\\\\&#10;=\\beta\_1+3\\beta\_4\\xi^2+2\\beta\_2\\xi-6\\beta\_4\\xi^2+3\\beta\_3\\xi^2+3\\beta\_4\\xi^2\\\\&#10;=\\beta\_1+2\\beta\_2\\xi+3\\beta\_3\\xi^2\\\\&#10;=f'\_1(\\xi)&#10;](https://latex.codecogs.com/png.latex?%0Af%27_2%28%5Cxi%29%3D%5Cbeta_1%2B%5Cbeta_43%5Cxi%5E2%2B2%5Cxi%28%5Cbeta_2-%5Cbeta_43%5Cxi%29%2B3%5Cxi%5E2%28%5Cbeta_3%2B%5Cbeta_4%29%5C%5C%0A%3D%5Cbeta_1%2B3%5Cbeta_4%5Cxi%5E2%2B2%5Cbeta_2%5Cxi-6%5Cbeta_4%5Cxi%5E2%2B3%5Cbeta_3%5Cxi%5E2%2B3%5Cbeta_4%5Cxi%5E2%5C%5C%0A%3D%5Cbeta_1%2B2%5Cbeta_2%5Cxi%2B3%5Cbeta_3%5Cxi%5E2%5C%5C%0A%3Df%27_1%28%5Cxi%29%0A
"
f'_2(\\xi)=\\beta_1+\\beta_43\\xi^2+2\\xi(\\beta_2-\\beta_43\\xi)+3\\xi^2(\\beta_3+\\beta_4)\\\\
=\\beta_1+3\\beta_4\\xi^2+2\\beta_2\\xi-6\\beta_4\\xi^2+3\\beta_3\\xi^2+3\\beta_4\\xi^2\\\\
=\\beta_1+2\\beta_2\\xi+3\\beta_3\\xi^2\\\\
=f'_1(\\xi)
")  

**(e) Show that
![f''\_1(\\xi)=f''\_2(\\xi)](https://latex.codecogs.com/png.latex?f%27%27_1%28%5Cxi%29%3Df%27%27_2%28%5Cxi%29
"f''_1(\\xi)=f''_2(\\xi)"). That is,
![f''(x)](https://latex.codecogs.com/png.latex?f%27%27%28x%29 "f''(x)")
is continuous at ![\\xi](https://latex.codecogs.com/png.latex?%5Cxi
"\\xi").**

The second derivatives of
![f\_1(x)](https://latex.codecogs.com/png.latex?f_1%28x%29 "f_1(x)") and
![f\_2(x)](https://latex.codecogs.com/png.latex?f_2%28x%29 "f_2(x)") are
  
![&#10;f''\_1(x)=2\\beta\_2+6\\beta\_3x\\\\&#10;f''\_2(x)=2(\\beta\_2-3\\beta\_4\\xi)+6x(\\beta\_3+\\beta\_4)&#10;](https://latex.codecogs.com/png.latex?%0Af%27%27_1%28x%29%3D2%5Cbeta_2%2B6%5Cbeta_3x%5C%5C%0Af%27%27_2%28x%29%3D2%28%5Cbeta_2-3%5Cbeta_4%5Cxi%29%2B6x%28%5Cbeta_3%2B%5Cbeta_4%29%0A
"
f''_1(x)=2\\beta_2+6\\beta_3x\\\\
f''_2(x)=2(\\beta_2-3\\beta_4\\xi)+6x(\\beta_3+\\beta_4)
")  

We can show that
![f''\_2(\\xi)](https://latex.codecogs.com/png.latex?f%27%27_2%28%5Cxi%29
"f''_2(\\xi)") is equivalent to
![f''\_1(\\xi)](https://latex.codecogs.com/png.latex?f%27%27_1%28%5Cxi%29
"f''_1(\\xi)"):   
![&#10;f''\_2(\\xi)=2(\\beta\_2-3\\beta\_4\\xi)+6\\xi(\\beta\_3+\\beta\_4)\\\\&#10;=2\\beta\_2-6\\beta\_4\\xi+6\\beta\_3\\xi+6\\beta\_4\\xi\\\\&#10;=2\\beta\_2+6\\beta\_3\\xi\\\\&#10;=f''\_1(\\xi)&#10;](https://latex.codecogs.com/png.latex?%0Af%27%27_2%28%5Cxi%29%3D2%28%5Cbeta_2-3%5Cbeta_4%5Cxi%29%2B6%5Cxi%28%5Cbeta_3%2B%5Cbeta_4%29%5C%5C%0A%3D2%5Cbeta_2-6%5Cbeta_4%5Cxi%2B6%5Cbeta_3%5Cxi%2B6%5Cbeta_4%5Cxi%5C%5C%0A%3D2%5Cbeta_2%2B6%5Cbeta_3%5Cxi%5C%5C%0A%3Df%27%27_1%28%5Cxi%29%0A
"
f''_2(\\xi)=2(\\beta_2-3\\beta_4\\xi)+6\\xi(\\beta_3+\\beta_4)\\\\
=2\\beta_2-6\\beta_4\\xi+6\\beta_3\\xi+6\\beta_4\\xi\\\\
=2\\beta_2+6\\beta_3\\xi\\\\
=f''_1(\\xi)
")  

**Therefore, ![f(x)](https://latex.codecogs.com/png.latex?f%28x%29
"f(x)") is indeed a cubic spline.**

## Execise 2

**Suppose that a curve
![\\hat{g}](https://latex.codecogs.com/png.latex?%5Chat%7Bg%7D
"\\hat{g}") is computed to smoothly fit a set of
![n](https://latex.codecogs.com/png.latex?n "n") points using the
following formula:   
![&#10;\\hat{g}=\\arg\\min\_g{\\left(\\sum\\limits\_{i=1}^n
(y\_i-g(x\_i))^2+\\lambda\\int\\left\[g^{(m)}(x)\\right\]^2
dx\\right)}&#10;](https://latex.codecogs.com/png.latex?%0A%5Chat%7Bg%7D%3D%5Carg%5Cmin_g%7B%5Cleft%28%5Csum%5Climits_%7Bi%3D1%7D%5En%20%28y_i-g%28x_i%29%29%5E2%2B%5Clambda%5Cint%5Cleft%5Bg%5E%7B%28m%29%7D%28x%29%5Cright%5D%5E2%20dx%5Cright%29%7D%0A
"
\\hat{g}=\\arg\\min_g{\\left(\\sum\\limits_{i=1}^n (y_i-g(x_i))^2+\\lambda\\int\\left[g^{(m)}(x)\\right]^2 dx\\right)}
")  
where ![g^{(m)}](https://latex.codecogs.com/png.latex?g%5E%7B%28m%29%7D
"g^{(m)}") represents the ![m](https://latex.codecogs.com/png.latex?m
"m")th derivative of ![g](https://latex.codecogs.com/png.latex?g "g")
(and
![g^{(0)}=g](https://latex.codecogs.com/png.latex?g%5E%7B%280%29%7D%3Dg
"g^{(0)}=g")). Provide example sketches of
![\\hat{g}](https://latex.codecogs.com/png.latex?%5Chat%7Bg%7D
"\\hat{g}") in each of the following scenarios.**

**(a)
![\\lambda=\\infty,m=0](https://latex.codecogs.com/png.latex?%5Clambda%3D%5Cinfty%2Cm%3D0
"\\lambda=\\infty,m=0")  
(b)
![\\lambda=\\infty,m=1](https://latex.codecogs.com/png.latex?%5Clambda%3D%5Cinfty%2Cm%3D1
"\\lambda=\\infty,m=1")  
(c)
![\\lambda=\\infty,m=2](https://latex.codecogs.com/png.latex?%5Clambda%3D%5Cinfty%2Cm%3D2
"\\lambda=\\infty,m=2")  
(d)
![\\lambda=\\infty,m=3](https://latex.codecogs.com/png.latex?%5Clambda%3D%5Cinfty%2Cm%3D3
"\\lambda=\\infty,m=3")  
(e)
![\\lambda=0,m=3](https://latex.codecogs.com/png.latex?%5Clambda%3D0%2Cm%3D3
"\\lambda=0,m=3")**

The penalty term is the integral of the
![m](https://latex.codecogs.com/png.latex?m "m")th derivative of the
function ![g(x)](https://latex.codecogs.com/png.latex?g%28x%29 "g(x)")
raised to the power of two, multiplied by
![\\lambda](https://latex.codecogs.com/png.latex?%5Clambda "\\lambda").
Given that it is squared, the minimum value it can take is 0. When
![\\lambda=\\infty](https://latex.codecogs.com/png.latex?%5Clambda%3D%5Cinfty
"\\lambda=\\infty") the loss term is ignored so we can look only at the
penalty term; the function is hence minimised where the penalty term is
zero.

In scenario (a), the penalty term is zero where
![g(x)=0](https://latex.codecogs.com/png.latex?g%28x%29%3D0 "g(x)=0").
In scenario (b), the penalty term is zero where
![g(x)](https://latex.codecogs.com/png.latex?g%28x%29 "g(x)") is equal
to any constant, because the derivative of a constant is zero. For
scenario (c), the penalty term is zero where
![g(x)](https://latex.codecogs.com/png.latex?g%28x%29 "g(x)") is a
linear function, because the second derivative of a linear function is
zero. In scenario (d),
![g(x)](https://latex.codecogs.com/png.latex?g%28x%29 "g(x)") would be a
quadratic function, because the third derivative of a quadratic function
is zero.

![](ISLR_chap7_conceptual_files/figure-gfm/unnamed-chunk-1-1.png)<!-- -->

![g(x)](https://latex.codecogs.com/png.latex?g%28x%29 "g(x)") in
scenario (e) would be a function that interpolates all values for x
because it is completely unconstrained; in this case, the penalty term
is zero and so only the sum of squares matters.

## Exercise 3

**Suppose we fit a curve with basis functions
![b\_1(X)=X](https://latex.codecogs.com/png.latex?b_1%28X%29%3DX
"b_1(X)=X"),
![b\_2(X)=(X-1)^2I(X\\geq 1)](https://latex.codecogs.com/png.latex?b_2%28X%29%3D%28X-1%29%5E2I%28X%5Cgeq%201%29
"b_2(X)=(X-1)^2I(X\\geq 1)"). (Note that
![I(X\\geq 1)](https://latex.codecogs.com/png.latex?I%28X%5Cgeq%201%29
"I(X\\geq 1)") equals 1 for
![X\\geq1](https://latex.codecogs.com/png.latex?X%5Cgeq1 "X\\geq1") and
![0](https://latex.codecogs.com/png.latex?0 "0") otherwise.) We fit the
linear regression model   
![&#10;Y=\\beta\_0+\\beta\_1b\_1(X)+\\beta\_2b\_2(X)+\\epsilon&#10;](https://latex.codecogs.com/png.latex?%0AY%3D%5Cbeta_0%2B%5Cbeta_1b_1%28X%29%2B%5Cbeta_2b_2%28X%29%2B%5Cepsilon%0A
"
Y=\\beta_0+\\beta_1b_1(X)+\\beta_2b_2(X)+\\epsilon
")  
and obtain coefficient estimates
![\\hat{\\beta}\_0=1](https://latex.codecogs.com/png.latex?%5Chat%7B%5Cbeta%7D_0%3D1
"\\hat{\\beta}_0=1"),
![\\hat{\\beta}\_1=1](https://latex.codecogs.com/png.latex?%5Chat%7B%5Cbeta%7D_1%3D1
"\\hat{\\beta}_1=1"),
![\\hat{\\beta}\_2=-2](https://latex.codecogs.com/png.latex?%5Chat%7B%5Cbeta%7D_2%3D-2
"\\hat{\\beta}_2=-2"). Sketch the estimated curve between
![X=-2](https://latex.codecogs.com/png.latex?X%3D-2 "X=-2") and
![X=2](https://latex.codecogs.com/png.latex?X%3D2 "X=2"). Note the
intercepts, slopes and other relevant information.**

The slope starts to decrease at
![X=1](https://latex.codecogs.com/png.latex?X%3D1 "X=1") - when
![X\<1](https://latex.codecogs.com/png.latex?X%3C1 "X\<1"), the slope is
one (and hence a straight line), and thereafter starts to decrease
because of the quadratic basis function
![b\_2](https://latex.codecogs.com/png.latex?b_2 "b_2") having a
negative coefficient. The ![X](https://latex.codecogs.com/png.latex?X
"X") intercept is at ![X=-1](https://latex.codecogs.com/png.latex?X%3D-1
"X=-1") and the ![Y](https://latex.codecogs.com/png.latex?Y "Y")
intercept is at ![Y=1](https://latex.codecogs.com/png.latex?Y%3D1
"Y=1").
![](ISLR_chap7_conceptual_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

## Exercise 4

**Suppose we fit a curve with basis functions ![b\_1(X)=I(0\\leq
X\\leq2)-(X-1)I(1\\leq
X\\leq 2)](https://latex.codecogs.com/png.latex?b_1%28X%29%3DI%280%5Cleq%20X%5Cleq2%29-%28X-1%29I%281%5Cleq%20X%5Cleq%202%29
"b_1(X)=I(0\\leq X\\leq2)-(X-1)I(1\\leq X\\leq 2)"),
![b\_2(X)=(X-3)I(3\\leq
X\\leq4)+I(4\<X\\leq5)](https://latex.codecogs.com/png.latex?b_2%28X%29%3D%28X-3%29I%283%5Cleq%20X%5Cleq4%29%2BI%284%3CX%5Cleq5%29
"b_2(X)=(X-3)I(3\\leq X\\leq4)+I(4\<X\\leq5)"). We fit the linear
regression model   
![&#10;Y=\\beta\_0+\\beta\_1b\_1(X)+\\beta\_2b\_2(X)+\\epsilon&#10;](https://latex.codecogs.com/png.latex?%0AY%3D%5Cbeta_0%2B%5Cbeta_1b_1%28X%29%2B%5Cbeta_2b_2%28X%29%2B%5Cepsilon%0A
"
Y=\\beta_0+\\beta_1b_1(X)+\\beta_2b_2(X)+\\epsilon
")  
and obtain coefficient estimates
![\\hat{\\beta}\_0=1](https://latex.codecogs.com/png.latex?%5Chat%7B%5Cbeta%7D_0%3D1
"\\hat{\\beta}_0=1"),
![\\hat{\\beta}\_1=1](https://latex.codecogs.com/png.latex?%5Chat%7B%5Cbeta%7D_1%3D1
"\\hat{\\beta}_1=1"),
![\\hat{\\beta}\_2=3](https://latex.codecogs.com/png.latex?%5Chat%7B%5Cbeta%7D_2%3D3
"\\hat{\\beta}_2=3"). Sketch the estimated curve between
![X=-2](https://latex.codecogs.com/png.latex?X%3D-2 "X=-2") and
![X=2](https://latex.codecogs.com/png.latex?X%3D2 "X=2"). Note the
intercepts, slopes and other relevant information.**

Where ![X\<0](https://latex.codecogs.com/png.latex?X%3C0 "X\<0"),
![Y](https://latex.codecogs.com/png.latex?Y "Y") is
![1](https://latex.codecogs.com/png.latex?1 "1"). Where ![0\\leq
X\\leq1](https://latex.codecogs.com/png.latex?0%5Cleq%20X%5Cleq1
"0\\leq X\\leq1"), ![Y](https://latex.codecogs.com/png.latex?Y "Y") is
![2](https://latex.codecogs.com/png.latex?2 "2"). Thereafter, the curve
is a downward sloping straight line with slope
![-1](https://latex.codecogs.com/png.latex?-1 "-1"), due to the second
term in basis function ![b\_1](https://latex.codecogs.com/png.latex?b_1
"b_1"). The basis function
![b\_2](https://latex.codecogs.com/png.latex?b_2 "b_2") does not affect
values for ![X](https://latex.codecogs.com/png.latex?X "X") between
![-2](https://latex.codecogs.com/png.latex?-2 "-2") and
![2](https://latex.codecogs.com/png.latex?2 "2").
![](ISLR_chap7_conceptual_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

## Exercise 5

**Consider two curves,
![\\hat{g}\_1](https://latex.codecogs.com/png.latex?%5Chat%7Bg%7D_1
"\\hat{g}_1") and
![\\hat{g}\_2](https://latex.codecogs.com/png.latex?%5Chat%7Bg%7D_2
"\\hat{g}_2"), defined by   
![&#10;\\hat{g}\_1=\\arg\\min\_g{\\left(\\sum\\limits\_{i=1}^n
(y\_i-g(x\_i))^2+\\lambda\\int\\left\[g^{(3)}(x)\\right\]^2
dx\\right)},\\\\&#10;\\hat{g}\_2=\\arg\\min\_g{\\left(\\sum\\limits\_{i=1}^n
(y\_i-g(x\_i))^2+\\lambda\\int\\left\[g^{(4)}(x)\\right\]^2
dx\\right)}\\\\&#10;](https://latex.codecogs.com/png.latex?%0A%5Chat%7Bg%7D_1%3D%5Carg%5Cmin_g%7B%5Cleft%28%5Csum%5Climits_%7Bi%3D1%7D%5En%20%28y_i-g%28x_i%29%29%5E2%2B%5Clambda%5Cint%5Cleft%5Bg%5E%7B%283%29%7D%28x%29%5Cright%5D%5E2%20dx%5Cright%29%7D%2C%5C%5C%0A%5Chat%7Bg%7D_2%3D%5Carg%5Cmin_g%7B%5Cleft%28%5Csum%5Climits_%7Bi%3D1%7D%5En%20%28y_i-g%28x_i%29%29%5E2%2B%5Clambda%5Cint%5Cleft%5Bg%5E%7B%284%29%7D%28x%29%5Cright%5D%5E2%20dx%5Cright%29%7D%5C%5C%0A
"
\\hat{g}_1=\\arg\\min_g{\\left(\\sum\\limits_{i=1}^n (y_i-g(x_i))^2+\\lambda\\int\\left[g^{(3)}(x)\\right]^2 dx\\right)},\\\\
\\hat{g}_2=\\arg\\min_g{\\left(\\sum\\limits_{i=1}^n (y_i-g(x_i))^2+\\lambda\\int\\left[g^{(4)}(x)\\right]^2 dx\\right)}\\\\
")  
where ![g^{(m)}](https://latex.codecogs.com/png.latex?g%5E%7B%28m%29%7D
"g^{(m)}") represents the ![m](https://latex.codecogs.com/png.latex?m
"m")th derivative of ![g](https://latex.codecogs.com/png.latex?g "g").**

**(a) As
![\\lambda\\rightarrow\\infty](https://latex.codecogs.com/png.latex?%5Clambda%5Crightarrow%5Cinfty
"\\lambda\\rightarrow\\infty"), will
![\\hat{g}\_1](https://latex.codecogs.com/png.latex?%5Chat%7Bg%7D_1
"\\hat{g}_1") or
![\\hat{g}\_2](https://latex.codecogs.com/png.latex?%5Chat%7Bg%7D_2
"\\hat{g}_2") have the smaller training RSS?  
(b) As
![\\lambda\\rightarrow\\infty](https://latex.codecogs.com/png.latex?%5Clambda%5Crightarrow%5Cinfty
"\\lambda\\rightarrow\\infty"), will
![\\hat{g}\_1](https://latex.codecogs.com/png.latex?%5Chat%7Bg%7D_1
"\\hat{g}_1") or
![\\hat{g}\_2](https://latex.codecogs.com/png.latex?%5Chat%7Bg%7D_2
"\\hat{g}_2") have the smaller test RSS?  
(c) For ![\\lambda=0](https://latex.codecogs.com/png.latex?%5Clambda%3D0
"\\lambda=0"), will
![\\hat{g}\_1](https://latex.codecogs.com/png.latex?%5Chat%7Bg%7D_1
"\\hat{g}_1") or
![\\hat{g}\_2](https://latex.codecogs.com/png.latex?%5Chat%7Bg%7D_2
"\\hat{g}_2") have the smaller training and test RSS?**

As
![\\lambda\\rightarrow\\infty](https://latex.codecogs.com/png.latex?%5Clambda%5Crightarrow%5Cinfty
"\\lambda\\rightarrow\\infty"), the less constrained curve will have a
smaller training RSS as it will fit the data more closely with a higher
order polynomial. This would be
![\\hat{g}\_2](https://latex.codecogs.com/png.latex?%5Chat%7Bg%7D_2
"\\hat{g}_2") because its penalty term uses a higher order derivative.

We do not have enough information to determine with certainty which
curve would have a higher or lower test RSS. While it is likely that
![\\hat{g}\_1](https://latex.codecogs.com/png.latex?%5Chat%7Bg%7D_1
"\\hat{g}_1") would have a lower test RSS than
![\\hat{g}\_2](https://latex.codecogs.com/png.latex?%5Chat%7Bg%7D_2
"\\hat{g}_2") because the latter would overfit the data, if we have a
lot of data where the relationship between the predictors and the
response variable is very non-linear,
![\\hat{g}\_2](https://latex.codecogs.com/png.latex?%5Chat%7Bg%7D_2
"\\hat{g}_2") may provide a better fit and hence have a lower test RSS.

Where ![\\lambda=0](https://latex.codecogs.com/png.latex?%5Clambda%3D0
"\\lambda=0"), the two curves are identical because the penalty terms
are zero and hence they would have the same training and test RSS.
