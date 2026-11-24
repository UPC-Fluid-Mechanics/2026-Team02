# Theoretical design of an axial fan for tunnel ventilation (SODECA THT/IMP-LS-UNI-50-2/4T-6-F400)

## 1.- Dimensions

The reference machine is a unidirectional axial jet fan used for tunnel and car park ventilation. The nominal commercial impeller diameter is 500 mm. Theoretical design calculations use the **dimensions measured in the group's CAD assembly**, rather than replacing those dimensions with the nominal catalogue designation.

### 1.1.- Commercial assembly dimensions

The manufacturer provides the following overall dimensions for the THT/IMP-LS-50 model:

<img width="1000" alt="Dimensions Fan" src="https://github.com/user-attachments/assets/c1c9b665-8b0b-4547-bff5-b25fd3dc717a" />

*Figure 1. Dimensional drawing of the commercial SODECA fan. Source: SODECA, THT/IMP technical catalogue, page 5. **[TO VERIFY]** Confirm the drawing and model variant match the selected commercial reference.*

| Dimension | Value (mm) |
|:--|--:|
| A | 546 |
| B | 549 |
| C | 742 |
| E — Overall length | 1445 |
| L — Casing length | 1200 |
| X | 560 |
| X1 | 255 |
| Z | 778 |
| Z1 | 808 |

### 1.2.- CAD rotor dimensions and design section

The following geometrical information was provided from CAD measurements:

| Parameter | Symbol | Value |
|:--|:--:|--:|
| Rotor outer diameter | $D_t$ | 494 mm |
| Hub outer diameter at the rotor | $D_h$ | 130.5 mm |
| Diameter stated for outlet section | $D_{out}$ | 514 mm |
| Number of rotor blades | $Z$ | 6 |
| Rotor tip radius | $r_t=D_t/2$ | 247.00 mm |
| Hub radius | $r_h=D_h/2$ | 65.25 mm |
| Blade radial span | $h=r_t-r_h$ | 181.75 mm |
| Arithmetic mean radius | $r_m=(r_t+r_h)/2$ | 156.125 mm |
| Root-mean-square radius | $r_{m,RMS}=\sqrt{(r_t^2+r_h^2)/2}$ | 180.65 mm |

**Assumption 1:** The rotor and hub are represented as concentric circular sections, and local flow blockage by blade thickness is neglected when calculating the preliminary annular passage area.

$$
A=\frac{\pi}{4}(D_t^2-D_h^2)
=\frac{\pi}{4}(0.494^2-0.1305^2)
=\boxed{0.178290\;\mathrm{m^2}}.
$$

The geometric circular area associated with the stated 514 mm outlet diameter is:

$$
A_{out,geom}=\frac{\pi}{4}(0.514)^2
=\boxed{0.20750\;\mathrm{m^2}}.
$$

## 2.- Performance and operating requirements

The commercial reference is the SODECA THT/IMP-LS-UNI-50-2/4T-6-F400, an axial jet fan that supplies momentum to the surrounding air to promote longitudinal ventilation.

The performance data about the fan presented:

**| Parameter | value |**
|:--|--:|--:|
| Rotational speed (rpm) | **1445** |
| Volumetric flow rate (m³/h) | **9770** |
| Outlet air velocity (m/s) | **13.09** |
| Thrust (N) | **40.55** |

*Table 1. Previously recorded data attributed to SODECA QuickFan.

From the parameters listed above it's possible to calculate the flow rate and the pressure of the model. 

$$
Q=\frac{9770}{3600}=\boxed{2.713889\;\mathrm{m^3/s}},\qquad
N=1445\;\mathrm{rpm}.
$$

**Assumption 3:** The reference air properties are $\rho=1.20\;\mathrm{kg/m^3}$ and $\mu=1.81\times10^{-5}\;\mathrm{Pa\,s}$.

The dynamic pressure corresponding to the **nominal outlet jet velocity** is:

$$
p_{d,jet}=\frac12\rho v_{jet}^2
=\frac12(1.20)(13.1)^2
=\boxed{102.966\;\mathrm{Pa}}.
$$

**Assumption 4 (preliminary pressure model):** Only for the purpose of calculating an initial D1/D2 design point, **$\Delta p_{0,est}=p_{d,jet}=102.966\;\mathrm{Pa}$** is adopted as a provisional idealized rotor total-pressure rise. 

As a consistency check, the geometric circular outlet area gives:

$$
\frac{Q}{A_{out,geom}}
=\frac{2.713889}{0.20750}
=13.079\;\mathrm{m/s}\approx13.1\;\mathrm{m/s}.
$$

This agreement supports the **geometric area used to report nominal jet velocity**.

Figure 2 illustrates this general concept. It is included as a theoretical reference and does not represent the performance of the selected SODECA fan.

<img width="329" height="297" alt="Generic fan characteristic curves" src="https://github.com/user-attachments/assets/dff147b8-1ce6-42f5-a30b-d37b3cbed890" />

*Figure 2. Generic fan characteristic curves; these are not measured curves of the selected SODECA fan.*

## 3.- Preliminary power estimate

The estimated jet power is:

$$
P_{jet}=Q\,p_{d,jet}
=2.713889(102.966)
=\boxed{279.44\;\mathrm{W}}.
$$

**Assumption 5:** The preliminary global jet-power-to-electrical-input efficiency is $\eta_{jet,overall}=0.50$, solely for an illustrative estimate; this is **not** a measured efficiency or a value confirmed by the manufacturer.

$$
P_{electrical,est}=\frac{P_{jet}}{\eta_{jet,overall}}
=\frac{279.44}{0.50}
=\boxed{558.88\;\mathrm{W}\approx0.56\;\mathrm{kW}}.
$$

SODECA stated a low-speed installed motor rating of 1.30 kW. The estimated 0.56 kW must not be presented as a verified measured consumption.

Because provisional $\Delta p_{0,est}=p_{d,jet}$, the idealized hydraulic power $Q\Delta p_{0,est}$ is numerically also 279.44 W. This numerical equality is a consequence of **Assumption 3**, not an independently measured hydraulic performance result.

