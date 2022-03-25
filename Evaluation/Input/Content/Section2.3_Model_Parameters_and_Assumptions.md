### 2.3.1 Absorption

Particle dissolution for the formulation has been selected.

### 2.3.2 Distribution

Physico-chemical parameters were set to the reported values (see [Section 2.2.1](#221-in-vitro-and-physico-chemical-data)). It was assumed that the major binding partner in plasma is albumin.

After testing the available organ-plasma partition coefficient and cell permeability calculation methods available in PK-Sim, observed clinical data were best described by choosing the partition coefficient calculation by `Rodgers and Rowland` and cellular permeability calculation by `PK-Sim Standard`.

### 2.3.3 Metabolism and Elimination

Two metabolic pathways were implement in the model:

* Saturable CYP2C19 mediated metabolization.
* Linear FMO mediated to account for lumped non-CYP metabolization.

Data after repeated dosing indicates some sort of time-dependent elimination. The addition of an inhibitory metabolite may be an explanation. However, it would be very challenging to incorporate the kinetics of such a metabolite in the existing model, taking into account that no data on IC50 or Ki are available for such a metabolite. Therefore, it was decided to account for the time-dependency by simply including a time-dependent autoinhibition on CYP2C19 enzyme system.

Given the available data, the parameters Kinact and Kinact_half defining the time-dependent autoinhibition could not be estimated together (not separately identifiable). Assuming Kinact is enzyme but not substance specific, it was decided to fix Kinact to the value reported by [Wu 2014](#5-references) for omeprazole and only estimate Kinact_half.

### 2.3.4 Automated Parameter Identification

Following parameter values were estimated for the base model:

- Km_2C19

- Vmax_2C19

- Intrinsic Clearance FMO (i.e. non CYP2C19 metabolism)

- Kinact<sub>half</sub> CYP2C19 for time-dependent autoinhibition
