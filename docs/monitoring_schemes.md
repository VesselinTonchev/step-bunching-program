
# Monitoring schemes

## General note

Monitoring schemes are one of the methodological cores of the step-bunching program.

They are not an auxiliary plotting layer added after the simulation, but a structured way of extracting physically meaningful information from the evolution of the vicinal surface.

In the present repository, the monitoring logic is based mainly on the formulation introduced in the study of the **C+–C− model**, where two simultaneous monitoring schemes were used to analyze the bunching process in detail. Although that paper is mainly focused on a **B2-type** case, the same monitoring logic is in principle applicable to **B1-type** systems as well. :contentReference[oaicite:1]{index=1}

## Why monitoring is central

The step-bunching problem is not exhausted by integrating equations of motion and plotting step trajectories.

To characterize the bunching process in a systematic way, one must monitor:

- how bunches form and evolve in time,
- how bunch properties depend on bunch size,
- where the minimal interstep distance appears,
- how bunch width scales,
- and how numerical results can be compared directly with experimental measurements.

This is why monitoring stands at the junction of:

- simulation,
- scaling analysis,
- classification,
- and experiment–theory comparison. :contentReference[oaicite:2]{index=2}

## Defining bunches and terraces

Before the monitoring schemes are defined, one must decide how to distinguish a bunch from a terrace.

A natural criterion is used in the C+–C− study:

> if the distance between two neighboring steps is smaller than the initial vicinal distance, this is a **bunch distance**.

This criterion provides the operational basis for identifying:

- the beginning of a bunch,
- the end of a bunch,
- the terrace between bunches,
- and the quantities that should be recorded. :contentReference[oaicite:3]{index=3}

## Monitoring Scheme I (MS-I)

### Character

MS-I is a **snapshot monitoring scheme**.

It collects information from the current surface profile at fixed moments in time and is therefore designed to follow the **time evolution** of the instability. This is illustrated in Fig. 3a of the 2010 paper. :contentReference[oaicite:4]{index=4}

### Main quantities

Typical quantities recorded by MS-I are:

- number of bunches,
- average bunch size \( N \),
- average bunch width \( L_b \),
- average interstep distance in the bunch,
- minimal interstep distance in the entire step system,
- average terrace width,
- average distance between steps on a terrace. :contentReference[oaicite:5]{index=5}

### Operational logic

The code proceeds through the list of step-step distances and:

1. identifies distances smaller than the initial vicinal distance,
2. groups adjacent such distances into the same bunch,
3. identifies the end of the bunch when a larger distance appears,
4. identifies terraces as regions of larger distances between bunches.

Thus MS-I gives a sequence of time-stamped measurements of the evolving bunched vicinal surface. :contentReference[oaicite:6]{index=6}

### Main role

MS-I is the natural scheme for obtaining:

- time scaling of bunch size,
- time scaling of bunch width,
- evolution of terrace width,
- and global dynamical trends in the bunching process. :contentReference[oaicite:7]{index=7}

## Monitoring Scheme II (MS-II)

### Character

MS-II is a **cumulative monitoring scheme**.

Instead of focusing only on the current time snapshot, it accumulates information for all bunches of a given size \( N \) encountered during the whole integration time. Again, this is illustrated schematically in Fig. 3a of the 2010 paper. :contentReference[oaicite:8]{index=8}

### Main quantities

Typical quantities recorded by MS-II are:

- bunch width \( L_b \),
- minimal bunch distance \( l_{min} \),
- first bunch distance \( l_1 \),
- last bunch distance \( l_{last} \). :contentReference[oaicite:9]{index=9}

### Operational logic

Whenever a bunch with a given size \( N \) is encountered during the simulation:

- the corresponding quantities are updated,
- their averages for this bunch size are stored,
- and the process continues cumulatively through the whole run. :contentReference[oaicite:10]{index=10}

### Main role

MS-II is the natural scheme for obtaining:

- size scaling of \( L_b \),
- size scaling of \( l_{min} \),
- the behavior of \( l_1 \) and \( l_{last} \),
- and other bunch-size-dependent quantities.

This makes MS-II particularly important for classification and universality analysis. :contentReference[oaicite:11]{index=11}

## Why the two schemes must run simultaneously

The simultaneous use of MS-I and MS-II is one of the strongest methodological ideas of the step-bunching program.

Their roles are different but complementary:

- **MS-I** gives the time evolution of the bunching process,
- **MS-II** gives the dependence of bunch properties on bunch size.

The agreement of the two schemes for overlapping dependencies is not trivial and serves as a mutual validation of the monitoring procedure. In the 2010 paper this equivalence is explicitly emphasized, for example in the discussion around Fig. 4. :contentReference[oaicite:12]{index=12}

Thus the two monitoring schemes are not redundant duplicates, but two coordinated views of the same evolving system.

## Quantities monitored in practice

The 2010 paper, especially around Fig. 3b, makes clear which geometrical quantities are central:

- initial vicinal distance \( l \),
- step height \( h_0 \),
- bunch size \( N \),
- bunch width \( L_b \),
- minimal bunch distance \( l_{min} \),
- terrace width between bunches,
- first and last bunch distances \( l_1 \) and \( l_{last} \). :contentReference[oaicite:13]{index=13}

These quantities should be regarded as the basic monitored observables in the repository.

## Relation to B2-type bunching

The C+–C− model is a representative **B2-type** case.

Its monitoring reveals a characteristic B2 signature:

- the minimal bunch distance decreases with increasing bunch size,
- and the minimal interstep distance appears at the **beginning (trailing edge)** of the bunch rather than in the middle. :contentReference[oaicite:14]{index=14}

This is one of the reasons why the 2010 paper is especially useful as a template for monitoring logic in the B2 domain.

## Applicability to B1-type bunching

Although the monitoring framework was developed in a B2-oriented context, the same two schemes can also be applied to **B1-type** systems.

In that case the diagnostic outcome differs:

- \( l_{min} \) does not decrease with increasing bunch size,
- one characteristic length scale is sufficient,
- and the monitored size-scaling relations reflect B1-type behavior rather than B2-type behavior.

Thus the same monitoring architecture can serve both classes, while the resulting dependencies distinguish between them.

## Relation to experiment

A major strength of the monitoring schemes is that they are not limited to numerical integration.

The same monitored quantities can be organized in the same coordinates for experimental data, enabling direct comparison between:

- simulation and experiment,
- model class and measured morphology,
- and scaling predictions and observed bunch behavior. :contentReference[oaicite:15]{index=15}

This is one of the main reasons why monitoring in the step-bunching program should be treated as a core scientific layer, not merely as a computational convenience.

## Programmatic meaning

Within this repository, the monitoring schemes should be understood as:

- a bridge between dynamics and scaling,
- a bridge between classification and numerics,
- a bridge between numerics and experiment,
- and one of the most reusable methodological assets of the whole step-bunching line.

## Practical direction for this repository

The future implementation work in this repository should therefore aim at:

1. implementing MS-I in a modern, reusable form,
2. implementing MS-II in a modern, reusable form,
3. making their outputs directly comparable,
4. enabling plotting templates for both schemes,
5. and preparing the same monitoring layer for both B1-type and B2-type systems.

## Closing statement

The monitoring schemes introduced in the 2010 C+–C− study should be regarded as one of the central methodological achievements of the step-bunching program.

Even though they were developed in a B2-type context, they provide a general framework for structuring the bunching process and are therefore suitable as a shared monitoring backbone across the broader step-bunching domain. :contentReference[oaicite:16]{index=16}
