---
layout: doc
title: Phenotypic & Trial Data
subtitle: Organizing multi-environment field trials, traits, and observations.
---

Phenotypic data captures observable characteristics measured across field trials, glasshouses, or growth chambers.

## Data Hierarchy

* **Datasets**: Groupings of trial observations collected within a specific experiment or season.
* **Locations**: Geographic sites with latitude, longitude, elevation, and country metadata.
* **Traits/Variables**: Standardized definitions including trait name, short name, data type (`numeric`, `categorical`, `date`, `text`), and measurement units.

## Observation Variables

In agricultural and breeding data standards, an **observation variable** defines a recorded measurement unambiguously by pairing three components: the **trait** (the biological characteristic, quality, or behavior being evaluated, such as plant height or fruit firmness), the **method** (the specific procedure, instrument, or protocol used to measure or score it, such as a ruler at maturity or a penetrometer), and the **scale** (the valid units, numeric range, or categorical scoring system used to express the result, such as centimeters or a 1–9 visual severity scale). Combining all three prevents ambiguous data - ensuring that values collected across different trials, teams, years, or breeding databases mean the exact same thing and can be reliably compared or analyzed together.

Since v5, Germinate supports ontology-based observation variables with the distinction of trait, method and scale.

![Observation Variables Overview table]({{ '/assets/images/phenotypic/variables.png' | relative_url }})
<p class="image-caption" markdown="1">Observation Variables Overview table: The main table showing observation variables (called traits) pre-filtered to show `Phenological` traits, with `Estimation` methods and `Date` scales.</p>

### Visualizations for Variables

There are various ways in which data can be visualized from a variable's point of view. The main differentiating factor between the visualizations is the scale's data type. Numerical and date-based variable values are visualized in a different way (box plots) to categorical or text-based variables (bar charts). In either case, there are various ways in which you can break the data shown in the chart down. Examples of these are:

- **Datasets**: When data for a variable has been recorded in multiple datasets, the chart can show the data points from each dataset to more easily compare them.
- **Germplasm**: Often it's useful to highlight the data points from a selection of germplasm entries against the rest of the data. Select any number of germplasm entries to highlight.
- **Plots**: Plots break the germplasm selection down even further by letting you select the individual observation units for each germplasm.
- **Groups**: Groups highlight pre-defined subsets of germplasm.
- **Years**: For a temporal context, data can be broken down by year of recording which lets you see developments/differences over time.
- **Taxonomies**: When working with multiple subtaxa of a specific crop or even completely different genera, these can be selected as highlights.
- **Reps**: Differences between replicates within a trial can highlight interesting insights.
- **Treatments**: The main reason for the application of different treatmens within a trial is to see the effect each treatment has on the result. Select any number of treatments to see how their data differs.

![Observation Variables Data]({{ '/assets/images/phenotypic/trait-boxplot.png' | relative_url }})
<p class="image-caption" markdown="1">Observation Variables Data: Visualization showing observation values for the variable `Plant height`. The boxplot breaks the data points down by replicate (`1` and `2`) as well as showing the overall combined data.</p>

![Observation Variables Data]({{ '/assets/images/phenotypic/trait-boxplot2.png' | relative_url }})
<p class="image-caption" markdown="1">Observation Variables Data: Another example showing the variable-specific boxplots. This time, the year of recording is used to break the points down into separate boxes.</p>

![Observation Variables Data Highlight]({{ '/assets/images/phenotypic/trait-boxplot-highlight.png' | relative_url }})
<p class="image-caption" markdown="1">Observation Variables Data Highlight: The `Highlight items` selector lets you pick how to break down the chart data.</p>

## Recording Observations

Each observation links the following entries:

- **Germplasm**: The entry in Germinate for which this phenotypic observation was recorded.
- **Variable**: The ontology variable (trait + method + scale) that was used to record this measurement.
- **Dataset**: The dataset/study this observation is part of. This includes information about the trial site, associated individuals, general trial information, and linked data resources.
- **Replicate**: The replicate this observation was taken from (defaults to 1).
- **Block**: The block this observation was taken from.
- **Treatment**: The treatment that may have been applied to the observation unit (e.g. low/high nitrogen, drought, etc.).
- **Timestamp**: The exact time point when the measurement was taken.
- **Layout position**: Row, column, and potentially GPS coordinates associated with the observation unit.
