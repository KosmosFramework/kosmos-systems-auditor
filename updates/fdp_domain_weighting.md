# FDP Domain-Specific Weighting System
## Proposed Addition to Master Reference File

**Date:** February 24, 2026  
**Source:** KOSMOS FDP Tools and Templates Appendix (formalized)  
**Status:** Proposed for integration into MRF

---

## Rationale

The baseline FDP framework currently uses equal weighting (all FDPs = 1.0) or relies on auditor judgment for emphasis. This approach fails to systematically align audit focus with domain-specific failure modes. A governance system audited with technology-system priorities will miss critical vulnerabilities.

Domain-specific weighting recognizes that **different system types have different primary risks:**
- Economic systems fail primarily through value extraction
- Technological systems fail primarily through opacity and bias
- Governance systems fail primarily through power concentration
- And so on...

This refinement formalizes eight weight vectors that align FDP emphasis with empirically-observed failure patterns.

---

## The Eight System Domains

Each domain is defined by its **core failure mode**—the primary ethical and functional risk pattern that distinguishes it from other system types.

### 1. Economic Systems (Firms, Markets, Platforms)

**Core Failure Mode:** Value extraction (unnatural) vs. regeneration (natural)

| FDP | Weight | Rationale |
|-----|--------|-----------|
| RE (Reciprocal Ethics) | 3.0 | Critical for distributive economics - who benefits/bears costs |
| SP (Symbiotic Purpose) | 2.0 | Essential for stakeholder value vs shareholder extraction |
| CLM (Closed-Loop Materiality) | 2.0 | Environmental sustainability of production |
| DA (Distributed Agency) | 1.0 | Standard weighting |
| CH (Contextual Harmony) | 1.0 | Standard weighting |
| ET (Emergent Transparency) | 1.0 | Standard weighting |
| AR (Adaptive Resilience) | 1.0 | Standard weighting |
| IH (Intellectual Honesty) | 1.0 | Standard weighting |

**Examples:** Amazon, Uber, manufacturing firms, retail chains

---

### 2. Technological Systems (Algorithms, AI, Apps, Platforms)

**Core Failure Mode:** Opacity, bias, and brittle failure

| FDP | Weight | Rationale |
|-----|--------|-----------|
| ET (Emergent Transparency) | 3.0 | Data responsibility and algorithmic accountability |
| IH (Intellectual Honesty) | 2.0 | Limitation acknowledgment crucial for AI/algorithms |
| AR (Adaptive Resilience) | 2.0 | System robustness and learning capacity |
| SP (Symbiotic Purpose) | 1.0 | Standard weighting |
| RE (Reciprocal Ethics) | 1.0 | Standard weighting |
| CLM (Closed-Loop Materiality) | 1.0 | Standard weighting |
| DA (Distributed Agency) | 1.0 | Standard weighting |
| CH (Contextual Harmony) | 1.0 | Standard weighting |

**Examples:** ChatGPT, recommendation algorithms, facial recognition, social media platforms

---

### 3. Ecological Systems (Land Use, Resource Management, Pollution)

**Core Failure Mode:** Thermodynamic and ecological viability violations

| FDP | Weight | Rationale |
|-----|--------|-----------|
| CH (Contextual Harmony) | 3.0 | Environmental enhancement essential |
| CLM (Closed-Loop Materiality) | 2.0 | Circular material flows critical |
| AR (Adaptive Resilience) | 2.0 | Ecosystem resilience capacity |
| SP (Symbiotic Purpose) | 1.0 | Standard weighting |
| RE (Reciprocal Ethics) | 1.0 | Standard weighting |
| DA (Distributed Agency) | 1.0 | Standard weighting |
| ET (Emergent Transparency) | 1.0 | Standard weighting |
| IH (Intellectual Honesty) | 1.0 | Standard weighting |

**Examples:** Waste management, mining operations, agricultural systems, forestry

---

