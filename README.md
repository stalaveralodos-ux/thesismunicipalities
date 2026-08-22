<p align="center">
  <img src="./assets/banner.svg" alt="Municipal Social Rights Lab" width="100%">
</p>

<p align="center">
  <em>An open research infrastructure operationalising a comparative constitutional study of Turin, Barcelona, and Athens.</em>
</p>

---

## About

The Municipal Social Rights Lab turns a doctoral thesis on the constitutional role of municipalities in the governance of social rights into a transferable, reproducible research infrastructure. It is built on *The Constitutional Role of Municipalities in the Governance of Social Rights: A Comparative Study of Turin, Barcelona, and Athens* (Silvia Talavera Lodos, Sant'Anna, 2026).

The thesis develops a commitment-impact framework that separates what a municipality is legally and fiscally able to do, what it actually attempts, and what residents experience in practice through coverage, accessibility, and inclusion. This project keeps that separation intact. It is not a city ranking. It is a measurement framework for studying how constitutional design shapes the local realisation of education, health, and housing rights, built to extend beyond the original three cities once validated.

## Scope

The unit of analysis is City × Right × Year, which allows the project to grow over time and across cities rather than reducing any single city to one static score. Every indicator distinguishes what the thesis establishes empirically from what this project proposes as an extension still awaiting validation, and every observation carries its evidence trail: source, year, evidence type, and confidence.

## Current phase

The project is in Phase 0, evidence extraction. Before any code or dashboard, the thesis itself is being read chapter by chapter to build a structured evidence table and an indicator codebook grounded in what the source material actually says. Progress so far covers the conceptual framework, the full comparative discussion of constitutional capacity across the three cities, and the closing synthesis for all nine city-right combinations. What remains is documented openly in the methodology notes rather than assumed complete.

## Repository structure

```
municipal-social-rights-lab/
├── README.md
├── assets/
│   └── banner.svg
├── data/
│   └── metadata/
│       └── indicator-codebook-phase0.csv
├── methodology/
│   ├── evidence-extraction-phase0.md
│   ├── conceptual-framework.md
│   ├── indicator-codebook.md
│   └── evidence-protocol.md
├── src/
├── notebooks/
└── docs/
```

Folders shown without a file yet are placeholders for the phases ahead and will fill in as the codebook and data model stabilise.

## Working principles

A weight is never assigned without a sensitivity check attached to it. A missing value is flagged, never guessed. A proposed extension is labelled as such until it survives replication against the thesis cases, and only then is it treated as load-bearing. Qualitative coding stays visible rather than hidden behind a single number, since most of the underlying evidence is documentary and interpretive rather than a clean statistical series.

## Citation

If you use this project or its dataset, please cite the underlying thesis alongside the repository itself. A `CITATION.cff` file will be added once the Phase 3 dataset is published.

## License

To be confirmed on first public data release.

---

<p align="center"><sub>Municipal Social Rights Lab &middot; by Silvia Talavera Lodos</sub></p>
