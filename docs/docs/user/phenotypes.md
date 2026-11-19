---
layout: doc
title: Phenotypic & Trial Data
subtitle: Organizing multi-environment field trials, traits, and observations.
---

Phenotypic data captures observable characteristics measured across field trials, glasshouses, or growth chambers.

## Data Hierarchy

* **Datasets:** Groupings of trial observations collected within a specific experiment or season.
* **Locations:** Geographic sites with latitude, longitude, elevation, and country metadata.
* **Traits:** Standardized definitions including trait name, short name, data type (`numeric`, `categorical`, `date`, `text`), and measurement units.

## Recording Observations

Each observation links a **Germplasm accession**, a **Trait**, a **Location**, and a **Timestamp**. Germinate supports both raw plot-level measurements and summarized accession means.
