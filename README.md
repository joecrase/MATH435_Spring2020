[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/joecrase/MATH435_Spring2020/master)

# Purpose
The purpose of this repo is to catalog the changes I have needed to make to the lecture notes.  
The professor uses the Julia v0.6.0 Kernal. The current Kernal at the time of writing this, and  
the one that I will be updating it to is Julia v1.3.1. There will be a running list of known changes  
such as deprications or alterations to functions and the equivalent. If known are found it will be  
noted. If a file is fully fixed, it will have the _Fixed_ suffix.

## How to use
In order to properly view the files, there are a few software requirments.
1) Version 1.3.1 of Julia
2) Jupyter
3) Add IJulia to your 1.3.1 installation of Julia, and ensure the Jupyter program can see that as 
	as a kernal

## The Process
I go through the old version of the lecture notes, and open them in v1.3.1. I then go through instruction by instruction and test if they still work. If a problem occurs, I research what changes need to be made to get it working the way it originally was. I also have v0.6 of Julia to run the old commands as well. 

### Current Progress (in lecture order)
- [ ] Section 1.1 : Mathematical Preliminaries and Error Analysis
- [x] Section 1.2 : Roundoff Errors
- [x] Section 2.0 : Solving Nonlinear Equations
- [x] Section 2.1 : Bisection Method
- [x] Section 2.2 : Fixed Point Iteration
- [x] Section 2.3 : Newton's Method and Its Extensions
- [x] Section 2.6 : Zeros of Polynomials and Horner's Method
- [ ] Section 3.0 : Interpolation and Polynomail Approximation
- [ ] Section 3.1 : Lagrange Interpolation
- [ ] Section 3.3 : Divided Differences and Newton's Form
- [ ] Section 3.4 : Hermite Interpolation
- [ ] Section 8.0 : The Case for Piecewise Polynomial Interpolation
- [ ] Section 8.1 : The Discrete Least Squares Approximation
- [ ] Section 8.2 : Orthogonal Polynomials and (Continuous) Least Squares Approximation
- [ ] Section 8.3 : Chebyshev Polynomials and Economization of Power Series
- [ ] Section 4.3 : Elements of Numerical Integration
- [ ] Section 4.4 : Composite Numerical Integration
- [ ] Section 4.7 : Gaussian Quadrature


## List of Updates to old (non-working) functions
### Old function -> Updated function
- realmin() -> floatmin()
- realmax() -> floatmax()
- bits() -> bitstring()
- sqrt(i) -> sqrt(Complex(i))
- linespace(a, b, c) -> range(a, stop=b, length=c)
- abs(x) where x is an array -> broadcast(abs, x)
- e -> MathConstants.e
- printf -> Requires a using Printf statement


## List of broken functions (no fixes)
- ?Roots shows no documentation, despite the rest of the library functioning
- ?ODE shows no documentation, despite the rest of the library functioning  

## Slightly different behaivors
- Overall, the results from custom function will show more decimal numbers then previously by default
