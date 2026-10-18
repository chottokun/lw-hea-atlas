# LW-HEA Autonomous Discovery Suite & Open Knowledge Atlas
### Autonomous Discovery Infrastructure for Ultra-Lightweight, High-Specific-Stiffness, and Ultra-Corrosion-Resistant High-Entropy Alloys

[日本語 (Japanese)](README.md) | **English**

---

## 💡 What are Light-Weight High-Entropy Alloys (LW-HEAs)?

**High-Entropy Alloys (HEAs)** fundamentally diverge from conventional alloy design strategies based on "one or two principal elements with micro-alloying additions." By incorporating five or more principal elements in near-equiatomic proportions, HEAs leverage high configurational entropy to stabilize single-phase solid solutions, demonstrating outstanding strength, thermal stability, and corrosion resistance as next-generation structural materials.

However, traditional representative HEAs (e.g., the Cantor alloy `CoCrFeMnNi` and refractory HEAs like `NbMoTaW`) predominantly rely on dense transition metals, resulting in high densities ranging from **6.0 to 12.0 g/cm³**. Consequently, they face an intrinsic structural limitation: they cannot meet the aggressive weight-reduction demands of aerospace, automotive, energy, and advanced robotics applications.

In contrast, **Light-Weight High-Entropy Alloys (LW-HEAs)** strategically utilize light elements such as Al (aluminum) and Ti (titanium) as their primary framework. They represent an ambitious frontier in materials science, aiming to achieve a density below that of pure titanium (**ρ ≤ 4.51 g/cm³**) while simultaneously securing higher specific stiffness than conventional titanium alloys (**E/ρ > 25 GPa·g⁻¹cm³**) and superior corrosion resistance in marine chloride environments.

### Why an "Experimental Exploration" using Autonomous AI and Materials Informatics?
Multi-component systems combining light elements (Al, Si) and early transition metals (Ti, V, Cr, Nb, etc.) inherently present severe thermodynamic and physicochemical trade-offs: large negative enthalpies of mixing promote the precipitation of **brittle intermetallic phases (Laves phases and brittle silicides)** at grain boundaries, and chemical potential differences among constituent elements can accelerate **micro-galvanic corrosion**.

To address this challenge, this project explores how a materials scientist can leverage generative AI and autonomous agents. Specifically, it represents a personal exploratory initiative to investigate: **"Can an autonomous AI agent coupled with lightweight physical evaluation engines in Materials Informatics (MI) uncover meaningful design hypotheses in complex multi-component spaces?"**
As a result of this closed-loop exploration, promising candidate compositions were identified. In materials science, real-world constraints such as manufacturability, safety margins, and scaling factors are paramount. While this work remains a computational and conceptual exploration, it demonstrates how efficiently such multi-objective design spaces can be mapped.

---

> [!IMPORTANT]
> ### ⚠️ Research Nature & Disclaimer
> The contents of this repository and the interactive dashboard represent an **exploratory and experimental computational study driven by autonomous AI agents and materials informatics (MI) techniques**.
> 
> 1. **Desk Screening and Working Hypotheses**:
>    The proposed alloy compositions, physical models (Point Defect Model, corrosion prediction formulations, Pugh ratios, HPBI, RKI, etc.), and thermodynamic screening results are **computational screenings and working hypotheses** derived from literature data and physicochemical principles. They do not guarantee absolute accuracy, completeness, or fitness for specific engineering applications.
> 2. **Need for Experimental Validation**:
>    These findings precede experimental validation, including actual ingot casting (VAR), microstructural characterization (XRD/TEM/SEM), and wet electrochemical corrosion testing. They are presented as a starting point for experimentalists, collaborative research, or as a roadmap of possibilities for unexplored materials spaces.
> 3. **Disclaimer Regarding Intellectual Property & Freedom-to-Operate (FTO)**:
>    Any patent claim comparisons, design-around notes, or clearance assessments mentioned in this repository and its Wiki represent **exploratory, preliminary trial screenings performed automatically by an AI agent for illustrative purposes only**. They illustrate formal composition differences against a limited sample of patent publications and **do NOT constitute legal advice, patent opinions, non-infringement certifications, or guarantees of Freedom to Operate**. Commercial manufacturing, testing, sales, or patent filings must be preceded by rigorous prior-art searches and legal infringement opinions conducted by qualified patent attorneys.

---

