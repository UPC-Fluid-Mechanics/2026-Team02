# Release 1 — Axial fan for tunnel ventilation

## 1. Scope and shared design inputs

This release develops a preliminary six-blade axial fan design for tunnel ventilation using a SODECA jet fan as the commercial reference. The analysis focuses on the low-speed condition. The design provides the geometry and velocity triangles for preliminary CFD, while the experimental proposal specifies how airflow, pressure and power would be measured.

| Quantity | Main design case | Status |
|---|---:|---|
| Number of blades | 6 | Preliminary group selection |
| Rotational speed | 1445 rpm | Low-speed design case |
| Nominal diameter | 500 mm | Commercial reference; check the clear diameter and mounting interface separately |
| Volume flow rate | 9770 m³/h (2.714 m³/s) | Nominal reference adopted in the group analysis |
| Reference jet velocity | 13.1 m/s | Value reported in the group's analysis |
| Pressure scale | 102.97 Pa | Estimated as dynamic pressure from jet velocity; not a measured fan pressure rise |
| Installed motor rating | 1.30 kW | Value reported in the group analysis; not measured power consumption |

**[GROUP — CONFIRM]** The group calculations use THT/IMP-LS-UNI-50-2/4T-6-F400. The supplied STEP filename identifies THT/IMP-C-UNI-50-2/4T-6. Verify whether the drawing and operating data describe the same assembly. Link the catalogue row and state whether the proposed test is for the new fan or the commercial assembly. Treat 2915 rpm as a comparison case, unless the group extends the scope.

## 2. Design

### 2.1 Specification and dimensionless parameters

*Course reference: D1.*

The group's initial analysis uses an air density of 1.20 kg/m³, dynamic viscosity of 1.81 × 10⁻⁵ Pa·s, no inlet prerotation and an ideal Euler calculation. At 1445 rpm, the estimated jet dynamic pressure is 102.97 Pa and the corresponding ideal air power is about 279 W. These figures depend on the jet-velocity approximation.

With the full nominal circular cross-section, the preliminary mean axial velocity is 13.82 m/s. The original D1 velocity triangle is evaluated at the **blade tip**, with a peripheral velocity of 37.83 m/s and a calculated outlet tangential component of 2.27 m/s under the stated assumptions.

| D1 result | 1445 rpm case | 2915 rpm comparison |
|---|---:|---:|
| Reference airflow (m³/h) | 9770 | 19 700 |
| Flow coefficient | 0.14348 | 0.14341 |
| Pressure coefficient | 0.01499 | 0.01496 |
| Specific speed | 8.842 | 8.854 |
| Specific diameter | 0.924 | 0.924 |

**[DESIGN — ADD]** Insert the Cordier diagram and define the coefficients. Include the first performance estimate with its assumptions and distinguish catalogue references from predictions for the new design.

### 2.2 Geometry description of all the parts of the axial fan

| Part | Current information | What to show in the report |
|---|---|---|
| Rotor and blades | Six blades; Ø500 mm nominal reference; preliminary mean-radius chord 35.43 mm | Label the profile, chord, span and blade orientation; distinguish proposed geometry from the commercial reference. |
| Hub | Ø250 mm assumed in the mean-line model | Show the adopted diameter and its connection to the rotor and drive. |
| Casing and connections | Commercial STEP available; variant to confirm | Show the casing, actual flow diameter, mounting interface and main dimensions. |
| Drive, supports and accessories | Configuration to confirm | Identify the motor and support assembly, and any silencers or guards included in the proposed design. |

**[DESIGN — ADD]** Insert an annotated view of the assembly and a cross-section. Identify parts only where they are present in the confirmed design.

### 2.3 Materials and characteristics

**[DESIGN — ADD]** For each applicable component (blades, hub, casing and supports), state the proposed material, the relevant property and why it was selected. Cite a source for any material specification. Distinguish the materials of the commercial reference from the materials proposed for the new design.

### 2.4 Mean-line analysis

*Course reference: D2; D3 may inform later spanwise development.*

The updated mean-line calculation uses an assumed hub diameter of 250 mm and evaluates the triangle at a mean radius of 187.5 mm. It uses the annular flow area of 0.1473 m², which gives an axial velocity of 18.43 m/s. This differs from D1 because D1 used the full circular area and evaluated its triangle at the tip. Use the **D2 mean-radius triangle**, with one explicit angle convention, as the input for the CFD cascade.

