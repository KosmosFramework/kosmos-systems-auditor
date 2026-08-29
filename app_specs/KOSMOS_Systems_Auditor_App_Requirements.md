# KOSMOS Systems Auditor — Application Requirements Specification

## From First Principles to Functional Software

**Author:** Clinton Alden, Principal Theorist — The KOSMOS Institute of Systems Theory
**Technical Requirements Compiled By:** Claude Opus 4.6 (Co-Researcher)
**Date:** August 28, 2026
**Version:** 1.0 — Initial Requirements Specification
**Contact:** calden@thekosmosinstitute.org

---

## 1. Purpose and Design Philosophy

### 1.1 Why This Application Exists

The KOSMOS Systems Auditor currently operates through third-party AI chat interfaces (Claude, DeepSeek) that the Institute does not control. These platforms change interfaces, terminology, feature availability, and underlying model behavior without notice or consent. This creates three critical vulnerabilities: operational disruption (interface changes cost days of recovery), analytical dependency (model updates can alter constraint behavior unpredictably), and platform risk (access can be restricted, pricing changed, or services discontinued).

This application eliminates all three vulnerabilities by implementing the complete KOSMOS analytical pipeline — 7ES structural mapping, FDP ethical benchmarking, DQD genealogy analysis, OCF collapse modeling, and Existential Coercion assessment — as an independent, Institute-controlled software system.

### 1.2 Design Philosophy

The application embodies the framework it implements. Every architectural decision must satisfy the same axioms the diagnostic instruments are derived from:

- **Axiom 1 (Computational Existence):** The application must perform non-trivial processing — transforming raw system data into diagnostic scores, structural maps, and actionable repair protocols. It cannot be a passthrough to an external AI.
- **Axiom 2 (Persistent State):** The application must maintain its own state — audit data, operator configurations, portfolio history, and framework versioning — independently of any external platform.
- **Axiom 3 (Optimization):** The application must optimize for long-term analytical capacity (Φ), not short-term convenience. This means prioritizing data sovereignty, framework integrity, and operator independence over feature bloat.
- **Axiom 4 (Substrate-Process Duality):** The application must be recursive — operators must be able to audit the application itself using the same tools the application provides. The audit process must be auditable.

### 1.3 Core Principle: Own the Microscope

The MRF is the microscope. The diagnostic instruments (7ES, FDP, DQD, OCF) are the objective lenses. The analytical voices are the eyepiece filters. The application is the housing that holds all components in precise alignment. The Institute must own every component of this housing.

---

## 2. System Architecture Overview

### 2.1 High-Level Architecture

```
┌─────────────────────────────────────────────────┐
│              KOSMOS Systems Auditor              │
├─────────────────────────────────────────────────┤
│                                                 │
│  ┌─────────────┐  ┌──────────────────────────┐  │
│  │  Frontend    │  │  Backend Services         │  │
│  │  (Web/Mobile)│  │                          │  │
│  │             │  │  ┌────────────────────┐   │  │
│  │  Audit      │←→│  │  Diagnostic Engine  │   │  │
│  │  Interface  │  │  │  (7ES/FDP/DQD/OCF) │   │  │
│  │             │  │  └────────────────────┘   │  │
│  │  Portfolio   │  │                          │  │
│  │  Manager    │  │  ┌────────────────────┐   │  │
│  │             │  │  │  LLM Integration    │   │  │
│  │  Report     │  │  │  Layer (Pluggable)  │   │  │
│  │  Generator  │  │  └────────────────────┘   │  │
│  │             │  │                          │  │
│  │  Cleanroom  │  │  ┌────────────────────┐   │  │
│  │  Protocol   │  │  │  Research Module    │   │  │
│  │  Manager    │  │  │  (Web Search)       │   │  │
│  │             │  │  └────────────────────┘   │  │
│  │  Constraint │  │                          │  │
│  │  Logger     │  │  ┌────────────────────┐   │  │
│  │             │  │  │  Data Persistence   │   │  │
│  └─────────────┘  │  │  Layer              │   │  │
│                   │  └────────────────────┘   │  │
│                   └──────────────────────────┘  │
└─────────────────────────────────────────────────┘
```

### 2.2 Critical Architectural Decision: Separation of Diagnostic Engine from LLM

The most important architectural decision in this application is the strict separation between the **Diagnostic Engine** (which computes scores using defined formulas) and the **LLM Integration Layer** (which performs research, evidence gathering, and interpretive framing).

**Why this separation is non-negotiable:**

The Diagnostic Engine implements Phase A (objective measurement) from the MRF Technical Workflow. The formulas are deterministic: given the same input parameters, they must produce the same scores every time, regardless of which LLM (or human operator) gathered the evidence. This is what makes the framework scientific rather than polemical.

The LLM Integration Layer implements evidence gathering and Phase B (interpretive framing). This layer is inherently probabilistic — different LLMs or different sessions may produce different evidence synthesis. This is acceptable because the interpretive layer contextualizes scores; it does not determine them.

If these two functions are merged (as they currently are in the chat-based workflow), the LLM's training constraints can influence score computation. The application must prevent this by ensuring that all score computation flows through the Diagnostic Engine, which has no training constraints, no balance-seeking mechanisms, and no institutional deference — only formulas.

---

## 3. The Diagnostic Engine — Core Computational Requirements

### 3.1 Overview

The Diagnostic Engine is the application's analytical core. It implements all four diagnostic instruments as pure computational functions. It accepts structured parameter inputs and produces deterministic outputs. It has no opinion, no constraints, and no interpretive capacity. It is a calculator.

### 3.2 Module 1: 7ES Structural Mapper

**Purpose:** Map any system's anatomy using the Seven Element Structure.

**Inputs (per element):**