> [!NOTE]
> ### 🌐 Repository Architecture & Delivery
> This repository serves as an **Open Knowledge Atlas & Web Viewer**, compiling screening results, multi-objective Pareto-optimal candidates, unexplored composition maps, and literature insights (knowledge graphs) generated via autonomous AI agents and physical evaluation engines into interactive web dashboards and Wiki-style Markdown documents.
> All composition data, Pareto frontiers, ingot weighing tools, and technical documentation can be explored directly in any modern web browser without configuring complex local computational environments.

---

## 🎯 Exploration Objectives (Mission & Charter)

* **Mission**: Simultaneously satisfy ultra-high corrosion resistance (**log₁₀(I_corr) ≤ -7.0 A/cm²** in 3.5 wt% NaCl) × lightweight (**ρ ≤ 4.50 g/cm³**) × high specific stiffness (**E/ρ > 25 GPa·g⁻¹cm³**) to identify Pareto-optimal compositions and systematically chart unexplored possibility landscapes.
* **Charter (Phase Selection Constraints)**: Principal elements **n ≥ 5**, individual concentrations **5.0 ≤ c_i ≤ 35.0 at%**, configurational entropy **ΔS_mix ≥ 1.5R**, atomic size difference **δ ≤ 6.6%**, phase stability **Ω ≥ 1.1** (or coherent B2 nano-precipitation regime), valence electron concentration **VEC < 6.87**, targeting single-phase BCC or BCC + coherent ordered B2 nanostructures.

---

## 📊 Objective-Specific 7-Track Optimal Portfolio

A balanced portfolio strictly adhering to Charter constraints (5–35 at% per element, 100.0 at% total, L₁ distance ≥ 10 at% from known literature alloys):

| # | Track Name | Representative Composition (at%) | ρ (g/cm³) | E/ρ | B/G (Pugh) | corr | logI | PREN | δ (%) | Ω_net | σ_Tm (K) | pv | Features & Recommended Use |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **①** | **Baseline Flagship** | **Al30.0 Ti35.0 V15.0 Cr10.0 Nb5.0 Si5.0** | 4.45 | 29.70 | 2.24 | 93.81 | **-7.90** | 38.0 | 6.52 | 0.87 | 556 | 92.0 | **Primary candidate**. Sc/Mg-free, compatible with standard Vacuum Arc Remelting (VAR). |
| **②** | **Maximum Corrosion Resistance** | **Al33.0 Ti35.0 V5.0 Cr13.0 Nb9.0 Si5.0** | 4.49 | 29.70 | 2.19 | **96.36** | **-8.09** | 52.0 | 6.57 | 0.82 | 548 | 94.5 | V reduced to 5%, Cr boosted to 13% for maximum passivation. |
| **③** | **Pitting-Resistant / High-Modulus** | **Al30.0 Ti35.0 V15.0 Cr10.0 Mo5.0 Si5.0** | 4.50 | **30.73** | 2.18 | 92.81 | **-7.85** | **47.0** | 6.55 | 0.88 | 570 | 91.6 | Mo substituted for Nb. Exceptional pitting resistance in marine chloride environments. |
| **④** | **Si-Free High-Toughness** | **Al30.0 Ti35.0 V10.0 Cr15.0 Zr5.0 Sc5.0** | 4.42 | 30.57 | 2.09 | 93.64 | **-8.00** | 50.5 | **4.98** | 0.87 | 514 | **96.2** | Zero silicide embrittlement risk, minimal lattice distortion. High room-temperature toughness. |
| **⑤** | **Strict Ω ≥ 1.10 Solid Solution** | **Al25.0 Ti35.0 V15.0 Cr10.0 Nb5.0 Sc10.0** | 4.44 | 28.46 | **2.25** | 89.34 | **-7.88** | 40.5 | 6.38 | **1.15** | 525 | 92.0 | Academic flagship strictly satisfying Yeh's Ω ≥ 1.10 criterion. |
| **⑥** | **Low-Segregation (Nb/Mo-Free)** | **Al35.0 Ti35.0 V10.0 Cr10.0 Mn5.0 Si5.0** | 4.50 | 29.35 | 2.15 | 89.20 | **-7.68** | 33.0 | 6.62 | 0.81 | **483** | 94.5 | High-melting elements excluded. Minimal melting point variance (σ_Tm = 483 K) for homogeneous ingots. |
| **⑦** | **Ultra-Low Density (Track B MA+SPS)**| **Al30.0 Ti35.0 V5.0 Cr15.0 Zr10.0 Mg5.0** | **4.41** | **29.96** | 2.06 | 89.07 | **-7.40** | 40.5 | 6.40 | 0.99 | 538 | 63.2 | Ultra-lightweight with Mg addition. Solid-state sintering only (MA+SPS; reaches ρ = 4.14 with 10% Mg). |

