# Solidification Science: From Thermodynamics to Interface Dynamics

This repository documents the foundational principles of solidification, a multi-scale process where a liquid melt transforms into a solid crystalline structure.

---

## 1. Thermodynamic Foundation
Solidification is driven by the minimization of the system's Gibbs free energy.
* **Driving Force:** The transformation from liquid to solid occurs because the chemical potential of the solid phase ($\mu_s$) is lower than that of the liquid phase ($\mu_l$) below the equilibrium melting temperature ($T_m$).
* **Undercooling ($\Delta T$):** The difference $\Delta T = T_m - T$ provides the thermodynamic driving force for the phase change.



---

## 2. Nucleation Theory
Before macroscopic solidification can begin, stable solid nuclei must form within the liquid.

* **Homogeneous Nucleation:** Occurs spontaneously within the bulk liquid due to random thermal fluctuations. The energy barrier for forming a stable nucleus of radius $r$ is:
  $$\Delta G = -\frac{4}{3}\pi r^3 \Delta G_v + 4\pi r^2 \gamma$$
  where $\Delta G_v$ is the volume energy density and $\gamma$ is the interfacial energy.
* **Heterogeneous Nucleation:** In reality, nucleation occurs on surfaces (container walls, impurities) because they reduce the effective interfacial energy required for nucleus formation.



---

## 3. Interface Dynamics & Mass Balance

Once stable nuclei form, they grow into the liquid. The movement of this boundary is governed by heat and solute transport.

### 3.1 The Stefan Boundary Condition (Energy)
The movement of the solid-liquid interface $\Gamma(t)$ is controlled by the dissipation of latent heat ($L$). The interface velocity ($v$) is proportional to the heat flux gradient:
$$v \cdot L = k_s \left( \frac{\partial T_s}{\partial n} \right) - k_l \left( \frac{\partial T_l}{\partial n} \right)$$

### 3.2 Mass Balance (Solute Partitioning)
As the solid grows, solute atoms are partitioned. The equilibrium partition coefficient is $k = C_s^* / C_l^*$. The conservation of mass at the interface is:
$$v C_l^* (1 - k) = D_l \left( \frac{\partial C_l}{\partial x} \right)$$



---

## 4. Stability Analysis: Constitutional Supercooling
If the actual temperature gradient in the liquid is less than the equilibrium freezing point gradient caused by solute pile-up, the liquid ahead of the interface becomes "supercooled." 
* This leads to **interface instability**, causing a planar interface to transition into **cellular** or **dendritic** morphologies.

---

## 📚 Repository Roadmap
- `thermodynamics/`: Basic free energy calculations.
- `nucleation/`: Models for critical nucleus size and activation energy.
- `transport/`: Solvers for the diffusion and Stefan boundary equations.
- `dendritic_growth/`: Simulations of unstable interface growth.

---

*This repository provides the theoretical framework necessary for understanding phase transformations in materials engineering.*
