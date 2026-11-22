# Theoretical design of an axial fan for tunnel ventilation (TJHT/2/4-500-C)

## 1.-Dimensions

The reference fan is the SODECA THT/IMP-LS-UNI-50-2/4T-6-F400, a unidirectional axial jet fan with a nominal impeller diameter of 500 mm, designed for tunnel and car park ventilation.

The commercial assembly consists of a galvanized steel casing with reduced length, an axial impeller, an electric motor, silencers, a protective grille, an outlet deflector and mounting supports.

The manufacturer provides the following dimensions for the THT/IMP-LS-50 model. The symbols correspond to the dimensional drawing shown in Figure 1. All dimensions are expressed in millimetres.

<img width="1000" alt="Dimensions Fan" src="https://github.com/user-attachments/assets/c1c9b665-8b0b-4547-bff5-b25fd3dc717a" />

*Figure 1. Dimensional drawing of the SODECA THT/IMP-LS-50. All dimensions are in mm. Source: SODECA, THT/IMP technical catalogue, page 5.*

| Dimension | Value (mm) |
|-----------|--------------|
| A | 546 |
| B | 549 |
| C | 742 |
| E – Overall length | 1445 |
| L – Casing length | 1200 |
| X | 560 |
| X1 | 255 |
| Z | 778 |
| Z1 | 808 |

The nominal impeller diameter of 500 mm is used as the initial reference for the theoretical fan design. The detailed rotor geometry will be defined in the next stages of the project.

## 2.- Performance

The project uses the SODECA THT/IMP-LS-UNI-50-2/4T-6-F400 as a commercial reference for the theoretical design of an axial jet fan for tunnel ventilation. The fan generates an axial air jet that transfers momentum to the surrounding air, promoting longitudinal airflow through the tunnel.

The selected fan operates at two rotational speeds, providing different airflow rates and thrust levels. The manufacturer specifies the following performance characteristics:

| Parameter | High speed | Low speed |
|-----------|------------|-----------|
| Rotational speed (rpm) | 2915 | 1445 |
| Volumetric flow rate (m³/h) | 19700 | 9766 |
| Outlet air velocity (m/s) | 26.4 | 13.09 |
| Thrust (N) | 165 | 40.55 |

*Table 1. Performance characteristics of the SODECA THT/IMP-LS-UNI-50-2/4T-6-F400. Source: SODECA QuickFan selection software.*

For the preliminary theoretical design, the low-speed operating condition (1445 rpm) is selected as the reference point. This operating condition provides a volumetric flow rate of approximately 9770 m³/h and a jet thrust of 40.55 N.

The dynamic pressure of the air jet can be estimated using:

$$
p_d = \frac{1}{2}\rho v^2
$$

Assuming an air density of 1.2 kg/m³ and an outlet velocity of 13.09 m/s:

$$
p_d = \frac{1}{2}(1.2)(13.09)^2 \approx 103\ \mathrm{Pa}
$$

This value represents the estimated jet dynamic pressure and should not be interpreted as the total pressure rise across the fan.

Fan characteristic curves describe the relationship between pressure and airflow at a given rotational speed. They can also show how efficiency changes across the operating range.

Figure 2 illustrates this general concept. It is included as a theoretical reference and does not represent the performance of the selected SODECA fan.

<img width="329" height="297" alt="image" src="https://github.com/user-attachments/assets/dff147b8-1ce6-42f5-a30b-d37b3cbed890" />

*Figure 2. Generic fan characteristic curves.*


## 3.- Estimated power consumption

A preliminary estimate of the electrical power consumption is obtained from the reference airflow rate and the estimated dynamic pressure of the air jet.

The selected low-speed operating condition corresponds to a volumetric flow rate of 9766 m³/h, an outlet velocity of 13.09 m/s and a rotational speed of 1445 rpm.

The dynamic pressure of the jet, calculated in Section 2, is approximately 103 Pa.

The aerodynamic power associated with the air jet can be estimated as:

$$
P_{\mathrm{jet}} = Q p_d
$$

where Q is the volumetric flow rate in m³/s and p_d is the jet dynamic pressure in Pa.

Using the reference operating conditions:

$$
Q = \frac{9766}{3600} = 2.713\ \mathrm{m^3/s}
$$

$$
P_{\mathrm{jet}} = 2.713 \times 103
\approx 279\ \mathrm{W}
$$

