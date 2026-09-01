# DIKWP Semantic Capital Foundry 13.0.0

> Compile scattered organisational knowledge into signed, testable, governable and reusable **Cognitive Asset Capsules**.

**Mode**

`SCF13_KNOWLEDGE_EQUITY_SEMANTIC_CAPITAL_COMPILE_GOVERNED_REUSE_REALITY_CLOSURE`

## Why this product now

Generic information, code examples and model access are becoming cheaper and more widely available. The commercial scarcity is moving toward a different layer:

- which problem is worth solving and for whose benefit;
- which evidence is authoritative in a specific organisation;
- which exceptions, failure histories and boundaries change a decision;
- how expert judgment can be compiled into a repeatable workflow;
- how a workflow is tested before release and revised after reality contact;
- who contributed, authorized, operates, pays for and bears the risk of the asset.

A conventional knowledge base stores text. A generic RAG system retrieves text. Semantic Capital Foundry creates a **governed executable asset**: a versioned harness, a signed Purpose Contract, provenance-bearing semantic cards, validation and hidden-test evidence, capability boundaries, economics assumptions and an append-only decision trail.

## What is sold

The product unit is not a prompt and not a chatbot. It is a `.cacpkg` **Cognitive Asset Capsule**:

```text
source corpus + ownership/consent
                │
                ▼
D / I / K / W / P / Experience / Boundary semantic cards
                │
                ▼
candidate harnesses: deterministic rules + induced structure + external builder proposals
                │
                ▼
validation-only selection under policy, quality and cost gates
                │
                ▼
sealed hidden-test evaluation
                │
                ▼
signed portable capsule + registry + governed runtime + decision receipts
                │
                ▼
production outcomes → correction → new version or retirement
```

A strong builder model may propose a candidate harness. It cannot grant itself a new tool, data scope, network channel, external action or evaluation privilege. The open core validates every candidate against the signed capability envelope and opens the hidden test only after selection.

## Core capabilities

- Local-first ingestion for Markdown, text, JSON, JSONL and CSV.
- Source digest, owner, licence, scope and provenance retention.
- Heuristic DIKWP plus Experience and Boundary semantic typing.
- Deterministic rule harness and bilingual lexical-harness induction.
- Import of human- or model-authored candidate harnesses without authority expansion.
- Validation selection followed by sealed hidden-test evaluation.
- Non-compensatory Semantic Capital Quality Vector.
- Purpose Contract with owner, beneficiary, permitted actions, review labels, risk/budget/operator roles and revocation process.
- Mesh95-style attribution and burden ledger.
- Signed `.cacpkg` capsule with file inventory and HMAC reference signature.
- SQLite registry, local runtime, append-only hash-chain decision receipts and OpenTelemetry-shaped local events.
- Harness-capability diff: model weights may remain unchanged while the system still requires recertification.
- Assumption-bound ROI calculator and standalone offline dashboard.
- Loopback-only reference API by default; no outbound network call in the core runtime.

## One-minute demonstration

Requires Python 3.10 or later and no third-party runtime dependency.

```bash
python run.py --workspace outputs/demo demo --reset
```

Open:

```text
outputs/demo/dashboard.html
```

The demonstration builds a bilingual after-sales triage capsule from three synthetic policy/experience documents and 168 synthetic labelled records. Four harness candidates are evaluated. The candidate is selected with validation data only; the hidden test is loaded after selection. The synthetic rule-generated test produces perfect results by construction and therefore demonstrates pipeline integrity, **not production accuracy**.

Run a capsule:

```bash
python run.py --workspace outputs/demo run \
  --capsule outputs/demo/capsules/cac_returns_triage-1.0.0.cacpkg \
  --input '{"issue":"adapter produced smoke","hazard":true,"product_type":"physical","days_since_purchase":2,"receipt":true,"unopened":false,"defect":true,"consumed":false,"value":399}'
```

Verify:

