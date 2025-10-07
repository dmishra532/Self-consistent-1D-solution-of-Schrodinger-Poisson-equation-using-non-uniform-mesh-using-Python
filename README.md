# Self-consistent-1D-solution-of-Schrodinger-Poisson-equation-using-non-uniform-mesh-using-Python
Self consistent 1D solution of Schrodinger-Poisson equation using non-uniform mesh 
The Self-Consistent 1D Solution of Schrödinger-Poisson Equation using Non-Uniform Mesh is a computational physics/semiconductor device modeling project. Let me explain what this involves:
What is the Schrödinger-Poisson System?
This is a coupled system of equations used to model quantum mechanical behavior in semiconductor devices (like transistors, quantum wells, and nanostructures).
The Two Equations:

Schrödinger Equation (Quantum Mechanics):

   -ℏ²/2m* · d²ψ/dx² + V(x)ψ = Eψ

Describes electron wavefunctions and energy levels
ψ = wavefunction, E = energy eigenvalues
V(x) = potential energy profile


Poisson Equation (Electrostatics):

   d²V/dx² = -ρ(x)/ε

Describes electric potential distribution
ρ(x) = charge density
ε = permittivity

Why "Self-Consistent"?

<img width="412" height="157" alt="image" src="https://github.com/user-attachments/assets/87de428c-cd34-4974-be18-a28124234da0" />

The two equations are coupled and must be solved iteratively:

Why Non-Uniform Mesh?
Problem with Uniform Mesh:

Equal spacing everywhere wastes computational resources
Some regions need fine resolution (quantum wells, interfaces)
Other regions need coarse resolution (bulk regions)

Non-Uniform Mesh Advantages:

Fine mesh where potential/wavefunction changes rapidly
Coarse mesh in slowly varying regions
Better accuracy with fewer grid points
Reduced computational cost

<img width="747" height="244" alt="image" src="https://github.com/user-attachments/assets/3b5d75f5-c2c6-4bbe-8e3c-e68a4913657c" />

Numerical Solution Method
Finite Difference Method:
The second derivative is approximated as:
d²ψ/dx² ≈ (ψᵢ₊₁ - 2ψᵢ + ψᵢ₋₁)/hᵢ²
For non-uniform mesh, the spacing hᵢ varies with position.
