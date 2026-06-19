# CKR Roadmap

This roadmap describes planned work for turning the CKR proposal into an experimental research system. The phases are intentionally framed as future validation work, not completed results.

## Phase 1: Claim Extraction Prototype

Build a minimal pipeline that converts raw documents into candidate claims while preserving source provenance.

Planned outputs:

- Document ingestion prototype
- Claim extraction prompts or models
- Source-to-claim traceability
- Initial quality checks

## Phase 2: Data-Card Schema Implementation

Define and implement a structured metadata schema for each extracted claim.

Planned outputs:

- JSON schema for data cards
- Required provenance fields
- Status and safety labels
- Validation scripts

## Phase 3: Consensus Scoring

Design a scoring method that combines agent agreement, evidence quality, uncertainty, source reliability, rarity, and contradiction signals.

Planned outputs:

- Scoring formula or model
- Agent review records
- Confidence calibration experiments
- Error analysis plan

## Phase 4: Knowledge Graph and Contradiction Detection

Create a graph representation for topics, claims, sources, contradictions, and supporting evidence.

Planned outputs:

- Claim clustering workflow
- Graph schema
- Contradiction edge detection
- Review interface requirements

## Phase 5: Human Audit Workflow

Add a human review process for ambiguous, rare, unsafe, or high-impact claims.

Planned outputs:

- Audit queue design
- Reviewer decision rules
- Audit logging
- Disagreement resolution process

## Phase 6: Small Model Experiments

Run controlled experiments comparing raw training data against CKR-refined training data on small models.

Planned outputs:

- Baseline raw-data training setup
- CKR-refined training setup
- Evaluation metrics
- Reproducible experiment logs

## Phase 7: Scaling Validation

Evaluate whether benefits observed at small scale continue at larger data and model scales.

Planned outputs:

- Scaling study design
- Larger-domain datasets
- Cost and quality analysis
- Independent reproducibility checklist
