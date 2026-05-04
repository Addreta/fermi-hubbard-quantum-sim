# 1D Fermi-Hubbard Quantum Simulation

Classical simulation pipeline for the 1D Fermi-Hubbard model
using QuSpin, OpenFermion, and Qiskit.

## Central Finding
Trotter error grows with U/t, bounded above by the commutator norm ||[H_hop, H_int]|| and the onset of spin-charge
separation, providing a physical criterion for when Trotterization fails.

## Pipeline
QuSpin (exact) → OpenFermion (JW mapping) → Qiskit + SciPy (Trotter simulation)

## Requirements
pip install quspin openfermion qiskit qiskit-aer qiskit-nature qiskit-algorithms

## Reference

Motivated by Chowdhury et al. (IBM quantum hardware, Fermi-Hubbard simulation) 
and the Google Willow demonstration of 2D Fermi-Hubbard dynamics beyond exact 
classical simulation (Faisal Alam et al., 2025).
