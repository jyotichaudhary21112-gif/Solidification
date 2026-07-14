# Solidification Theory & Interface Dynamics

Welcome to this repository! This project serves as a technical compilation of the governing physical laws, mathematical derivations, and boundary conditions required to simulate and understand the **solidification of alloys**.

---

## 📖 Overview
Solidification is a classic "moving-boundary problem" in materials science. Whether simulating dendritic growth, planar front stability, or solute partitioning, the core of the physics relies on coupling thermal and mass transport at the solid-liquid interface.

---

## ⚙️ Core Governing Principles

### 1. The Stefan Boundary Condition (Energy Balance)
The Stefan condition dictates the velocity $v$ of the solid-liquid interface $\Gamma(t)$. It accounts for the balance between the latent heat released during the phase transformation and the thermal energy conducted away through the solid and liquid phases.



**The Derivation:**
By equating the latent heat release rate ($L \cdot v$) to the net heat flux at the interface (via Fourier’s Law), we define:
$$v \cdot L = k_s \left( \frac{\partial T_s}{\partial n} \right) - k_l \left( \frac{\partial T_l}{\partial n} \right)$$
* $L$: Latent heat of fusion.
* $k_s, k_l$: Thermal conductivities of solid and liquid.
* $\frac{\partial T}{\partial n}$: Normal temperature gradient at the interface.

---

### 2. Mass Balance & Solute Partitioning
In alloy solidification, solute atoms are redistributed between the solid and liquid phases. This is governed by the equilibrium partition coefficient $k$:

$$k = \frac{C_s^*}{C_l^*}$$



**Mass Flux Conservation:**
At the interface, the solute rejected by the advancing solid must equal the diffusion flux in the liquid (Fick's First Law):
$$v(C_l^* - C_s^*) = D_l \left( \frac{\partial C_l}{\partial x} \right)$$

By substituting $C_s^* = k C_l^*$, we obtain the fundamental mass balance equation for the solute boundary layer:
$$v C_l^* (1 - k) = D_l \left( \frac{\partial C_l}{\partial x} \right)$$

---

## 🚀 Key Topics Covered
* **Interface Dynamics:** Tracking the evolution of $\Gamma(t)$.
* **Constitutional Supercooling:** The transition from planar to dendritic growth modes.
* **Solute Boundary Layer:** Understanding how growth velocity $v$ influences solute pile-up at the front.
* **Coupled Growth:** How thermal gradients and mass diffusion work together to dictate final microstructure.

---

## 🛠 Numerical Implementation Tips
When implementing these equations in code (e.g., Finite Difference or Phase-Field methods), consider these stability parameters:
* **Stability Criterion:** Always ensure your time step $\Delta t$ satisfies the diffusion limit: $\Delta t < \frac{(\Delta x)^2}{2D}$.
* **Non-Dimensionalization:** To simplify simulations, use the Peclet number $Pe = \frac{v \cdot \lambda}{2D}$ to normalize your boundary layers.

---

## 📚 References
* *Materials Modelling using Density Functional Theory: Properties & Predictions*, F. Giustino.
* Standard texts on solidification processing and dendritic growth theory.

---

*This repository is maintained for educational purposes. Contributions and corrections regarding numerical implementations are welcome!*
