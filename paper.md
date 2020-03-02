---
title: 'QmmmScript: A complete tutorial and adaptable, semi-automated workflow for running hybrid quantum mechanics/molecular mechanics simulations of protein systems with charmm and turbomole'
tags:
  - Python
  - charmm
  - turbomole
  - qmmm
  - molecular simulation
authors:
  - name: Dirk B. Auman
    orcid: 0000-0001-8764-958X
    affiliation: "1" # (Multiple affiliations must be quoted)
affiliations:
 - name: Ville Kaila, Professor and Chair of Biochemistry, Stockholm University
   index: 1
date: 20 March 2020
bibliography: paper.bib

# Summary

The forces on stars, galaxies, and dark matter under external gravitational
fields lead to the dynamical evolution of structures in the universe. The orbits
of these bodies are therefore key to understanding the formation, history, and
future state of galaxies. The field of "galactic dynamics," which aims to model
the gravitating components of galaxies to study their structure and evolution,
is now well-established, commonly taught, and frequently used in astronomy.
Aside from toy problems and demonstrations, the majority of problems require
efficient numerical tools, many of which require the same base code (e.g., for
performing numerical orbit integration).

`Gala` is an Astropy-affiliated Python package for galactic dynamics. Python
enables wrapping low-level languages (e.g., C) for speed without losing
flexibility or ease-of-use in the user-interface. The API for `Gala` was
designed to provide a class-based and user-friendly interface to fast (C or
Cython-optimized) implementations of common operations such as gravitational
potential and force evaluation, orbit integration, dynamical transformations,
and chaos indicators for nonlinear dynamics. `Gala` also relies heavily on and
interfaces well with the implementations of physical units and astronomical
coordinate systems in the `Astropy` package [@astropy] (`astropy.units` and
`astropy.coordinates`).

`Gala` was designed to be used by both astronomical researchers and by
students in courses on gravitational dynamics or astronomy. It has already been
used in a number of scientific publications [@Pearson:2017] and has also been
used in graduate courses on Galactic dynamics to, e.g., provide interactive
visualizations of textbook material [@Binney:2008]. The combination of speed,
design, and support for Astropy functionality in `Gala` will enable exciting
scientific explorations of forthcoming data releases from the *Gaia* mission
[@gaia] by students and experts alike.

# Citations

# Figures

I might include a snapshot of each active site from the two examples
<!--
!Figures can be included like this:
![Caption for example figure.\label{fig:example}](figure.png)
!and referenced from text using \autoref{fig:example}.

!Fenced code blocks are rendered with syntax highlighting:
!```python
!for n in range(10):
!    yield f(n)
!```	
-->	

# Acknowledgements

We acknowledge contributions from Person A, Person B, and Person C (perhaps Christopher Rowley’s group?)

# References
