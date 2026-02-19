# Nova Itera Reference Page Template Database

**Author:** Ariel J. Furlow
**Organization:** Nova Itera Research Group
**Version:** 1.0.0
**Created:** 2026-02-19
**Schema:** [`schemas/template-metadata-schema.yaml`](../schemas/template-metadata-schema.yaml)
**Database File:** [`schemas/template-database.yaml`](../schemas/template-database.yaml)

---

## Purpose

This database is the central repository for all Nova Itera reference page templates.
It provides a structured, citable, and version-controlled store for every writing
style, tone, format, and note type used across Nova Itera research operations.

Any Notion page, research document, or workflow output that references a specific
template style can cite it by its `template_id` from this database.

---

## Template ID Convention

All templates follow the naming convention:

```
nova-itera/<category>/<slug>@<version>
```

**Example:**
```
nova-itera/note-formats/context-transfer-note@1.0.0
```

---

## Categories

| Category | Description | Status |
|---|---|---|
| `note_formats` | Structured note types (Context Transfer, Intelligence Note, etc.) | Active |
| `transcript_formats` | Formats for transcribing sessions, interviews, AI conversations | Active |
| `writing_styles` | Defined prose styles for research writing | Pending |
| `tones` | Registered tone profiles for different output contexts | Pending |
| `research_formats` | Research briefings, methodology summaries, findings reports | Pending |
| `workflow_formats` | Workflow documentation, process notes, pipeline docs | Pending |
| `session_formats` | Session open/close, handoff, state capture formats | Pending |
| `audit_formats` | Audit trail entries, provenance notes, integrity logs | Pending |

---

## Current Template Index

### Note Formats

| Template ID | Name | Complexity | Maturity |
|---|---|---|---|
| `nova-itera/note-formats/context-transfer-note@1.0.0` | Context Transfer Note | Medium | Stable |
| `nova-itera/note-formats/intelligence-note@1.0.0` | Intelligence Note Style | High | Stable |

### Transcript Formats

| Template ID | Name | Complexity | Maturity |
|---|---|---|---|
| `nova-itera/transcript-formats/transcript-note@1.0.0` | Transcript Format | Low | Stable |

---

## Schema Reference

Each template entry in the database conforms to the **30-Parameter Template Metadata
Schema**, which is organized into 9 semantic groups:

| Group | Parameters | Description |
|---|---|---|
| Core Identification | 5 | ID, name, version, dates |
| Classification & Taxonomy | 5 | Category, type, tags |
| Functional Characteristics | 5 | Summary, use cases, patterns |
| Requirements & Specifications | 5 | Inputs, outputs, dependencies |
| Workflow Integration | 4 | Stages, integration, automation |
| Quality & Maturity Metrics | 4 | Complexity, maturity, validation |
| User & Audience | 3 | Audience, expertise, time |
| Governance & Provenance | 4 | Attribution, history, license |
| Performance Characteristics | 3 | Strengths, limitations, optimization |

Full schema: [`schemas/template-metadata-schema.yaml`](../schemas/template-metadata-schema.yaml)

---

## Adding a New Template

1. Open `schemas/template-database.yaml`
2. Navigate to the appropriate category section
3. Append a new entry following the 30-parameter schema
4. Assign a unique `template_id` using the convention above
5. Set `creation_date`, `author`, and `attribution` fields
6. Commit with a message that includes the `template_id`
7. Update `database_meta.total_templates` count

---

## Authorship & Provenance

This database and its schema are original works by **Ariel J. Furlow**, Nova Itera
Research Group. The 30-parameter taxonomy, category structure, and template ID
convention constitute original intellectual contributions.

All entries in this database are governed by the repository license (Apache-2.0)
and must include proper attribution when derived works are created.

---

*Nova Itera Research Group — Ariel J. Furlow — 2026*
