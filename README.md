# AP1000 Thermal-Hydraulic and Thermo-Mechanical Analysis

![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Nuclear Engineering](https://img.shields.io/badge/Field-Nuclear%20Fission%20Plants-blue)
![MATLAB](https://img.shields.io/badge/Tool-MATLAB%20%26%20XSteam-orange)
![AP1000](https://img.shields.io/badge/Reactor-AP1000-red)
![ASME](https://img.shields.io/badge/Standard-ASME%20BPVC%20Sec%20III-purple)
![Collaboration](https://img.shields.io/badge/Team-3%20Members-green)

## 📖 Overview

This comprehensive study presents the complete thermal-hydraulic and thermo-mechanical analysis of the **AP1000 Pressurized Water Reactor** core, covering three interconnected aspects of nuclear fuel performance and reactor safety:

1. **Passive Decay Heat Removal System (PDHRS)** – Design and verification of a natural circulation loop for post-shutdown heat removal, based on buoyancy-driven flow and saturation conditions.

2. **Hot Subchannel Analysis** – Steady-state thermal-hydraulic evaluation of the most limiting subchannel under nominal Beginning of Life (BOL) conditions, including coolant enthalpy, cladding temperature, boiling regimes, void fraction, CHF, and DNBR.

3. **Thermo-Mechanical Fuel Pin Verification** – Structural assessment of the cladding according to ASME BPVC Section III, including mechanical and thermal stresses, buckling verification, and gas plenum sizing at end-of-life conditions.

The work follows a progressive analytical sequence from global system design to local subchannel performance and finally to material-level structural integrity, providing a complete picture of the thermal-mechanical behavior of an AP1000 fuel assembly.

> **🔬 Key Contribution:** This study demonstrates the robustness of the AP1000 design under both nominal and end-of-life conditions, showing that all relevant thermal limits (MDNBR = 1.967 > 1.85) and structural limits (Tresca stress < 3Sₘ) are satisfied with comfortable margins.

## 🔬 Key Features

### Assignment 1: Passive Decay Heat Removal System
- **Natural Circulation Loop:** Buoyancy-driven flow from density gradients between hot and cold legs.
- **Hydraulic Modeling:** Darcy-Weisbach friction losses, localized losses (k_cooler = 20, k_heater = 40).
- **Parametric Study:** Loop height as function of pipe diameter (NPS 4" to 12").
- **Roughness Effects:** Comparison between smooth (ε = 0) and rough (ε = 5.0×10⁻⁵ m) pipes.
- **Design Optimization:** Identification of optimal pipe diameter for practical loop height (NPS 12" → h = 8.21 m).

### Assignment 2: Hot Subchannel Analysis
- **Axial Power Profile:** Chopped cosine distribution with extrapolated height.
- **Boiling Regime Transition:** ONB detection (z_ONB = -0.184 m) and bubble detachment (z_D = 0.937 m).
- **Two-Phase Modeling:** Flow quality, void fraction (Zuber-Findlay & Fauske slip-ratio), heat partitioning.
- **CHF & DNBR:** W-3 correlation, spacer grid correction, Tong/Lin non-uniform heat flux correction.
- **Thermal Limits:** MDNBR = 1.967, T_fcl,max = 2094.11°C < 2804.44°C (melting point).

### Assignment 3: Thermo-Mechanical Verification
- **Buckling Analysis:** Critical external pressure (p_cr = 45.97 MPa > p_coolant = 15.5 MPa).
- **Stress Evaluation:** Primary (mechanical) and secondary (thermal) stresses via Lame's equations.
- **ASME Compliance:** Tresca equivalent stress verification (σ'_a = 127.65 MPa < 3Sₘ).
- **Gas Plenum Sizing:** End-of-life fission gas (Xe/Kr) and impurities (N₂, H₂O) volume calculation.
- **Ideal Gas Validation:** Supercritical H₂O state confirms ideal gas assumption validity.

## 📊 Key Results

| Parameter | Value | Significance |
| :--- | :--- | :--- |
| **PDHRS Loop Height (Smooth)** | `16.91 m` | Baseline design with NPS 10" pipe |
| **PDHRS Loop Height (Rough)** | `17.20 m` | Surface roughness increases requirements |
| **Optimal NPS (h < 10 m)** | `12"` | h = 8.21 m, most practical design |
| **ONB Location** | `z = -0.184 m` | Subcooled nucleate boiling starts |
| **Bubble Detachment** | `z = 0.937 m` | Vapour entrained in bulk flow |
| **Flow Quality (Outlet)** | `x_max = 0.03015` | Actual vapour mass fraction |
| **Void Fraction (Z-F)** | `α_max = 0.13377` | Drift-flux model prediction |
| **Fuel Centerline Temp** | `2094.11°C` | Below UO₂ melting point (2804.44°C) |
| **Minimum DNBR** | `1.967` | > 1.85 (nominal) & 1.30 (overpower) |
| **Critical Buckling Pressure** | `45.97 MPa` | > 15.5 MPa (coolant pressure) |
| **Tresca Equivalent Stress** | `127.65 MPa` | < 3Sₘ (ASME limit) |
| **Gas Plenum Height** | `39.65 cm` | Accommodates end-of-life fission gases |

> **⚠️ Key Insight:** The AP1000 design demonstrates significant safety margins across all analyzed parameters. The passive decay heat removal system is viable with appropriate pipe sizing. The hot subchannel maintains DNBR above regulatory limits, and the fuel cladding satisfies ASME structural requirements even at end-of-life conditions.

## 🛠️ Technologies & Tools

- **Computational Environment:** MATLAB (custom scripts with iterative solvers).
- **Thermodynamic Properties:** XSteam library for water/steam properties (IAPWS-IF97 formulation).
- **Thermal-Hydraulic Models:**
  - Darcy-Weisbach friction factor (Haaland correlation).
  - Jens-Lottes nucleate boiling correlation.
  - Griffith bubble detachment criterion.
  - Bowring/Rouhani heat partitioning models.
  - Zuber-Findlay drift-flux and Fauske slip-ratio void models.
  - W-3 critical heat flux correlation.
  - Tong/Lin non-uniform heat flux correction.
- **Structural Mechanics:**
  - Lame's equations for thick cylinders.
  - Thermoelastic stress analysis (logarithmic temperature profile).
  - ASME BPVC Section III stress limits (primary & secondary).
  - Euler buckling for thin cylindrical shells.
- **Geometry:** AP1000 fuel assembly (17×17 lattice, 264 rods/assembly, 157 assemblies).

### Assignment 1: Passive Decay Heat Removal System
[Full Report - Part 1](https://raw.githubusercontent.com/mattearmando-ing/AP1000-Thermal-Hydraulic_Thermo-Mechanical-Analysis/main/Assignment_1_Passive_Decay_Heat_Removal.pdf)

### Assignment 2: Hot Subchannel Analysis
[Full Report - Part 2](https://raw.githubusercontent.com/mattearmando-ing/AP1000-Thermal-Hydraulic_Thermo-Mechanical-Analysis/main/Assignment_2_Hot_Subchannel_Analysis.pdf)

### Assignment 3: Thermo-Mechanical Verification
[Full Report - Part 3](https://raw.githubusercontent.com/mattearmando-ing/AP1000-Thermal-Hydraulic_Thermo-Mechanical-Analysis/main/Assignment_3_Thermo_Mechanical_Verification.pdf)

---

## 📚 Assignments Breakdown

### Assignment 1: Passive Decay Heat Removal System
- Natural circulation loop design (Q = 34.8 MWₜₕ).
- Buoyancy vs. friction balance: (ρₗ - ρᵥ)gh = Σ losses.
- Parametric analysis: NPS 4" (h = 653 m) to NPS 12" (h = 8.21 m).
- Roughness impact: ε = 5.0×10⁻⁵ m increases h by ~1.7%.

### Assignment 2: Hot Subchannel Thermal-Hydraulics
- Chopped cosine axial power (q"_max = 1.631 MW/m²).
- Coolant enthalpy rise to saturation (x_eq,out = 0.04512).
- Cladding outer temperature: SP convection → nucleate boiling.
- Gap conductance iteration (fuel expansion & radiation).
- CHF: W-3 → spacer grid → 17×17 bundle → Tong/Lin correction.
- MDNBR = 1.967 @ z = 1.037 m.

### Assignment 3: Thermo-Mechanical Verification
- Zircaloy-4 properties at T_cl,ref = 649.85 K.
- Buckling: p_cr = 45.97 MPa (margin 3× vs coolant).
- Mechanical stresses: p_i = 30.85 MPa, p_o = 15.5 MPa.
- Thermal stresses: ΔT = 59.06°C across cladding.
- Tresca: σ'_a = 127.65 MPa < 3Sₘ = 232.2 MPa.
- Gas plenum: H_final = 39.65 cm (includes 15 cm spring allowance).

---

*Project developed for the "Nuclear Fission Plants" course – Politecnico di Torino (Academic Year 2025/2026).*
*Team: Matteo Armando, Tommaso Cogozzo, Federico Pala*
