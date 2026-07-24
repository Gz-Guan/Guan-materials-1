---
name: guan-materials-1
description: Domain-adaptive materials literature workflow for proposal, thesis, and experiment planning. Use when a user has only a materials research topic and needs literature discovery; supplies titles, DOIs, PDFs, or a reference list and needs classification or assistant-led reading; asks for a paper's background, methods, results, figures, limitations, or research gaps; asks whether a candidate innovation is already studied; or asks to build a long-term literature evidence archive. Supports metals, polymers, composites, ceramics, coatings, energy materials, and other materials directions without hard-coded material keywords.
---

# Guan-Materials-1

Convert a materials topic or paper into source-grounded evidence for research decisions. Default to assistant-led reading: do not quiz the user or require them to read and restate the introduction, methods, or results unless they explicitly request interactive learning.

## 1. Route The Input

Choose one route and skip irrelevant steps:

| User input | Action |
|---|---|
| Topic only | Complete the mandatory resource preflight before discovery. |
| Titles, DOIs, or a reference list | Verify metadata and classify; search only for missing metadata or full text. |
| PDF(s) | Skip discovery/download and analyze directly. |

### Mandatory Resource Preflight For Topic-Only Requests

Before any literature search, candidate-paper list, topic recommendation, innovation audit, or proposal conclusion, ask for and record all four items below in one compact request:

1. intended output: proposal, experiment design, review, thesis, or another stated output;
2. institutional library portal and available databases;
3. whether an authorized browser session is currently logged in;
4. whether local PDFs, a reference list, a Zotero/EndNote library, or a project folder already contains papers.

Treat the preflight as complete only when the objective, access status, and existing-literature status are known. `No institutional access`, `not logged in`, and `no local papers` are valid recorded statuses. Do not search, return candidate records, recommend a topic, or make novelty/mechanism claims while any status is unknown.

If local PDFs or a reference library exist, inspect and classify them first. If authorized institutional access exists, search that route before public metadata. Use public metadata only for DOI verification, open-access discovery, or gaps not covered by the local/authorized sources. If the user cannot provide a resource route, state the public-metadata-only limitation and obtain explicit permission before proceeding.

For a topic-only request that already states its objective, ask only for the remaining preflight items in the first response. Do not search in that same response. Detect browser-control capability only after preflight. If authorized browser control and a logged-in institutional session are available, download only lawful open-access or institution-authorized full text. If not, return verified title, DOI, publisher/database route, and library search path for manual download. Do not request credentials, OTPs, cookies, or session files. Do not mass-download; present candidates first and use small confirmed batches.

## 2. Build A Domain-Adaptive Search Strategy

Do not hard-code material names, welding terms, or exclusion terms. Extract the user's topic into a concept card:

| Concept | Examples |
|---|---|
| Research object | material, molecular system, composite, coating, structure, specimen form |
| Action or phenomenon | joining, synthesis, modification, degradation, transport, phase change, modeling |
| Target response | strength, toughness, adhesion, conductivity, barrier property, stability, biocompatibility |
| Boundary | thickness, temperature, environment, application, equipment, scale |

Create a query family rather than one broad keyword string:

1. `core`: object AND action/phenomenon.
2. `focused`: core AND target response.
3. `boundary`: focused AND one decisive boundary when the result set is still broad.
4. `synonym variants`: expand object, action, and response terms with spelling, abbreviation, and established field synonyms.

Use title/abstract/keyword fields whenever a database supports them. Search the user's authorized library databases first. Use structured public metadata for DOI verification and open-access discovery, not as the only source of a precision search. Select databases by field: use Web of Science, Scopus, publisher databases, CNKI, Wanfang, PubMed, or preprint sources only when appropriate to the topic and the user's access.

## 3. Run Two Retrieval Passes

Before starting Pass A, self-check: `Did I complete or receive an explicit waiver for the topic-only resource preflight?` If not, stop and ask the unresolved preflight questions. Label any preflight-incomplete work `not started`; never label it as candidate literature or proposal evidence.

### Pass A: Recall

Retrieve a limited candidate pool, normally 20-30 records. Rank first by conceptual match, then publication date/full-text availability, then citation count. Never allow citation count alone to rank a broad query.

### Pass B: Precision

Independently inspect title, abstract, DOI, material/system, and actual method for every retained candidate. Reject records that fail a required concept. Detect recurrent off-topic clusters and derive project-specific exclusion terms only after inspecting the first pool.