| Result for six blades at 1445 rpm | Value |
|---|---:|
| Blade pitch at mean radius | 196.35 mm |
| Adopted maximum diffusion factor | 0.45 |
| Maximum pitch-to-chord ratio | 8.420 |
| Minimum chord from the diffusion criterion | 23.32 mm |
| Preliminary chord for a lift coefficient of 1 | 35.43 mm |

The minimum chord is a lower bound. The 35.43 mm value follows the preliminary D2 lift target of approximately 1 in the course notebook. A range of 0.3–0.7 has been suggested informally and is pending confirmation. Holding the present D2 assumptions fixed, a target of 0.5 would give a mean-radius chord of about 69 mm. If a different lift target is adopted, update the cascade geometry before comparing CFD with D2.

**[DESIGN — ADD]** Insert the mean-radius triangles and the calculations supporting blade count and chord. Specify the selected profile, incidence and stagger if available, and identify any remaining material or geometry choices.

#### Optional D3 progress

**[DESIGN — ADD IF AVAILABLE]** Summarise progress on spanwise chord and angles and any direct or inverse radial calculations already performed. The full radial analysis is listed under Release 2 in the course criteria. D3 gives its own lift and diffusion targets for radial design; do not treat the D2 mean-radius value as a spanwise requirement.

## 3. CFD

### 3.1 CAD description

*Course reference: C1.*

The STEP file is a commercial assembly reference. The preliminary mean-line CFD case should identify the actual 2D profile and cascade geometry used, based on D2.

**[CFD — ADD]** Provide the SimScale case link and a view of the fluid domain. Record the profile, chord, pitch, blade orientation and dimensions used. Explain the relationship between the cascade geometry and the reference STEP assembly.

### 3.2 Mesh description

*Course reference: C2.*

**[CFD — ADD]** Include a mesh image, cell count, base size and refinements near the profile. Explain the near-wall treatment used. The formal mesh convergence and GCI results can be added later under the course's Release 2 criteria.

### 3.3 Boundary conditions

*Course reference: C3.*

**[CFD — ADD]** Include inlet, outlet, blade-wall and lateral boundary conditions, with values and units. Explain how inlet velocity and angle relate to D2. 

#### Preliminary mean-line simulation results

Once the case is run, add the first flow result and compare a common quantity, such as outlet flow angle, against D2 using the same convention. Record results as pending until a run is available.

**Section ownership:** The design and CFD teams should insert the existing figures and SimScale evidence in Sections 2 and 3. Sections 4.1–4.3 address the experimental assessment criteria.



## 4. Experimentation

The proposed aerodynamic test focuses on the designed six-blade fan at 1445 rpm unless the group confirms a different test article. The instrument and bench proposals below are sized initially around 2.714 m³/s. They do not represent laboratory measurements.

### 4.1 Relevant variables of the axial fan

| Variable | Role in the experiment |
|---|---|
| Airflow $Q$ (m³/s) | Independent coordinate of the performance curve. Calculate it from nozzle differential, calibration and density. |
| Nozzle differential pressure (Pa) | Raw measurement used to calculate airflow. |
| Fan pressure (Pa) | Aerodynamic result. Define measurement planes and state whether each result is static or total. |
| Rotational speed (rpm) | Controlled operating condition; measure actual speed at each point. |
| Shaft torque (N·m) and active electrical power (W) | Record the available power input. Torque and speed give shaft power; the analyser gives electrical input. |
| Air temperature, absolute pressure and relative humidity | Inputs for air density. |
| Efficiency | Derived from airflow, fan pressure and the stated shaft or electrical power boundary. |

### 4.2 Proposed instrumentation for measuring and data acquisition

*Course references: E1 and E2.*

#### Airflow measurement

The proposal uses calibrated nozzles in an inlet chamber. The nozzle differential pressure, air density and nozzle calibration are used to determine airflow. The ISA 1932 and long-radius nozzles were considered as in-duct alternatives. A calibrated bellmouth is also a candidate for inlet measurement. A nozzle bank is proposed because the open throat area can be changed to maintain a useful pressure signal over different flow ranges.

For a first estimate using the simplified method in E3, the pressure differential across identical open nozzles is:

$$
\Delta p_n \approx \frac{\rho}{2}\left(\frac{Q}{C_d A_n}\right)^2.
$$

Here $Q$ is the volumetric airflow (m³/s), $A_n$ is the sum of the open throat areas (m²), $C_d$ is the discharge coefficient, and $\rho$ is air density (kg/m³). Trial geometry: two identical Ø400 mm throats, air density 1.20 kg/m³ and a provisional coefficient of 0.985 taken from the classroom example. This coefficient is not a calibration for the proposed nozzles. Both throats open give a total area of 0.2513 m².