### 4. Governance/Political (Laws, Agencies, Constitutions)

**Core Failure Mode:** Concentration of power and inequity

| FDP | Weight | Rationale |
|-----|--------|-----------|
| DA (Distributed Agency) | 3.0 | Decentralization of power most critical |
| RE (Reciprocal Ethics) | 2.0 | Fair distribution of burdens/benefits |
| AR (Adaptive Resilience) | 2.0 | Self-correction capacity essential |
| SP (Symbiotic Purpose) | 1.0 | Standard weighting |
| CLM (Closed-Loop Materiality) | 1.0 | Standard weighting |
| CH (Contextual Harmony) | 1.0 | Standard weighting |
| ET (Emergent Transparency) | 1.0 | Standard weighting |
| IH (Intellectual Honesty) | 1.0 | Standard weighting |

**Examples:** SAVE Act, DOGE, election laws, regulatory agencies, constitutions

---

### 5. Social/Community (NGOs, Movements, Local Organizations)

**Core Failure Mode:** Mission drift and erosion of local trust

| FDP | Weight | Rationale |
|-----|--------|-----------|
| SP (Symbiotic Purpose) | 3.0 | Genuine mutual benefit vs mission drift |
| RE (Reciprocal Ethics) | 2.0 | Fair distribution among members |
| CH (Contextual Harmony) | 2.0 | Positive local integration critical |
| DA (Distributed Agency) | 1.0 | Standard weighting |
| CLM (Closed-Loop Materiality) | 1.0 | Standard weighting |
| AR (Adaptive Resilience) | 1.0 | Standard weighting |
| ET (Emergent Transparency) | 1.0 | Standard weighting |
| IH (Intellectual Honesty) | 1.0 | Standard weighting |

**Examples:** Non-profits, community organizers, mutual aid networks, social movements

---

### 6. Financial (Banks, Funds, Crypto, Insurance)

**Core Failure Mode:** Opaque risk and asymmetric gain

| FDP | Weight | Rationale |
|-----|--------|-----------|
| ET (Emergent Transparency) | 3.0 | Expose hidden leverage/risk critical |
| RE (Reciprocal Ethics) | 2.0 | Prevent exploitative terms |
| IH (Intellectual Honesty) | 2.0 | Authenticity vs PR/greenwashing |
| SP (Symbiotic Purpose) | 1.0 | Standard weighting |
| CLM (Closed-Loop Materiality) | 1.0 | Standard weighting |
| DA (Distributed Agency) | 1.0 | Standard weighting |
| CH (Contextual Harmony) | 1.0 | Standard weighting |
| AR (Adaptive Resilience) | 1.0 | Standard weighting |

**Examples:** Banks, hedge funds, cryptocurrency systems, insurance companies

---

### 7. Infrastructure (Energy, Water, Transport, Communication)

**Core Failure Mode:** Unreliable service and unsustainable resource use

| FDP | Weight | Rationale |
|-----|--------|-----------|
| AR (Adaptive Resilience) | 3.0 | Resilience under stress most critical |
| CLM (Closed-Loop Materiality) | 2.0 | Resource circularity essential |
| CH (Contextual Harmony) | 2.0 | Environmental fitness required |
| SP (Symbiotic Purpose) | 1.0 | Standard weighting |
| RE (Reciprocal Ethics) | 1.0 | Standard weighting |
| DA (Distributed Agency) | 1.0 | Standard weighting |
| ET (Emergent Transparency) | 1.0 | Standard weighting |
| IH (Intellectual Honesty) | 1.0 | Standard weighting |

**Examples:** Power grids, water systems, highways, telecommunications, internet infrastructure

---

### 8. Informational/Media (News, Social Media, Publishing)

**Core Failure Mode:** Manipulation and misinformation