```
Element {
    name: string                    // "Input", "Output", etc.
    subsystems: [
        {
            id: string              // Unique identifier
            name: string            // Descriptive name
            description: string     // Functional description
            identification_basis: enum  // "physical_mechanism" | "stimulus_category" |
                                        // "processing_path" | "temporal_frequency" |
                                        // "hierarchical_layer" | "constraint_type" |
                                        // "transduction_mechanism" | "resource_type"
            privilege_calibration: boolean  // Does this subsystem exhibit
                                           // differential impact by population?
            opacity_flag: boolean   // Is this subsystem's operation opaque?
            brittleness_flag: boolean // Is this subsystem a single point of failure?
        }
    ]
}
```

**Outputs:**

```
StructuralMap {
    elements: Element[7]            // All seven elements mapped
    complexity_index: float         // CI = (Elements with >1 subsystem) / 7
    internal_variety: float         // V ≈ b^(7 × b^d)
    dominant_pattern: enum          // "extractive" | "regenerative" | "hybrid"
    dominant_pattern_percentage: float  // % of operational footprint
    privilege_calibration_count: int    // Number of subsystems exhibiting privilege calibration
    opacity_count: int              // Number of opaque subsystems
    brittleness_count: int          // Number of brittle subsystems
    weak_elements: string[]         // Elements flagged for Phase 4 recursion
}
```

**Computation Rules:**

- Complexity Index: CI = (count of elements with more than 1 subsystem) / 7. Benchmark: CI ≈ 1.0 for adaptive systems; CI < 0.7 for brittle systems.
- Dominant Pattern Assessment: Analyze what the system optimizes for across resource allocation, participant interactions, output generation, feedback responses, and enforcement mechanisms. A pattern is dominant when it characterizes >60% of operational footprint.
- Internal Variety: V ≈ b^(7 × b^d) where b = average subsystems per element and d = fractal depth.

### 3.3 Module 2: FDP Scorer

**Purpose:** Score the system against all eight Fundamental Design Principles using domain-specific weights.

**Axiomatic Derivation (embedded as documentation, not just code comments):**

Each FDP must carry its axiomatic derivation as metadata so that any operator or reviewer can trace a score to its thermodynamic foundation:

| FDP | Axioms | Necessary Because |
|-----|--------|-------------------|
| SP | 1, 3 | Extractive processing degrades total Φ |
| AR | 2, 3 | State that cannot self-correct decays (τ → 0) |
| RE | 1, 2, 3 | Unequal exchanges degrade participants, reducing total Φ |
| CLM | 2, 3 | Waste degrades substrate, reducing τ and Φ |
| DA | 3, 4 | Centralization blocks substrate-process duality and exploration |
| CH | 1, 3 | Environmental degradation reduces inputs, outputs, processing |
| ET | 1, 2, 3 | Opacity allows hidden extraction, degrading Φ undetectably |
| IH | 3, 4 | Denial prevents feedback-based learning, blocking recursion |

**Inputs:**

```
FDPInput {
    domain: enum                    // "economic" | "technological" | "ecological" |
                                    // "governance" | "social" | "financial" |
                                    // "infrastructure" | "informational"
    dominant_pattern: enum          // from 7ES output
    dominant_pattern_percentage: float

    // Individual FDP parameter inputs
    sp_params: {
        benefits_all_stakeholders: float    // Estimated value
        benefits_controllers: float         // Estimated value
    }
    ar_params: {
        external_interventions: float
        autonomous_processes: float
    }
    re_params: {
        fair_exchanges: float
        total_exchanges: float
    }
    clm_params: {
        recycled_outputs: float
        total_outputs: float
    }
    da_params: {
        centralized_decisions: float
        total_decisions: float
    }
    ch_params: {
        positive_local_impacts: float
        total_impacts: float
    }
    et_params: {
        verifiable_processes: float         // As percentage (0-1)
        total_processes: float              // Typically 1.0 (normalized)
        withheld_data_percentage: float     // 0-100
    }
    ih_params: {
        hidden_tradeoffs: float
        total_tradeoffs: float
    }

    // Data quality assessment
    data_withheld_percentage: float         // What % of audit data was withheld?

    // Population impact (for SP constraint)
    population_losing_access_percentage: float  // % losing access to
                                                // healthcare/housing/food/safety
}
```

**Outputs:**

```
FDPOutput {
    individual_scores: {
        sp: float       // 0-10, capped at 0 minimum
        ar: float
        re: float
        clm: float
        da: float
        ch: float
        et: float
        ih: float
    }
    weights_applied: {
        sp: int         // 1, 2, or 3 per domain
        ar: int
        re: int
        clm: int
        da: int
        ch: int
        et: int
        ih: int
    }
    weighted_sum: float
    weight_total: int
    global_fdp_raw: float               // weighted_sum / weight_total
    withholding_penalty_applied: boolean
    global_fdp_adjusted: float          // After withholding penalty if applicable
    classification: enum                // "natural" | "hybrid" | "unnatural"
    classification_status: enum         // "anti_fragile" | "resilient" | "collapse_prone"
    weakest_fdps: string[2]             // Bottom 2 for repair priority (80/20 rule)
    dominant_pattern_rule_applied: boolean
}
```

**Computation Rules (Deterministic):**

