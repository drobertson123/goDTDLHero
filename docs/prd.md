stepsCompleted: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11]
inputDocuments:
  - analysis/brainstorming-session-2025-12-02.md
workflowType: 'prd'
lastStep: 11
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

## User Journeys

**Journey 1: Primary Modeler – Building a Calm, Unified Workspace**  
A senior modeler starts the day with a 700-node DTDL file that has grown messy after weeks of parallel edits. Opening goDTDLHero in the browser, the document loads once and the text view, tree view, and inspector all snap to the same JSON heartbeat. They collapse a telemetry branch in the graph and immediately see the text editor fold to the same region. Relationship auras highlight which interfaces are re-used across twins, so deciding where to add new commands no longer requires juggling tabs. Every keystroke mirrors into the tree view without lag, and local WASM validation fires silently in the background. When a telemetry schema mismatch appears, a halo warms around the affected node and a breadcrumb takes the modeler straight to the offending JSON. After 30 focused minutes they commit coherent changes, export a pristine JSON file, and leave without context-switch fatigue.

**Journey 2: Primary Modeler – Triage Under Pressure**  
Late in the evening a pilot deployment surfaces a telemetry bug traced to a specific interface. The modeler pulls the production file into goDTDLHero while offline on a train ride home. The inspector warns of stale data and offers to diff against the live template once connectivity returns, but editing can proceed immediately. Search filters scoped by relationship colors narrow the view to impacted components, and the modeler toggles to the graph overlay to confirm there are no orphaned references. When the train enters a dead zone, validation keeps running locally; issues queue as calm notifications. As soon as the connection returns, goDTDLHero surfaces a gentle conflict banner showing which nodes changed upstream and helps merge them without rework. The fix is validated in under two minutes, exported, and ready for the ops team before arrival.

**Journey 3: Primary Modeler – Extracting Reality into a Model**  
A consultant arrives onsite to bootstrap a new digital twin. Instead of hand-crafting every interface, they connect goDTDLHero to a live system endpoint. The tool ingests sample payloads, proposes DTDL fragments, and shows them side-by-side with the canonical JSON document. The modeler accepts suggestions, edits inline to align naming conventions, and watches projection layers keep the single source of truth clean. AI hints suggest validation templates for each telemetry pattern so the consultant can hand the client a repeatable rule set. Within a single workshop session, the twin structure, validation rules, and documentation links all originate from the same canvas, giving the client immediate confidence.

### Journey Requirements Summary

- Unified surface synchronization between text, tree, inspector, and graph overlays.
- Cohesive guidance language (auras, halos, breadcrumbs, search filters) that stays calm at scale.
- Offline-first editing with queued validations, conflict detection, and merge assistance once connectivity returns.
- Local WASM validation with queued notifications and sub-150 ms responsiveness under load.
- Live system ingestion that proposes DTDL fragments plus AI-assisted templates for validation and documentation.
- Export fidelity guarantees (lossless JSON round-trips) and diff/compare tooling for production triage.

## Innovation & Novel Patterns

### Detected Innovation Areas

- **Single-surface paradigm:** Text editor, graph explorer, and inspector all operate on one canonical JSON heartbeat, eliminating context switches that plague today’s DTDL tooling.
- **Calm guidance language:** Relationship auras, validation halos, breadcrumbs, and search filters share the same visual vocabulary so modelers interpret structure, quality, and documentation cues instantly.
- **Local WASM validation + offline edits:** Validation logic runs in-browser, enabling sub-150 ms feedback loops, offline authoring, and conflict-aware re-sync without remote services.
- **Live twin ingestion with AI templates:** The tool ingests production payloads, proposes DTDL fragments, and layers AI-suggested validation templates so consultants can bootstrap twins in a single workshop.
- **AI copilot trajectory:** Roadmap calls for on-canvas tutoring that learns modeler intent, suggests modeling moves, and reuses template repositories—pushing beyond traditional IDE assistance.

### Market Context & Competitive Landscape

