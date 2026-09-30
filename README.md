# Explainable AI for Antimicrobial Resistance (XAI-AMR)

This repository contains the screening records, classification criteria, and primary-study synthesis data used in a systematic review of "Explainable Artificial Intelligence (XAI) for Antimicrobial Resistance (AMR)".

The repository provides the underlying data used for study screening and evidence synthesis, including primary research studies and review articles.



# Repository Contents

# 1. `Research_Screening.csv`

This file contains the screening record for the retrieved **primary research articles**.

The screening table includes:

- Paper title
- Authors
- Publication year
- Screening decision (`INCLUDE` / `EXCLUDE`)
- Reason for inclusion
- Reason for exclusion
- DOI
- Scopus EID
- Screening basis

The screening was performed based on title and abstract screening, with inclusion/exclusion decisions documented for each record.


# 2. `Review_Screening.csv`

This file contains the screening record for **review articles** identified for the review-of-reviews analysis.

The table includes:

- Paper title
- Authors
- Publication year
- Screening decision (`INCLUDE` / `EXCLUDE`)
- Reason for inclusion
- Reason for exclusion
- DOI
- Scopus EID
- Screening basis

The included review articles form the basis for the review-of-reviews synthesis.



# 3. `PRIMARY SYNTHESIS TABLE.xlsx`

This is the main synthesis table for the included primary empirical studies.

The table captures bibliographic, methodological, XAI, and evaluation-related characteristics, including:

- Study identification and bibliographic information
- Country/setting
- Pathogen/species
- Antimicrobial drug class
- Data modality and modality design
- Dataset source and volume
- ML/DL models
- Best-performing model
- Performance metrics
- XAI methods used
- Multimodal XAI integration
- XAI rigor and comparability
- Explanation stability and reproducibility
- Biological/mechanistic grounding
- Clinical translation and deployment
- Explanation comprehensibility
- Deployment feasibility
- Supporting evidence for the classifications

The primary synthesis table contains **45 included primary studies**.


# 4. `TABLE1 CLASSIFICATION CRITERIA.pdf`

This document provides the detailed criteria used to classify attribute coverage in the **review-of-reviews analysis**.

The framework contains 21 attributes covering areas such as:

- AMR coverage
- Multiple pathogens/microbial classes
- Multiple data modalities
- Multimodal integration
- Prediction/ML
- XAI/explainability
- XAI methods
- XAI method comparison
- Explanation quality
- Explanation faithfulness
- Explanation stability
- Explanation reproducibility
- AMR-specific XAI evaluation framework
- Biological/mechanistic grounding
- Genotype–phenotype relationship
- Clinical validation
- External validation
- Generalizability
- Reproducibility
- Standardization
- AMR-specific multimodal XAI

Each attribute is classified as "Not Covered", "Partially Covered", or "Clearly Covered" according to the definitions provided in the document.


## Color Coding in the Primary Synthesis Table

The `PRIMARY SYNTHESIS TABLE.xlsx` uses **cell background colors instead of ✓, △, and × symbols** for the categorical classifications.

### Legend

| Color | Meaning | Symbol |
| 🟩 Green | Clearly Covered / Yes | ✓ |
| 🟨 Yellow | Partially Covered / Intermediate | △ |
| 🟥 Red | Not Covered / No | × |

Therefore:

- *Green cells* indicate that the corresponding criterion is **clearly covered or satisfied**.
- *Yellow cells* indicate **partial, limited, or intermediate coverage**.
- *Red cells* indicate that the criterion is **not covered or not satisfied**.

The color coding is a visual representation of the underlying categorical classification and should be interpreted together with the corresponding evidence columns.



## Interpretation of the Classification

The classifications are **evidence-based categorical assessments**, not numerical scores.

For example:

- A **green** classification means that the study provides clear evidence satisfying the relevant criterion.
- A **yellow** classification means that the criterion is addressed only partially, indirectly, or with limited evidence.
- A **red** classification means that the criterion is not meaningfully addressed.

The distinction between categories follows the predefined classification criteria rather than subjective ranking.

For example, for explanation faithfulness:

- **Not Covered:** Faithfulness is not discussed.
- **Partially Covered:** Related concepts are addressed indirectly, but no dedicated faithfulness framework is used.
- **Clearly Covered:** Faithfulness is explicitly evaluated using identifiable methodology or evidence such as perturbation or feature-removal tests. :contentReference[oaicite:1]{index=1}

Similarly, explanation stability and reproducibility are treated as distinct properties: stability concerns consistency under changes such as runs, samples, or conditions, whereas explanation reproducibility concerns obtaining the same explanations under the same model/data/conditions. :contentReference[oaicite:2]{index=2}

---

## Primary Study Synthesis

The primary synthesis table organizes the included studies according to their:

1. **Study and dataset characteristics**
2. **ML/DL methodology**
3. **XAI methodology**
4. **Multimodal integration**
5. **XAI evaluation rigor**
6. **Explanation stability and reproducibility**
7. **Biological/mechanistic grounding**
8. **Clinical translation and deployment**
9. **Explanation comprehensibility**
10. **Deployment feasibility**

Evidence fields are provided alongside the categorical assessments to document the basis for each classification.



## Review-of-Reviews Classification

The review articles are evaluated using a 21-attribute framework.

The framework distinguishes between:

- **Multiple modalities** and **multimodal integration**
- **Biological plausibility** and **XAI faithfulness**
- **General research reproducibility** and **explanation reproducibility**
- **Clinical relevance** and **clinical validation**
- **Multimodal AMR modelling + XAI** and the broader presence of multimodal/XAI discussions

These distinctions are explicitly defined in the classification criteria. For example, the framework states that discussing multiple modalities separately does not constitute multimodal integration. :contentReference[oaicite:3]{index=3}

Likewise, the AMR-specific multimodal XAI category requires the review to address **AMR + multimodal data + AI/ML + explainability together**, rather than merely discussing multimodal approaches and XAI separately. :contentReference[oaicite:4]{index=4}

---

## Data and Evidence Principles

The classifications in the synthesis tables are based on evidence reported in the corresponding studies/reviews.

A criterion is not considered satisfied merely because:

- an approach is mentioned;
- a related concept is discussed;
- a method is listed without comparison;
- biological plausibility is claimed without evidence of model faithfulness;
- clinical data are used without clinical validation; or
- multiple modalities are present without actual multimodal integration.

The classification framework therefore separates **presence**, **partial evidence**, and **explicit evaluation**.

---

## Purpose of the Repository

The repository is intended to support:

- transparency of the systematic-review screening process;
- reproducibility of study selection;
- traceability of synthesis decisions;
- inspection of the evidence underlying categorical classifications;
- reuse of the extracted primary-study data; and
- verification of the review-of-reviews classification framework.

The files should be considered together when reproducing or auditing the synthesis.



## File Structure

```text
.
├── README.md
├── Research_Screening.csv
├── Review_Screening.csv
├── PRIMARY SYNTHESIS TABLE.xlsx
└── TABLE1 CLASSIFICATION CRITERIA.pdf
