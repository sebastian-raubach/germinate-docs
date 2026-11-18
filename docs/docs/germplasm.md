---
layout: doc
title: Germplasm & Passport Data
subtitle: Managing accessions, pedigrees, taxonomy, and MCPD standards.
---

Germinate stores core plant material records following the **Multi-Crop Passport Descriptors (MCPD)** standard.

## Key Concepts

* **Accession (Germplasm):** The primary unit representing a distinct cultivar, breeding line, landrace, or wild relative.
* **Taxonomy:** Hierarchical classification covering Genus, Species, and Subtaxa.
* **Biological Status:** Categorizes material using standard FAO/Bioversity codes (e.g., `100` Wild, `300` Traditional cultivar/landrace, `400` Breeding/research material).

## Pedigree Management

Germinate supports parent-child relationships (`parent_id` and `child_id`) to track crosses and breeding histories.

1. Define maternal and paternal accessions in the Germplasm table.
2. Link relationships via the **Pedigree** import template.
3. Inspect multi-generation lineages using the interactive pedigree viewer.
