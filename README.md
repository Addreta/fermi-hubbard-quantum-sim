# 1D Fermi-Hubbard Quantum Simulation

Classical simulation pipeline for the 1D Fermi-Hubbard model
using QuSpin, OpenFermion, and Qiskit.

## Central Finding

Trotter error grows monotonically with U/t, driven by the linearly increasing commutator norm ‖[H_hop, H_int]‖ ∝ U/t, which controls the per-step error bound. The 2nd-order (Strang) decomposition consistently reduces accumulated error by ~1 order of magnitude. The large-U/t regime, where spin-charge separation is manifest in the correlation dynamics, coincides with the parameter space where simulation cost is highest.

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
