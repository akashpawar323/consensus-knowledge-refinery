# CKR Architecture

This document describes the proposed architecture for Consensus Knowledge Refinery (CKR). The system is a research proposal and requires future implementation, experiments, and validation.

## Raw Corpus

The raw corpus is the initial collection of source documents, web pages, papers, manuals, examples, and other text sources considered for training data. At this stage, the corpus may contain duplication, outdated statements, contradictions, weak provenance, low-quality writing, or unsafe material.

CKR assumes that raw text should not be treated as uniformly reliable. Each document should carry source metadata such as origin, collection date, license status, and domain.

## Claim Extraction

Claim extraction converts raw text into candidate knowledge units. A claim may be a factual statement, definition, procedural step, answer, warning, or relationship between concepts.

The planned prototype should preserve provenance links back to the original source text. Extracted claims should remain auditable, rather than becoming anonymous generated summaries.

## Specialist Agent Ensemble

The specialist agent ensemble reviews extracted claims from multiple perspectives. Example roles may include factual verifier, contradiction finder, safety reviewer, domain specialist, provenance checker, and compression reviewer.

The ensemble is proposed as a way to collect diverse signals. Agreement among agents is useful evidence, but it does not prove that a claim is true.

## Semantic Clustering

Semantic clustering groups claims that express similar ideas. This step is intended to reduce duplicate data, identify repeated claims across sources, and expose conflicting versions of the same topic.

Clusters may include accepted claims, uncertain claims, rejected claims, and disputed claims. The goal is to preserve useful uncertainty instead of flattening every topic into one answer.

## Consensus Scoring

Consensus scoring estimates the reliability and usefulness of each claim. The score may consider agent agreement, source quality, provenance strength, contradiction signals, rarity, safety status, and human audit feedback.

The score is a decision-support signal, not a truth guarantee. Future experiments must test whether the scoring method improves training data quality.

## Knowledge Graph

The knowledge graph links topics, claims, sources, contradictions, supporting evidence, and related concepts. It is proposed as a structure for traceability and contradiction detection.

Graph edges may represent support, disagreement, duplication, dependency, temporal validity, or domain context.

## Reliability Calibration

Reliability calibration adjusts confidence estimates using evidence quality, source trust, audit outcomes, and observed model behavior in downstream experiments.

This step is planned for future validation. Calibration should be measured against held-out audits and task performance rather than assumed to work by design.

## Human Audit

Human audit is the review layer for high-impact, ambiguous, rare, unsafe, or disputed claims. Auditors can accept, reject, revise, or escalate claims.

The audit process should focus on transparency, provenance, and consistent decision rules. Human review is especially important for safety-sensitive domains.

## Data-Card Decision Rules

Data cards store structured metadata for each claim. Decision rules use fields such as confidence, rarity, safety, status, and provenance to determine whether a claim enters the refined corpus.

Example statuses include `accepted`, `rejected`, `disputed`, `needs_review`, and `unsafe`.

## Refined Corpus

The refined corpus is the proposed output of CKR. It should contain higher-density, provenance-aware training material with reduced duplication and explicit metadata.

Future experiments should compare models trained on raw data against models trained on CKR-refined data under controlled settings.
