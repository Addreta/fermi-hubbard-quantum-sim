# 1D Fermi-Hubbard Quantum Simulation

Classical simulation pipeline for the 1D Fermi-Hubbard model
using QuSpin, OpenFermion, and Qiskit.

## Central Finding

- Trotter error grows with U/t (monotonically for 2nd order, more slowly and non-monotonically for 1st order), while the commutator norm ‖[H_hop, H_int]‖ ∝ U/t, which sets the leading 1st-order error bound, grows linearly. 
- The 2nd-order (Strang) decomposition reduces accumulated error by roughly an order of magnitude or more for U/t ≲ 2, with the advantage shrinking to ~1.5–2× for U/t ≥ 8 (L=4, dt=0.1). - The large-U/t regime, where the correlation dynamics show fast charge oscillations and slow spin dynamics, is expected to be where simulation cost is highest.

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
