
Python tools for calculating the spectral heat current from the data produced by non-equilibrium molecular dynamics simulation using LAMMPS (http://lammps.sandia.gov) software.

SHCPostProc.py: Class for performing the post-processing
calcFC.py: Class for calculating the force constants (note that the definition of the "left" and "right" interfaces must be the same in the NEMD simulation and in the calculation of the force constants)
calcSHC.py: Script demonstrating how the post-processing class is used and how the data could be saved to file
example/: Self-contained example for calculating the spectral heat current flowing across a slab of amorphous Si. The script to be run is called "silicon_example.py", and it (i) prepares the box of atoms, (ii) calls LAMMPS to perform the quenching procedure contained in LAMMPS input file "quench_Si.lmp", (iii) calls LAMMPS to perform the actual NEMD calculation for a-Si (amorphous_interface.lmp.), and (iv) performs the post-processing using the tools calcSHC.py and calcFC.py.

Note that calling LAMMPS from Python requires that you have compiled LAMMPS as a dynamically shared library (liblammps.so), which must be found in the library path ($LD_LIBRARY_PATH). Calling LAMMPS from Python is described in detail in the LAMMPS manual: http://lammps.sandia.gov/doc/Section_python.html.

TO-DO LIST:
- Documentation for calcSHC.py
- Documentation for the example
- Preparation of visualization files