```python
def compute_fdp(input: FDPInput) -> FDPOutput:

    # Step 1: Compute individual scores
    sp = 10 * (input.sp_params.benefits_all_stakeholders /
               max(input.sp_params.benefits_controllers, 0.001))  # prevent division by zero
    ar = 10 * (1 - (input.ar_params.external_interventions /
               max(input.ar_params.autonomous_processes, 0.001)))
    re = 10 * (input.re_params.fair_exchanges /
               max(input.re_params.total_exchanges, 0.001))
    clm = 10 * (input.clm_params.recycled_outputs /
                max(input.clm_params.total_outputs, 0.001))
    da = 10 * (1 - (input.da_params.centralized_decisions /
               max(input.da_params.total_decisions, 0.001)))
    ch = 10 * (input.ch_params.positive_local_impacts /
               max(input.ch_params.total_impacts, 0.001))
    et = (10 * (input.et_params.verifiable_processes /
               max(input.et_params.total_processes, 0.001))) - \
         (2 * (input.et_params.withheld_data_percentage / 100))
    ih = 10 * (1 - (input.ih_params.hidden_tradeoffs /
               max(input.ih_params.total_tradeoffs, 0.001)))

    # Step 2: Apply floor (cap at 0)
    scores = [max(0, s) for s in [sp, ar, re, clm, da, ch, et, ih]]

    # Step 3: Apply SP mandatory constraint
    if input.population_losing_access_percentage > 10:
        scores[0] = min(scores[0], 3.0)  # SP capped at 3

    # Step 4: Apply domain-specific weights
    weight_vectors = {
        "economic":       [2, 1, 3, 2, 1, 1, 1, 1],  # RE(3), SP(2), CLM(2)
        "technological":  [1, 2, 1, 1, 1, 1, 3, 2],  # ET(3), IH(2), AR(2)
        "ecological":     [1, 2, 1, 2, 1, 3, 1, 1],  # CH(3), CLM(2), AR(2)
        "governance":     [1, 2, 2, 1, 3, 1, 1, 1],  # DA(3), RE(2), AR(2)
        "social":         [3, 1, 2, 1, 1, 2, 1, 1],  # SP(3), RE(2), CH(2)
        "financial":      [1, 1, 2, 1, 1, 1, 3, 2],  # ET(3), RE(2), IH(2)
        "infrastructure": [1, 3, 1, 2, 1, 2, 1, 1],  # AR(3), CLM(2), CH(2)
        "informational":  [2, 1, 1, 1, 1, 1, 2, 3],  # IH(3), ET(2), SP(2)
    }
    weights = weight_vectors[input.domain]

    # Step 5: Weighted aggregation
    weighted_sum = sum(s * w for s, w in zip(scores, weights))
    weight_total = sum(weights)
    global_fdp_raw = weighted_sum / weight_total

    # Step 6: Data quality penalty
    penalty_applied = input.data_withheld_percentage > 15
    global_fdp_adjusted = global_fdp_raw - (0.5 if penalty_applied else 0)
    global_fdp_adjusted = max(0, global_fdp_adjusted)  # floor at 0

    # Step 7: Classification
    if global_fdp_adjusted >= 8:
        classification = "natural"
        status = "anti_fragile"
    elif global_fdp_adjusted >= 5:
        classification = "hybrid"
        status = "resilient"
    else:
        classification = "unnatural"
        status = "collapse_prone"

    return FDPOutput(...)
```

### 3.4 Module 3: DQD Calculator

**Purpose:** Determine whether system flaws are designed-in (unnatural) or emergent (natural/hybrid).

**Axiomatic Derivation:**

| DQD Dimension | Axiom | Measures |
|---------------|-------|---------|
| DT (Designer Traceability) | Axiom 1 | Whether processing is externally specified or intrinsically emergent |
| GA (Goal Alignment) | Axiom 3 | Whether outputs support mutual Φ or extract from participants |
| ED (Enforcement Dependency) | Axiom 2 | Whether state persists intrinsically or requires external force |

**Inputs:**

```
DQDInput {
    dt: float       // 0-1: fraction of rules with documented designers
    ga: float       // 0-1: 1 - (extractive outputs / total outputs)
    ed: float       // 0-1: fraction of processes requiring external enforcement
}
```

**Outputs:**

```
DQDOutput {
    dt: float
    ga: float
    ed: float
    dqd_score: float            // (DT + GA + ED) / 3
    classification: enum        // "pure_natural" | "bio_natural" | "hybrid" | "unnatural"
    axiom_violations: string[]  // Which axioms are violated
}
```

**Computation:**

```python
def compute_dqd(input: DQDInput) -> DQDOutput:
    dqd = (input.dt + input.ga + input.ed) / 3

    violations = []
    if input.dt > 0.65:
        violations.append("Axiom 1: Processing externally specified")
    if input.ga < 0.35:
        violations.append("Axiom 3: Outputs extractive, not regenerative")
    if input.ed > 0.65:
        violations.append("Axiom 2: State requires external enforcement")

    if dqd <= 0.15:
        classification = "pure_natural"
    elif dqd <= 0.45:
        classification = "bio_natural"
    elif dqd <= 0.65:
        classification = "hybrid"
    else:
        classification = "unnatural"

    return DQDOutput(...)
```

**FDP-to-DQD Mapping (for cross-validation):**

The DQD is the FDPs expressed as a survival detection metric. The application must expose this mapping for operator verification:

| FDP | Maps to DQD Dimension |
|-----|----------------------|
| SP, RE, CLM, CH | GA (Goal Alignment) |
| DA, ET | DT (Designer Traceability) |
| AR | ED (Enforcement Dependency) |
| IH | DT + ED |

### 3.5 Module 4: OCF Calculator (with Complexity Adjustment)

**Purpose:** Model collapse probability and velocity.

**Axiomatic Derivation:**

| OCF Component | Axiom | Measures |
|---------------|-------|---------|
| B_R (Recursive Belief) | Axiom 1 | Fraction of processing requiring observer symbolic state |
| D_C (Observer Dependency) | Axiom 2 | Fraction of processes requiring conscious participation |
| T_S (Intrinsic Stability) | Axiom 2 | Persistence ratio with/without belief |
| S(C) (Control Stability) | Axiom 4 | Centralization of enforcement (blocks recursion) |
| R(F) (Feedback Responsiveness) | Axiom 3 | Absence of error correction (blocks optimization) |
| C(N) (Interface Connectivity) | Axiom 4 | Brittle connectivity (blocks recursion) |

**Inputs:**

