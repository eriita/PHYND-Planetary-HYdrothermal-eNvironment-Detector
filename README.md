# PHYND — Planetary HYdrothermal eNvironment Detector

PHYND is a Python- and Google Colab–based analysis tool for detecting and
characterizing low‑ and high‑temperature mineral assemblages in CRISM
hyperspectral data from Mars. The tool is designed to identify spatially
coherent alteration assemblages in impact crater settings, where mineralogy
may reflect low‑temperature aqueous alteration, burial diagenesis, or
impact‑generated hydrothermal processes.


## Scientific motivation

Low‑temperature assemblages are characterized by combinations of H₂O, OH
overtone, and Al‑, Fe‑, and Mg‑OH absorptions diagnostic of smectite minerals
such as **montmorillonite**, **nontronite**, and **saponite**. High‑temperature
assemblages are characterized by broader Fe/Mg‑OH absorption basins and
associated OH features consistent with **chlorite‑**, **illite‑**,
**prehnite‑**, and **epidote‑bearing** alteration.

Composite band‑depth images (post atmospheric correction) are constructed for
each assemblage type to improve robustness to noise and sub‑pixel mixing at
CRISM spectral and spatial resolution. The low‑ and high‑temperature
classifications refer to inferred formation conditions of mineral assemblages,
rather than to individual absorption band chemistry alone.


## Method overview

PHYND combines physically and statistically motivated spectral metrics with
spatial context to identify candidate alteration assemblages. The tool outputs:

- Multiple diagnostic band‑depth maps relevant to both low‑temperature and
  high‑temperature assemblages.
- Composite band‑depth images representing the average spectral response of
  each assemblage type.
- A normalized difference index highlighting the relative dominance of
  high‑ versus low‑temperature assemblages relative to neutral background
  mineralogy.
- Pixel‑scale segmentation identifying pixels likely to contain
  high‑temperature assemblages, performed using combined absolute and
  background‑relative thresholds.
- Mean spectral profiles of segmented pixels and automated absorption‑feature
  analysis applied post‑segmentation to characterize diagnostic spectral
  features.

No unique mineral identification beyond CRISM spectral resolving capability is
attempted; results are intended to identify mineral assemblage classes and
their spatial context.