| FDP | Weight | Rationale |
|-----|--------|-----------|
| IH (Intellectual Honesty) | 3.0 | Truthfulness/accountability paramount |
| ET (Emergent Transparency) | 2.0 | Source/algorithm transparency critical |
| SP (Symbiotic Purpose) | 2.0 | Public good vs engagement extraction |
| RE (Reciprocal Ethics) | 1.0 | Standard weighting |
| CLM (Closed-Loop Materiality) | 1.0 | Standard weighting |
| DA (Distributed Agency) | 1.0 | Standard weighting |
| CH (Contextual Harmony) | 1.0 | Standard weighting |
| AR (Adaptive Resilience) | 1.0 | Standard weighting |

**Examples:** News organizations, social media platforms, publishing houses, information databases

---

## Calculation Methodology

### Weighted Global FDP Score

```
FDP_global = Σ(FDP_i × Weight_i) / Σ(Weight_i)
```

Where:
- FDP_i = individual FDP score (0-10 scale)
- Weight_i = domain-specific weight for that FDP
- Σ = sum across all 8 FDPs

### Example Calculation: SAVE Act (Governance/Political System)

**Step 1: Assign Raw FDP Scores**
- SP = 0.5
- AR = 1.2
- RE = 0.8
- CLM = 2.1
- DA = 0.5
- CH = 3.0
- ET = 2.5
- IH = 1.8

**Step 2: Apply Governance/Political Weights**
- SP = 0.5 × 1.0 = 0.5
- AR = 1.2 × 2.0 = 2.4
- RE = 0.8 × 2.0 = 1.6
- CLM = 2.1 × 1.0 = 2.1
- DA = 0.5 × 3.0 = 1.5
- CH = 3.0 × 1.0 = 3.0
- ET = 2.5 × 1.0 = 2.5
- IH = 1.8 × 1.0 = 1.8

**Step 3: Calculate Weighted Score**
```
Numerator = 0.5 + 2.4 + 1.6 + 2.1 + 1.5 + 3.0 + 2.5 + 1.8 = 15.4
Denominator = 1.0 + 2.0 + 2.0 + 1.0 + 3.0 + 1.0 + 1.0 + 1.0 = 12.0

FDP_global = 15.4 / 12.0 = 1.28
```

**Classification:** Unnatural (0.0-4.9 range), Collapse-Prone

---

## Domain Classification Decision Tree

**Question 1: What is the system's primary function?**

- Creating/distributing economic value → **Economic**
- Processing information/making decisions algorithmically → **Technological**
- Managing natural resources/environmental impact → **Ecological**
- Governing/regulating human behavior → **Governance/Political**
- Building community/collective action → **Social/Community**
- Managing financial assets/risk → **Financial**
- Providing essential services/utilities → **Infrastructure**
- Creating/distributing information/content → **Informational/Media**

**Question 2: If system spans multiple domains, which failure mode is PRIMARY?**

Example: A social media platform could be:
- Technological (algorithms)
- Informational/Media (content distribution)
- Economic (advertising business model)

**Primary failure mode analysis:**
- Is opacity/bias the main risk? → Technological
- Is misinformation the main risk? → Informational/Media
- Is value extraction the main risk? → Economic

**Guidance:** Choose the domain whose failure mode, if manifested, would cause the most severe systemic harm.

---

## Data Quality Assessment

Maintain data quality scoring to ensure weighted scores aren't false precision:

| Quality Factor | Score (1-5) | Assessment Criteria |
|----------------|-------------|---------------------|
| Data Completeness | [1-5] | 5=Complete, 1=Major gaps |
| Source Reliability | [1-5] | 5=Primary sources, 1=Unverified |
| Measurement Accuracy | [1-5] | 5=Precise metrics, 1=Estimates |
| Time Relevance | [1-5] | 5=Current data, 1=Outdated |

**Data Quality Penalty:** If average quality < 3.0, reduce Global FDP by 0.5 points

This prevents reporting FDP_global = 1.28 when data quality is poor. Report as FDP_global ≈ 1.3 or FDP_global = 1.3 ± 0.5 depending on data quality.