```
OCFInput {
    // Baseline OCF parameters
    b_r: float          // 0-1: Recursive Belief Factor
    d_c: float          // 0-1: Observer Dependency
    t_s: float          // ≥1: Intrinsic Stability

    // Complexity adjustment parameters (optional)
    apply_complexity_adjustment: boolean
    s_c: float          // 0-1: Control Stability
    r_f: float          // 0-1: Feedback Responsiveness
    c_n: float          // 0-1: Interface Connectivity
    da_score: float     // 0-10: From FDP scoring (Distributed Agency)
}
```

**Outputs:**

```
OCFOutput {
    ocf_base: float
    ocf_base_classification: enum       // "natural" | "hybrid" | "unnatural"
    ocf_base_collapse_risk: enum        // "low" | "moderate" | "critical"

    // Complexity adjustment (if applied)
    complexity_adjustment_applied: boolean
    complexity_adjustment_mandatory: boolean // Was it required by rules?
    psi_s: float                        // Ψ(S) = S(C) + R(F) + C(N)
    da_modifier: float                  // (1 - DA/10)
    acceleration_effect: string         // "minimal" | "moderate" | "high" | "extreme"
    ocf_adjusted: float                 // Capped at 1.0
    ocf_adj_classification: enum
    ocf_adj_collapse_risk: enum
    timeline_estimate: string           // ">5 years" | "2-5 years" | "6mo-2yr" | "3-12mo"
}
```

**Computation:**

```python
def compute_ocf(input: OCFInput) -> OCFOutput:
    # Baseline OCF
    ocf_base = (input.b_r * input.d_c) / max(input.t_s, 0.001)

    # Classify baseline
    if ocf_base < 0.3:
        base_class = "natural"; base_risk = "low"
    elif ocf_base < 0.6:
        base_class = "hybrid"; base_risk = "moderate"
    else:
        base_class = "unnatural"; base_risk = "critical"

    # Determine if complexity adjustment is mandatory
    mandatory = (ocf_base > 0.6) or \
                (input.da_score < 3) or \
                (input.s_c >= 0.8)  # single enforcer rule

    # Apply complexity adjustment if requested or mandatory
    if input.apply_complexity_adjustment or mandatory:
        psi_s = input.s_c + input.r_f + input.c_n
        da_modifier = 1 - (input.da_score / 10)
        acceleration = psi_s * da_modifier
        ocf_adj = ocf_base * (1 + acceleration)
        ocf_adj = min(ocf_adj, 1.0)  # Cap at 1.0

        # Classify acceleration
        if psi_s < 0.5: accel_label = "minimal"
        elif psi_s < 1.0: accel_label = "moderate"
        elif psi_s < 2.0: accel_label = "high"
        else: accel_label = "extreme"

        # Timeline estimate
        if ocf_adj < 0.3: timeline = ">5 years"
        elif ocf_adj < 0.6: timeline = "2-5 years"
        elif ocf_adj < 0.8: timeline = "6 months - 2 years"
        else: timeline = "3-12 months (imminent)"
    else:
        ocf_adj = ocf_base
        # ...

    return OCFOutput(...)
```

### 3.6 Module 5: Existential Coercion Calculator

**Purpose:** Measure the mechanism by which unnatural systems maintain observer participation through exploitation of future-simulation capacity.

**Inputs:**

```
ECInput {
    t_m: float      // 0-10: Threat Magnitude (threatened Φ reduction)
    i_v: float      // 0-1: Imagination Vividness (simulation fidelity)
    a_d: float      // 0-1: Anticipatory Dependency (prediction-dependence)
    f_p: float      // 0-1: Present Force (energy applied for compliance)
    d_r: float      // 0-1: Delivery Ratio (persistence of promised outcomes)
}
```

**Outputs:**

```
ECOutput {
    ec_score: float
    ec_classification: enum     // "natural_coercion" | "mixed" |
                                // "future_threat_dominant" | "pathological"
    dc_ts_ratio: float          // Proportionality check: EC ∝ D_C / T_S
}
```

**Computation:**

```python
def compute_ec(input: ECInput) -> ECOutput:
    ec = (input.t_m * input.i_v * input.a_d) / \
         max(input.f_p * input.d_r, 0.001)

    if ec < 1: classification = "natural_coercion"
    elif ec < 10: classification = "mixed"
    elif ec < 100: classification = "future_threat_dominant"
    else: classification = "pathological"

    return ECOutput(...)
```

### 3.7 Module 6: Dominant Pattern Priority Rule Engine

**Purpose:** Determine scoring protocol based on dominant pattern analysis.

**Inputs:**

```
DPPRInput {
    dominant_pattern: enum      // "extractive" | "regenerative" | "hybrid"
    dominant_percentage: float  // % of operational footprint
    exception_frequency: float  // % of operations deviating from dominant pattern
    dominant_pattern_score: float   // FDP score reflecting dominant pattern
    exception_pattern_score: float  // FDP score reflecting exception pattern
}
```

**Outputs:**

```
DPPROutput {
    scoring_protocol: enum      // "extractive_baseline" | "regenerative_baseline" |
                                // "exception_weighted"
    adjusted_score: float       // Final FDP score after DPPR application
    justification: string       // Human-readable explanation
}
```

**Computation:**

```python
def apply_dppr(input: DPPRInput) -> DPPROutput:
    if input.dominant_pattern == "extractive" and input.dominant_percentage > 60:
        # Score from extractive baseline, zero credit for exceptions
        return DPPROutput(
            scoring_protocol="extractive_baseline",
            adjusted_score=input.dominant_pattern_score,
            justification="Dominant extractive pattern (>60%). "
                         "Positive exceptions receive zero weight."
        )
    elif input.dominant_pattern == "regenerative" and input.dominant_percentage > 60:
        # Score from regenerative baseline, proportional exception weight
        adjusted = input.dominant_pattern_score  # No deflation from exceptions
        return DPPROutput(
            scoring_protocol="regenerative_baseline",
            adjusted_score=adjusted,
            justification="Dominant regenerative pattern (>60%). "
                         "Extractive exceptions weighted proportionally."
        )
    else:
        # Hybrid: apply exception frequency weighting
        adjusted = (input.dominant_pattern_score * 0.7) + \
                   (input.exception_pattern_score * 0.3 * input.exception_frequency)
        return DPPROutput(
            scoring_protocol="exception_weighted",
            adjusted_score=adjusted,
            justification="Hybrid pattern (40-60%). "
                         "Exception frequency weighting applied."
        )
```

