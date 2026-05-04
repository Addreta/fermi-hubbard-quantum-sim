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

## References

Motivated by:

- Chowdhury et al., *Applied Physics Reviews* (2026), DOI: 10.1063/5.0306069  
  Quantum simulation of the 1D Fermi-Hubbard model on IBM superconducting hardware, 
  1st and 2nd order Trotterization with constant circuit depth, Néel observable dynamics.

- Alam et al., arXiv:2510.26845 (2025)  
  Programmable digital quantum simulation of 2D Fermi-Hubbard dynamics using 72 superconducting qubits (Google Willow), 
  magnetic polarons, stripe order, and thermalisation beyond exact classical simulation.