---

## 🎛️ If-Then Boundary Relaxation Studies

Quantitative exploration of the vast materials space unlocked by relaxing initial strict boundaries by just a few percent:

* **Scenario A: Density Boundary Relaxation (ρ ≤ 4.50 → 4.65 g/cm³)**
  - **Impact**: Bypasses the 2nd Impossibility Theorem (no Si/Sc-free alloy can meet ρ ≤ 4.50), **unlocking 505 Si/Sc-free pure valve-metal alloys (`Al-Ti-V-Cr-Nb-Zr`)**.
  - **Representative Solution**: `Al35 Ti35 V10 Cr10 Nb5 Zr5` (ρ = 4.53 g/cm³, δ = 5.42%, silicide_risk = 0, logI = -7.73). Highly reliable structural material with zero silicide risk.
* **Scenario B: Permitting Minor Additions of a 6th Element (c_Si = 2.0–3.5 at%)**
  - **Impact**: Mitigates lattice distortion induced by mandatory 5 at% Si (δ ≈ 6.5–6.7%), **unlocking 3,110 Nb/Mo-free homogeneous alloys (`Al-Ti-V-Cr-Mn-Si`) with δ < 6.0%**.
  - **Representative Solution**: `Al34 Ti35 V14 Cr7 Mn7.5 Si2.5` (ρ = 4.48, δ = 5.85%, σ_Tm = 482 K). Silicide precipitation risk halved with dramatically improved processability.
* **Scenario C: Principal Element Upper Bound Relaxation (c_i ≤ 40 at%)**: Ti/Al-enriched design across medium-to-high entropy boundaries (ΔS ≥ 1.45R).
* **Scenario D: Rapid Solidification & Additive Manufacturing (AM / LPBF / Sputtered Thin Films)**: Reaching extreme stiffness and hardness beyond equilibrium solid solubility limits.

---

## 🔬 Core Physical & Chemical Mechanisms (Design Principles & Theoretical Insights)

1. **Mathematical Necessity of 6-Component Systems (1st Impossibility Theorem)**:
   In 5-component `Al-Ti-V-Cr-Nb` (5–35 at% each), simultaneously achieving ρ ≤ 4.50 g/cm³ and ΔS ≥ 1.5R is mathematically impossible. Minimizing density alone yields ρ = 4.458 g/cm³ (`Al35 Ti35 V20 Cr5 Nb5`), but composition skewness caps ΔS_mix at 1.403R. Fulfilling the high-entropy threshold (≥ 1.50R) requires heavier elements, pushing density to ρ ≥ 4.62 g/cm³. Hence, introducing Si (ρ = 2.33 g/cm³) at 5 at% or Sc to form a 6-component system is a thermodynamic necessity.
2. **Density Limit of Pure Transition Metal + Al Systems (2nd Impossibility Theorem)**:
   Si/Sc-free pure valve-metal systems (`Al-Ti-V-Cr-Nb-Zr`) have a minimum density of ρ_min = 4.532 > 4.50 g/cm³, leading to 100% rejection under standard criteria. Introducing a third lightweight element (Si or Sc) beyond Al and Ti is a strict mathematical requirement for Track A.
3. **Crystallographic Size-Buffering Role of Titanium**:
   Removing Ti (atomic radius r = 1.47 Å) does not degrade stiffness, but atomic size difference explodes to δ = 8.1–11.2%, causing BCC lattice collapse. Ti serves as an indispensable size buffer bridging large-radius elements (Al, Sc) and small-radius elements (Cr, V, Si).
4. **Point Defect Model (PDM) & Semiconductor Defect Compensation**:
   With high Al concentrations (≥ 30 at%), n-type donor defects (oxygen vacancies V_O••) proliferate in the passive film. These are electrochemically compensated via 5-component hybridization with p-type Cr₂O₃, highly insulating TiO₂, and amorphous SiO₂ (SDCI = 1.67 ≥ 1.5).