```bash
python run.py verify-capsule outputs/demo/capsules/cac_returns_triage-1.0.0.cacpkg
python run.py --workspace outputs/demo verify-ledger
python -m unittest discover -s tests -v
```

## Compile a customer project

```bash
python run.py --workspace outputs/customer compile \
  --task examples/returns_triage/task.json \
  --contract examples/returns_triage/purpose_contract.json \
  --corpus examples/returns_triage/corpus \
  --train examples/returns_triage/data/train.jsonl \
  --validation examples/returns_triage/data/validation.jsonl \
  --hidden-test examples/returns_triage/data/hidden_test.jsonl \
  --economics examples/returns_triage/economics.json
```

Optional builder candidates can be placed in a directory and supplied with `--candidate-dir`. They are treated as proposals, not authorities.

## Commercial entry points

The Apache-2.0 community core is intended to create adoption and an independently inspectable standard. Revenue is expected from the work that enterprises cannot obtain merely by copying code:

1. **Cognitive Asset Discovery Pilot** — identify one high-volume decision, establish provenance and owner rights, and produce the first measured capsule.
2. **Private Foundry Deployment** — private connectors, identity, KMS/HSM signing, private registry, evaluation operations, observability and support.
3. **Regulated Decision Assurance** — domain-specific policy mapping, independent validation, change control, review workflow and evidence export.
4. **Capsule Operations** — monitoring, drift evaluation, revision, retirement, cross-model portability and portfolio governance.
5. **Knowledge Owner Marketplace** — licensed domain capsules, contributor attribution and revenue-sharing controls; this is a roadmap module, not implemented in the alpha core.

Illustrative pricing and economics in the commercial report are planning assumptions, not a quotation or guarantee.

## Relationship to adjacent DIKWP systems

- **DIKWP-EIDOS 9.5** is an upstream owner-governed essence compiler. It identifies durable semantic invariants, decision competence, revision worldlines, rights and frontier residuals.
- **TrustPlane OS** provides a portfolio-level Purpose–evidence–memory–action–accountability control plane.
- **ProofLedger** and **AgentTrace** provide claim–evidence assurance and replayable traces.
- **TIANHENG 12.0** governs system-capability changes, multi-agent organization and stop authority.
- Semantic Capital Foundry converts selected knowledge and boundaries into a commercially deployable, versioned cognitive asset and leaves the above governance lineage visible.

## Security and governance invariants

```text
EXTERNAL_AUTOMATIC_ACTION_AUTHORITY = 0
REWARD_DOES_NOT_CREATE_AUTHORITY = 1
HIDDEN_TEST_VISIBLE_TO_BUILDER = 0
POLICY_BEFORE_QUALITY_BEFORE_COST = 1
ATTRIBUTION_AND_SOURCE_CONTINUITY = 1
HUMAN_REVOCATION_PRECEDENCE = 1
```

The reference server binds to `127.0.0.1` and requires an API key for non-health endpoints. The default HMAC secret is a demonstration convenience and must be replaced with enterprise KMS/HSM signing. The runtime does not transfer money, contact external parties, execute arbitrary code or call external models.

## Evidence boundaries

This is an alpha reference implementation. It does not prove that a corpus is true, that a semantic card captures tacit expertise, that a harness will work in a production domain, that a model is safe, that a workflow complies with a specific law, or that an ROI scenario will be achieved. Customer deployment requires local data rights, domain validation, security architecture, legal analysis, acceptance testing, named responsibility and operational monitoring.

## Development

```bash
python -m compileall -q src tests run.py
python -m unittest discover -s tests -v
python -m pip wheel . --no-deps -w dist
```

## Licence and attribution

Software is licensed under Apache License 2.0. Corpus content retains its own rights and licences. Open-source availability does not grant confidential knowledge, free consulting, custom implementation, support, patents, trademarks, identity, voice, certification, institutional endorsement or official-representation rights.

Please retain accurate attribution to the DIKWP research programme and Yucong Duan where the research lineage is materially used. See `NOTICE` and `CITATION.cff`.
