# PHYND — Planetary HYdrothermal eNvironment Detector

PHYND is a Python- and Google Colab–based analysis tool for detecting and
characterizing low‑ and high‑temperature mineral assemblages in CRISM
hyperspectral data from Mars. The tool is designed to identify spatially
coherent alteration assemblages in impact crater settings, where mineralogy
may reflect low‑temperature aqueous alteration, burial diagenesis, or
impact‑generated hydrothermal processes.


## Scientific motivation

Low‑temperature assemblages are characterized by endmember smectite minerals
such as **montmorillonite**, **nontronite**, and **saponite**. High‑temperature
assemblages are characterized by endmember **chlorite‑**, **illite‑**,
**prehnite‑**, and **epidote‑bearing** alteration.

Composite band‑depth images (post atmospheric correction) are constructed for
each assemblage type to improve robustness to noise and sub‑pixel mixing at
CRISM spectral and spatial resolution. The low‑ and high‑temperature assemblage
classifications refer to inferred formation conditions of mineral assemblages,
rather than to individual absorption band chemistry or unique mineral identificaion.


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
attempted; results are intended to identify mineral assemblage-level temperature classes and
their spatial context, supporting interpretation of alteration processes within impact crater envrionments.

