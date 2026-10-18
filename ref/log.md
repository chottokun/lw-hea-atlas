# Change Log

This file tracks all additions, modifications, and updates to the Lightweight High-Entropy Alloy (LW-HEA) Open Knowledge Format (OKF) knowledge bundle.

## [4.1.0] - 2026-10-18
### Added
- **Dynamic Extreme Environments Expansion (+2 sources, Total 819 items)**:
  - Added `SRC-815` (`10.3390/hydrogen3020016`): Hydride formation and hydrogen embrittlement risk in Ti-V-Cr-Zr-Nb refractory BCC alloys, proving the critical role of Al/Si in blocking hydrogen permeation.
  - Added `SRC-816` (`10.1016/j.actamat.2023.119490`): Repassivation kinetics and tribocorrosion resistance in multi-principal element alloys, validating ultrafast passive film recovery driven by high valve-metal content (Ti, Cr, Al, Nb).

## [4.0.0] - 2026-10-18
### Added
- **Science Plugin Advanced Passivation & Experimental Benchmark Expansion (Total 817 items)**:
  - Added `SRC-813` (`10.3390/ma16072922`): Experimental validation of $\text{AlCrTiV}_{0.5}$ achieving $I_{\text{corr}} = 0.131\text{ }\mu\text{A/cm}^2$ ($\log_{10} I_{\text{corr}} \approx -6.88$) in 0.6 M NaCl and demonstration of micro-galvanic coupling degradation by Cu segregation.
  - Added `SRC-814` (`10.1016/j.jmrt.2020.10.002`): Point Defect Model (PDM) electronic structure analysis showing n-type $\text{Al}_2\text{O}_3$ donor defect proliferation and its electrochemical compensation by p-type $\text{Cr}_2\text{O}_3$ and dielectric $\text{TiO}_2/\text{SiO}_2$ passivating network.
- **Physical Model & TDD Integration**:
  - Integrated experimental corrosion parity test and Semiconductor Defect Compensation Index (SDCI) into TDD physics test suite.

## [3.5.0] - 2026-10-17
### Added
- **Unexplored Domains Expansion (+198 unique sources, Total 815 items)**:
  - Domain 1: Public mechanical property & crystal structure datasets (MPEA/HEA compilation databases).
  - Domain 2: d-electron alloy theory (Bo-Md parameters, $C_{11}-C_{12}$ shear softening avoidance, $p\text{-}d$ covalent hybridization).
  - Domain 3: Point Defect Model (PDM), XPS cation depth profiling, and Mott-Schottky semiconductor passivity.
  - Domain 4: CALPHAD phase equilibria, coherent B2/A2 nano-precipitation, and C14/C15 Laves phase solvus boundaries.
  - Domain 5: Tribocorrosion in 3.5 wt% NaCl, hydrogen embrittlement, and marine stress corrosion cracking (SCC).
  - Domain 6: Patent literature and vacuum arc melting / SPS sintering processing documents.
- **Abstract Recovery via OpenAlex**:
  - Restored rich full abstracts for 26 previously truncated Elsevier/Springer papers.
- **Re-linked LLM-Wiki Knowledge Graph**:
  - Re-linked all 815 sources with bidirectional Wiki-Links (`[[...]]`) and GitHub Markdown relative links.
  - Updated all 8 Topic Hubs and `ref/wiki/_Graph_Map.md` to reflect 815 connected nodes.
  - Regenerated `ref/index.md` master deduplication registry.

## [3.0.0] - 2026-10-17
### Added
- **LLM-Wiki Knowledge Graph Architecture (`ref/wiki/`)**:
  - Created `ref/wiki/_Graph_Map.md` with Mermaid knowledge graph topology and full hub navigation.
  - Created 8 specialized Topic Hub Wiki notes.
  - Added 37 new targeted publications on Track A (`AlCrTiV`, `TiCrVNbAl`, `AlNbTiVZr`, `AlTiVCrSi`), $p\text{-}d$ orbital hybridization, and Mott-Schottky passive film analysis.
  - Injected bidirectional Wiki-Links (`[[...]]`) into all source files.

## [2.1.0] - 2026-10-17
### Added
- Expanded search to broad multi-database and open scientific repositories (Crossref + arXiv preprints + OpenAlex) bringing total collection to 580 unique items.

## [1.1.0] - 2026-10-17
### Added
- Created `sources/` directory for direct archival of original academic literature abstracts, formulations, and patent claims.

## [1.0.0] - 2026-10-17
### Added
- Initial creation of the OKF knowledge bundle for autonomous materials discovery.