## 4.- Applications

According to the manufacturer, THT/IMP-type axial jet fans are intended to generate high-velocity jets for ventilation and, for appropriately certified variants, smoke-control applications in enclosed spaces such as car parks. This project uses the commercial SODECA fan as a reference for **tunnel longitudinal ventilation**, where the jet transfers momentum to the surrounding air and assists in pollutant dilution and air movement. The model designation used in the project contains **F400**.

Reference: [SODECA official website](https://www.sodeca.com). 

## 5.- Examples of other axial jet fans for tunnel ventilation

These products were selected by the group as commercial comparisons based principally on reported dynamic pressure. Their stated pressure values must not automatically be treated as rotor total-pressure rise.

| Manufacturer and model | Rotational speed (rpm) | Estimated dynamic pressure (Pa) | Diameter | Airflow (m³/h) |
|:--|--:|--:|--:|--:|
| Soler & Palau — TJHT/2/4-500-C | 1440 | 94 | 500 mm | 8800 |
| Zitrón — JZp 4/H-1,5/0,37-2/4 RE F400 | 2845 | 220 | 400 mm | 8700 |
| Novovent — JET WINDER 4-560T-4 0.55 kW | 1500 | 78 | 490 mm | 10087 |

References: 

Novovent: https://fnpgroup.es/

Zitrón: https://zitron.com/?lang=es

Novovent: https://www.solerpalau.com/es-es/


## 6.- Dimensionless parameters and position in the Cordier diagram

This section follows the definitions presented in the D1 notebook and in Dixon and Hall (Chapter 2). The reference length is the **measured rotor diameter $D=D_t=0.494$ m** and the operating point is **1445 rpm only**.

$$
\omega=\frac{2\pi N}{60}
=\frac{2\pi(1445)}{60}
=\boxed{151.320\;\mathrm{rad/s}}.
$$

The mean axial speed through the rotor annulus is:

$$
c_x=\frac{Q}{A}
=\frac{2.713889}{0.178290}
=\boxed{15.222\;\mathrm{m/s}}.
$$

**Assumption 6:** Steady, incompressible flow with uniform mean axial velocity across the rotor annulus; the mean axial speed is assumed unchanged between rotor inlet and outlet ($c_{x1}=c_{x2}=c_x$). This is a one-dimensional simplification, not a measured profile.

### 6.1.- Flow coefficient

$$
\phi=\frac{Q}{\omega D^3}
=\frac{2.713889}{151.320(0.494)^3}
=\boxed{0.14877}.
$$

### 6.2.- Pressure coefficient

$$
\psi=\frac{\Delta p_{0,est}}{\rho\omega^2D^2}
=\frac{102.966}{1.20(151.320)^2(0.494)^2}
=\boxed{0.01536}.
$$

### 6.3.- Hydraulic power coefficient

$$
\hat P=\frac{Q\Delta p_{0,est}}{\rho\omega^3D^5}
=\phi\psi
=\boxed{0.002284}.
$$

### 6.4.- Reynolds number

The Reynolds number here is defined using the rotor diameter and the annular mean axial speed:

$$
Re_D=\frac{\rho c_xD}{\mu}
=\frac{1.20(15.222)(0.494)}{1.81\times10^{-5}}
=\boxed{4.99\times10^5}.
$$

The Reynolds number based on the **blade chord and inlet relative speed** is calculated separately in Section 9.

### 6.5.- Specific speed and specific diameter

$$
\Omega_s=\frac{\omega\sqrt Q}{(\Delta p_{0,est}/\rho)^{3/4}}
=\boxed{8.842},
$$

$$
D_s=\frac{D(\Delta p_{0,est}/\rho)^{1/4}}{\sqrt Q}
=\boxed{0.9127}.
$$

| Dimensionless parameter | Symbol | Calculated value at 1445 rpm |
|:--|:--:|--:|
| Flow coefficient | $\phi$ | 0.14877 |
| Pressure coefficient | $\psi$ | 0.01536 |
| Hydraulic power coefficient | $\hat P$ | 0.002284 |
| Diameter-based Reynolds number | $Re_D$ | $4.99\times10^5$ |
| Specific speed | $\Omega_s$ | 8.842 |
| Specific diameter | $D_s$ | 0.9127 |

### 6.6.- Position in the Cordier diagram

Figure 3 is the **Dixon-and-Hall-style Cordier diagram**. The horizontal axis is the logarithmic specific diameter $D_s$ and the vertical axis is the logarithmic specific speed $\Omega_s$.

$$
\boxed{(D_s,\Omega_s)_{1445\,rpm}=(0.9127,\,8.842)}.
$$

<img width="1448" height="1086" alt="Gráfico de Cordier con punto destacado_edited" src="https://github.com/user-attachments/assets/0069a14b-c0cb-4f1f-90b6-b0e924f753ea" />

*Figure 3. Cordier diagram based on Dixon and Hall. The **orange low-speed marker** indicates the 1445 rpm condition in the characteristic axial-flow region.

## 7.- Geometry of the axial fan components

The commercial reference and preliminary theoretical fan have the following principal components. **The blade chord, profile and stagger are design choices, not CAD measurements of a finalized blade.**

| Component | Description / function |
|:--|:--|
| Rotor blades | Six blades impart tangential momentum to the airflow | $Z=6$; $D_t=494$ mm; preliminary mean-radius chord selected in Section 9 |
| Hub | Connects blade roots to rotating assembly | $D_h=130.5$ mm |
| Shaft / rotor coupling | Transmits torque | Attached to the hub by elastic coupling |
| Casing / duct | Contains flow and supports assembly | Existing commercial dimensions in Section 1 |
| Motor | Drives the rotor | Low-speed operation at 1445 rpm |
| Motor mounting supports | Secure motor inside the structure | Little structure under the motor attached inside the rube of the fan occupying the less space possible to not obstruct the air flow |
| Outlet | Delivers jet to surrounding air | Stated diameter 514 mm |
| Protective grille, deflector and silencers | Safety/noise/jet management where applicable | Present in commercial product description, located in the entrance of the fan |

## 8.- Materials and characteristics. Justification

Material specifications are listed below according to manufacturing facilities

| Component | Material | manufacturing justification |
|:--|:--|:--|
| Rotor blades | Aluminum | Low | Reduces rotor mass and rotational inertia. Suitable for manufacturing complex aerodynamic blade geometries by casting. |
| Hub | Aluminum  | Reduces rotating mass while providing a mechanically resistant connection to the shaft. |
| Shaft / coupling | Steel | Suitable for transmitting motor torque and resisting torsional and fatigue loads. |
| Casing | S235JR GALVA   | Economical material suitable for sheet-metal forming, welding and structural support. |
| Motor supports | S235JR GALVA | Suitable for welded or bolted supports connecting the motor assembly to the casing. |
| Protective elements (if present) | S235JR GALVA | Provides protection against contact with rotating components and foreign objects. It's easy to produce |
| Motor casing | Aluminum | Most common material for low power motors |

## 9.- Mean-line analysis and preliminary blade design

The flow model is steady and two-dimensional. The final airfoil selection and radial design will be done in Release 2.

**Assumption 7:** The inlet has no pre-swirl: $c_{\theta1}=0$. This is a boundary-condition assumption; the absence of upstream guide vanes does not by itself prove that the real inflow has zero swirl.

**Assumption 8:** The provisional rotor pressure rise follows the Euler energy-transfer equation is applied ideally, with no losses in the velocity-triangle calculation. This **does not imply a real overall fan efficiency of 100%**.

### 9.1.- Velocity triangles at the mean radius

$$
U_m=\omega r_m=151.320(0.156125)
=\boxed{23.625\;\mathrm{m/s}}.
$$

$$
c_{x1}=c_{x2}=c_x=15.222\;\mathrm{m/s},\qquad c_{\theta1}=0.
$$

For the idealized rotor:

$$
\Delta p_{0,est}=\rho U_m(c_{\theta2}-c_{\theta1}),
$$

$$
c_{\theta2}=\frac{102.966}{1.20(23.625)}
=\boxed{3.632\;\mathrm{m/s}}.
$$

The inlet and outlet relative speeds are:

$$
w_1=\sqrt{c_x^2+U_m^2}
=\boxed{28.104\;\mathrm{m/s}},
$$

$$
w_2=\sqrt{c_x^2+(U_m-c_{\theta2})^2}
=\boxed{25.128\;\mathrm{m/s}}.
$$

Using positive relative-flow angles measured from the axial direction toward the direction opposing blade motion:

$$
\beta_1=\arctan\left(\frac{U_m}{c_x}\right)
=\boxed{57.206^\circ},
$$

$$
\beta_2=\arctan\left(\frac{U_m-c_{\theta2}}{c_x}\right)
=\boxed{52.716^\circ}.
$$

$$
\beta_m=\arctan\left(\frac{\tan\beta_1+\tan\beta_2}{2}\right)
=\boxed{55.086^\circ}.
$$

| Velocity-triangle quantity | Inlet (1) | Outlet (2) |
|:--|--:|--:|
| Axial absolute velocity $c_x$ (m/s) | 15.222 | 15.222 |
| Absolute tangential velocity $c_\theta$ (m/s) | 0 | 3.632 |
| Relative velocity magnitude $w$ (m/s) | 28.104 | 25.128 |
| Relative flow angle $\beta$ (deg) | 57.206 | 52.716 |


### 9.2.- Blade count, pitch and diffusion criterion

The number of blades is fixed at $Z=6$. At the arithmetic mean radius:

$$
s=\frac{2\pi r_m}{Z}
=\frac{2\pi(0.156125)}{6}
=\boxed{0.163494\;\mathrm{m}=163.49\;\mathrm{mm}}.
$$

**Assumption 9:** For preliminary dimensioning, the allowable Lieblein diffusion factor is taken as $DF_{max}=0.45$. The D2 example also discusses values around 0.5. The selected design is checked against this conservative 0.45 limit.

$$
DF=1-\frac{w_2}{w_1}
+\frac{c_{\theta2}-c_{\theta1}}{2w_1}\frac{s}{l}.
$$

Setting $DF=DF_{max}$ and solving for the maximum pitch-to-chord ratio gives:

$$
\left(\frac{s}{l}\right)_{max}
=\frac{2w_1}{c_{\theta2}-c_{\theta1}}
\left(DF_{max}-1+\frac{w_2}{w_1}\right)
=\boxed{5.325}.
$$

$$
l_{min,DF}=\frac{s}{(s/l)_{max}}
=\frac{163.49}{5.325}
=\boxed{30.70\;\mathrm{mm}}.
$$

This lower bound prevents excessive diffusion in the simplified mean-radius model; it is **not** the final chord selection.

### 9.3.- Chord selection for the target lift coefficient

**Assumption 10:** A preliminary two-dimensional section drag coefficient $C_D=0.02$ is adopted. Its validity for the actual airfoil at the operating Reynolds number remains to be established.

**Design requirement:**  $C_L\approx0.75$ to remain below its preferred approximate upper range of 0.8–0.9.

The mean-line cascade relation from Dixon and Hall, Equation (3.26a), is:

$$
C_L=2\frac{s}{l}\cos\beta_m
(\tan\beta_1-\tan\beta_2)
-C_D\tan\beta_m.
$$

The previously considered chord of $l=47$ mm would give:

$$
\left(\frac{s}{l}\right)_{47mm}
=\frac{163.494}{47}=3.479,
\qquad \boxed{C_{L,47mm}=0.921}.
$$

Solving the lift equation for $C_{L,target}=0.75$:

$$
l=\frac{2s\cos\beta_m(\tan\beta_1-\tan\beta_2)}
{C_{L,target}+C_D\tan\beta_m}
=\boxed{57.35\;\mathrm{mm}}.
$$

A rounded **preliminary design chord $l=57.5$ mm** is adopted. This is a proposed dimension for subsequent CAD work, **not** a measured chord or a CFD-validated result.

$$
\frac{s}{l}=\frac{163.494}{57.5}=\boxed{2.843},
\qquad
\sigma=\frac{l}{s}=\boxed{0.352}.
$$

$$
\boxed{C_L=0.748},\qquad
\boxed{DF=0.290}.
$$

The corresponding blade-section Reynolds number based on the inlet relative velocity is:

$$
Re_l=\frac{\rho w_1l}{\mu}
=\frac{1.20(28.104)(0.0575)}{1.81\times10^{-5}}
=\boxed{1.07\times10^5}.
$$

| Quantity | Proposed 57.5 mm chord |
|:--|--:|
| Blade count $Z$ | 6 |
| Pitch $s$ (mm) | 163.49 |
| Chord $l$ (mm) | **57.50** |
| Pitch-to-chord $s/l$ | **2.843** |
| Solidity $l/s$ | **0.352** |
| Required $C_L$ | **0.748** |
| Diffusion factor $DF$ | **0.290** |

The rounded chord satisfies the selected mean-radius $C_L$ target and the diffusion-factor criterion within the adopted theoretical assumptions.

### 9.4.- Preliminary blade orientation and aerodynamic limitations

The calculated **flow angles** are $\beta_1=57.206^\circ$ and $\beta_2=52.716^\circ$. They are derived from the idealized velocity triangles and do **not** define a unique airfoil shape.

**Assumption 11:** It has been considered $\xi=53^\circ$ as a **preliminary chord stagger**, in analogy with the C3 cascade classroom example. The corresponding *chord-referenced* incoming angle is:

$$
\alpha_{chord}=\beta_1-\xi
=57.206^\circ-53^\circ
=\boxed{4.206^\circ}.
$$


## 11.- Computational fluid dynamics (CFD)

The CFD work presented in this release corresponds to a **preliminary two-dimensional cascade simulation** based on the methodology developed in the C3 course notebook. Its purpose at this stage is to define and test the CAD preparation, mesh strategy and boundary conditions required for the numerical analysis.

**Assumption 12 (preliminary CFD iteration):** The CFD model was generated before the rotor dimensions were updated using the measurements obtained from the group's CAD assembly. Consequently, the simulation corresponds to an earlier mean-line design iteration and must not be interpreted as a numerical validation of the current geometry defined in Section 9.

The main differences are summarised below:

| Parameter | Preliminary CFD case | Current design, Section 9 |
|:--|--:|--:|
| Mean radius $r_m$ (mm) | 187.50 | 156.125 |
| Blade pitch $s$ (mm) | 196.35 | 163.49 |
| Blade chord $l$ (mm) | 47.0 | 57.5 |
| Blade count $Z$ | 6 | 6 |
| Rotational speed $N$ (rpm) | 1445 | 1445 |

The CFD geometry and operating conditions will therefore be updated in Release 2 once the blade geometry and radial design have been established.

## 11.1 CAD description

The preliminary numerical model represents a single blade passage of the rotor at the mean radius. Periodic boundaries are used in the pitchwise direction so that only one blade section has to be simulated.

The airfoil used in this preliminary model is a **NACA 65(1)-212** profile. This profile is adopted as a numerical reference because it is the profile used in the C3 cascade exercise. It is **not assumed to be the actual SODECA blade profile or the final profile of the designed rotor**.

The geometry was obtained by modifying the original C3 airfoil model in SimScale. The original profile was first scaled to a chord of 60 mm and rotated to the $50^\circ$ stagger angle used in the classroom example. For the project simulation, an additional scale factor was applied:

$$
\frac{47}{60}=0.7833,
$$

resulting in a preliminary chord:

$$
l=\boxed{47\ \mathrm{mm}}.
$$

An additional rotation of $3^\circ$ was applied around the $z$ axis, resulting in a total preliminary stagger angle:

$$
\xi=50^\circ+3^\circ=\boxed{53^\circ}.
$$

For this iteration, the blade pitch was:

$$
s=\boxed{196.35\ \mathrm{mm}},
$$

and therefore:

$$
\frac{s}{l}=\frac{196.35}{47}
=\boxed{4.18}.
$$

The pitchwise limits of the computational domain were consequently placed at:

$$
y=\pm\frac{s}{2}
=\boxed{\pm0.098175\ \mathrm{m}}.
$$

The $x$ direction represents the axial direction of the fan and the $y$ direction represents the tangential direction of the cascade. The domain is treated as a quasi-two-dimensional blade passage following the approach of the C3 exercise.

The resulting CAD therefore represents a simplified mean-radius cascade and does not include the hub, casing, blade radial variation, tip clearance or the complete three-dimensional rotor.

<img width="1000" alt="Preliminary NACA 65(1)-212 airfoil geometry" src="images/CFD/CFD_geometry.png" />

*Figure 4. Preliminary NACA 65(1)-212 airfoil geometry used in the two-dimensional cascade model in SimScale.*

## 11.2 Mesh description

A **Hex-dominant parametric mesh** was used following the C3 numerical methodology.

The background computational domain was defined by the following limits:

| Coordinate | Minimum (m) | Maximum (m) |
|:--|--:|--:|
| $x$ | -0.300 | 0.900 |
| $y$ | -0.098175 | 0.098175 |
| $z$ | 0 | 0.060 |

The main background mesh discretisation was:

$$
\boxed{100\times10\times1}.
$$

Only one cell is used in the $z$ direction because the objective of this simulation is to approximate the flow through a two-dimensional cascade section.

A local refinement region was introduced around the airfoil and its near wake. The refinement box extends from:

$$
(-0.05,-0.098175,0)
$$

to:

$$
(0.15,0.098175,0.06)\;\mathrm{m}.
$$

A **refinement level of 2** was assigned to this region.

A boundary-layer mesh was also applied to the airfoil surface. The settings used were:

| Boundary-layer parameter | Value |
|:--|--:|
| Number of layers | 2 |
| Expansion ratio | 1.2 |
| Final layer thickness | 0.5 |
| Minimum thickness | 0.01 |

These settings follow the preliminary meshing strategy introduced in C3. The mesh is refined close to the blade and in the wake, where the largest velocity gradients are expected.

No formal grid-convergence or GCI analysis is performed in this preliminary Release 1 model. According to the project structure, the detailed mesh verification and GCI assessment will be addressed in Release 2.

<img width="1000" alt="Computational mesh with local refinement around the airfoil" src="images/CFD/mesh_refinement.png" />

*Figure 5. Computational mesh of the two-dimensional cascade domain, showing the local refinement region around the airfoil.*

## 11.3 Boundary conditions

Air was assigned as the working fluid and the flow was modelled as incompressible.

The inlet boundary condition corresponds to the velocity triangle used in the preliminary CFD iteration. The imposed relative velocity components were:

$$
\mathbf{w}_1=
(18.429,\ 28.373,\ 0)
\;\mathrm{m/s}.
$$

Therefore, the relative inlet flow angle was:

$$
\beta_1=
\tan^{-1}\left(
\frac{28.373}{18.429}
\right)
=\boxed{56.995^\circ}.
$$

Considering the preliminary stagger angle $\xi=53^\circ$, the corresponding chord-referenced incidence in this numerical case is:

$$
i_{CFD}=\beta_1-\xi
=56.995^\circ-53^\circ
=\boxed{3.995^\circ\approx4^\circ}.
$$

This incidence corresponds specifically to the **preliminary CFD case** and must not be interpreted as the definitive design incidence of the final blade profile.

The boundary conditions applied in SimScale were:

| Boundary | Type | Condition |
|:--|:--|:--|
| Minimum $x$ | Velocity inlet | $\mathbf{w}_1=(18.429,\ 28.373,\ 0)$ m/s |
| Maximum $x$ | Pressure outlet | Static pressure $p=0$ Pa |
| Minimum and maximum $y$ | Periodic | Repetition of the neighbouring blade passages |
| Airfoil surface | Wall | No-slip wall with turbulence wall function |
| Minimum and maximum $z$ | Symmetry | Quasi-two-dimensional approximation |

The periodic boundaries reproduce an infinite cascade with the specified blade pitch, while the symmetry conditions suppress the intended spanwise variation of the preliminary two-dimensional model.

A force-and-moment result control was applied to the same airfoil wall surface used in the wall boundary condition. This allows the aerodynamic forces acting on the blade section to be monitored during the calculation.

The configuration presented here documents the numerical methodology used in Release 1. Since the theoretical design was subsequently updated using the measured CAD rotor dimensions, the pitch, chord and inlet velocity components of this CFD case will be revised before using CFD results for the definitive rotor assessment.

## 12.- Experimentation: measurement of magnitudes and data acquisition (E1)

The selected test specimen is the complete commercial SODECA **THT/IMP-C-UNI-50-2/4T-6**, corresponding to the STEP model selected by the group. The proposed test will use the low-speed setting of **1,445 rpm**. The catalogue maximum airflow of **9,770 m³/h (2.714 m³/s)** is used as a reference to size the flow meter [9].
The actual airflow will be measured on the test bench.

The commercial fan is distinct from the theoretical rotor described in Design. The pressure and power estimates in Sections 2–3 are theoretical inputs. No experimental results are reported in this release.

The STEP cross-section shows an internal diameter of **514 mm** at bothends. The chamber will be connected to the motor-side inlet, as shown in Section 14.2. The mounting plate and fastening details remain to be defined.

| Quantity | Proposed measurement or calculation | Purpose |
|:--|:--|:--|
| Air volume flow rate, $Q$ (m³/s) | Calculate from the pressure difference across the calibrated nozzle bank, $\Delta p_n$, and air density. | Determine the operating point. |
| Fan static and total pressures, $p_{fs}$ and $p_f$ (Pa) | Measure chamber pressure relative to ambient on a second channel; derive the fan pressures using the configuration in Section 14 and confirmed outlet area. | Build the pressure–flow curves. |
| Rotational speed, $n$ (rpm) | Measure with an optical tachometer where there is a safe line of sight to a rotating target. | Check stability and document the test speed. |
| Air temperature $T$ (°C), barometric pressure $p_a$ (Pa) and relative humidity RH (%) | Measure at the inlet or a representative ambient location as appropriate for each variable. | Calculate air density $\rho$ and report test conditions. |
| Electrical active input power, $P_{\mathrm{el}}$ (W) | Measure at the test fan's motor supply with a three-phase power analyser; exclude the auxiliary fan's power. | Determine overall efficiency relative to the electrical input. |
| Shaft torque, $M$ (N·m), if accessible | Measure only if a suitable torque sensor can be coupled to the shaft without invalidating the test configuration. Then $P_{\mathrm{shaft}}=2\pi nM/60$. | Obtain shaft power and, if available, fan efficiency based on shaft power. |
| Air power and electrical-input efficiency | Calculate $P_{\mathrm{air}}\approx Qp_f$ and $\eta_{\mathrm{el}}=P_{\mathrm{air}}/P_{\mathrm{el}}$ at low pressure rise. | Compare performance at different flow rates. |

The design estimate of approximately 103 Pa comes from the jet velocity. It is separate from the nozzle differential pressure and cannot be treated as a measured fan pressure rise. Likewise, the installed motor rating of 1.30 kW is not the actual electrical input at a test point. A free-discharge jet thrust test, if required, would be a separate measurement under the approach described in ISO 13350 [9, 15].

### 12.1.- Flow measurement and preliminary nozzle sizing

The catalogue maximum airflow of **9,770 m³/h (2.714 m³/s)** is used as
the sizing reference for the flow meter [9].

| **Flow-measurement option** | **Fit to the proposed test** |
|:--|:--|
| ISA 1932 nozzle | Used in the course example. It remains an option for a duct-based bench if the pressure loss is acceptable. |
| Long-radius nozzle | Another option for a duct-based bench. Its throat diameter would need to be selected for the expected airflow and pressure differential. |
| Rounded-entry chamber nozzles | **Selected for the preliminary bench.** Two identical nozzles in parallel allow one to be closed at low airflow to increase the differential-pressure signal. The main drawback is the space required for the chamber. |

The choice follows the proposed chamber arrangement in Section 14.
If the chamber does not fit in the laboratory, the duct-based options
should be reconsidered [8, 16].

The flow meter uses the pressure difference across the nozzle bank,
$\Delta p_n$, to calculate airflow. For sizing, the same relation is
rearranged to estimate the pressure difference at a given airflow:

```math
A_n=N_{\mathrm{open}}\frac{\pi d_n^2}{4},
\qquad
Q\approx C_d A_n\sqrt{\frac{2\Delta p_n}{\rho}},
\qquad
\Delta p_n\approx\frac{\rho}{2}
\left(\frac{Q}{C_d A_n}\right)^2.
```

Here, $A_n$ is the total open throat area, $N_{\mathrm{open}}$ is the
number of open nozzles, $d_n$ is the throat diameter of each nozzle,
$C_d$ is the discharge coefficient and $\rho$ is the air density.
The preliminary calculation assumes $d_n=0.400\ \mathrm{m}$ and
$\rho=1.20\ \mathrm{kg/m^3}$. The coefficient $C_d=0.985$ is taken
from the course inlet-chamber example [8] as a sizing assumption.

**Worked example: two open nozzles at the catalogue reference airflow.**

```math
Q_{\mathrm{ref}}=\frac{9{,}770}{3{,}600}
=2.7139\ \mathrm{m^3/s},
\qquad
A_n=2\frac{\pi(0.400\ \mathrm{m})^2}{4}
=0.2513\ \mathrm{m^2}.
```

```math
\Delta p_n\approx
\frac{1.20}{2}\left(\frac{2.7139}{0.985\times0.2513}\right)^2
=72.1\ \mathrm{Pa}.
```

| **Reference airflow (m³/h)** | **Open nozzles** | **Estimated nozzle differential (Pa)** |
|--:|--:|--:|
| 9,770 | 2 | 72.1 |
| 4,885 | 2 | 18.0 |
| 4,885 | 1 | 72.1 |

With both nozzles open, halving the airflow reduces the estimated
differential to one quarter. At 4,885 m³/h, using only one nozzle
halves the open area and raises the estimated differential back to
72.1 Pa. Closing a nozzle changes the bench resistance, so the
operating point must be readjusted to compare both configurations at
the same airflow.

The proposed pressure sensor's basic accuracy limit of ±1.25 Pa
corresponds to a first-order effect on the calculated airflow of about
**±0.9% at 72.1 Pa** and **±3.5% at 18.0 Pa** [10]. This accounts
only for the pressure reading; the wider uncertainty assessment is
presented in Section 13.

### 12.2.- Selection of digital differential-pressure instruments

Two **WIKA A2G-500** differential-pressure transmitters with digital
display and Modbus RTU output are proposed. Both use the **±250 Pa
hardware version**, with different initial measurement settings [10].

| **Instrument** | **Measurement** | **Initial setting** |
|:--|:--|:--|
| WIKA A2G-500 — Channel 1 | Pressure difference across the nozzles, $\Delta p_n$. The high-pressure port is connected upstream and the low-pressure port downstream. | **0 to 250 Pa** |
| WIKA A2G-500 — Channel 2 | Chamber pressure relative to the laboratory, $p_{\mathrm{ch},g}$. The positive port is connected to the chamber and the negative port to ambient. | **−150 to +150 Pa**, to be checked during commissioning |

The first setting covers the **18–72 Pa** signals estimated in Section
12.1. The second channel is bidirectional because the chamber pressure
may be below ambient. WIKA specifies a basic accuracy of **±1.25 Pa
at 23 °C** for this hardware version [10].

Both readings will be recorded on a PC via **Modbus RTU over RS-485**.
The two channels will be zeroed before testing by exposing both ports of
each transmitter to the same pressure. Check that the selected ranges
cover the actual operating points before starting the test sweep.

### 12.3.- Air temperature measurement and data recording

Air temperature will be measured using a **TC Direct type T thermocouple,
ref. 405-388**, with a **Ø1.5 mm × 300 mm** sheath, connected to the
**TC Direct USB data logger, ref. 357-730** [11]. The probe tip will be
positioned in the inlet airflow, clear of the wall. Air temperature will
be used together with barometric pressure and relative humidity to
calculate air density.

The logger will be set to **type T, °C and one reading per second**.
The logger clock and the pressure acquisition PC clock will be aligned
before the test. For each operating point, the initial plan is to record
a **30 s window after the readings stabilise**. The temperature data
will then be downloaded via USB and matched to the pressure data using
timestamps and the operating-point ID.

> [!CAUTION]
> 🟥 **12-C · Instrumentation to verify.** Confirm availability of the
> proposed instruments or equivalent laboratory equipment. Obtain the
> thermocouple tolerance and logger accuracy, and check that the laboratory
> PC can download and export the recorded data.
> 
## 13.- Preliminary assessment of measurement uncertainty (E2)

### 13.1.- Input specifications

| Source | Available specification or preliminary treatment |
|:--|:--|
| WIKA pressure channels | Basic accuracy ±1.25 Pa for the ±250 Pa hardware range at 23 °C, per PE 88.05. Selecting a smaller display range does not improve the stated basic accuracy. Reassess zero drift, ambient-temperature effects, installation and repeatability [10]. |
| Nozzle area and $C_d$ | Obtain separate contributions from throat measurement, coefficient calibration and nozzle configuration. |
| Testo 465 | Basic specification ±(0.02% of reading + 1 digit), with 1 rpm resolution at 1,445 rpm: approximately ±1.29 rpm under the stated conditions [13]. |
| Testo 622 | Absolute pressure ±(3 hPa + 1 digit); RH ±(2 percentage points + 1 digit) at 25 °C and 10–90% RH [12]. |
| Type-T probe and logger | Obtain the combined accuracy from the two specifications or from a calibration of the complete temperature chain. |
| Hioki PW3337 | At 45–66 Hz the product page specifies basic active-power accuracy of ±(0.1% of reading + 0.05% of full scale) below 50% of full scale, and ±0.15% of reading at or above 50% of full scale. Apply the detailed manual for the chosen wiring, range and power factor; include external current transducers if used [14]. |

### 13.2.- Worked example at one assumed operating point

The course uncertainty task calls for a representative point, preferably near the BEP. A verified curve for the tested assembly is not available in this report, so the example uses a representative **assumed** flow below the catalogue maximum. Its value demonstrates the propagation method and does not locate the BEP.

Take $Q=2.40\ \mathrm{m^3/s}$ (8,640 m³/h), both nozzles open, $\Delta p_n=56.39\ \mathrm{Pa}$ calculated using Section 12.1, $p_{\mathrm{ch},g}=-25\ \mathrm{Pa}$, and $P_{\mathrm{el}}=600\ \mathrm{W}$. These figures illustrate the method; the point is not a measurement or an identified BEP. For this calculation only, use $A_2=\pi(0.514)^2/4=0.2075\ \mathrm{m^2}$ as a geometric proxy and $\rho=1.20\ \mathrm{kg/m^3}$. With the preliminary pressure model in Section 14, this gives $p_{fd}=80.27\ \mathrm{Pa}$, $p_f=105.27\ \mathrm{Pa}$ and $\eta_{\mathrm{el}}=0.4211$ (air power $P_{\mathrm{air}}=252.64\ \mathrm{W}$).

Treat the basic bounds of the two separate WIKA channels as independent rectangular input distributions, so $u(\Delta p_n)=u(p_{\mathrm{ch},g})=1.25/\sqrt{3}=0.722\ \mathrm{Pa}$. Use a **hypothetical** ±3 W bound for the electrical power chain to demonstrate the calculation; this is not an accuracy claim for the Hioki. Temperature, geometry and nozzle calibration are held fixed in this partial example. The flow and outlet dynamic pressure depend on the same $Q$, so their influence on efficiency is propagated through that common variable.

$$
u(Q)\approx \frac{Q}{2\Delta p_n}u(\Delta p_n),\qquad
u^2(p_f)\approx \left(\frac{2p_{fd}}{Q}u(Q)\right)^2+u^2(p_{\mathrm{ch},g}).
$$

$$
u^2(P_{\mathrm{air}})\approx
\left((p_f+2p_{fd})u(Q)\right)^2
+\left(Q\,u(p_{\mathrm{ch},g})\right)^2 .
$$

$$
u^2(\eta_{\mathrm{el}})\approx
\left(\frac{p_f+2p_{fd}}{P_{\mathrm{el}}}u(Q)\right)^2
+\left(\frac{Q}{P_{\mathrm{el}}}u(p_{\mathrm{ch},g})\right)^2
+\left(\frac{\eta_{\mathrm{el}}}{P_{\mathrm{el}}}u(P_{\mathrm{el}})\right)^2 .
$$

| Output | Partial standard uncertainty $u$ | Relative to assumed value |
|:--|--:|--:|
| Volume flow rate $Q$ | 0.0154 m³/s | 0.64% |
| Fan total pressure $p_f$ | 1.26 Pa | 1.19% |
| Electrical active power $P_{\mathrm{el}}$ | 1.73 W | 0.29% |
| Air power $P_{\mathrm{air}}$ | 4.43 W | 1.76% |
| Electrical-input efficiency $\eta_{\mathrm{el}}$ | 0.00749 (0.75 percentage points) | 1.78% |

> [!CAUTION]
> 🟥 **13-A · Data needed to replace the illustrative example.** Request a **traceable curve for the selected fan at 1,445 rpm**, with its mounting and efficiency definition, if the group has one. Otherwise identify a point from the eventual bench sweep. Keep the example as shown for Release 1. In the full budget, use the actual power analyser range and calibration, add repeatability, pressure-tap effects, nozzle diameter and coefficient, density and outlet-area contributions. Compare the appropriate uncertainty with the limits in the clauses referenced in Section 14. A maximum of electrical-input efficiency must not be reported as a shaft-efficiency BEP without shaft-power data.

## 14.- Preliminary test bench and application of UNE-EN ISO 5801 (E3)

### 14.1.- Mounting category and reference setups

A **Type 2 inlet-chamber concept for Category A** is proposed, following the course inlet-chamber example. The fan inlet faces the chamber with no test duct attached; its outlet discharges freely into the laboratory. The fan is mounted on the chamber end wall with a sealed interface outside the inlet passage. Any inlet duct added later would change the boundary condition and require the installation category to be reviewed. A similar layout can be found in **ANSI/AMCA 210-25, Figure 15**, an inlet chamber with multiple nozzles, settling screens and a variable supply system [8, 16].

This is an academic proposal for a pressure–flow characterisation. UNE-EN ISO 5801:2019 is the course reference for the standardized airways approach. ISO 5801 directs jet fan testing to ISO 13350; consequently, these chamber measurements would not certify the thrust or performance of the complete jet fan in free installation [15].

For the verification of the proposed rig, the course notebook on test benches points to Clauses 5–6 for mounting categories, Clauses 3 and 15 for fan pressures and power, Clause 12.5 and Annex A for flow measurement, and Clause 17 for uncertainty. It also points to Clause 12.9 and Annex H for humid-air properties. AMCA Figure 15 is a comparable bench example; it does not replace verification against the course's UNE-EN ISO reference [8, 15, 16].

### 14.2.- Sketch and preliminary dimensions

```mermaid
flowchart TB
    subgraph supply["Upstream supply and flow control"]
      direction LR
      AMB["Room air"] --> AUX["Variable-speed auxiliary fan"] --> UP["Upstream plenum and inlet temperature"]
    end
    subgraph chamber["Inlet chamber"]
      direction TB
      NZ["Two parallel nozzles Ø400 mm — One can be blanked"] --> DN["Downstream pressure taps"]
      DN --> SET["Settling screens"] --> CH["Chamber pressure tap"]
    end
    UP --> NZ
    CH --> FAN["Test fan on end wall — No inlet duct"] --> OUT["Free outlet to laboratory"]
    UP -.->|High port| DP["Channel 1 — Nozzle differential"]
    DN -.->|Low port| DP
    CH -.->|High port| PG["Channel 2 — Chamber gauge pressure"]
    AMB -.->|Low port reference| PG
```

*Figure 14.1. Draft layout for Release 1. Solid arrows show airflow; dashed arrows show pressure lines or references. The sketch is not to scale and the dimensions below are proposed.*

For a side view, draw the chamber envelope around the nozzle plate and screens, put the test fan on the downstream end wall and leave the outlet open. In the view looking at the nozzle plate, draw the two throat centres at mid-height with a 1.24 m separation. Label the two nozzle taps, the chamber tap, the ambient reference and the inlet temperature probe; show the last two separately from the airflow path. The dimensions below are sufficient to redraw these two views without selecting a fan flange or inventing tap coordinates.

| Element | Preliminary dimension or choice | Basis |
|:--|:--|:--|
| Chamber internal width × height × axial length | 2.50 m × 1.40 m × 5.0 m, excluding auxiliary supply hardware and outlet clearance | Initial envelope to check against laboratory space and the selected reference layout. |
| Nozzle plate | Two 0.400 m throats at the same height and 1.24 m centre-to-centre | Centred in the chamber section: nearest side wall is 0.63 m from each centre; top and bottom are 0.70 m from the centres. |
| Nozzle exit to first settling screen downstream | 1.10 m preliminary axial spacing | AMCA Figure 15 gives a reference comparison of 2.5 throat diameters, or 1.00 m at Ø0.400 m. |
| Test-section duct lengths | Inlet 0 m; outlet 0 m | This proposal omits ducts connected to the fan's inlet or outlet so that the selected Category A arrangement is retained. |
| Fan interface | Nominal fan diameter Ø500 mm for layout only; actual chamber aperture and bolt pattern to be measured | The nominal rotor diameter is not a flange dimension. The Design section's Ø514 mm outlet is used only as a geometric proxy pending verification. |
| Nozzle centres for the plate view | $(x,y)=(0.63,0.70)$ and $(1.87,0.70)$ m, measured from the lower left inside corner | Geometric coordinates for the proposed plate only. |
| Pressure taps shown in the sketch | One station upstream of the nozzle bank, one downstream, and a separate chamber station after the screens | Indicate the relative positions in the draft. Assign numerical distances once the selected standard layout is checked. |

The chamber cross-section is $3.50\ \mathrm{m^2}$. Compared with a nominal 0.500 m circular inlet proxy ($0.196\ \mathrm{m^2}$), the area ratio is about 17.8; the course uses a ratio greater than 5 as an initial inlet-chamber check. At $Q=2.714\ \mathrm{m^3/s}$ the chamber's mean velocity is about 0.78 m/s, which supports the first approximation of chamber static pressure as inlet total pressure. The nozzle spacing and wall distances are also above the comparison values of §6.3.4 in AMCA 210-25 (3 and 1.5 throat diameters, respectively). These checks do not establish compliance with the complete ISO geometry [8, 16].

For the preliminary free-outlet model, $p_{fs}\approx -p_{\mathrm{ch},g}$ and $p_f\approx p_{fs}+p_{fd}$, where $p_{fd}=\rho(Q/A_2)^2/2$. This assumes the upstream total pressure is represented by the chamber pressure, the outlet static pressure is ambient and the selected area and density conventions are valid. Record the nozzle differential and the chamber gauge pressure separately. Verify the pressure stations and outlet area definition before using the model to process test data.

### 14.3.- Changing the operating point

Keep the test fan at its low-speed setting and vary the upstream auxiliary supply to obtain several steady flow points. Start with both nozzles open. Close one only for the lower-flow range if the pressure signal becomes too small, and repeat a point in the overlap to compare the configurations. The same nozzle bank measures flow in each case; the auxiliary supply sets the point. Record the actual speed and both pressure channels at every setting. Repeat one setting to assess repeatability.

Plot $p_{fs}(Q)$, $p_f(Q)$ and $\eta_{\mathrm{el}}(Q)$ after reducing the data. A comparison with CFD or Design requires matching the test geometry, speed, pressure definitions and measurement planes. The maximum flow achieved and the range of the pressure channels will depend on the rig and must be checked in commissioning.

> [!CAUTION]
> 🟥 **14-A · Confirm the bench envelope and mounting.** Obtain the **laboratory footprint and outlet clearance**, the **dimensioned inlet/outlet drawing** for the fan confirmed in 12-A and the **auxiliary fan curve**, if available. Check whether the 2.50 m × 1.40 m × 5.0 m chamber fits and whether the supply can overcome the estimated losses over the intended flow range. If it does not fit, compare the existing lab bench or a single-nozzle layout. The Release 1 sketch and tentative dimensions can remain as a proposal while these inputs are sought.

> [!CAUTION]
> 🟥 **14-B · Verify the standard layout before producing construction drawings.** Using the course copy of UNE-EN ISO 5801, confirm the Category A arrangement, the mounting interface, measurement planes, screen spacing and the definition of outlet area. Replace the indicative tap positions and Ø514 mm proxy with the checked values. Keep the preliminary calculation separate from any claim of compliance.

## 15.- References

1. UPC course repository: `0_Preliminary/P1_preparing_course.md` — *Quality criteria*, Design, Release 1.
2. UPC course repository: `1_Design/D1_fundamentals_and_dimensional_analysis.ipynb` — dimensional coefficients and Cordier analysis. **[TO VERIFY]** Confirm exact notebook filename if the repository has been updated.
3. UPC course repository: `1_Design/D2_mean_line_analysis_and_2d_cascade.ipynb` — velocity triangles, Lieblein diffusion factor, pitch/chord and lift coefficient.
4. UPC course repository: `2_CFD/C3_aerodynamics_of_2D_cascade.ipynb` — illustrative chord-angle/stagger setup; **not** a validated optimum for this rotor.
5. Dixon, S. L. and Hall, C. A., *Fluid Mechanics and Thermodynamics of Turbomachinery*, Chapters 2, 3 and 5.
6. SODECA THT/IMP technical catalogue and QuickFan selection tool. **[TO COMPLETE]** Exact catalogue document/edition, model variant, original output and page numbers.
7. Measurements of the group's CAD assembly: $D_t=494$ mm, $D_h=130.5$ mm, $D_{out}=514$ mm and $Z=6$. **[TO COMPLETE]** CAD filename and revision.