---

## Classification Thresholds (Unchanged)

| FDP Range | System Type | Status |
|-----------|-------------|--------|
| 8.0-10.0 | Natural | Anti-fragile |
| 5.0-7.9 | Hybrid | Resilient |
| 0.0-4.9 | Unnatural | Collapse-prone |

Domain weighting affects the calculated score but **does not change** the threshold boundaries.

---

## Impact on Existing Audits

### Backward Compatibility

Systems previously audited with equal weighting or ad-hoc weights **remain validly classified**. Domain weighting strengthens conclusions by systematically emphasizing domain-specific risks rather than reversing classifications.

### SAVE Act Example

**Previous approach (ad-hoc):**
- Used weights: SP=3, RE=3, IH=2, ET=2, DA=2
- Emphasis on purpose, ethics, honesty

**Proper Governance/Political weighting:**
- Should use: DA=3, RE=2, AR=2, all others=1
- Emphasis on power distribution, fairness, self-correction

**Impact:** DA was underweighted (2.0 instead of 3.0), AR was underweighted (1.0 instead of 2.0). Recalculation with proper weights would yield **lower Global FDP**, strengthening the Unnatural classification. The audit conclusion remains correct but the magnitude of dysfunction was underestimated.

No retroactive recalculation required unless practitioner chooses to apply enhanced precision.

---

## Implementation Guidelines

### For New Audits

1. **Classify system domain** using decision tree
2. **Apply appropriate weight vector** from the eight options
3. **Calculate individual FDP scores** (0-10 scale) as normal
4. **Apply weighted formula:** `FDP_global = Σ(FDP_i × Weight_i) / Σ(Weight_i)`
5. **Assess data quality** and apply penalty if needed
6. **Classify result** using standard thresholds (Natural/Hybrid/Unnatural)
7. **Document domain classification** and rationale in audit report

### For Existing Audits

- No action required - classifications remain valid
- **Optional:** Recalculate with proper weights for enhanced precision
- **Recommended:** Use proper weights for any future reassessments
- **Note:** Proper weighting typically strengthens existing conclusions

### For Hybrid/Multi-Domain Systems

- Identify **primary failure mode** (which risk is most severe?)
- Use that domain's weight vector
- **Document** multi-domain nature and rationale for primary classification
- **Alternative:** Create custom weight vector averaging relevant domains (advanced users only)

---

## Common Pitfalls

**Pitfall 1: Wrong domain classification**
- Symptom: FDP scores don't align with intuitive system dysfunction
- Solution: Verify primary function and failure mode, consider multi-domain nature

**Pitfall 2: Using generic weights out of habit**
- Symptom: All systems scored similarly regardless of type
- Solution: Consciously select domain before calculating

**Pitfall 3: False precision with poor data**
- Symptom: Reporting FDP_global = 1.283 when data is estimated
- Solution: Apply data quality penalty, round appropriately

**Pitfall 4: Creating custom weights without justification**
- Symptom: Adjusting weights to get desired outcome
- Solution: Use standard domain vectors unless strong empirical rationale exists

---

## Summary of Changes

**What Changes:**
- Add formal domain-specific weight vectors (8 domains)
- Add weighted calculation formula
- Add domain classification decision tree
- Add data quality penalty mechanism

**What Stays the Same:**
- All 8 FDP definitions
- Individual FDP calculation formulas
- Classification thresholds (Natural/Hybrid/Unnatural)
- 7ES linkages
- All other framework components

**Impact:**
- More systematic alignment with domain-specific risks
- Reduced auditor subjectivity in weighting
- Enhanced comparability across audits
- Typically strengthens existing classifications (lower scores for dysfunctional systems)

---

**Status:** Proposed addition to Master Reference File  
**Source:** KOSMOS FDP Tools and Templates Appendix  
**Backward Compatible:** Yes (no retroactive recalculation required)  
**Integration Point:** FDP Scoring Framework section of MRF

---