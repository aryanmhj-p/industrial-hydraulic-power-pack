# Industrial Electro-Hydraulic Power Unit (HPU) Design & Sizing

[![SolidWorks](https://img.shields.io/badge/CAD-SolidWorks-red.svg)](#)
[![Fluid Power](https://img.shields.io/badge/Standard-ISO_1219-blue.svg)](#)
[![Manifold](https://img.shields.io/badge/Architecture-Rexroth_NG6_(CETOP_03)-orange.svg)](#)
[![Course](https://img.shields.io/badge/Sharif_University-Hydraulics_%26_Pneumatics-black.svg)](#)

A comprehensive mechanical and fluid power engineering project covering the catalog-based analytical sizing, Euler buckling verification, modular sandwich-plate manifold architecture, custom bellhousing development, and full 3D CAD packaging in SolidWorks for an industrial electro-hydraulic power unit.

> 📄 **Full Documentation:**  
> Detailed component selections, mathematical derivations, schematics, and complete manufacturing drawings are compiled in the engineering report:  
> 🔗 **[Read Full Engineering Report (PDF)](./docs/Hydraulic Power Pack Report.pdf)**

---

## 📌 Technical Summary & Specifications

| Parameter | Value | Engineering Verification / Source |
| :--- | :---: | :--- |
| **System Working Pressure** | **150 bar** | Peak relief set at 160 bar (Rexroth ZDB6DP) |
| **Actuator Linear Velocity** | **5.0 cm/s** | Meter-out throttling via Rexroth Z2FS6 |
| **Piston Bore / Rod Diameter** | **Ø100 / Ø45 mm** | Stroke: 1000 mm (Rexroth CD210 Series) |
| **Extension Push Force** | **117.81 kN** | Verified safe against Euler buckling |
| **Euler Buckling Safety Factor** | **S.F. = 2.11** | $P_{cr} = 249.0 \text{ kN}$ vs $F_{push} = 117.81 \text{ kN}$ |
| **Flow Demand per Actuator** | **23.56 L/min** | Casappa Polaris PLP 20-14 gear pump |
| **Electric Prime Mover** | **7.5 kW (10 HP)** | Motogen 132M4B 3-phase induction motor |
| **Reservoir Sump Capacity** | **120 Liters** | Exceeds standard sizing guidelines ($>3\times Q$) |

---

## ⚙️ Core Engineering Modules

### 1. Actuator Sizing & Column Buckling Stability
- **Hydraulic Thrust:** Designed for a continuous working pressure of 150 bar, providing $F_{push} = 117.81\text{ kN}$ extension thrust and $F_{pull} = 93.95\text{ kN}$ retraction pull.
- **Euler Critical Load Analysis:** Using pin-clevis mounting ($K = 1.0$) across maximum extended length ($L_{max} = 1294\text{ mm}$):
  $$P_{cr} = \frac{\pi^2 E I}{L^2} = \frac{\pi^2 \times (210 \times 10^9\text{ Pa}) \times (2.013 \times 10^{-7}\text{ m}^4)}{(1.294\text{ m})^2} \approx 249.0\text{ kN}$$
  The resulting safety factor of **$S.F. = 2.11$** guarantees column stability under full system pressure.

### 2. Pump, Drive Sizing & Custom Bellhousing Interface
- **Hydraulic Pump:** Selected Casappa Polaris **PLP 20-14** ($14.53\text{ cm}^3/\text{rev}$, SAE "A" 2-bolt mounting).
- **Flexible Coupling:** KTR ROTEX® 28 Type 1b jaw coupling ($T_{design} \approx 75\text{ N}\cdot\text{m}$, rated $95\text{ N}\cdot\text{m}$).
- **Custom Bellhousing Design:** Engineered a rigid adapter housing in SolidWorks to couple the **IEC 132M B5** motor flange (Ø300 mm) with the **SAE "A"** pump flange (Ø82.55 mm spigot), complete with full production drawing and machining tolerances.

### 3. Modular NG6 (CETOP 03) Manifold Stacking Architecture
To minimize external hose routing, mitigate leakage risks, and withstand industrial vibrations, discrete piping was replaced with standard vertical sandwich-plate valve stacks:
- **3-Station Actuator Subplate:** 
  1. Rexroth **4WE6J6X** (4/3 directional closed-center J-spool, 24V DC).
  2. Rexroth **Z2S6-1-6X** (Pilot-operated double check for zero-leakage load holding).
  3. Rexroth **Z2FS6-3-4X** (Dual meter-out throttle check for speed regulation).
  4. Rexroth **Z1S6P05** (Sandwich check on P-channel).
- **1-Station Safety & Unloading Subplate:**
  1. Rexroth **M-2SED6PK** (2/2 solenoid poppet valve for unloaded idle circulation).
  2. Rexroth **ZDB6DP3** (Direct-acting relief valve set at 160 bar).

### 4. Reservoir Sump Construction & DFM Guidelines
Modeled in SolidWorks ($700 \times 500 \times 550\text{ mm}$, 10 mm top plate) adhering to strict industrial maintenance practices:
- **Internal Baffle Plate with Equalization Cutouts (Rat-Holes):** Isolates turbulent/warm return fluid from the calm suction zone while preventing stagnant dead zones.
- **Foam Prevention:** Return line immersed below minimum oil level with a $45^\circ$ angled cut.
- **Sloped Floor & Debris Trapping:** Sloped bottom leading to a magnetic drain plug for settling sludge and water drainage.
- **Maintenance & Rigging:** Elevated 50 mm feet for bottom convective air cooling and four M12 DIN 580 eyebolts for crane lifting.

---

## 🛠️ Complete Bill of Materials (BOM)

Hard piping is routed with **Ø12 mm seamless precision steel tubing** with **DIN 2353 / ISO 8434-1** bite-type fittings (Parker Hannifin DMC/DEL series) and BSP Parallel (ISO 1179-2) threads. Complete itemized specs are cataloged in the engineering report.

---

## 👥 Project Information & Authors

- **Arian Mahjoubi** – Sharif University of Technology ([LinkedIn](https://www.linkedin.com/in/aryan-mahjoubi-ba66a0261) / [GitHub](https://github.com/aryanmhj-p))
- **Seyed Mohammad Mehdi Sadeghi** – Sharif University of Technology
- **Course:** Hydraulics and Pneumatics  
- **Course Instructor:** Prof. M. Durali *(Department of Mechanical Engineering, Sharif University of Technology)*
