---
stepsCompleted: [1, 2, 3]
inputDocuments:
  - analysis/brainstorming-session-2025-12-02.md
workflowType: 'prd'
lastStep: 3
project_name: 'goDTDLHero'
user_name: 'Doug'
date: '2025-12-02'
---

# Product Requirements Document - goDTDLHero

**Author:** Doug
**Date:** 2025-12-02

## Executive Summary

goDTDLHero delivers a unified surface for authoring and visualizing Digital Twin Definition Language (DTDL) models inside a Go-powered WebAssembly app. It keeps modelers immersed by binding a precision text editor, a JSON Hero/JSONCrack-style graph explorer, and an always-on inspector to the same JSON source of truth. The product tackles the two frictions teams report today: losing context while jumping between editors and waiting on remote validators. By pairing calm, relationship-aware overlays with lazy-loaded performance tactics, we give digital-twin architects confidence to evolve thousand-node models without lag or visual noise.

### What Makes This Special

- A single editing surface that fuses text, graph, and inspector views so every change is visible everywhere without panel juggling.
- A cohesive guidance language—relationship auras, validation halos, breadcrumbs, and search filters all reuse the same visual vocabulary to keep large models comprehensible.
- Local WASM-based DTDL validation plus Canvas/WebGL overlays provide instant, offline feedback even when rendering 1K+ nodes.
- A single in-memory JSON document with projection layers guarantees every visualization and teaching moment reflects canonical data.

## Project Classification

**Technical Type:** developer_tool  
**Domain:** general  
**Complexity:** low

Classification rationale: Keywords such as “DTDL editor,” “go-app WebAssembly tool,” “single in-memory JSON document,” and “local WASM validation” map directly to the developer_tool signals (tooling, SDK-like behavior, IDE-style flows). No regulated-industry cues surfaced, so the general domain with low complexity applies. This keeps focus on developer productivity requirements (language matrices, documentation, validation ergonomics) instead of compliance checklists, with the option to revisit if domain constraints emerge later.

## Success Criteria

### User Success

- 90% of editing activity happens on the unified surface without panel juggling, and frustration scores stay below 2/5 in beta surveys.
- 80% of evaluators describe the guidance language (auras, halos, breadcrumbs) as “calming” or “confidence-building.”
- Modelers resolve validation issues on 1K-node models in <2 minutes because errors, text, and graph stay synchronized.

### Business Success

- Month 3: “Cleanly functional” release with three design-partner teams using goDTDLHero weekly and contributing qualitative feedback proving the context-preserving experience.
- Month 12: AI-guided workflows automate most authoring actions, delivering 40% faster updates for paying customers and landing at least two enterprise pilots.

### Technical Success

- Rendering pipeline maintains sub-16 ms frames while manipulating 1K-node graphs.
- Local WASM validation completes in under 150 ms for standard DTDL models and never blocks editing.
- Single JSON source remains canonical—projection sync checks pass automatically, and save/load round trips remain lossless.
- Offline-first reliability keeps core editing functional without a network and flags sync conflicts within 5 seconds once reconnected.

### Measurable Outcomes

- Median “open-edit-validate-save” flow finishes within 4 minutes for 500+ node documents.
- Post-session CES ≥ 4/5 by the fourth usability cycle.
- Adoption milestones: 10 active workspaces by month 3, 50 by month 12 with AI guidance enabled.
- <1% of exported files fail downstream validation pipelines.

## Product Scope

### MVP - Minimum Viable Product

Open any DTDL document, edit it in synchronized text and tree views, keep the single JSON source authoritative, run local validation, and save back to disk without losing fidelity. Includes the baseline guidance language (relationship auras plus validation halos) and offline-first behavior.

### Growth Features (Post-MVP)

Enhance ergonomics (batch edits, inspector depth, graph gestures), integrate AI guidance that suggests fixes and modeling moves, and add connectors that ingest DTDL models from live twin systems.

### Vision (Future)

Deliver an AI copilot that tutors modelers, offer a repository of templates and validation recipes, automate end-to-end validation, and integrate deeply with real-time data sources so twins stay synchronized with production telemetry.

