# Solidification Theory: Interface Dynamics & Mass Balance

This document outlines the fundamental governing equations for the solidification of alloys, specifically the movement of the solid-liquid interface ($\Gamma(t)$) and the redistribution of solute atoms.

---

## 1. The Stefan Boundary Condition (Energy Balance)

The Stefan condition determines the velocity ($v$) of the moving solid-liquid interface. It is derived from the requirement that the latent heat released during the phase transformation must be balanced by the thermal flux conducted away from the interface.

### Step-by-Step Derivation

1.  **Define a Control Volume:** Consider an interface element at position $x = s(t)$. In a small time interval $\Delta t$, the interface advances by $\Delta x = v \Delta t$.
2.  **Heat Release:** As the interface advances, a volume $dV = A \cdot \Delta x$ transforms from liquid to solid. If $L$ is the latent heat per unit volume, the total heat released is $Q = L \cdot A \cdot \Delta x$.
3.  **Thermal Flux:** By Fourier’s Law, the heat conducted through the phases is $q = -k \nabla T$. The net heat flux conducted away from the interface is:
    $$q_{net} = [k_s (\nabla T_s) - k_l (\nabla T_l)] A \Delta t$$
4.  **Conservation Law:** Equating the heat released to the net heat conducted:
    $$L \cdot A \cdot (v \Delta t) = [k_s \nabla T_s - k_l \nabla T_l] A \Delta t$$
5.  **Final Stefan Condition:** Simplifying for the interface velocity $v$:
    $$v \cdot L = k_s \left( \frac{\partial T_s}{\partial n} \right) - k_l \left( \frac{\partial T_l}{\partial n} \right)$$



---

## 2. Mass Balance Equations (Solute Partitioning)

In alloy solidification, solute atoms are partitioned between the solid and liquid phases. This is governed by the equilibrium partition coefficient $k$:

### Partition Coefficient

The distribution of solute atoms between the solid and liquid phases is governed by the partition coefficient $k$:
### Partition Coefficient

The distribution of solute atoms between the solid and liquid phases is governed by the partition coefficient $k$:

$$k = \frac{C_s}{C_l}$$

Where:
* $C_s$ is the solute concentration in the solid at the interface.
* $C_l$ is the solute concentration in the liquid at the interface.





### Step-by-Step Derivation

1. **Solute Flux Balance:** As the solid advances at velocity $v$, it must conserve mass at the interface.
2. **Mass Flux into/out of the Interface:**
    * Flux entering the solid: $v \cdot C_s^*$
    * Flux arriving from the liquid: $v \cdot C_l^*$
3. **Diffusion Contribution:** The excess solute rejected at the interface creates a concentration gradient. This must be balanced by diffusion into the liquid (Fick's First Law):
    $$J = D_l \left( \frac{\partial C_l}{\partial x} \right)$$
4. **Conservation Equation:** The net accumulation must equal the diffusion flux:
    $$v(C_l^* - C_s^*) = D_l \left( \frac{\partial C_l}{\partial x} \right)$$


### Final Mass Balance

By substituting the partition coefficient relationship $C_s^* = k C_l^*$, we arrive at the standard form for the solute boundary layer:

$$v C_l^* (1 - k) = D_l \left( \frac{\partial C_l}{\partial x} \right)$$

---

## 3. Summary of Governing Equations

For a complete solidification model, these equations are coupled through the interface velocity $v$.

| Physical Principle | Equation |
| :--- | :--- |
| **Diffusion** | $\frac{\partial C}{\partial t} = D \nabla^2 C + v \frac{\partial C}{\partial x}$ |
| **Stefan Condition** | $v = \frac{1}{L} (k_s \nabla T_s - k_l \nabla T_l)$ |
| **Mass Balance** | $v C_l^* (1 - k) = D_l \nabla C_l$ |

### Physical Implications
* **Constitutional Supercooling:** Occurs when the liquid ahead of the interface is at a temperature lower than its equilibrium freezing point, leading to interface instability and dendritic growth.
* **Coupled Growth:** The velocity $v$ is determined by the balance of thermal and mass transport. As cooling rate increases, $v$ increases, significantly refining the microstructural length scale.

---

### Numerical Implementation Notes
* **Stability Criterion:** If using finite difference schemes, ensure the time step $\Delta t$ satisfies: 
    $$\Delta t < \frac{(\Delta x)^2}{2D}$$
* **Non-Dimensionalization:** Define the Peclet number $Pe = \frac{v \cdot \lambda}{2D}$ to simplify the boundary layers during calculation.