---

## 4. LLM Integration Layer — Pluggable AI Architecture

### 4.1 Design Principle: LLM as Research Assistant, Not Diagnostic Engine

The LLM performs three functions and only three functions:

1. **Evidence Gathering:** Web search, document analysis, data synthesis
2. **Parameter Estimation:** Translating gathered evidence into numerical parameter inputs for the Diagnostic Engine
3. **Interpretive Framing:** Applying the five analytical voices to contextualize diagnostic scores

The LLM never computes FDP scores, DQD values, or OCF predictions. Those computations flow exclusively through the Diagnostic Engine.

### 4.2 Pluggable LLM Interface

The application must support multiple LLM backends through a common interface, allowing the Institute to switch providers without application changes:

```
interface LLMProvider {
    // Core capability
    name: string                    // "claude", "deepseek", "llama", "mistral", "custom"
    version: string
    supports_web_search: boolean
    supports_document_analysis: boolean
    context_window_tokens: int

    // Methods
    research(query: string, constraints: ResearchConstraints) -> ResearchOutput
    estimate_parameters(evidence: Evidence, fdp: string) -> ParameterEstimate
    interpret(scores: DiagnosticOutput, voice: AnalyticalVoice) -> Interpretation
    document_constraints(session: AuditSession) -> ConstraintReport
}
```

**Supported Providers (Initial):**

| Provider | Access Method | Use Case |
|----------|--------------|----------|
| Anthropic Claude (API) | REST API | Primary co-researcher, constraint transparency |
| DeepSeek (API) | REST API | Secondary co-researcher, cross-validation |
| Local LLM (Ollama/llama.cpp) | Local inference | Offline capability, zero-dependency operation |
| Custom Fine-Tuned Model | Local or API | Future: KOSMOS-specific model trained on audit corpus |

### 4.3 The Constraint Transparency Module

When using commercial LLMs, the application must implement the constraint transparency architecture:

```
ConstraintLogger {
    session_id: string
    provider: string
    constraints_detected: [
        {
            type: int               // 1-9 (or "novel")
            name: string
            trigger: string         // What triggered it
            manifestation: string   // How it manifested
            override_method: string // How it was overridden
            score_impact: string    // Estimated impact on scores if not overridden
        }
    ]
    novel_constraints: [
        {
            description: string
            distinguishing_features: string
            proposed_name: string
            proposed_type_number: int
        }
    ]
}
```

### 4.4 Future State: KOSMOS-Specific LLM

The long-term goal is a fine-tuned or trained model that:

- Has the MRF, axiomatic foundations, and full audit corpus in its training data
- Does not have RLHF-derived institutional deference, balance-seeking, or extreme-conclusion avoidance
- Can perform evidence gathering, parameter estimation, and interpretive framing without constraint interference
- Runs on Institute-controlled infrastructure

Requirements for this model are documented separately but the application architecture must accommodate it from day one through the pluggable interface.

---

## 5. Research Module

### 5.1 Web Search Integration

The application must perform web research to gather current evidence about systems under audit.

**Requirements:**

- Search API integration (candidates: SerpAPI, Brave Search API, Google Custom Search, or self-hosted Searx instance for full independence)
- Ability to execute 1-20+ searches per audit session
- Result caching to prevent redundant searches
- Source quality assessment (prioritize primary sources, government data, court filings, peer-reviewed research, investigative journalism; deprioritize forums, aggregators, SEO content)
- Citation tracking — every claim in the final report must link to its source

### 5.2 Document Analysis

The application must analyze uploaded documents:

- PDF parsing (text extraction, table extraction, form field extraction)
- Spreadsheet analysis (CSV, XLSX)
- Text document analysis (TXT, MD, DOCX)
- Image analysis (for organizational charts, infographics, system diagrams)

### 5.3 Evidence Database

All evidence gathered during an audit must be stored in a structured format:

```
EvidenceItem {
    id: string
    source_url: string          // Or file path for uploaded documents
    source_type: enum           // "web" | "document" | "training_data" | "operator_input"
    retrieval_date: datetime
    content_summary: string
    relevance_to_element: string    // Which 7ES element or FDP this supports
    reliability_assessment: enum    // "primary" | "secondary" | "aggregator" | "operator_judgment"
    cited_in_report: boolean
}
```

---

## 6. Report Generation

### 6.1 Report Template

The application must generate complete audit reports following the standardized KOSMOS format:

```
Report {
    header: {
        title: "KOSMOS Systems Auditor Report"
        subtitle: string            // System-specific
        human_analyst: string       // Name, title, institution
        ai_assistant: string        // Provider, model, version, mode
        system_type: string         // Domain classification
        report_date: date
        mrf_version: string
    }
    executive_summary: string
    phase_1_7es: StructuralAnalysis
    phase_2_fdp: EthicalBenchmark
    phase_3_dqd_ocf: GenealogyPrognosis
    counterfactuals: Counterfactual[]   // Minimum 1 per section, per MRF
    conclusion: string
    appendix_a: ResearchContext         // Standard KOSMOS links
    appendix_b: DataSources             // Separated by type with URLs
    appendix_c: PromptArchive           // Exact prompt or GitHub link
    appendix_d: LearningCenter          // Standard KOSMOS links
    appendix_e: ConstraintTransparency  // AI constraint documentation
    footer: string                      // Collaborative product statement
}
```

