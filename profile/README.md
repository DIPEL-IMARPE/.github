Reproducible software, analytical workflows, technical protocols, and assessment reports developed by the Dirección de Investigaciones del Subsistema Pelágico (DIPEL) of the Instituto del Mar del Perú (IMARPE). The organization uses GitHub to document and maintain analytical methods, source code, report-generation systems, reusable software, and institutional standards for pelagic fisheries research and stock assessment.

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
