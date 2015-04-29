# pyminuit3

An experiment to re-implement MINUIT in Python.

## What is MINUIT?

MINUIT is the package most physicists use to fit their models to data.

There's a FORTRAN version from ~ 1975 and a C++ re-implementation from ~ 2005: 
http://en.wikipedia.org/wiki/MINUIT

These days, everyone uses the C++ version that is distributed with ROOT
(and receives minor updates) or the standalone C++ version that was
released in ~ 2005.

## Existing MINUIT Python wrappers

There's currently three Python wrappers for C++ MINUIT: pyminuit, pyminuit2 and iminuit.

The pyminuit and pyminuit2 project docs recommend the use of iminuit,
so it's not that bad, there is one recommended package to use MINUIT from Python.

## What and why of pyminuit3? 

- Avoid the C++ MINUIT dependency. Only use Python and Numpy.
- Implement (optionally) parallel function evaluation to allow
  use of multi-core and multi-CPU (using the API of emcee?)
- Replace the 1000s of lines of C++ by a few 100s of lines of
  easy to understand Python, i.e. have an implementation of MINUIT
  that someone can understand (and maybe modify for their application)
  more easily.
- We would like to have a liberal license, like MIT or BSD-3, so that this
  can be included in the future in packages like scipy.optimize.
  But it's not possible, because there's no high-level description of what MINUIT
  actually does, so to re-implement it one needs to read the code which is LGPL.
  The 1975 MINUIT paper contains the core method description (update formula,
  stopping criterion), but many little details that make MINUIT (and MIGRAD specifically)
  robust and better than e.g. the plain BFGS implementation in scipy.optimize
  like checks to stay numerically stable or the line search are not described.

## Status

Not started.