- Most DTDL authoring today happens through Visual Studio, basic text editors, or split-pane graph tools that don’t keep projections synchronized. goDTDLHero’s “one surface, one heartbeat” approach is a new pattern rather than an incremental UI tweak.
- Offline-first validation plus conflict-aware merges are rare in digital-twin tooling, giving the product a differentiator for enterprise field work.
- Live ingestion and AI template suggestions shorten kickoff cycles compared to manual schema mapping; no mainstream competitor offers that experience in-browser without custom services.

### Validation Approach

- **Experience studies:** Run side-by-side tests comparing the unified surface against traditional split tools; success is ≥25% faster completion of complex edits and frustration scores under 2/5.
- **Performance telemetry:** Instrument WebGL overlays and WASM validators to prove sub-16 ms frames and <150 ms validation even on 1K-node models.
- **Field pilots:** Conduct onsite ingestion sessions capturing time-to-first-model metrics; target completing baseline twins within a single workshop.
- **AI assist metrics:** Track acceptance rates of AI suggestions and time saved per modeling action to ensure automation provides tangible value.

### Risk Mitigation

- **Fallback editing modes:** Keep a classic split-pane view in reserve if the unified canvas hits accessibility or performance constraints.
- **Validation guardrails:** Offer remote validator hooks so users can compare local WASM results with authoritative services.
- **AI governance:** Provide explainable suggestions, quick rejection paths, and rationale logging to avoid “mystery edits.”
- **Live ingestion safety:** Sandbox connectors and diff previews prevent noisy production payloads from corrupting the canonical JSON.

## Developer Tool Specific Requirements

### Project-Type Overview
goDTDLHero is delivered strictly as a browser-hosted developer tool focused on Digital Twin Definition Language (DTDL) modeling. It does not expose SDKs or command-line interfaces; instead, it concentrates on a single immersive surface compiled to Go-powered WebAssembly.

### Technical Architecture Considerations
- Deployment target: desktop-class browsers loaded from a Go backend or CDN; no native binaries.
- Rendering stack: go-app UI with Canvas/WebGL overlays, all shipped via WASM.
- Storage: local JSON editing with save/export; any cloud persistence is handled outside the product.
- Authentication: limited to hosting needs (workspace login, optional SSO) since no external SDK surface exists.

### Language Matrix
- Authoring: DTDL JSON only; the product behaves like an IDE specialized for that schema.
- Implementation: Go + WASM internally; no public Go/TypeScript/Python bindings to maintain.
- No code generation or DSL output planned for launch.

### Installation & Access
- Distribution: hosted web experience (e.g., app.godtdlhero.com) served over HTTPS.
- Offline support: leverage PWA caching for repeat users, though first load requires connectivity.
- No package manager artifacts (npm, pip, Go modules) or VS Code extensions to publish.

### API & Surface Area
- User-facing APIs remain inside the app (file upload, live system connectors). No public REST or SDK endpoints.
- Live ingestion connectors must enforce sandboxing and diff previews before touching the canonical JSON document.

### Documentation & Examples
- Adopt the Diátaxis framework:
  - Tutorials: “Model your first twin” walkthroughs using sample payloads and validation halos.
  - How-to guides: triage schema errors, configure live ingestion, run offline validation loops.
  - Reference: inspector semantics, guidance language legend, validation states.
  - Explanations: rationale for the single-surface paradigm, WebGL overlays, and local validation choices.
- Provide a curated library of DTDL sample models and validation rule templates to accelerate onboarding.

### Migration Guidance
- No automated migration tooling; documentation should cover importing/exporting raw JSON for teams moving between goDTDLHero and existing editors.

### Implementation Considerations
- Monitor WASM bundle size and frame timing to keep the browser experience smooth on commodity laptops.
- Build documentation publishing into the release pipeline so Diátaxis sections stay current.
- Note optional future surfaces (IDE extensions, SDK hooks) as out-of-scope for MVP but keep interfaces modular for later expansion.

## Project Scoping & Phased Development

### MVP Strategy & Philosophy

**MVP Approach:** Experience MVP focused on proving the calm, unified editing surface that keeps text, graph, and inspector in lockstep.  
**Resource Requirements:** 3–4 person pod covering a Go/WASM engineer for the editor and validation core, a WebGL/performance engineer for graph overlays, a UX/interaction designer documenting the guidance language, plus part-time PM/QA for telemetry and documentation.

### MVP Feature Set (Phase 1)