To obtain a preliminary estimate of the electrical power consumption, an overall jet-power efficiency of 50% is assumed. This is a simplified design assumption and not a value provided by the manufacturer.

$$
P_{\mathrm{electrical,est}}
= \frac{P_{\mathrm{jet}}}{\eta_{\mathrm{overall}}}
= \frac{279}{0.50}
\approx 558\ \mathrm{W}
$$

The estimated electrical power consumption is therefore approximately 0.56 kW under the assumed efficiency.

According to the SODECA technical catalogue, the selected fan has a nominal motor power of 1.30 kW at low speed. This represents the installed motor power rating and should not be interpreted as the actual electrical power consumption at the operating point.

The estimated consumption of 0.56 kW is preliminary and will be reviewed during the next design stages.


## 4.-Applications

According to the manufacturer, the SODECA THT/IMP series consists of axial jet fans designed to generate high-velocity air jets for ventilation and smoke control in enclosed spaces, particularly car parks.

These fans transfer momentum to the surrounding air, promoting airflow over long distances without requiring conventional air distribution ductwork.

This project focuses on tunnel ventilation, using the SODECA THT/IMP-LS-UNI-50-2/4T-6-F400 as a commercial reference. In tunnels, jet fans can be used to promote longitudinal airflow, dilute pollutants during normal operation and assist smoke management in emergency situations.

The selected model is unidirectional and has an F400 classification, indicating that the commercial fan is certified for operation at 400°C for two hours according to EN 12101-3. This certification applies to the commercial product and is not claimed for the theoretical design developed in this project.

