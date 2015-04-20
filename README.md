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
- MIT licensed, i.e. compatible with the scientific Python packages.
  This requires that we don't look at the MINUIT code. Hopefully the
  formulas and description from the 1975 paper is enough ...

## Status

Not started.

