# Guan-Materials-1

Guan-Materials-1 is an installable Codex plugin for materials literature discovery, assistant-led paper reading, novelty auditing, and long-term evidence archiving. It supports metals, polymers, composites, ceramics, coatings, energy materials, and other materials research directions.

## What It Does

- Routes topic-only, title/DOI-list, and PDF inputs without redundant questions.
- Builds material-agnostic search queries from research object, method, response, and boundary.
- Uses a two-pass retrieval workflow to reduce off-topic results.
- Reads PDFs directly and returns a proposal-ready evidence card.
- Separates measurements, model predictions, author interpretations, and reader hypotheses.
- Audits candidate research gaps without overstating novelty.
- Keeps a master index plus evidence workbooks split every 50 papers.

## Installation

1. Clone or download this repository.
2. In Codex, add this repository root as a local marketplace. The manifest is at `.agents/plugins/marketplace.json`.
3. Install the `guan-materials-1` plugin from the Plugins view.

For command-line setup:

```text
codex plugin marketplace add <repository-root>
```

## Optional Capabilities

The plugin packages only its workflow. It can use available Codex capabilities for literature search, institution-authorized downloads, browser control, PDF reading, spreadsheets, and document writing. It stays usable without them through local PDFs, manual links, Markdown cards, and CSV/Excel-ready records.

The plugin never packages institutional credentials, browser sessions, proprietary databases, or user research files.

## Documentation

Read [docs/使用说明.md](docs/使用说明.md) for the complete workflow, input routes, search logic, evidence-card fields, archive design, and troubleshooting.
