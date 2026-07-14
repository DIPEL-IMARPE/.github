Reproducible software, analytical workflows, technical protocols, and assessment reports developed by the **Dirección de Investigaciones del Subsistema Pelágico (DIPEL)** of the **Instituto del Mar del Perú (IMARPE)**.
The organization uses GitHub to document and maintain analytical methods, source code, report-generation systems, reusable software, and institutional standards for pelagic fisheries research and stock assessment.

## Repository naming convention

Repositories associated with a particular species, stock, or assessment unit follow the structure:

```text
speciesSTOCK-analysis-or-product-repository-type
```

The species and stock codes are written together, without a hyphen. The remaining components are separated with hyphens and describe the analytical purpose and the repository class.

```text
<species><STOCK>-<analysis-or-product>-<repository-type>
```

### Naming components

| Component | Format | Function | Examples |
|---|---|---|---|
| `species` | Lowercase abbreviation | Identifies the species or resource group | `anc`, `jjm`, `spb`, `cdf`, `pcm`, `pel` |
| `STOCK` | Uppercase abbreviation | Identifies the stock, assessment unit, or geographic domain | `NC`, `SUR`, `TP`, `SP` |
| `analysis-or-product` | Lowercase kebab-case | Describes the method, model, indicator, process, or product | `cpue-standardization`, `survey-indicators`, `stock-assessment` |
| `repository-type` | Controlled final term | Identifies the principal function of the repository | `protocol`, `manual`, `workflow`, `report` |

### Resource codes currently used

| Code | Resource |
|---|---|
| `anc` | Peruvian anchovy |
| `jjm` | Jack mackerel / jurel |
| `spb` | Bonito |
| `cdf` | Common dolphinfish / perico |
| `pcm` | Pacific chub mackerel / caballa |
| `pel` | Pelagic resources |

### Stock and assessment-unit codes

| Code | Assessment unit |
|---|---|
| `NC` | North–central stock or assessment unit |
| `SUR` | Southern stock or assessment unit |
| `TP` | National Peruvian assessment domain |
| `SP` | Peruvian stock |

The precise biological and geographic definition of each assessment unit should also be documented in the corresponding repository README and metadata.

### Examples

```text
cdfTP-cpue-sdmtmb-workflow
│  │       │       │
│  │       │       └──────── repository type: reproducible analytical workflow
│  │       │
│  │       └──────────────── analytical method: CPUE standardization using sdmTMB
│  │
│  └──────────────────────── stock or management unit: Peruvian national domain
│
└─────────────────────────── species: common dolphinfish / perico
```

Packages, organization-level repositories, templates, handbooks, and websites are exempt from the species–stock prefix when their scope covers multiple resources or the organization as a whole. Examples include `pelagicSurvey`, `PBPtools`, `.handbook`, and `dipel-imarpe.github.io`.

---

## Repository map

