# 1D Fermi-Hubbard Quantum Simulation

Classical simulation pipeline for the 1D Fermi-Hubbard model
using QuSpin, OpenFermion, and Qiskit.

## Central Finding
Trotter error grows with U/t in direct correspondence with the
commutator norm ||[H_hop, H_int]|| and the onset of spin-charge
separation — providing a physical criterion for when Trotterization fails.

## Pipeline
QuSpin (exact) → OpenFermion (JW mapping) → Qiskit (VQE + Trotter)

## Requirements
pip install quspin openfermion qiskit qiskit-aer qiskit-nature qiskit-algorithms

## Reference
Motivated by Chowdhury et al., Applied Physics Reviews (2026)
