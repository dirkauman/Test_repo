---
title: 'QmmmScript: A complete tutorial and adaptable, semi-automated workflow for running hybrid quantum mechanics/molecular mechanics simulations of protein systems with charmm and turbomole'
tags:
  - python
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
date: 15 March 2020
bibliography: paper.bib
---

# Summary

Constructing accurate physical models of biomolecular systems often presents a challenge, since many of the important properties of biomolecules arise from the coupling of physical processes across multiple scales of time and space. Choosing a level of theory to apply to a physical system comes down to balancing a trade-off between accuracy and computational cost, and for so-called "multiscale systems", any one level of physical theory alone is either insufficiently accurate or computationally infeasable for treating the phenomena at other relevant scales. Multiscale computational modeling, where mutiple levels of physical theory are applied and integrated, is becoming an increasingly valuable and popular means of investigating the physical and catalytic properties of complex chemical systems, particuarly proteins and protein complexes.

For molecular modeling, the most common theoretical division separates quantum mechanical models, which use wavefunction methods and include information about electrons, and molecular mechanics (aka molecular dynamics) models, which approximate bonded and non-bonded interactions as a linear combination of classical potentials. Most simulation software suites developed to date accordingly focus on one of the two catagories, with programs like Charmm, Amber, and Gromacs representing molecular dynamics and programs like Turbomole, Gaussian, and MOPAC representing quantum chemistry. In the absence of a standard environment for multiscale modeling across the qm-mm divide, the primary strategy for academic groups running qmmm simulations has been to create custom software that cycles between calling a dedicated mm program and a dedicated qm program, iteratively taking the output coordinates of one program and converting it to input for the other. However, these custom scripts are rarely distributed to the public, and much less so alongside a tutorial and a minimal working example. This presents a significant obstacle to the more widespread adoption of the technique.

QmmmScript represents one such "in-house" solution for enabling qmmm calculations, using charmm for the MM calculations and turbomole for the QM calculations (both popular choices of chemical modeling software in their respective domains). Beyond the core python3 program `shuttle.py` that shuttles coordinate data between charmm and turbomole, QmmmScript includes python and tcl scripts for automatically generating the necessary charmm input and qm-mm boundary/link atom definitions as a stream file, as well as series of template charmm scripts for executing each stage of a typically simulation pipeline. The user need only modify the initial tcl script to define the quantum atoms for their system (using VMD's selection language), and potentially the parameter sections of the geometry optimization and production run scripts if non-default settings are desired (different timestep, convergence criteria, temperature, etc).

Included is a detailed tutorial with line-by-line instructions of how to go from an intial pdb structure to a final qmmm trajectory, with two fully worked-out examples. The first, the "minimal working example", models the side chain of a single buried cystein residue in CipA, a small soluble protein. The second, a "real-world example" from ongoing research in our group, treats several protein residues and water molecules at the quantum level to model the protein transfer reaction of the membrane-bound Nqo13 subunit of T. thermophilus complex I.

We intend QmmmScript to be an educational resource and a practical scientific tool for both new students and existing researchers.

# Acknowledgements

We acknowledge contributions from Person A, Person B, and Person C (perhaps Christopher Rowley’s group?)

# References
