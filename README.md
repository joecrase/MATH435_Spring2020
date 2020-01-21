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

### Current Progress
- [ ] section 1.1 : 
- [x] section 1.2 : Roundoff Errors
- [x] section 2.0 : Solving Nonlinear Equations

## List of Updates to old (non-working) functions
### Old function -> Updated function

- realmin() -> floatmin()
- realmax() -> floatmax()
- bits() -> bitstring()
- sqrt(i) -> sqrt(Complex(i))
- linespace(a, b, c) -> range(a, stop=b, length=c)
- abs(x) where x is an array -> broadcast(abs, x)
- e -> MathConstants.e

## List of broken functions (no fixes)
- ?Roots shows no documentation, despite the rest of the library functioning

## Slightly different behaivors
- Overall, the results from custom function will show more decimal numbers then previously by default