**Core User Journeys Supported:**
- Journey 1 – Calm, unified workspace for 500–1K node edits.
- Journey 2 – Offline or low-connectivity triage with conflict-aware validation queues.

**Must-Have Capabilities:**
- Single JSON heartbeat driving synchronized text editor, tree or graph, and inspector with near-instant projection updates.
- Local WASM validation delivering sub-150 ms feedback, queued alerts, and diffable breadcrumbs.
- Offline-first editing via PWA caching, conflict banners, and merge assistance once reconnected.
- Cohesive guidance language primitives (relationship auras, validation halos, breadcrumbs, scoped search) implemented consistently.
- Lossless DTDL import/export with pre-save diff previews.

### Post-MVP Features

**Phase 2 (Post-MVP):**
- Live system ingestion connectors with sandboxed diff previews (Journey 3).
- Ergonomic boosters: batch edits, deeper inspector controls, richer graph gestures.
- AI-assisted validation hints that suggest fixes and modeling moves.
- Team workflows such as shared workspace state and lightweight commenting.

**Phase 3 (Expansion):**
- Full AI copilot that tutors on-canvas, reuses template libraries, and automates modeling sequences.
- Template repositories and validation-recipe marketplaces with governance hooks.
- Real-time telemetry integrations to keep models synchronized with production pipelines.
- Optional SDK or extension surfaces (VS Code extension, CLI) built atop modular APIs.

### Risk Mitigation Strategy

**Technical Risks:** WebAssembly bundle size, Canvas/WebGL performance on commodity laptops, and validator parity with cloud services. Mitigate with performance telemetry budgets, fallback rendering modes, and remote validator comparison hooks.

**Market Risks:** Teams may view existing IDE flows as sufficient or distrust offline validation. Mitigate via design-partner studies, published benchmarks, and documentation that spotlights conflict-resolution stories.

**Resource Risks:** A small pod could struggle to finish graph, validation, and offline flows simultaneously. Mitigate by time-boxing graph embellishments, deferring live ingestion to Phase 2, and leaning on shared UI components plus automated test harnesses.

## Functional Requirements

### Unified Editing Surface

- FR1: Modelers can open any valid DTDL document inside a unified workspace that shares a single canonical JSON source across all projections.
- FR2: Modelers can edit the canonical JSON through the text view while every change instantly reflects in tree, graph, and inspector projections.
- FR3: Modelers can manipulate tree or graph structures while the text editor and inspector follow the same focus.
- FR4: Modelers can synchronize focus across views so navigation context stays aligned.
- FR5: Modelers can inspect node metadata, schema snippets, and relationships through an always-on inspector bound to the selected entity.
- FR6: Modelers can save the canonical document back to disk with lossless fidelity and reversible history checkpoints.

### Guidance, Visualization & Discovery

- FR7: Modelers can visualize relationship auras that expose dependencies, reuse, and impact zones across the model.
- FR8: Modelers can see validation halos, breadcrumbs, and calm notifications that pinpoint issues without overwhelming the workspace.
- FR9: Modelers can search and filter nodes by name, type, relationship color, or custom tags to isolate relevant structures quickly.
- FR10: Modelers can create and revisit breadcrumbs or bookmarks to jump between distant regions of large models.
- FR11: Modelers can toggle visualization overlays to keep the canvas readable without losing context.

### Validation & Quality Guardrails

- FR12: Modelers can run local DTDL validation entirely within the browser and receive actionable results while editing.
- FR13: The system can queue validation events during rapid editing and surface aggregated results once computations finish.
- FR14: Modelers can compare local validation findings with remote validator outputs when connectivity is available.
- FR15: The system can highlight schema, reference, or telemetry conflicts inside every projection simultaneously when validation fails.
- FR16: Modelers can capture rationale when overriding or dismissing validation findings so future audits retain context.

### Offline, Sync & Conflict Handling

- FR17: Modelers can continue editing when offline with all pending operations stored locally until connectivity returns.
- FR18: The system can surface connectivity state, replay queued validations, and reconcile pending actions once the network is restored.
- FR19: Modelers can merge local edits with upstream versions using diff previews before committing or exporting changes.
- FR20: The system can detect conflicting edits between local and remote copies and guide users through conflict resolution steps.