| Sizing scenario | Airflow | One throat open | Two throats open |
|---|---:|---:|---:|
| Half nominal | 1.357 m³/s | 72 Pa | 18 Pa |
| Nominal reference | 2.714 m³/s | — | 72 Pa |
| 120% of nominal | 3.257 m³/s | — | 104 Pa |

The low and high flows are screening scenarios, not measured points. The nozzle differential is the measurement signal. The permanent losses of the nozzle assembly and bench must be evaluated separately to check which flows can be reached.

**[COMPLETAR]** Confirm the required flow interval, the calibrated nozzle size and available chamber space. Recalculate the differential for the selected combinations and choose the pressure range accordingly.

As an E1 screening check, three candidate throat diameters give the following signals using the same provisional coefficient and density.

| Trial throat diameter (two open) | Estimated nozzle signal at 2.714 m³/s |
|---|---:|
| 350 mm | 123 Pa |
| 400 mm | 72 Pa |
| 450 mm | 45 Pa |

Keep Ø400 mm as the baseline for the sketch. A larger throat gives a smaller pressure signal; the final choice depends on chamber space, the sensor accuracy at low pressure and the pressure losses the bench can accommodate.

#### Initial range check

The screening flows correspond to 4885, 9770 and 11 724 m³/h. These are design scenarios, not points already reached by the fan. With both Ø400 mm nozzles open, halving airflow reduces the signal by a factor of four, from about 72 Pa to 18 Pa. Opening only one nozzle at half flow restores about 72 Pa. This is why the nozzle combination must be recorded for every test point. A 0–250 Pa candidate range covers the calculated signals for these combinations, but range coverage alone does not prove that the instrument is accurate enough.

For illustration, the same 1 Pa standard uncertainty in differential pressure would contribute about 2.8% to relative airflow uncertainty at 18 Pa, and about 0.7% at 72 Pa, from the pressure term alone. Compare candidate manometers at the smallest signal expected in each combination, using the exact manufacturer's specification and the selected acquisition mode.

**[E1 — FIRST TASK]** Enter the exact range, resolution and accuracy at the relevant pressures for the proposed digital manometer. For the thermocouple, record probe and logger specifications separately. Add a datasheet page or table reference for each figure. The fan pressure channel must be selected independently once its pressure references are fixed.

#### Instruments and data recording

| Quantity | Candidate or method | Recording and selection notes |
|---|---|---|
| Nozzle differential pressure | WIKA A2G-50 with digital display; provisional 0–250 Pa configuration | Connect across the bank. Confirm variant, low-pressure accuracy, resolution and output. |
| Fan pressure | Second WIKA A2G-50 as a candidate | Select the signed range independently of the nozzle channel, once pressure taps and references are defined. |
| Air temperature | TC Direct WiFi logger with supplied Type K thermocouple | Place the probe at a representative inlet or metering section. Export time-stamped data to Excel. The probe is specified at ±1.5 °C over 0–200 °C; check the logger contribution separately. |
| Absolute air pressure and relative humidity | Laboratory barometer and hygrometer | Record both with temperature to estimate air density. Confirm equipment models and calibration. |
| Rotational speed | Testo 465 optical tachometer | Record actual rpm at each test point. Confirm access to a suitable rotating target. |
| Active electrical power | HIOKI PW3360 | Select appropriate clamps and define the electrical measurement boundary. |
| Shaft torque, if accessible | HBK T22 | Check installation space, couplings and expected torque before selecting a range. |

Keep a separate record for each stable point and repeat measurement: point ID, time, regulator setting, nozzle combination, rpm, nozzle differential, raw fan-side pressures, temperature, barometric pressure, humidity, active power and torque if measured. Use the same point ID or timestamp across instruments.

**[COMPLETAR CON EL LABORATORIO]** Add the actual model, range, resolution, accuracy, calibration and recording method for each instrument. For the pressure readings, specify either manual logging or the acquisition inputs and signal used. State where each pressure is measured and how the installation converts it into fan pressure.

#### E2 — Preliminary uncertainty assessment

Start at the nominal reference point of 2.714 m³/s at 1445 rpm. The best efficiency point is not known. Record the specification for each selected instrument and distinguish accuracy, resolution and calibration uncertainty before converting them into standard uncertainties.