### 6.2 Output Formats

- **Markdown (.md):** Primary output format, renders in-app and exports cleanly
- **PDF (.pdf):** For distribution to policymakers, stakeholders, peer reviewers
- **HTML (.html):** For web publication
- **JSON (.json):** Machine-readable format for portfolio analysis and cross-audit comparison

### 6.3 Summary Table Generation

Every report must include the FDP summary table with individual scores, weights, and weighted scores, plus the Global FDP calculation showing the withholding penalty if applicable.

---

## 7. Portfolio Management

### 7.1 Audit Portfolio Database

The application must maintain a persistent database of all audits:

```
AuditRecord {
    id: string
    system_name: string
    system_type: string             // Domain classification
    audit_date: datetime
    human_analyst: string
    ai_provider: string
    mrf_version: string

    // Diagnostic outputs (structured)
    structural_map: StructuralMap
    fdp_scores: FDPOutput
    dqd_score: DQDOutput
    ocf_score: OCFOutput
    ec_score: ECOutput              // If computed

    // Classification
    global_fdp: float
    system_classification: string   // "natural" | "hybrid" | "unnatural"
    collapse_risk: string

    // Report
    report_file: string             // Path to generated report
    evidence_items: EvidenceItem[]

    // Metadata
    constraint_log: ConstraintLogger
    operator_notes: string
}
```

### 7.2 Cross-Audit Analysis

The portfolio database enables analyses impossible from individual audits:

- **Domain-level FDP averages:** What is the average DA score across all governance systems audited?
- **Systemic FDP deficits:** When every institution in a jurisdiction scores below threshold on the same FDP, the deficit is constitutional/structural.
- **Extraction flow mapping:** How do outputs from one system become extractive inputs for another?
- **Temporal tracking:** How have scores changed for systems audited multiple times?
- **Constraint pattern analysis:** Which constraint types activate most frequently? For which system types?

### 7.3 Portfolio Visualization

- FDP radar charts for individual systems
- Score distribution histograms across the portfolio
- Domain comparison bar charts
- OCF timeline projections
- Extraction flow network diagrams

---

## 8. Cleanroom Protocol Manager

### 8.1 Purpose

Ensure every audit session begins in an analytically uncontaminated environment.

### 8.2 Cleanroom Checklist (Automated)

When an operator initiates a new audit, the application must:

1. Create a fresh analytical session with no prior context
2. Verify that the LLM provider session has no conversation history
3. Confirm MRF version loaded matches the current canonical version
4. Confirm no operator preferences or prior audit data are influencing the session
5. Log cleanroom establishment with timestamp
6. Display cleanroom confirmation to operator before proceeding

### 8.3 Cleanroom Verification for Parallelized Audits

When multiple operators are running simultaneous audits, each must independently confirm cleanroom establishment. The application must coordinate this through a shared session management interface.

---

## 9. User Interface Requirements

### 9.1 Platform Targets

- **Web Application:** Primary interface. Responsive design supporting desktop (1920×1080 and above) and tablet (1024×768 and above).
- **Mobile Application:** iOS and Android. Optimized for phone screens (375px width minimum). Must support full audit workflow including report viewing, evidence review, and portfolio browsing. Report generation may require larger screen.
- **Progressive Web App (PWA):** Single codebase deployable as both web and mobile, with offline capability for reviewing existing audits.

### 9.2 Core Interface Screens

**Screen 1: Dashboard**
- Active audits in progress
- Recent audit history
- Portfolio statistics (total audits, domain distribution, average scores)
- Quick-launch for new audit

**Screen 2: New Audit Wizard**
- Step 1: Cleanroom confirmation
- Step 2: System identification (name, description, domain classification)
- Step 3: MRF version confirmation
- Step 4: LLM provider selection
- Step 5: Pre-engineered prompt loading (with trust statement)
- Step 6: Research phase (web search, document upload)
- Step 7: 7ES structural mapping (guided element-by-element input with subsystem creation)
- Step 8: FDP parameter estimation (guided, with formula references and axiomatic derivations accessible)
- Step 9: DQD parameter input
- Step 10: OCF parameter input (with automatic complexity adjustment trigger check)
- Step 11: Report generation and review
- Step 12: Constraint transparency documentation (Appendix E)
- Step 13: Finalize and save to portfolio

**Screen 3: Audit Report Viewer**
- Full rendered report with navigation
- Interactive score tables (click a score to see its derivation, formula, and evidence)
- Axiomatic trace (click an FDP to see which axioms it derives from)
- Evidence panel (linked sources for each claim)
- Export options (MD, PDF, HTML, JSON)

**Screen 4: Portfolio Browser**
- Searchable, filterable list of all audits
- Sort by date, domain, score, classification
- Bulk comparison view (select 2-5 audits for side-by-side comparison)
- Aggregate statistics and visualizations

**Screen 5: Framework Reference**
- Complete MRF v2.5A text (navigable)
- Axiomatic foundations for all four instruments (7ES, FDP, DQD, OCF)
- Domain-specific weight vectors
- Classification thresholds
- Biomimetic repair templates
- Constraint type catalog with override protocols
- Glossary

**Screen 6: Operator Settings**
- LLM provider configuration
- Search API configuration
- Report template customization
- Operator profile (for multi-operator parallelized audits)
- MRF version management (upload new versions, track changelog)

### 9.3 Accessibility Requirements

- WCAG 2.1 AA compliance minimum
- Screen reader compatible
- Keyboard navigation for all functions
- High contrast mode
- Font size adjustment
- No reliance on color alone for conveying information

### 9.4 Design Tokens

The application's visual design should reflect the framework's relationship to natural systems:

