# Agent Instructions — TuLAUT Dataset Catalog

This repository is the source for the TuLAUT GitHub Pages site (tulaut.github.io), a curated catalog of datasets. It's plain Jekyll (`jekyll-theme-minimal`, see `_config.yml`) with no build step or validation — every file you write here must already be in its final, correct form.

## Your job

When a user asks you to add a dataset, do exactly two things and stop:

1. Create one new dataset card: `ds_<Name>.md` at the repo root.
2. Add one new row for it to the table in `README.md`.

Don't do anything beyond that unless explicitly asked — see "Hard constraints" below.

## Inputs you need from the user

The user will describe the dataset in their message (name, links, description, paper info, etc.). Required, at minimum:
- A dataset name/title
- A link to where the data actually lives (repo, DOI, data portal, ...)

Everything else is optional — populate it if given, otherwise use a `-` placeholder exactly as existing cards already do. Never invent descriptions, authors, years, institutions, task labels, or domain labels that weren't given to you. If the name or data link is missing, ask before creating anything.

## Step 1 — Check for an existing entry first

Before creating anything, check whether this dataset already has a card: look at the `ds_*.md` filenames at the repo root and skim `README.md`'s table for a matching name or link. If you find a likely duplicate, tell the user instead of creating a second entry.

## Step 2 — Create the dataset card

File: `ds_<Name>.md` at the repo root (same level as `README.md`, next to the other `ds_*.md` files).
- `<Name>` is a short, unique identifier with no spaces, built from the dataset's name (e.g. `ds_CobotAnomaly.md`, `ds_MZVAV.md`) — follow the CamelCase/underscore style already used by the other files in this directory.
- Use `ds_dummy.md` as the structural template. Its sections, in order:

  ```
  ## <Dataset title>

  ### Description
  <one or more paragraphs, using the user's own content — not invented>

  ### Link to <what this actually is — e.g. "GitHub repository with data" / "repository with data" / "Zenodo record" / "DaRUS record">
  [<label>](<url>)

  ### Published Papers

  | Title    | Authors       | Year |
  |:-|:-|:-|
  |[<paper title>](<paper url>) | <authors> | <year> |
  ```

- Adapt the link section's heading to name the actual host — don't always say "GitHub" (existing cards use "Link to GitHub repository with data", "Link to repository with data", "Link to Zenodo record", etc., depending on what was actually given).
- If no paper was given, keep the "Published Papers" table with one row of `-` placeholders (see `ds_MZVAV.md`) rather than deleting the section.
- Add a trailing `### Contact` section only if the user gave you contact info (email, ORCID, ...); otherwise leave it out entirely.
- The `##` title should be descriptive enough to be cited on its own — this mirrors the authoring checklist in `guidelines.md` (see below).

## Step 3 — Add the README entry

`README.md` has one table, under `### Available Datasets`, with columns `Data Set | Task | Domain`. Append one new row at the bottom of that table (existing rows are in insertion order, not alphabetical — don't resort the table):

```
| [<Display Name>](https://tulaut.github.io/ds_<Name>) | <task keywords> | <domain> |
```

Get this part exactly right — it's the one place it's easy to get subtly wrong:
- The link is **`https://tulaut.github.io/ds_<Name>`** (the published Pages URL) — **not** a `github.com/...` link, **not** a relative link like `ds_<Name>.md`, and **without** the `.md` extension. Every existing row follows this pattern; copy it exactly.
- `<Display Name>` is a short human-readable label — it doesn't have to match the card's `##` title verbatim (e.g. the card titled "Data Sets for Evaluation of Building Fault Detection and Diagnostics Algorithms" is listed as "Building Fault Detection and Diagnostics").
- `<task keywords>`: comma-separated, lowercase, matching the style of existing rows (e.g. `anomaly detection`, `diagnosis`, `planning`, `classification`, `prediction`, `condition monitoring`). Only include what the user told you or what's obvious from the description they gave you; use `-` if not known.
- `<domain>`: short label for the industry/application area (e.g. `process plants`, `chemical plant`, `building automation`). Use `-` if genuinely not known rather than guessing.

## Updating an existing card

If the user asks you to update/correct an already-published dataset (not add a new one), edit only that one `ds_*.md` file and, if the changed details affect it, its matching README row — nothing else. The same constraints below still apply.

## Hard constraints

- **No git commands, period.** Don't run `git add`, `git commit`, `git push`, or anything else that touches git state — not even staging. Just create/edit the files and leave the working tree for the user to review and commit themselves.
- **Never delete anything** — not files, not existing README rows, not content inside other cards.
- **Never push, and never open a PR**, unless explicitly asked.
- **Scope your edits.** Touch only the new `ds_*.md` file and its one new row in `README.md` (or, for an update, the single card/row being corrected). Don't touch `guidelines.md`, `_config.yml`, or unrelated dataset cards.
- **Don't fabricate.** Descriptions, authors, years, tasks, and domains must come from what the user gave you. Use `-` placeholders where information is missing, matching existing cards.

## When you're done

Tell the user which file(s) you created or changed and summarize the new content (or point them at the diff). They review, commit, and push themselves.

## `guidelines.md`

That file is a legal/metadata checklist (in German) for dataset authors and curators — copyright, personal data, licensing, citability of the title, completeness of metadata. It's aimed at the humans deciding whether a dataset is fit to publish, not at you. You're not expected to evaluate legal or privacy compliance — if something the user gives you looks obviously sensitive (e.g. personal data with no mention of anonymization/consent, no license anywhere), flag it to them, but the judgment call is theirs.