| Result | Inputs to include in the uncertainty calculation |
|---|---|
| Airflow | Nozzle differential, density, throat area and discharge coefficient |
| Fan pressure | Pressure readings and, where applicable, flow, density and section area used for velocity corrections |
| Shaft power | Torque and rotational speed |
| Electrical input power | Analyzer and current clamps |
| Efficiency | Airflow, fan total pressure and selected power input |

For the trial nozzle equation, assuming independent inputs:

$$
\left(\frac{u_Q}{Q}\right)^2 =
\left(\frac{u_{C_d}}{C_d}\right)^2+
\left(\frac{u_{A_n}}{A_n}\right)^2+
\frac14\left(\frac{u_{\Delta p_n}}{\Delta p_n}\right)^2+
\frac14\left(\frac{u_\rho}{\rho}\right)^2.
$$

A hypothetical standard uncertainty of 1 Pa at a nozzle reading of 72 Pa would contribute 0.69% to relative standard uncertainty in airflow. This is a sensitivity example, not the specification of the selected sensor or the total uncertainty.

For the low-pressure approximation, air power is $P_{air}\approx Q\Delta p_t$. Shaft power is $P_{shaft}=M(2\pi n/60)$, where $M$ is torque in N·m and $n$ is speed in rpm. Use $P_{air}/P_{shaft}$ for fan efficiency or $P_{air}/P_{el}$ for overall efficiency from electrical input. Record which boundary was used. Propagate uncertainty from the raw inputs, preserving shared quantities such as airflow when it also contributes to the pressure calculation.

**[COMPLETAR E2]** Fill this table with measured or explicitly justified provisional inputs. Use the actual instrument specifications. Indicate the coverage factor if reporting expanded uncertainty.

| Result | Value at selected point | Standard uncertainty | Relative uncertainty |
|---|---|---|---|
| Airflow | 2.714 m³/s, reference | Pending | Pending |
| Fan pressure | Pending pressure definition and value | Pending | Pending |
| Input power | Pending shaft or electrical input | Pending | Pending |
| Efficiency | Pending the above inputs | Pending | Pending |

**[E2 — INPUT SHEET]** Fill in the values below at the same operating point before calculating the four uncertainties. Record the bound or calibration uncertainty from the datasheet, its units and the rule used to convert it into standard uncertainty. If pressure is reconstructed rather than measured directly, include the raw pressures and velocity-correction inputs. If power is measured electrically, include the current probes and identify the result as overall efficiency.

| Quantity or input | Value for first calculation | Source to attach |
|---|---|---|
| Nozzle differential | 72 Pa estimated for 2 × Ø400 mm | Final flowmeter geometry, calibration and pressure instrument datasheet |
| Fan total pressure rise | Pending | Defined measurement planes and pressure reduction from E3 |
| Shaft torque and speed, or electrical active power | 1445 rpm reference; power or torque pending | Actual measurement configuration and instrument datasheet |
| Air density inputs | 1.20 kg/m³ in the screening calculation | Temperature, barometric pressure and humidity instrument specifications |
| Nozzle area and coefficient | 0.2513 m² and 0.985 in the screening calculation | Actual throat dimensions and nozzle calibration |


### 4.3 Application of UNE-EN ISO 5801:2019 to the axial fan

*Course reference: E3. The test bench proposal below uses the installation example from that session.*

The preliminary arrangement follows the Category A inlet-chamber example from E3: the fan is mounted at the chamber outlet and discharges freely. This is a concept for the aerodynamic pressure–flow test requested in the course. ISO 5801's public scope refers jet fan testing to ISO 13350. If the objective includes thrust rating of the complete jet fan, agree the applicable method with the lecturer. Compliance remains to be checked against the selected installation drawing and requirements.

~~~mermaid
flowchart LR
    A["Air supply and flow control"] --> N["Calibrated nozzles"]
    N --> C["Inlet chamber"]
    C --> F["Fan at 1445 rpm"]
    F --> O["Free discharge"]
    N -. "Nozzle differential" .-> D["Airflow channel"]
    C -. "Chamber pressure relative to ambient" .-> P["Fan pressure channel"]
~~~

*Figure 1. Functional sketch, not to scale. Positions of conditioning devices, pressure taps and measurement planes remain to be checked.*