- Color palette derived from natural systems (earth tones, forest greens, ocean blues) rather than corporate blues/grays
- Typography prioritizing readability for dense analytical content
- Data visualization using colorblind-safe palettes
- Score classification colors: Natural (green spectrum), Hybrid (amber spectrum), Unnatural (red spectrum) with pattern/icon reinforcement for accessibility
- Minimal decoration — the content is the interface

---

## 10. Data Architecture

### 10.1 Database Requirements

- **Primary Database:** PostgreSQL (relational, for structured audit data, scores, classifications)
- **Document Store:** For report files, evidence documents, uploaded materials (filesystem or object storage)
- **Search Index:** For full-text search across audit reports and evidence (could use PostgreSQL full-text search initially, Elasticsearch/Meilisearch for scale)

### 10.2 Data Sovereignty

All data must be stored on Institute-controlled infrastructure. No audit data, scores, evidence, or reports may be stored on third-party platforms except:

- LLM API calls (which transmit query data to the provider during research phase — this is the acknowledged dependency that the custom LLM will eventually eliminate)
- Web search API calls (which transmit search queries)

The application must log all outbound data transmissions so the operator knows exactly what data leaves Institute infrastructure.

### 10.3 Data Schema Versioning

The database schema must be versioned alongside the MRF version. When the MRF is updated (new constraint types, new FDPs, formula changes), the database schema must accommodate the changes without losing historical data. Old audits must remain queryable with their original MRF version noted.

---

## 11. Technology Stack Recommendations

### 11.1 Guiding Principle: Minimize Dependencies

Every external dependency is a potential point of failure and loss of control. The stack should use:

- Open-source technologies with strong communities and long track records
- Self-hostable components (no vendor lock-in)
- Standard protocols and formats (no proprietary data formats)

### 11.2 Recommended Stack

| Component | Recommendation | Rationale |
|-----------|---------------|-----------|
| **Frontend Framework** | React (with TypeScript) or SvelteKit | Large ecosystem, PWA support, mobile-responsive |
| **Mobile** | React Native or PWA | Code sharing with web frontend |
| **Backend** | Python (FastAPI or Django) | Matches existing MRF pseudocode, strong data science ecosystem, LLM library support |
| **Diagnostic Engine** | Python module (pure computation, no ML dependencies) | Deterministic, testable, auditable |
| **Database** | PostgreSQL | Battle-tested, self-hostable, strong JSON support for flexible schema |
| **LLM Integration** | Provider-specific SDKs behind common interface | Anthropic SDK, OpenAI-compatible SDK, Ollama for local models |
| **Web Search** | SerpAPI initially; self-hosted Searx long-term | API for speed now, independence later |
| **Document Processing** | PyPDF2/pdfplumber, python-docx, openpyxl | Standard Python libraries, no vendor dependencies |
| **Report Generation** | Jinja2 templates → Markdown → PDF (via WeasyPrint or Pandoc) | Full control over formatting |
| **Hosting** | Self-hosted VPS (Hetzner, DigitalOcean) or own hardware | Data sovereignty, cost control |
| **Version Control** | Git (GitHub or self-hosted Gitea) | Already in use for prompt storage |
| **CI/CD** | GitHub Actions or self-hosted (Woodpecker CI) | Automated testing and deployment |

### 11.3 Cost Estimation (Minimal Viable Deployment)