Source: [SODECA — THT/IMP Technical Catalogue](https://www.sodeca.com).

## 5.- Examples of different axial fans dedicated to tunnel ventilation

SOLER & PALAU (TJHT/2/4-500-C)
- VELOCIDAD: 1440 RPM
- PRESIÓN: 94 Pa (Ø500 mm)
- CAUDAL: 8800 m^3/h

ZITRÓN (JZp 4/H-1,5/0,37-2/4 RE F400)
- VELOCIDAD: 2845 RPM
- PRESIÓN: 220 Pa (Ø400 mm)
- CAUDAL: 8700 m^3/h

NOVOVENT (JET WINDER 4-560T-4 0.55 kW)
- VELOCIDAD: 1500 RPM
- PRESIÓN: 78 Pa (Ø490 mm)
- CAUDAL: 10087 m^3/h
# Theoretical design of an axial fan for tunnel ventilation (SODECA THT/IMP-LS-UNI-50-2/4T-6-F400)

> **Scope — Design, Release 1.** This section covers the four Design requirements specified in `0_Preliminary/P1_preparing_course.md`: specifications and dimensionless parameters, geometry of the fan components, materials and their justification, and mean-line analysis. The detailed radial distribution, final airfoil selection and final rotor geometry belong to Release 2.
>
> **Model identification:** The commercial reference used in this study is **SODECA THT/IMP-LS-UNI-50-2/4T-6-F400**. **[TO VERIFY]** An older heading in `PROJECT.md` mentions `TJHT/2/4-500-C`, which is a different model designation. Check the exact reference against the group's original catalogue before submitting.

## 1.- Dimensions

The project is based on a unidirectional axial jet fan for tunnel ventilation. The assembly comprises a cylindrical casing, a six-bladed axial impeller, a central hub, an electric motor and its supports, and the remaining protective or mounting elements of the commercial unit.

**[FIGURE REQUIRED]** Retain the dimensional drawing already uploaded in the existing `PROJECT.md` as *Figure 1*, together with its original SODECA catalogue citation. Do not delete its existing GitHub image link when replacing the Design section.

The commercial assembly dimensions already included in the project are listed below. **[TO VERIFY]** Confirm the letter-to-dimension correspondence against Figure 1 and the manufacturer's drawing.

| Catalogue dimension | Value (mm) |
|:--|--:|
| A | 546 |
| B | 549 |
| C | 742 |
| E — overall length | 1445 |
| L — casing length | 1200 |
| X | 560 |
| X1 | 255 |
| Z | 778 |
| Z1 | 808 |

The following dimensions have been measured or identified from the supplied CAD model and are used in the theoretical rotor calculation:

| Rotor / outlet dimension | Symbol | Value |
|:--|:--:|--:|
| Outer rotor diameter | $D_t$ | 494 mm |
| Hub diameter at the rotor | $D_h$ | 130.5 mm |
| Nominal outlet diameter | $D_{out}$ | 514 mm |
| Number of rotor blades | $Z$ | 6 |
| Rotor tip radius | $r_t=D_t/2$ | 247.00 mm |
| Hub radius | $r_h=D_h/2$ | 65.25 mm |
| Arithmetic mean radius | $r_m=(r_t+r_h)/2$ | 156.125 mm |
| Blade span (radial height) | $h=r_t-r_h$ | 181.75 mm |

**Assumption A1:** The annular area is calculated using the measured outer rotor and hub diameters, both treated as circular and concentric. Any local flow blockage from the blade thickness is neglected at this preliminary stage.

$$
A=\frac{\pi}{4}\left(D_t^2-D_h^2\right)
 =\frac{\pi}{4}\left(0.494^2-0.1305^2\right)
 =0.178290\;\mathrm{m^2}
$$

The circular area corresponding to the stated outlet diameter is:

$$
A_{out,nom}=\frac{\pi D_{out}^2}{4}
 =\frac{\pi(0.514)^2}{4}=0.20750\;\mathrm{m^2}.
$$

**[TO VERIFY]** The 514 mm diameter is treated as a *nominal geometric outlet diameter*, not as a measured unobstructed free-flow area. The final available area depends on the configuration at the outlet.

For comparison, the root-mean-square (RMS) radius is:

$$
r_{m,RMS}=\sqrt{\frac{r_t^2+r_h^2}{2}}=0.18065\;\mathrm{m}.
$$

**Assumption A2:** The **arithmetic mean radius, $r_m=0.156125$ m**, is used consistently throughout Release 1 to define the two-dimensional mean-line cascade. A change to the RMS criterion would require recalculating blade speed, pitch and velocity triangles; the RMS radius is not mixed with the arithmetic-radius results below.

## 2.- Performance and design requirements

The selected commercial reference is operated at two rotational speeds. **Only the 1445 rpm configuration is designed in the present Release 1 analysis.** The higher-speed data are retained in the existing Release 0 commercial description, but are not used below.

| Parameter | Symbol | Low-speed reference value |
|:--|:--:|--:|
| Rotational speed | $N$ | 1445 rpm |
| Volume flow rate | $Q$ | approximately 9770 m³/h |
| Jet air velocity | $v_{jet}$ | approximately 13.1 m/s |
| Number of blades | $Z$ | 6 |
| Rotor diameter measured in CAD | $D_t$ | 0.494 m |
| Hub diameter measured in CAD | $D_h$ | 0.1305 m |
| Outlet diameter measured in CAD | $D_{out}$ | 0.514 m |
| Installed motor power | $P_{motor,rated}$ | **[TO VERIFY AGAINST CATALOGUE]** |
| Absorbed mechanical/electrical power at 1445 rpm | $P_{abs}$ | **[DATA REQUIRED: NOT AVAILABLE]** |
| Total pressure rise across the rotor | $\Delta p_0$ | **[DATA REQUIRED: NOT MEASURED]** |

**[SOURCE PRECISION]** The existing `PROJECT.md` table contains 9766 m³/h and 13.09 m/s at low speed. The present preliminary calculation uses their rounded approximations, $Q=9770$ m³/h and $v_{jet}=13.1$ m/s, to remain consistent with the preceding calculation sheets. Update all derived values together if the unrounded catalogue data are adopted.

**Assumption A3:** Air properties are constant: density $\rho=1.20\;\mathrm{kg/m^3}$ and dynamic viscosity $\mu=1.81\times10^{-5}\;\mathrm{Pa\,s}$.

**Assumption A4:** The flow is steady and incompressible for the preliminary analytical model. Its axial velocity is uniform over the annular section, and it is taken as unchanged between rotor inlet and outlet ($c_{x1}=c_{x2}=c_x$).

**Assumption A5:** The flow approaches the rotor without inlet pre-swirl ($c_{\theta1}=0$). This is a theoretical inlet boundary condition; absence of upstream guide vanes alone does not prove zero pre-swirl in operation.

**Assumption A6:** Ideal Euler energy transfer is assumed for the preliminary velocity triangles ($\eta_{Euler}=1$). Real aerodynamic, mechanical and motor losses are not included in this approximation.

**Assumption A7 — pressure estimate:** Until a measured or manufacturer-specified rotor **total** pressure rise is available, the *jet dynamic pressure* is used as a **surrogate estimate**, not as an experimentally verified fan total-pressure rise:

$$
\Delta p_{0,est}\equiv\frac12\rho v_{jet}^{2}
 =\frac12(1.20)(13.1)^2
 =102.966\;\mathrm{Pa}.
$$

This estimate is used consistently below, but the equality between the rotor total-pressure rise and free-jet dynamic pressure is **not generally exact**: inlet kinetic energy, swirl, losses and the measurement stations may affect the actual rotor pressure rise.

As a useful geometrical check, the nominal outlet speed is:

$$
v_{out,nom}=\frac{Q}{A_{out,nom}}=\frac{9770/3600}{0.20750}=13.079\;\mathrm{m/s},
$$

which is close to the rounded commercial jet speed of 13.1 m/s. This checks the nominal area–flow–velocity relation, **not** the total-pressure assumption.

The angular speed and estimated ideal hydraulic power are:

$$
\omega=\frac{2\pi N}{60}=\frac{2\pi(1445)}{60}=151.320\;\mathrm{rad/s},
$$

$$
P_{h,est}=Q\Delta p_{0,est}
 =\left(\frac{9770}{3600}\right)(102.966)
 =279.44\;\mathrm{W}.
$$

**[DATA REQUIRED]** The absorbed shaft power and real efficiency cannot be obtained from $P_{h,est}$ alone. The installed/rated power of the commercial motor must not be reported as the measured absorbed shaft power.

## 3.- Dimensionless parameters and Cordier diagram

Following notebook `D1_fundamentals_and_dimensional_analysis.ipynb`, the rotor diameter $D=D_t=0.494$ m is the reference length for the dimensionless coefficients. The definitions use angular speed in rad/s, volume flow rate in m³/s and the **estimated** total-pressure rise.

The mean axial velocity and the flow coefficient are:

$$
c_m=c_x=\frac{Q}{A}=\frac{9770/3600}{0.178290}=15.222\;\mathrm{m/s},
$$

$$
\phi=\frac{Q}{\omega D^3}
=\frac{9770/3600}{151.320(0.494)^3}
=\boxed{0.14877}.
$$

The pressure coefficient is:

$$
\psi=\frac{\Delta p_{0,est}}{\rho\omega^2D^2}
=\frac{102.966}{1.20(151.320)^2(0.494)^2}
=\boxed{0.01536}.
$$

The hydraulic power coefficient is:

$$
\hat P=\frac{P_{h,est}}{\rho\omega^3D^5}
=\phi\psi
=\boxed{0.002284}.
$$

The Reynolds number based on the rotor diameter, using the annular mean axial velocity, is:

$$
Re_D=\frac{\rho c_m D}{\mu}
=\frac{1.20(15.222)(0.494)}{1.81\times10^{-5}}
=\boxed{4.99\times10^5}.
$$

The specific speed and specific diameter, as defined in D1, are:

$$
\Omega_s=\frac{\omega\sqrt Q}{(\Delta p_{0,est}/\rho)^{3/4}}
=\boxed{8.842},
$$

$$
D_s=\frac{D(\Delta p_{0,est}/\rho)^{1/4}}{\sqrt Q}
=\boxed{0.9127}.
$$

| Dimensionless parameter | Symbol | Value at 1445 rpm |
|:--|:--:|--:|
| Flow coefficient | $\phi$ | 0.14877 |
| Pressure coefficient | $\psi$ | 0.01536 |
| Hydraulic power coefficient | $\hat P$ | 0.002284 |
| Rotor Reynolds number | $Re_D$ | $4.99\times10^5$ |
| Specific speed | $\Omega_s$ | 8.842 |
| Specific diameter | $D_s$ | 0.9127 |

The point to be plotted in the Cordier diagram is therefore:

$$
\boxed{(D_s,\Omega_s)=(0.9127,\,8.842)}.
$$

![Cordier diagram — 1445 rpm design point](images/cordier_R1_1445rpm.png)

*Figure 2. Design point at 1445 rpm on a logarithmic Cordier-type diagram. The reference curve drawn in this figure is schematic; it is intended to illustrate the location of the calculated point, not to reproduce a digitized published optimum-efficiency curve. Based on the approximate pressure estimate, the location is consistent with an axial-flow machine. The classification and optimum operating condition remain subject to validation.*

**[IMAGE ACTION REQUIRED]** Upload the supplied `cordier_R1_1445rpm.png` to the `images/` directory of the group's GitHub repository, or replace the relative path above with the URL of the image uploaded directly through GitHub. Otherwise the figure will not render in `PROJECT.md`.

## 4.- Geometry of the axial fan components

At this preliminary stage, the main geometrical elements are identified as follows:

| Component | Geometry / function | Available information | Missing information |
|:--|:--|:--|:--|
| Rotor and blades | Six rotating blades exchange momentum with the air | $D_t=494$ mm; $Z=6$; preliminary mean-line chord estimated in Section 6 | Final NACA profile, blade twist, spanwise chord and airfoil thickness |
| Hub | Central support of the blades and rotor attachment | $D_h=130.5$ mm | Axial length, connection to shaft, attachment details |
| Casing | Cylindrical structure enclosing the rotor and supporting the assembly | Nominal dimensions in Section 1 | Local internal diameter at rotor, tip clearance, wall thickness |
| Electric motor | Provides shaft power to the rotor | Two-speed operation is stated in the commercial reference | Actual absorbed power, shaft connection, motor model and rating confirmation |
| Motor supports | Attach the motor/hub assembly to the casing | Visible in the supplied assembly views | Exact section, dimensions and flow blockage |
| Outlet section | Delivers the jet to the surrounding environment | Nominal diameter 514 mm | Effective unobstructed area and final outlet assembly details |
| Protective grille / deflector / silencers | Safety, jet guidance and noise control, where present | Mentioned in existing commercial assembly description | **[TO VERIFY]** Whether each element is present in the specific CAD configuration used for the project |

**Assumption A8:** The measured rotor and hub dimensions are used as the design envelope. The aerodynamic blade section, chord and installation angle are **design variables**, not confirmed measurements of the as-supplied commercial rotor.

**[FIGURE REQUIRED]** Insert a labelled CAD front view and a side or sectional view identifying rotor, hub, casing, motor, supports, inlet and outlet. Include dimensions only if directly measured or provided by the catalogue.

## 5.- Materials and characteristics. Justification

**[TO COMPLETE — GROUP INPUT REQUIRED]** The uploaded information does not identify the material grade or the mechanical properties of all parts reliably. No material designation or numerical property has been assumed.

| Component | Selected material / grade | Density | Mechanical / thermal characteristics | Manufacturing / selection justification |
|:--|:--|:--|:--|:--|
| Blades |  |  |  |  |
| Hub |  |  |  |  |
| Shaft / rotor connection |  |  |  |  |
| Casing |  |  |  |  |
| Motor supports |  |  |  |  |
| Protective grille / outlet elements (if present) |  |  |  |  |

**[TO COMPLETE]** Document the required operating temperature, corrosion/environmental requirements, expected loads and manufacturing constraints. A fire-performance classification appearing in a commercial reference does not by itself verify the proposed project's structural or thermal compliance.

## 6.- Mean-line analysis and preliminary blade dimensioning

The analysis follows notebook `D2_mean_line_analysis_and_2d_cascade.ipynb` and refers exclusively to the **arithmetic mean-radius section**. It is a steady, two-dimensional rotor cascade approximation, not a full radial blade design.

### 6.1.- Velocity triangles

From the geometry and operating point:

$$
U_m=\omega r_m=(151.320)(0.156125)=23.625\;\mathrm{m/s},
$$

$$
c_x=15.222\;\mathrm{m/s},\qquad c_{\theta1}=0.
$$

By the ideal Euler equation:

$$
\Delta p_{0,est}=\rho U_m(c_{\theta2}-c_{\theta1}),
$$

$$
c_{\theta2}=\frac{102.966}{1.20(23.625)}=3.632\;\mathrm{m/s}.
$$

The inlet and outlet relative velocity magnitudes are:

$$
w_1=\sqrt{c_x^2+U_m^2}=28.104\;\mathrm{m/s},
$$

$$
w_2=\sqrt{c_x^2+(U_m-c_{\theta2})^2}=25.128\;\mathrm{m/s}.
$$

Using positive relative angles measured from the axial direction toward the direction opposing rotation:

$$
\beta_1=\tan^{-1}\left(\frac{U_m}{c_x}\right)=\boxed{57.206^\circ},
$$

$$
\beta_2=\tan^{-1}\left(\frac{U_m-c_{\theta2}}{c_x}\right)=\boxed{52.716^\circ}.
$$

The mean relative-flow angle is:

$$
\beta_m=\tan^{-1}\left[\frac{\tan\beta_1+\tan\beta_2}{2}\right]
=55.086^\circ.
$$

| Quantity | Rotor inlet (1) | Rotor outlet (2) |
|:--|--:|--:|
| Axial absolute velocity $c_x$ (m/s) | 15.222 | 15.222 |
| Tangential absolute velocity $c_\theta$ (m/s) | 0 | 3.632 |
| Relative velocity $w$ (m/s) | 28.104 | 25.128 |
| Relative angle $\beta$ (deg) | 57.206 | 52.716 |

**[FIGURE REQUIRED]** Insert the inlet and outlet velocity triangles, indicating $U_m$, $c_x$, $c_\theta$, $w$ and the positive direction used for $\beta$. A labelled hand drawing is acceptable if the angles and reference system are unambiguous.

### 6.2.- Pitch, diffusion factor and minimum chord

The six blades are distributed uniformly at the mean radius. The pitch is:

$$
s=\frac{2\pi r_m}{Z}
 =\frac{2\pi(0.156125)}{6}
 =0.163494\;\mathrm{m}=163.49\;\mathrm{mm}.
$$

**Assumption A9:** A conservative diffusion-factor limit $DF_{max}=0.45$ is adopted for preliminary dimensioning, below the illustrative value of 0.50 used in the D2 classroom exercise.

Using the Lieblein diffusion-factor expression for the relative rotor flow:

$$
DF=1-\frac{w_2}{w_1}
+\frac{c_{\theta2}-c_{\theta1}}{2w_1}\frac{s}{l}.
$$

At the selected design limit:

$$
\left(\frac{s}{l}\right)_{max}
=\frac{2w_1}{c_{\theta2}-c_{\theta1}}
\left(DF_{max}-1+\frac{w_2}{w_1}\right)
=\boxed{5.325}.
$$

The corresponding minimum chord is:

$$
l_{min}=\frac{s}{(s/l)_{max}}
=\frac{163.49}{5.325}
=\boxed{30.70\;\mathrm{mm}}.
$$

This minimum is a **diffusion-based lower bound**, not a final aerodynamic or structural blade design.

### 6.3.- Chord selection using the required lift coefficient

**Assumption A10:** A representative blade-section drag coefficient $C_D=0.02$ is adopted as in D2, pending validation for the selected airfoil and Reynolds number.

The project's preferred mean-line design target is **$C_L\approx0.75$**, i.e., below the group's selected range of approximately 0.8–0.9; **$C_L=1$ is not the project's target**. The notebook D2 uses about 1.0 as an illustrative upper-order design level, not as a mandatory value.

The cascade relation (Dixon, Eq. 3.26a) gives:

$$
C_L=2\frac{s}{l}\cos\beta_m
(\tan\beta_1-\tan\beta_2)-C_D\tan\beta_m.
$$

For the previously considered chord of $l=47$ mm:

$$
\frac{s}{l}=\frac{163.494}{47}=3.479,
\qquad C_L=\boxed{0.921}.
$$

Therefore, **47 mm no longer meets the selected $C_L\approx0.75$ target** after correcting the rotor and hub diameters.

Solving the lift equation for the chord at $C_{L,target}=0.75$:

$$
l=\frac{2s\cos\beta_m(\tan\beta_1-\tan\beta_2)}
{C_{L,target}+C_D\tan\beta_m}
=\boxed{57.35\;\mathrm{mm}}.
$$

A **rounded preliminary chord $l=57.5$ mm** is selected for Release 1. This is a design proposal and must not be represented as a measured CAD chord or as a CFD-validated result.

The resulting mean-line parameters are:

$$
\frac{s}{l}=\frac{163.494}{57.5}=\boxed{2.843},
\qquad \sigma=\frac{l}{s}=\boxed{0.352}.
$$

$$
C_L=\boxed{0.748},
\qquad DF=\boxed{0.290}.
$$

The blade-section Reynolds number based on the inlet relative velocity is:

$$
Re_l=\frac{\rho w_1 l}{\mu}
=\frac{1.20(28.104)(0.0575)}{1.81\times10^{-5}}
=\boxed{1.07\times10^5}.
$$

| Mean-line design quantity | Previous chord | Proposed Release 1 chord |
|:--|--:|--:|
| Blade count $Z$ | 6 | 6 |
| Mean-radius pitch $s$ | 163.49 mm | 163.49 mm |
| Chord $l$ | 47.0 mm | **57.5 mm** |
| Pitch-to-chord ratio $s/l$ | 3.479 | **2.843** |
| Solidity $l/s$ | 0.287 | **0.352** |
| Lift coefficient $C_L$ | 0.921 | **0.748** |
| Diffusion factor $DF$ | 0.331 | **0.290** |

The chosen chord exceeds the minimum based on the diffusion factor, while meeting the mean-line lift target under the stated assumptions.

### 6.4.- Preliminary blade angles and limitations

The aerodynamic flow angles $\beta_1=57.206^\circ$ and $\beta_2=52.716^\circ$ come from the velocity triangles, **not from the as-yet-undefined airfoil geometry**.

**Assumption A11:** A preliminary stagger angle $\xi=53^\circ$ has been considered by analogy with the two-dimensional cascade example in the CFD notebook C3. The associated angle between the incoming relative flow and the airfoil **chord** is:

$$
\alpha_{chord}=\beta_1-\xi
=57.206^\circ-53^\circ
=\boxed{4.206^\circ}.
$$

This angle is **not necessarily the blade-metal incidence** $i=\beta_1-\beta'_1$: for a cambered profile, $\beta'_1$ (leading-edge camber-line tangent) generally differs from $\xi$ (chord direction). The $\sim4^\circ$ value must not be presented as an optimized airfoil angle of attack or as a CFD validation result.

**[TO COMPLETE IN RELEASE 2]** Select the actual airfoil, determine its camber, thickness, metal angles, spanwise twist and validated stagger. The optional Howell calculation from D2 can serve as a preliminary estimate, but should not be mixed with the fixed $53^\circ$ chord orientation unless the geometrical incidence and deviation conventions are reconciled.

### 6.5.- Current design status

The Release 1 analytical design has been completed **at the mean-radius preliminary level**, subject to the stated assumptions and outstanding data:

| Item | Current status |
|:--|:--|
| Measured rotor and hub diameters | Defined from CAD |
| Nominal operating point | Defined at 1445 rpm |
| Dimensionless coefficients and Cordier location | Calculated from estimated pressure head |
| Relative velocity triangles | Calculated (ideal Euler model) |
| Blade number and pitch | Defined at mean radius |
| Chord meeting $C_L\approx0.75$ | Preliminary selection: 57.5 mm |
| Diffusion factor check | Calculated: 0.290 |
| Final airfoil and stagger | Pending detailed blade design |
| True total-pressure rise and absorbed power | **Data required / validation pending** |
| Materials and component design | **Group input required** |

## 7.- References and source notes

1. `AdvancedFluidDynamicDesign-AxialFan-main/0_Preliminary/P1_preparing_course.md`, *Quality criteria — Design, Release 1*.
2. `1_Design/D1_fundamentals_and_dimensional_analysis.ipynb`, *Tasks* and *Your project*: flow/head/power coefficients, Reynolds number, specific speed/diameter, Euler approximation and Cordier diagram.
3. `1_Design/D2_mean_line_analysis_and_2d_cascade.ipynb`, *Tasks* and *Your project*: diffusion factor, pitch/chord, blade number, lift coefficient and preliminary cascade geometry.
4. Dixon, S. L. and Hall, C. A., *Fluid Mechanics and Thermodynamics of Turbomachinery*, Chapter 2 (dimensional analysis and Cordier diagram), Chapter 3 (two-dimensional cascades), and Chapter 5 (axial-flow compressors and ducted fans).
5. SODECA, THT/IMP technical catalogue and the commercial performance data already included in the existing project. **[TO COMPLETE]** Add the precise catalogue edition, document URL/page and confirm the model designation.
6. Measurements from the group's CAD model: rotor outer diameter 494 mm, hub diameter 130.5 mm, nominal outlet diameter 514 mm and six blades. **[TO COMPLETE]** Add the CAD source/filename and measurement date if required for traceability.