5. **Literature Benchmark Calibration & Predictive Hypotheses**:
   Using experimental literature data for AlCrTiV_0.5 (I_corr = 0.131 µA/cm² ⇒ log₁₀(I_corr) = -6.883 in 3.5 wt% NaCl, [Materials 2023](https://doi.org/10.3390/ma16072922)) as an anchor, segregation and entropy correction models were single-point calibrated. Baseline candidate A1 (model prediction logI = -7.90) represents a predictive working hypothesis exceeding this benchmark, awaiting wet electrochemical validation.
6. **MoO₄²⁻ Adsorption & Repassivation via Mo Doping**:
   In the A-Mo alloy, doping with 5 at% Mo boosts PREN from 38.0 to 47.0. Molybdate anion adsorption inside pit embryos competitively repels aggressive chloride ions (Cl⁻).

---

## 📖 Technical Documentation & Discussion Directory

| Document | Content Summary |
|---|---|
| [`RESEARCH_LOG.md`](./RESEARCH_LOG.md) | Full research trajectory, physical challenges, element ablation, unexplored maps, PDM analysis, and closed-loop iterations |
| [`05_wiki/possibility-landscape-and-scenarios.md`](./05_wiki/possibility-landscape-and-scenarios.md) | Computational unexplored composition maps, 4 major white-space islands, If-Then scenarios, Top 25 catalog |
| [`05_wiki/ablation-and-family-study.md`](./05_wiki/ablation-and-family-study.md) | Elemental ablation, exhaustive family analysis, and the 2nd Impossibility Theorem |
| [`05_wiki/lw-hea-design.md`](./05_wiki/lw-hea-design.md) | LW-HEA design principles (density, stiffness, corrosion physics, and PDM semiconductor defect theory) |
| [`05_wiki/fto-analysis.md`](./05_wiki/fto-analysis.md) | Exploratory patent claim comparison & preliminary FTO assessment sample (AI automated screening, non-guaranteed) |
| [`05_wiki/pareto-candidates.md`](./05_wiki/pareto-candidates.md) | Pareto-optimal candidates (Top 5 & 7-track portfolio specifications) |
| [`05_wiki/experimental-protocol.md`](./05_wiki/experimental-protocol.md) | 7-track experimental SOPs (sandwich charge melting, homogenization, water quenching, ASTM G5 electrochemical protocol) |
| `Closed-Loop MI Core` | Physics-Informed Bayesian Optimization (PIBO) experimental loop (internal core, proprietary) |

---

## 📚 Bibliographic Knowledge Base (819 Sources, OKF v4.1 LLM-Wiki Knowledge Graph)

- [`ref/index.md`](./ref/index.md) — OKF Master Index (819 deduplicated entries with DOIs and objective property values)
- [`ref/wiki/_Graph_Map.md`](./ref/wiki/_Graph_Map.md) — LLM-Wiki Knowledge Graph overview map (8 topic hubs)

---

## 💻 Interactive Dashboard Suite (v4.0 Final)

Viewable directly in any web browser (no local backend server required; fully offline compatible).

- **[04_dashboard/index.html](./04_dashboard/index.html)** — Comprehensive Portal & Integrated Dashboard
  - 🏆 **Top 25 Master Catalog & Radar Profiles**: Detailed specifications and property tradeoffs for all 7-track and relaxation candidates
  - 📊 **Interactive 2D/3D Pareto Frontiers (Plotly)**: Multi-dimensional visualization of density ρ vs specific modulus E/ρ vs corrosion resistance / Pugh ratio
  - 🎛️ **Boundary Relaxation Scenarios & Sensitivity Sliders**: Density relaxation (ρ ≤ 4.65 g/cm³), low-Si micro-addition, and partial derivative sensitivity analyses
  - ⚖️ **Vacuum Arc Remelting (VAR) Volatilization-Corrected Ingot Weighing Calculator**: Real-time Al/Cr evaporation compensation, log records, and CSV export
- **[04_dashboard/catalog.html](./04_dashboard/catalog.html)** — 7-Track & Top 25 Master Specifications (sorting, filtering, print-friendly)
- **[04_dashboard/possibility_map.html](./04_dashboard/possibility_map.html)** — 3D Unexplored Composition Space & 4 White-Space Islands Explorer
- **[04_dashboard/weighing.html](./04_dashboard/weighing.html)** — Shop-floor touch-friendly precision weighing checklist app

---

## Comments

- This is a personal project driven solely by personal curiosity and interest, conducted independently without any affiliation, funding, or institutional support.

*LW-HEA Autonomous Discovery Suite & Open Knowledge Atlas (2026)*