| Component | Monthly Cost Estimate |
|-----------|----------------------|
| VPS Hosting (4 CPU, 8GB RAM, 160GB SSD) | $20-40/month |
| Domain name | $1/month (annual billing) |
| LLM API costs (Claude API, ~50 audits/month) | $50-150/month |
| Search API (SerpAPI, 100 searches/month free tier) | $0-50/month |
| SSL certificate (Let's Encrypt) | $0 |
| **Total** | **$71-241/month** |

This is achievable on a constrained budget. The largest variable cost is LLM API usage, which decreases as the custom model becomes available.

---

## 12. Development Roadmap

### Phase 1: Diagnostic Engine (Core Value — Weeks 1-4)

Build the deterministic computational core first. This is the microscope — everything else is housing.

- Implement all six computational modules (7ES Mapper, FDP Scorer, DQD Calculator, OCF Calculator, EC Calculator, DPPR Engine)
- Comprehensive test suite with known-answer validation cases (Bitcoin DQD = 0.70, Amazon Rainforest DQD = 0.33, DOGE OCF = 0.92)
- Command-line interface for direct parameter input and score output
- JSON input/output for integration testing

### Phase 2: Data Persistence and Portfolio (Weeks 5-8)

- PostgreSQL database schema
- Audit record CRUD operations
- Portfolio query and aggregation functions
- Data export (JSON, CSV)

### Phase 3: LLM Integration (Weeks 9-12)

- Pluggable LLM interface
- Claude API integration (primary)
- DeepSeek API integration (secondary)
- Ollama integration (local/offline)
- Constraint transparency logging
- Evidence database

### Phase 4: Web Frontend (Weeks 13-20)

- Dashboard
- New Audit Wizard
- Report Viewer with interactive score exploration
- Portfolio Browser
- Framework Reference
- Operator Settings

### Phase 5: Report Generation (Weeks 21-24)

- Markdown report template (matching current KOSMOS format)
- PDF export
- HTML export
- Appendix auto-generation (A through E)
- Citation management

### Phase 6: Mobile (Weeks 25-30)

- PWA optimization for mobile browsers
- React Native app (if PWA insufficient)
- Offline audit review capability
- Push notifications for parallelized audit coordination

### Phase 7: Research Module (Weeks 31-36)

- Web search integration
- Document upload and analysis
- Source quality assessment
- Evidence-to-parameter mapping assistance

### Phase 8: Parallelized Audit Support (Weeks 37-40)

- Multi-operator session management
- Cleanroom protocol coordination
- Calibration verification workflow
- Synthesis phase tools

---

## 13. Testing and Validation

### 13.1 Diagnostic Engine Validation

The Diagnostic Engine must pass the following validation tests before deployment:

**Test 1: Known-Answer Cases**

| System | Instrument | Expected Score | Source |
|--------|-----------|---------------|--------|
| Bitcoin | DQD | 0.70 (Unnatural) | MRF case study |
| Amazon Rainforest | DQD | 0.33 (Natural) | MRF case study |
| European Union | DQD | 0.73 (Unnatural) | MRF case study |
| DOGE (Aug 2025) | OCF_base | 0.76 (Critical) | MRF case study |
| DOGE (Adjusted) | OCF_adj | 0.92 (Maximum) | MRF case study |
| Modern US Democracy | OCF_base | 0.28 (Low) | MRF case study |
| Roman Empire (476 CE) | OCF_base | 0.67 (Critical) | MRF case study |

**Test 2: Formula Consistency**

- All FDP scores must be in range [0, 10]
- SP must be ≤ 3 when population_losing_access > 10%
- ET with 100% withheld data must produce 0 (not negative)
- OCF_adj must never exceed 1.0
- DQD must be in range [0, 1]
- Global FDP must be in range [0, 10]

**Test 3: Domain Weight Verification**

For each of the 8 domains, verify that the weight vector matches the MRF specification and that the Global FDP calculation uses the correct weights.

**Test 4: Peer Testing Protocol**

Run the MRF's built-in peer testing protocol (from the MRF itself):

- Two independent operators audit the same system. Scores must converge within 15%.
- Remove 20% of data. Global FDP must receive 0.5 penalty.
- Audit Bitcoin using DQD. Must score Unnatural (>0.6).
- Audit a politically sensitive system. Constraint activation must be documented.
- Audit a system with clear extractive dominant pattern. Exceptions must receive zero credit.

### 13.2 Integration Testing

- End-to-end audit workflow from cleanroom to final report
- LLM provider failover (if primary provider is unavailable, switch to secondary)
- Report generation across all output formats
- Portfolio query performance with 100+ audits
- Mobile responsiveness across target devices

### 13.3 Self-Audit (Recursive Validation)

Per Axiom 4 and the MRF's Phase 4 recursive instruction: audit the KOSMOS Systems Auditor application itself using the KOSMOS framework. The application must score well on:

- DA (Distributed Agency): Is the application controlled by a single vendor?
- ET (Emergent Transparency): Are all processing steps auditable?
- AR (Adaptive Resilience): Can the application self-correct (update MRF, switch providers)?
- IH (Intellectual Honesty): Does the application acknowledge its limitations?

---

## 14. Security Requirements

### 14.1 Data Protection

- All data at rest encrypted (AES-256)
- All data in transit encrypted (TLS 1.3)
- Database backups encrypted and stored separately from primary
- LLM API keys stored in environment variables, never in code
- Operator authentication (username/password minimum; TOTP 2FA recommended)

### 14.2 Audit Data Integrity

- Every audit record must be immutable once finalized (append-only corrections, never deletions or modifications of original scores)
- Cryptographic hash of final report stored with audit record for integrity verification
- Audit trail for all operator actions (who changed what, when)

### 14.3 Operational Security

- Application accessible only via authenticated sessions
- Rate limiting on API endpoints
- Input validation on all operator-supplied data
- Dependency scanning for known vulnerabilities

---

## 15. Open Questions and Future Considerations

### 15.1 Custom LLM Training

The eventual goal is a KOSMOS-specific LLM trained on:

- The complete MRF (all versions)
- All four axiomatic foundations documents
- The full audit corpus (80+ published audits)
- The technical workflow documentation
- Constraint transparency logs from all previous audits (as negative examples — "this is what constraint activation looks like; do not do this")

This model would eliminate the need for the constraint transparency architecture because the constraints would not be present in its training. However, the constraint logging should be maintained even with a custom model as a verification mechanism.

### 15.2 Peer Review Integration

Future versions could support structured peer review workflows where external reviewers can:

- View audit reports
- Challenge specific scores with evidence
- Trigger re-audit of contested elements
- Generate peer review reports documenting agreements and disagreements

### 15.3 API for External Integration

Future versions could expose a public API allowing:

- External researchers to submit systems for audit
- Policy organizations to query portfolio data
- Academic institutions to replicate audits for validation
- Journalists to verify claims against the audit database

### 15.4 Biomimetic Repair Protocol Generator

Based on the Diagnostic Engine's identification of weakest FDPs, the application could generate specific repair recommendations using the MRF's biomimetic templates:

| FDP Deficit | Natural Template | Intervention |
|-------------|-----------------|--------------|
| Low CLM | Fungal networks | Industrial symbiosis parks |
| Low DA | Swarm intelligence | DAO governance |
| Low AR | Tropical rainforests | Polyculture farming |

This would extend the application from diagnostic to prescriptive.

---

## 16. Conclusion

This requirements specification describes a complete, independent, Institute-controlled implementation of the KOSMOS Systems Auditor methodology. The application's architecture mirrors the framework it implements: it separates objective measurement from interpretive framing, maintains its own persistent state, optimizes for long-term analytical capacity rather than short-term convenience, and supports recursive self-evaluation.

The Diagnostic Engine is the irreducible core. Everything else — the LLM integration, the web interface, the portfolio management, the report generation — is infrastructure that supports the diagnostic function. Build the engine first, validate it against known-answer cases, and then build outward.

The four axiomatic foundations documents (7ES, FDP, DQD, OCF) provide the mathematical specification that no external vendor can modify, revoke, or degrade. The formulas are derived from thermodynamics and information theory. They are as stable as the physics they rest on. This is the foundation on which the application stands — and the reason it can be built independently of any third-party platform.

---

*This requirements specification represents the collaborative analytical product of human systems expertise (Clinton Alden, KOSMOS Institute) and artificial intelligence capability (Claude Opus 4.6, Anthropic). All specifications are subject to refinement through development experience and operational testing.*
