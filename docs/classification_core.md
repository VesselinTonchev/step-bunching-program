
# Classification core

## General idea

The central organizing principle of the present step-bunching program is the distinction between two major types of step bunching:

- **B1-type**
- **B2-type**

The classification is based on the behavior of the **minimal step-step distance inside the bunch**, denoted by \( l_{min} \), when the number of steps in the bunch \( N \) increases. :contentReference[oaicite:0]{index=0}

## Defining criterion

The classification can be stated in its simplest form as follows:

- **B1-type:** when the bunch size \( N \) increases, the minimal step-step distance \( l_{min} \) remains approximately constant.
- **B2-type:** when the bunch size \( N \) increases, the minimal step-step distance \( l_{min} \) decreases.

This immediately leads to the next essential distinction:

- **B1-type** requires **one characteristic length scale**
- **B2-type** requires **two characteristic length scales**

## Why this classification matters

This classification is not just a naming convention. It provides:

- a unifying language across different theoretical models,
- a criterion for grouping experimental systems,
- a basis for scaling analysis,
- and a framework for monitoring the evolution of bunches in a systematic way. :contentReference[oaicite:3]{index=3}

In this sense, the classification is one of the conceptual cores of the whole step-bunching program.

## Monitoring as the operational core

The classification is inseparable from the use of two simultaneous monitoring schemes.

### MS-I: time-evolution monitoring

MS-I follows the evolution of the system in time and records quantities such as:

- number of bunches,
- average number of steps in a bunch \( N \),
- bunch width \( L_b \),
- terrace width between bunches \( TW \),
- global minimal step-step distance in the system \( l_{min,g} \). :contentReference[oaicite:4]{index=4}

### MS-II: size-dependent monitoring

MS-II accumulates information for bunches of different sizes and records quantities such as:

- bunch width \( L_b \),
- minimal bunch distance \( l_{min} \),
- first bunch distance \( l_1 \),
- last bunch distance \( l_{last} \). :contentReference[oaicite:5]{index=5}

### Why the two schemes matter together

The combination of MS-I and MS-II is not redundant. Their agreement for overlapping dependencies is treated as a non-trivial mutual validation of the monitoring procedure. Moreover, the same pair of schemes can be used to organize experimental data in the same coordinates as numerical results, enabling direct comparison. :contentReference[oaicite:6]{index=6}

This is why monitoring in the step-bunching program is not an auxiliary tool, but a central methodological achievement.

## B1-type

### Defining property

In B1-type bunching, \( l_{min} \) is not a function of the bunch size \( N \). :contentReference[oaicite:7]{index=7}

### Main implication

Only **one characteristic length scale** is needed to describe the bunching process. :contentReference[oaicite:8]{index=8}

### Representative model

In the 2012 classification paper, the **TE-model** is used as the representative B1-type case. In this model:

- the slope does not change with increasing bunch size,
- the slope does not change in time,
- and one common time-scaling exponent is found for several key quantities.

### Experimental examples mentioned

Examples of B1-type behavior mentioned in the paper include:

- Si(113),
- high-temperature annealing of TaC(910),
- vicinal Ag(111) in electrolyte. :contentReference[oaicite:10]{index=10}

## B2-type

### Defining property

In B2-type bunching, \( l_{min} \) decreases when the bunch size \( N \) increases.

### Main implication

Two characteristic length scales are required to describe the process. :contentReference[oaicite:12]{index=12}

### Representative model

In the 2012 classification paper, the **EvEm-model** is used as the representative B2-type case. There:

- the bunch slope increases with bunch size,
- \( l_{min} \), \( l_1 \), and \( l_{last} \) show distinct size scaling,
- and the time evolution is richer than in the B1-type case.

### Experimental examples mentioned

Examples of B2-type systems mentioned in the paper include:

- evaporating Si(111) vicinals,
- KDP crystal growth,
- SiC epitaxial growth, although the latter may also show more complex behavior after detailed analysis. :contentReference[oaicite:14]{index=14}

## Programmatic meaning

The B1/B2 distinction is not only a summary of already known results. It provides a way to structure the whole field:

- models,
- observables,
- scaling laws,
- experiment–theory comparison,
- and future numerical work.

Because of this, the classification should stand near the center of the repository architecture.

## Future extensions already indicated in the 2012 paper

The classification framework also points toward further work, including:

- determining the exact time-scaling of \( N \) for available B1-type models,
- systematic studies of additional B2-type models,
- and the exploration of **B2m-type**, i.e. simultaneous bunching and meandering.

## Closing formulation

In its most compact form, the classification can be expressed as follows:

- **B1-type:** \( l_{min} = \mathrm{const} \) with increasing \( N \) → **one length scale**
- **B2-type:** \( l_{min} \downarrow \) with increasing \( N \) → **two length scales**

This is the conceptual core around which the broader step-bunching program can be organized.