Examples of derived exclusions may be TiO2 photocatalysis for a titanium joining topic, drug delivery for a polymer processing topic, or electrode studies for a structural composite topic. Do not reuse an exclusion list across unrelated subjects.

If the first pool is contaminated, revise the query with field constraints and derived exclusions, then rerun. Report the rejection logic in compact form. Treat CNKI/Wanfang coverage as a separate authorized/manual check when programmatic search is unavailable.

For every retained paper, report title, first author, year, venue, DOI, access route, direct/near-neighbor/analogy relevance, A/B/C depth, and why it is relevant.

## 4. Read Papers Directly

Read the available full text before making strong claims. If only abstract/metadata is available, label every output `abstract-level clue` and do not archive it as final evidence.

Return this fixed evidence card:

1. `Paper role`: bibliographic identity, evidence type, and reading depth.
2. `Problem and introduction logic`: existing difficulty, knowledge gap, and stated aim.
3. `Actual contribution`: distinguish a contribution from routine background.
4. `Complete experimental or modeling route`: material/dimensions -> pre-treatment/interlayer or additives -> assembly -> parameters -> cooling/post-treatment -> characterization -> performance tests.
5. `Special design`: separately explain non-routine controls, staged treatments, unusual additives/interlayers, designed geometry, or special validation.
6. `Results and discussion`: summarize every numbered subsection with condition, observation, quantitative result, author explanation, and page/figure/table anchor.
7. `Core conclusion`: one sentence.
8. `Limits and prohibited extrapolations`: material, geometry, process, missing controls/tests, and evidence gaps.
9. `Proposal use`: one defensible claim the paper supports for the user's stated project.

For each mechanism, label `direct measurement`, `model prediction`, `author interpretation`, or `reader hypothesis`. Do not reduce interface quality to only void count when strength, bonded area, reaction layers, hardness, fracture position, leak rate, deformation, or durability were available.

Retain at most three figures per paper, and only when they clarify assembly, process sequence, decisive microstructure, or a key trend. Record figure number, page, purpose, and source path. Do not force figure retention.

## 5. Audit Candidate Innovation

At each paper close, identify actual limitations and candidate questions relevant to the user's project. Perform a bounded audit using the concept card, synonym variants, adjacent systems, recent international work, and Chinese databases when accessible.

Classify each candidate only as:

- `already studied`: state who did it and the meaningful difference.
- `partially studied`: state what is covered and what remains unsupported.
- `not found in this audit`: call it a candidate question, never an established innovation.

When a public metadata search returns poor relevance, say so and do not use it as novelty evidence. Tighten field constraints, revise exclusions, or defer the conclusion pending authorized database checks. Every 5-10 completed papers, merge repeated candidate questions and run one broader cross-paper audit. Record search terms, date range, sources, exclusions, and conclusion.

## 6. Archive Without Bloat

After each closed paper, add its evidence card to the day's pending archive set. Update archives only after the user explicitly ends the reading day.

Maintain three layers:

1. `Master index`: one lightweight row per paper with identifier, title, DOI, tags, status, archive volume, and card path.
2. `Evidence volumes`: one workbook per 50 papers (`001-050`, `051-100`, and so on) containing complete evidence cards, daily logs, and optional figure references.
3. `Paper cards`: one Markdown card per paper with source anchors and optional retained visuals.

At day end, batch-update completed papers only. Preserve formulas, styles, filters, and existing data. Verify changed ranges, formula errors, and rendered sheets before saving. Add one daily synthesis: confirmed evidence, boundaries, contradictions/trade-offs, candidate questions, and proposal sections supported.

## 7. Generate Supervisor Output

When asked to prepare a supervisor report, synthesize recent reading into confirmed findings, central technical contradiction, proposed experimental route and controls, variables and response metrics, candidate innovation audit status, decisions needed from the supervisor, and the next-week plan.

## Capability Integration

Use available built-in or installed capabilities when present; do not bundle their code or assume they exist on another computer:

- literature search/citation verification for discovery and audits;
- institution-authorized downloader and active-browser control for full text;
- PDF reader for text, figures, and anchors;
- spreadsheet editing for evidence volumes;
- document/proposal writing for reports.

If a capability is unavailable, preserve the workflow using verified manual links, local PDFs, Markdown cards, and CSV/Excel-ready records. State the fallback and continue.