### Live Ingestion & Intelligent Assistance

- FR21: Consultants can connect to approved telemetry or sample endpoints to ingest payloads into a staging area.
- FR22: Modelers can review, accept, or discard proposed DTDL fragments from ingestion before they modify the canonical JSON.
- FR23: The system can suggest validation templates, modeling moves, or guardrails based on detected patterns or AI hints.
- FR24: Modelers can run guided bootstrap workflows that pair ingestion steps with inline documentation and validation checks.

### Export, Sharing & Workspace Continuity

- FR25: Modelers can export the canonical JSON and related artifacts for downstream tooling.
- FR26: Modelers can compare multiple workspace states through diff views to understand change impact.
- FR27: Teams can share saved workspace contexts so reviews start from the same perspective.
- FR28: The system can warn users during export when the local state diverges from a tracked baseline or upstream file.

### Documentation, Templates & Learning

- FR29: Users can access Diátaxis-aligned tutorials, how-to guides, references, and explanations directly inside the application.
- FR30: Users can load curated DTDL sample models and validation rule templates as starting points for new projects.
- FR31: Users can attach documentation links, annotations, or onboarding notes to specific nodes to preserve institutional knowledge.

## Non-Functional Requirements

### Performance

- P1: Canvas, graph, and guidance overlays sustain 60 FPS (approximately 16 ms frames) on baseline developer laptops for documents up to 1K nodes, with graceful degradation strategies (progressive rendering, density caps) beyond that scale.
- P2: Local WASM validation returns initial findings within 150 ms for standard DTDL files and streams additional results so the editing thread never blocks.
- P3: Search, filter, and breadcrumb commands respond within 300 ms for documents up to 5K nodes so navigation feels instantaneous.
- P4: Save and export operations complete without UI freezes and emit completion states that downstream automation can trust.

### Reliability & Offline Continuity

- R1: The PWA shell caches core assets so the workspace loads and edits while offline; queued mutations persist across browser restarts.
- R2: Connectivity state is surfaced within two heartbeats, and queued validations or saves replay automatically once the network returns.
- R3: Conflict detection runs within five seconds of reconnection, presenting diff previews before merges proceed.
- R4: Local journaling captures every editing session so crashes or forced reloads can recover the last committed state without data loss.

### Security & Data Protection

- S1: DTDL documents remain client-side by default; no model data leaves the browser unless the user explicitly exports or invokes a connector.
- S2: All hosted surfaces use HTTPS/TLS, and any authentication defers to the hosting provider’s hardened identity stack.
- S3: Live ingestion connectors operate inside sandboxed WebAssembly modules, require explicit user opt-in, and expose diffs before mutating the canonical JSON.
- S4: Telemetry logs strip or hash user content so diagnostics never capture proprietary DTDL payloads.

### Scalability & Capacity Management

- SC1: Single workspaces handle at least 1K nodes without feature degradation, and up to 5K nodes remain operable through adaptive rendering.
- SC2: Multiple workspaces per browser profile share caches without cross-contamination, ensuring consultants can juggle clients safely.
- SC3: The system supports simultaneous validation queues without starving UI interactions.

### Accessibility & Guidance Clarity

- A1: Guidance primitives meet WCAG 2.1 AA contrast ratios and include shape or pattern cues for color-vision deficiencies.
- A2: Text editor, tree, graph, and inspector are fully operable via keyboard, with focus order synchronized across projections.
- A3: Notifications, validation results, and breadcrumbs expose screen-reader-friendly labels plus ARIA live regions so non-visual users receive the same feedback.
- A4: Motion-heavy interactions offer reduced-motion settings that preserve context without inducing fatigue.

### Integration & Extensibility

- I1: Live ingestion adapters declare required scopes, timeouts, and expected payload formats before execution so teams can review risk.
- I2: Remote validator hooks communicate over signed HTTPS endpoints and never block local editing; discrepancies surface as comparable reports.
- I3: Export pipelines produce deterministic JSON plus optional diff or validation artifacts so external CI/CD tooling can consume them without reformatting.
- I4: Documentation surfaces update atomically with releases, guaranteeing version-aligned references inside the app.

