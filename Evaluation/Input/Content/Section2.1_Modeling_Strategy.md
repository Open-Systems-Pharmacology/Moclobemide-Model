The general workflow for building an adult PBPK model has been described by Kuepfer et al. ([Kuepfer 2016](#5-references)). Relevant information on the anthropometry (height, weight) was gathered from the respective clinical study, if reported. Information on physiological parameters (e.g. blood flows, organ volumes, hematocrit) in adults was gathered from the literature and has been incorporated in PK-Sim® as described previously ([Willmann 2007](#5-references)). The  applied activity and variability of plasma proteins and active processes that are integrated into PK-Sim® are described in the publicly available 'PK-Sim® Ontogeny Database Version 7.3' ([PK-Sim Ontogeny Database Version 7.3](#5-references)).

In general, the following step-wise workflow was followed:

1. Fit total hepatic CL as a placeholder using single dose i.v. (50 mg ([Raaflaub 1984](#5-references)) and 150 mg ([Schoerlin 1987](#5-references))) data with renal clearance fixed to 0.034 ml/min/kg as derived from [Schoerlin 1987](#5-references) to select the appropriate distribution (i.e. partition coefficient) model.
2. Estimate the contribution of non-CYP2C19 mediated metabolism using data (p.o.) from CYP2C19 poor metabolizers (PM) ([Yu 2001](#5-references), [Gram 1995](#5-references)). This pathway is assumed to be mainly attributed to FMO (flavin-containing monooxygenase) – however, also other unspecific CL would be captured here. An Asian individual was used for simulations of data reported by [Yu 2001](#5-references).
3. Use single dose data (i.v. and p.o.) to estimate Vmax and Km of CYP2C19.
4. Predict concentrations after multiple oral dosing and compare to literature. Steady state levels were not predicted very well, and the model was refined by including time-dependent auto-inhibition to account for a change in CL over time.
5. Predict single and multiple doses profiles (both i.v. and p.o.) with the updated model and compare to published profiles. Qualify model by comparing predicted CL/F and Cmax to the corresponding parameters in a review across multiple studies. Population prediction to verify the variability components of the model.

A typical European male subject (age = 30 years, weight = 73 kg, height = 176 cm, BMI = 23.57 kg/m2) was created in PKsim using the predefined database “European (ICRP, 2002)”, by adding CYP2C19 ( PK-Sim RT PCR database) and FMO (other) expression and used in simulations, until stated otherwise. For simulations of Asian subjects, a typical Asian individual (Age = 30 y, weight = 60.03 kg, height = 169.96 cm, BMI = 20.78 kg/m2) was created from the predefined database “Asian (Tanaka, 1996)” by adding CYP2C19 ( PK-Sim RT PCR database) and FMO (other) expression.

For simulations of the [Ignjatovic 2009](#5-references) data set, a typical European female subject (Age = 30 years,
weight = 64 kg, height = 163 cm, BMI = 24.09 kg/m2) was created from the predefined
database “European (ICRP, 2002)” by adding CYP2C19 ( PK-Sim RT PCR database) and FMO (other) expression.

Initially, attempts were made to also unravel the contribution of the FMO3-specific clearance pathway and the unspecific pathway using the in vitro FMO-CL of moclobemide in a microsomal assay reported by [Hoskins 2001](#5-references). However, this route was abandoned as predictions were not in line with observations, potentially requiring the need for an in vivo - in vitro scaling factor. For the purpose of DDI predictions, the details of the CYP2C19 pathway only were considered relevant.

Population simulations were carried out to evaluate if the variability incorporated in the model matches the literature reports. A population of 2000 Asian subjects with age and weight in the same range as reported by [Yu 2001](#5-references) (age: 20-36 years, weight: 40-120 kg, 13% female) was generated, and the concentration time profile following a single dose of 300 mg p.o. was simulated for each virtual subject and summarized as mean +/- SD. The simulation was also performed for CYP2C19 poor metabolizers.

Details about input data (physicochemical, *in vitro* and clinical) can be found in [Section 2.2](#22-data).

Details about the structural model and its parameters can be found in [Section 2.3](#23-model-parameters-and-assumptions).
