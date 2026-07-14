# Thermodynamics of Solidification

This module covers the thermodynamic foundations of phase transformations, specifically transitioning from energy definitions to the equilibrium conditions for phase co-existence.

---

## 1. Internal Energy & First Law
The internal energy $U$ is a state function defined by the first law of thermodynamics. For a system undergoing infinitesimal equilibrium steps (assuming hydrostatic pressure work only):

$$dU = TdS - PdV$$

* **Limitations:** This form uses $S$ (entropy) and $V$ (volume) as natural variables, which are often difficult to control directly in experimental solidification setups.

---

## 2. Enthalpy and Constant Pressure Processes
To better represent experimental conditions (where pressure $P$ is typically constant), we utilize **Enthalpy ($H$)**:

$$H = U + PV$$
$$dH = TdS + VdP$$

In terms of natural variables $(T, P)$, the differential form is expressed using heat capacity at constant pressure ($C_p$):

$$dH = C_p dT + \left( \frac{\partial H}{\partial P} \right)_T dP$$

---

## 3. Gibbs Free Energy
For solidification experiments conducted at constant temperature and pressure, **Gibbs Free Energy ($G$)** is the most suitable potential:

$$G = H - TS$$
$$dG = VdP - SdT$$


---

## 4. Phase Equilibrium & Co-existence
For a closed system containing both solid ($s$) and liquid ($l$) phases, equilibrium is reached when the system's total free energy is minimized with respect to phase distribution ($\chi$):

$$\left( \frac{\partial G^m}{\partial \chi_s} \right) = G_s^m - G_l^m = 0$$

Therefore, the condition for equilibrium is:
$$G_s^m(T, P) = G_l^m(T, P)$$

---

## 5. The Clausius-Clapeyron Relation
To determine how the equilibrium temperature changes with pressure, we differentiate the equilibrium condition ($dG_s^m = dG_l^m$):

$$V_s^m dP - S_s^m dT = V_l^m dP - S_l^m dT$$

Rearranging leads to the **Clausius-Clapeyron equation**, defining the slope of the phase boundary in the $P-T$ plane:

$$\frac{dT}{dP} = \frac{V_l^m - V_s^m}{S_l^m - S_s^m}$$

* This relation is crucial for predicting phase boundaries and understanding the effect of pressure on melting points during solidification.

---

## 💡 Key Takeaways
* **State Functions:** We transition from $U \to H \to G$ to align thermodynamic variables with experimental control (moving from $S,V$ to $T,P$).
* **Equilibrium:** The chemical potentials of the solid and liquid phases must be identical at the interface.
* **Phase Stability:** The Clausius-Clapeyron equation quantifies the sensitivity of the melting point to external pressure.


### 4. Interfacial Thermodynamics & Gibbs-Thomson Effect

Beyond the bulk phase boundary defined by Clausius-Clapeyron, the local geometry of the solid-liquid interface significantly alters phase stability.

#### 4.1 The Curvature Penalty
When a solid nucleus forms within a liquid, it must overcome an energy barrier due to the surface energy ($\gamma_{sl}$) of the newly formed interface. For a curved interface with mean curvature $\bar{\kappa}$, the equilibrium condition is modified:

$$G_s^m + 2V_s^m \bar{\kappa} \gamma_{sl} = G_l^m$$



#### 4.2 The Gibbs-Thomson Equation
This curvature-induced pressure leads to the Gibbs-Thomson relation, which dictates the melting point depression for small particles or high-curvature growth fronts:

$$\Delta T_r = \frac{2\gamma_{sl} T_m}{L \cdot r}$$

* **$\Delta T_r$**: The depression in melting temperature due to curvature.
* **$r$**: The radius of curvature of the interface.
* **$L$**: Latent heat of fusion per unit volume.



---

### 5. Summary: Thermodynamic Driving Forces
Solidification is the result of competing energy factors:
1. **Bulk Free Energy ($\Delta G_v$):** The primary driver (proportional to undercooling $\Delta T$).
2. **Surface Energy ($\gamma_{sl}$):** The resistance to forming new interfaces (curvature penalty).

These two factors define the **critical nucleus size ($r^*$)** required for a solid to become stable:

$$r^* = \frac{2\gamma_{sl}}{\Delta G_v}$$

Anything smaller than $r^*$ will melt back into the liquid; anything larger will grow.
