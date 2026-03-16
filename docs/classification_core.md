
# Classification core

## General idea

This document contains the central classification logic of the step-bunching program.

The classification is based on the behavior of the minimal step-step distance inside a bunch, denoted by \( l_{min} \), when the number of steps in the bunch \( N \) increases.

This criterion leads to two major types of step bunching:

- **B1-type**
- **B2-type**

The distinction is not merely descriptive. It determines how bunching should be monitored, how scaling should be interpreted, and how theoretical and experimental systems should be grouped.

## Defining criterion

The classification can be summarized as follows:

- **B1-type**: when \( N \) increases, the minimal step-step distance in the bunch \( l_{min} \) remains approximately constant.
- **B2-type**: when \( N \) increases, the minimal step-step distance in the bunch \( l_{min} \) decreases.

This difference immediately implies a second one:

- **B1-type** requires **one characteristic length scale**.
- **B2-type** requires **two characteristic length scales**. :contentReference[oaicite:2]{index=2}

## Why this classification matters

The classification is important because it organizes a wide family of step-bunching phenomena that had previously been studied in partially disconnected ways.

It also provides a common language for:

- numerical modeling,
- scaling analysis,
- comparison between different theoretical models,
- and direct comparison between calculations and experiments.

## Monitoring as the operational core

A central feature of the classification program is the use of **two monitoring schemes** running simultaneously.

### MS-I: time evolution monitoring

MS-I is designed to follow the temporal evolution of the system.

Typical quantities include:

- number of bunches,
- average number of steps in a bunch \( N \),
- average bunch width \( L_b \),
- average terrace width between bunches \( TW \),
- global minimal step-step distance in the system \( l_{min,g} \).

### MS-II: size-dependent monitoring

MS-II accumulates information for each bunch size.

Typical quantities include:

- bunch width \( L_b \),
- minimal step-step distance in the bunch \( l_{min} \),
- first step-step distance \( l_1 \),
- last step-step distance \( l_{last} \). :contentReference[oaicite:5]{index=5}

### Why the two schemes matter together

The combination of MS-I and MS-II is not redundant.

Their agreement for matching dependencies is considered a non-trivial mutual validation of the monitoring procedure. Even more importantly, the same pair of schemes can be used to organize experimental data in the same coordinates as numerical results, making direct comparison possible. :contentReference[oaicite:6]{index=6}

This is one of the deepest strengths of the step-bunching program: monitoring is not an auxiliary add-on, but part of the scientific core.

## B1-type

### Defining property

For B1-type bunching, \( l_{min} \) does not change with increasing bunch size \( N \).

### Main consequence

Only one characteristic length scale is needed to describe the bunching process. :contentReference[oaicite:7]{index=7}

### Example used in the classification paper

The TE-model is used as a representative B1-type case. In that model:

- the slope does not change with increasing bunch size,
- the slope does not change in time,
- and the same time-scaling exponent is found for several quantities such as \( N \), \( TW \), and \( L_b \).

### Experimental examples mentioned

Examples of systems showing B1-type behavior include:

- Si(113),
- high-temperature annealing of TaC(910),
- vicinal Ag(111) in electrolyte. :contentReference[oaicite:9]{index=9}

## B2-type

### Defining property

For B2-type bunching, \( l_{min} \) decreases with increasing bunch size \( N \).

### Main consequence

Two characteristic length scales are needed to describe the bunching process. :contentReference[oaicite:10]{index=10}

### Example used in the classification paper

The EvEm-model is used as a representative B2-type case. In that model:

- the bunch with more steps has higher slope,
- \( l_{min} \), \( l_1 \), and \( l_{last} \) exhibit nontrivial size scaling,
- and the time evolution carries more structure than in the B1-type case.

### Experimental examples mentioned

Examples of systems showing B2-type behavior include:

- evaporating Si(111) vicinals,
- KDP crystal growth,
- SiC epitaxial growth, although in the latter a careful analysis may also reveal B1-type aspects. :contentReference[oaicite:12]{index=12}

## Programmatic meaning

The B1/B2 classification is not just a way to label plots after the fact.

It provides:

- a unifying criterion across different models,
- a way to structure monitoring,
- a framework for scaling interpretation,
- and a bridge between theory, numerics, and experiment.

This is why the classification should stand near the center of the repository architecture.

## Future development

The classification framework also points toward further work.

Among the directions explicitly indicated in the 2012 paper are:

- determining the exact time-scaling of \( N \) for available B1-type models,
- systematic studies of additional B2-type models,
- and exploration of cases that may lead to what is called **B2m-type**, i.e. simultaneous bunching and meandering. :contentReference[oaicite:13]{index=13}

In this sense, the classification is not only a summary of past work, but a generator of future research directions.
