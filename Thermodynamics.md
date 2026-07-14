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