| Section | Content | Access |
|---|---|---|
| 📦 Packages | R, Python, and C++ tools for marine and fisheries analysis | [View section](#packages) |
| 📘 Protocols and manuals | Standardized methodological protocols, operational manuals, and decision procedures | [View section](#protocols-and-manuals) |
| 🔁 Analytical processes | Reproducible pipelines for technical analyses | [View section](#analytical-processes) |
| 🐟 Resource reports | Reports and workflows organized by pelagic resource or stock | [View section](#resource-reports) |
| 📄 Operational reports | Reproducible technical and institutional reports | [View section](#operational-reports) |
| 📊 Dashboards and apps | Web applications and visual tools | [View section](#dashboards-and-apps) |
| ✍️ Manuscripts | Scientific papers and reproducible publication workflows | [View section](#manuscripts) |
| 🏛 Institutional repositories | Templates, handbook, profile, workflows, and environments | [View section](#institutional-repositories) |

> **Data policy:** Raw, confidential, sensitive, or restricted institutional data are not stored in public GitHub repositories. GitHub is used for source code, documentation, metadata, templates, analytical workflows, reproducible examples, and research software. When examples require data, repositories should use simulated, aggregated, anonymized, or openly licensed datasets.

---

<a id="packages"></a>

## 📦 Packages

Reusable R tools supporting pelagic surveys, fishing-logbook data, biomass estimation, retrospective comparisons, population projections, and catch-advice calculations.

| Repository | Main purpose | Primary language | Access |
|---|---|---|---|
| `pelagicSurvey` | Tools for processing, analyzing, and visualizing biological and acoustic information from pelagic surveys | R | [Repository](https://github.com/DIPEL-IMARPE/pelagicSurvey) |
| `PBPtools` | Tools for processing, analyzing, and visualizing data from the Programa de Bitácoras de Pesca | R | [Repository](https://github.com/DIPEL-IMARPE/PBPtools) |
| `retroSurvey` | Retrospective comparisons of scientific surveys, including coverage, spatial structure, and indicator consistency | R | [Repository](https://github.com/DIPEL-IMARPE/retroSurvey) |
| `popeProjection` | Population projection tools based on Pope-type cohort and catch calculations | R | [Repository](https://github.com/DIPEL-IMARPE/popeProjection) |
| `TAC` | Tools supporting total allowable catch calculations, scenarios, and decision outputs | — | [Repository](https://github.com/DIPEL-IMARPE/TAC) |
| `TBE` | Automation tools for analyzing pelagic acoustic-survey data and estimating biomass | R | [Repository](https://github.com/DIPEL-IMARPE/TBE) |

---

<a id="protocols-and-manuals"></a>

## 📘 Protocols and manuals

Methodological standards and operational documents used to standardize stock assessments, decision processes, and the digitization of biological and fishery information. Use `protocol` for normative methodologies and `manual` for step-by-step operational guidance.

| Repository | Main purpose | Primary language | Access |
|---|---|---|---|
| `jjmSP-stock-assessment-protocol` | Protocol for the stock assessment of Peruvian jack mackerel | TeX | [Repository](https://github.com/DIPEL-IMARPE/jjmSP-stock-assessment-protocol) |
| `pelTP-ebfp-fishery-protocol` | Manuals for digitizing biological and fishery information developed under the Estimation of Biological and Fishery Parameters project | TeX | [Repository](https://github.com/DIPEL-IMARPE/pelTP-ebfp-fishery-protocol) |
| `ancNC-tac-decision-table-protocol` | Protocol for constructing and applying total allowable catch decision tables for the north–central anchovy stock | TeX | [Repository](https://github.com/DIPEL-IMARPE/ancNC-tac-decision-table-protocol) |

> **Naming note:** Because `pelTP-ebfp-fishery-protocol` contains operational digitization manuals, `pelTP-ebfp-fishery-manual` would be the more specific name under the controlled repository-type vocabulary.

---

<a id="analytical-processes"></a>

## 🔁 Analytical processes

Reproducible pipelines for biological and fishery indicators, CPUE standardization, selectivity, catch-at-length analysis, and stock assessment.

| Repository | Main purpose | Primary language | Access |
|---|---|---|---|
| `spbTP-selectivity-at-size-workflow` | Estimation and diagnostics of selectivity-at-size for bonito | R | [Repository](https://github.com/DIPEL-IMARPE/spbTP-selectivity-at-size-workflow) |
| `ancNC-survey-indicators-workflow` | Estimation of acoustic, biological, population, and spatial survey indicators for the north–central anchovy stock | R | [Repository](https://github.com/DIPEL-IMARPE/ancNC-survey-indicators-workflow) |
| `ancSUR-cpue-standardization-workflow` | Standardization of catch per unit effort for the southern anchovy stock | R | [Repository](https://github.com/DIPEL-IMARPE/ancSUR-cpue-standardization-workflow) |
| `cdfTP-cpue-sdmtmb-workflow` | Spatio-temporal CPUE standardization for common dolphinfish using `sdmTMB` | R | [Repository](https://github.com/DIPEL-IMARPE/cdfTP-cpue-sdmtmb-workflow) |
| `ancNC-ss3-stock-assessment-workflow` | Stock Synthesis 3 assessment workflow for the north–central anchovy stock | Scheme | [Repository](https://github.com/DIPEL-IMARPE/ancNC-ss3-stock-assessment-workflow) |
| `ancNC-SPiCT-stock-assessment-workflow` | SPiCT stock-assessment workflow for the north–central anchovy stock | R | [Repository](https://github.com/DIPEL-IMARPE/ancNC-SPiCT-stock-assessment-workflow) |
| `ancNC-catch-at-length-workflow` | Processing, standardization, and analysis of catch-at-length information for the north–central anchovy stock | R | [Repository](https://github.com/DIPEL-IMARPE/ancNC-catch-at-length-workflow) |

---

<a id="resource-reports"></a>

## 🐟 Resource reports

Assessment reports and supporting report-generation systems organized by pelagic species and stock or management unit.

| Repository | Species | Stock / management unit | Main purpose | Primary language | Access |
|:---|:---|:---|:---|:---:|:---:|
| `ancNC-national-assessment-report` | Peruvian anchovy (*Engraulis ringens*) | North–central stock (`NC`) | National assessment of the north–central anchovy stock based primarily on scientific survey information | R | [Repository](https://github.com/DIPEL-IMARPE/ancNC-national-assessment-report) |
| `ancSUR-national-assessment-report` | Peruvian anchovy (*Engraulis ringens*) | Southern stock (`SUR`) | National assessment report for the southern anchovy stock | R | [Repository](https://github.com/DIPEL-IMARPE/ancSUR-national-assessment-report) |
| `pcmTP-national-assessment-report` | Pacific chub mackerel (*Scomber japonicus*) | Peruvian management unit (`TP`) | National assessment report for Pacific chub mackerel | Visual Basic 6.0 | [Repository](https://github.com/DIPEL-IMARPE/pcmTP-national-assessment-report) |
| `spbTP-national-assessment-report` | Pacific bonito (*Sarda chiliensis*) | Peruvian management unit (`TP`) | National assessment report for Pacific bonito | Scheme | [Repository](https://github.com/DIPEL-IMARPE/spbTP-national-assessment-report) |
| `cdfTP-national-assessment-report` | Common dolphinfish (*Coryphaena hippurus*) | Peruvian management unit (`TP`) | National assessment of common dolphinfish using a JABBA reference model | R | [Repository](https://github.com/DIPEL-IMARPE/cdfTP-national-assessment-report) |

---

<a id="operational-reports"></a>

## 📄 Operational reports

Reproducible technical and institutional reports that are not restricted to a single stock-assessment repository.

_No repositories are currently listed in this category._

---

<a id="dashboards-and-apps"></a>

## 📊 Dashboards and apps

Web applications, interactive dashboards, and visual tools for disseminating indicators and analytical outputs.

_No repositories are currently listed in this category._

---

<a id="manuscripts"></a>

## ✍️ Manuscripts

Scientific papers and reproducible publication workflows.

_No repositories are currently listed in this category._

---

<a id="institutional-repositories"></a>

## 🏛 Institutional repositories

Organization-level repositories for governance, templates, documentation, shared workflows, and public communication.

| Repository | Main purpose | Primary language | Access |
|---|---|---|---|
| `.github` | Public organization profile, contribution guidance, and shared GitHub configuration | — | [Repository](https://github.com/DIPEL-IMARPE/.github) |
| `.handbook` | Institutional handbook for repository governance, roles, branches, review, releases, documentation, and data policy | — | [Repository](https://github.com/DIPEL-IMARPE/.handbook) |
| `.template_analytical_processes` | Base template for reproducible analytical workflows in DIPEL-IMARPE | R | [Repository](https://github.com/DIPEL-IMARPE/.template_analytical_processes) |
| `dipel-imarpe.github.io` | Public website for DIPEL-IMARPE projects, software, workflows, and documentation | HTML | [Repository](https://github.com/DIPEL-IMARPE/dipel-imarpe.github.io) |

---

## Repository documentation requirements

Each analytical repository should include, at minimum:

1. A concise statement of its scientific or operational purpose.
2. The species, stock, assessment unit, and geographic scope.
3. The input-data requirements and data-access restrictions.
4. A description of the analytical workflow and principal outputs.
5. Reproducibility instructions, including software and package versions.
6. A minimal executable example using public, simulated, anonymized, or aggregated data.
7. The responsible technical team, citation information, license, and contribution rules.

---

<p align="center">
  <strong>DIPEL-IMARPE</strong><br>
  Dirección de Investigaciones del Subsistema Pelágico · Instituto del Mar del Perú
</p>
