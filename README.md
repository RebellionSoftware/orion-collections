# Orion Sample Collections

Ready-to-import prompt collections for [Orion](https://orionapp.dev) — a desktop app for testing, iterating, and evaluating LLM prompts.

These collections are designed to get you productive quickly, whether you're learning Orion's features or looking for practical prompts you can use every day. View the prompt notes for each prompt for more information.

<p align="center">
  <img src="logo_full.png" alt="Orion Logo" width="20%">
</p>

---

## Collections

### Getting Started
**File:** `01-getting-started/getting-started.orion.json`

A hands-on introduction to Orion's core features. Work through the prompts in order — each one introduces a new concept.

| Prompt | What it teaches |
|---|---|
| 01 — Hello, Orion | Sending a prompt, exploring the UI, the Raw tab |
| 02 — Template Variables | `{{variable}}` placeholders, the Variable Test Panel |
| 03 — Summarize Meeting Notes | File attachments, LLM-as-a-Judge assertions |
| 04 — Structured JSON Output | JSON mode, `valid_json` and `json_schema` assertions |

---

### Intermediate Techniques
**File:** `02-intermediate/intermediate.orion.json`

Covers the features that separate casual use from serious prompt engineering: batch processing, multi-assertion quality gates, prompt versioning, and model comparison.

| Prompt | What it teaches |
|---|---|
| 01 — Batch Sentiment Analysis | Batch mode with CSV, JSON schema assertions, LLM rubric |
| 02 — Content Classifier | Batch mode, flag detection, multi-assertion pipelines |
| 03 — Code Review Assistant | Batch mode, security-focused rubric assertions |
| 04 — Email Drafter | Baseline prompt for versioning demo |
| 05 — Email Drafter v2 | Version diff, improved assertions, `not_contains` |
| 06 — Model Comparison: Summarization | Head-to-head model comparison |

Includes supporting CSV files in `o2-intermediate/batch-data/`:
- `customer-reviews.csv` — 7 product reviews with varied sentiment
- `content-tags.csv` — 7 news articles + spam and clickbait examples
- `code-snippets.csv` — 4 code samples including real security vulnerabilities

---

### Everyday Productivity
**File:** `03-everyday-prompts/everyday-productivity.orion.json`

Practical prompts for common work tasks. Import, fill in your variables, and use them as-is or adapt them to your workflow.

| Prompt | What it does |
|---|---|
| Reply to This Email | Draft a ready-to-send reply given the received email and your intent |
| Summarize a Long Thread | Extract decisions, action items, and open questions from any thread |
| Explain This Code | Explain a code snippet calibrated to a specific audience |
| Write My PR Description | Turn rough change notes into a structured PR description |
| Weekly Status Update | Polish rough bullet points into a scannable weekly update |
| Tone Check & Rewrite | Check if a message reads the way you intended; rewrite if not |
| Brainstorm Angles | Get 5 non-obvious approaches to any problem or goal |

---

## How to Import

1. Open Orion
2. Click the **Import collection** button in the sidebar
3. Select the `.orion.json` file you want to import
4. The collection appears in your sidebar immediately

For collections that use CSV batch data, load the CSV separately:
1. Open the prompt
2. Click the **Batch** tab in the toolbar
3. Click **Load CSV** and select the file from the `02-intermediate/batch-data/` folder

---

## How to Use the Notes

Every prompt in these collections has a **Notes** section with usage instructions, example inputs, and tips. Click the **Notes button** in the prompt toolbar to open it.

---

## Requirements

- [Orion](https://orionapp.dev) desktop app
- At least one configured LLM provider (OpenAI, Anthropic, or any compatible API)
- For LLM-as-a-Judge assertions: configure an AI Features model in **Settings → Workspace → AI Features Model**

---

## Customizing Prompts

These prompts are starting points. Once imported, everything is editable:

- **Change the model** — swap any prompt to a different provider or model from the selector in the toolbar
- **Add or remove assertions** — open the Assertions panel and adjust the rules to match your quality bar
- **Clone and iterate** — use the **Clone** or **Version** options to fork a prompt and experiment without losing the original
- **Lock a prompt** — once you've dialed in a prompt you're happy with, lock it to prevent accidental edits

---

## Assertion Types Used

These collections demonstrate all of Orion's built-in assertion types:

| Type | What it checks |
|---|---|
| `contains` | Response includes a specific string |
| `not_contains` | Response does not include a specific string (e.g. placeholder text) |
| `min_length` / `max_length` | Response length within expected range |
| `valid_json` | Response parses as valid JSON |
| `json_schema` | Response matches a JSON Schema definition |
| `llm_rubric` | An AI judge scores the response against a quality rubric (1–5) |

---

## Contributing

Have a prompt collection that others would find useful? Open a pull request. Good collections are:

- **Focused** — a clear theme or use case
- **Documented** — Notes on every prompt explaining what it does and how to use it
- **Tested** — assertions that catch real failure modes, not just green checkboxes