A controllable upstream air supply is proposed to vary the airflow while keeping the test fan at 1445 rpm. Its placement and flow conditioning must be checked against the selected layout. Nozzle combinations are chosen to maintain a usable measuring signal. For a comparable real installation, the [EP BTB15,000 bench](https://www.ep-e.com/en/characteristic-curve-determination/) uses nozzles and publishes a range of 150–15,000 m³/h. Its dimensions and accuracy do not transfer to this proposal.

| Item | Preliminary input | What to add to the dimensioned sketch |
|---|---|---|
| Fan connection | Ø500 mm nominal reference | Measure mounting and clear diameters on the confirmed CAD or manufacturer drawing. |
| Nozzle bank | Two Ø400 mm trial throats | Check spacing, calibrated sizes and required wall clearances. |
| Chamber | Pending | Add width, height, length and locations of conditioning elements. |
| Connecting duct or transition | Pending, if used | Add diameter, length and pressure sections. |
| Outlet | Free discharge in the proposed concept | Mark the boundary and check available clearances. |

**[COMPLETAR E3]** Add a dimensioned side view with the fan connection, nozzles, chamber, regulator, airflow arrows and pressure taps. Cite the installation drawing or clauses consulted through the UPC and identify provisional dimensions.

#### Draft drawing notes

Use a side view for the airflow path and a small front view for the nozzle plate. In the front view, label the two trial throat diameters and represent each nozzle as independently open or closed. In the side view, show the regulator or auxiliary air supply, both sides of the nozzle plate, the chamber pressure reference, the inlet temperature probe, the mounting interface and the free outlet. Keep the nozzle differential taps separate from the fan pressure measurement. The nominal Ø500 mm identifies the fan size; use the CAD or drawing to obtain the actual connection and clear flow area.

| Dimension to record | Provisional value or label | How to obtain it |
|---|---|---|
| Nozzle throat diameter and count | 2 × Ø400 mm | Check the selected calibration, chamber fit and pressure signal. |
| Nozzle centres and wall clearance | Pending | Lay out the nozzle plate and check the selected test configuration. |
| Chamber width, height and length | W, H and L pending | Show on the side and front views; justify dimensions from the layout and the available space. |
| Fan mounting and clear diameter | Pending; nominal family size Ø500 mm | Read the actual mating interface and flow section from the confirmed model. |
| Transition or connecting duct | Diameter and length pending, if used | Add only the sections required by the selected test arrangement. |

## 5. Bibliography

- Course overview: P1 *Preparing course*, Release 1 and Release 2 quality criteria. Design notebooks: D1 cell 15, D2 cell 14 and D3 cell 7. CFD notebooks: C1 *SimScale and first simulation*, C2 *Boundary layer and GCI*, C3 *Aerodynamics of airfoil in a 2D cascade*.
- Course notebooks: E1 *Measurement of magnitudes*, cell 37; E2 *Uncertainty Management*, cell 34; E3 *UNE-EN ISO 5801:2019*, cells 3–6 and 9.
- Group documents: *Analisis_ventilador_axial_SODECA_dos_velocidades*, Sections 1–2; *Predimensionamiento_axial_SODECA_1445_2915_editable*, Sections 1 and 4–7. **[AÑADIR]** Link the group's final Design section and the catalogue row for the confirmed SODECA variant.
- [ISO 5801 public scope](https://www.iso.org/standard/56517.html); [ISO 13350 public scope](https://www.iso.org/standard/62033.html).
- [WIKA A2G-50 instructions](https://www.wika.com/media/Operating-instructions/Operating-instructions/Pressure/Pressure-sensors/oi_a2g_50_en_de.pdf); [TC Direct Type K probe and WiFi logger](https://www.tcdirect.co.uk/product-2-130-97/WiFi-Temperature-Data-Logger-with-Thermocouple).
- [Testo 465](https://www.testo.com/en-UK/testo-465/p/0563-0465); [HIOKI PW3360](https://www.hioki.com/global/products/pqa/power-loggers/id_5822); [HBK T22](https://www.hbkworld.com/es/products/transducers/torque/rotating/t22).

## 6. Completion checklist

| Who | What to complete before submission |
|---|---|
| Group | Confirm SODECA variant, test article and main operating point; link the matching catalogue and CAD. |
| Design | Insert existing diagrams and calculations, reconcile D1 and D2 assumptions, confirm the profile and chord, and document geometry and materials. |
| CFD | Insert the actual CAD/domain, mesh, boundary conditions and preliminary simulation evidence. |
| Experimentation | Select the instrument configurations from E1, document the proposed E3 layout with dimensions, and use these to complete E2. |

Remove the bracketed work notes after resolving them.
