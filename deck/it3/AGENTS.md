# Agents working in it3

This is a form.surf model repository: IT3 and IT3-WavePixel. Victor Logvinovich's program, with Jean-Claude Perez, in which the vacuum is a discrete deterministic crystal over $\mathbb{Q}(\sqrt{2}, \sqrt{3}, \sqrt{5})$ and the periodic table is a binary register.
Format: form.surf/1, specified at https://form.surf/guides/developers/format.

This repository is community-written. Its records state Victor Logvinovich and Jean-Claude Perez's
own claims from public sources. They are AI-extracted and unreviewed
unless a record's `provenance.reviewed` is true. It is not written or
endorsed by Victor Logvinovich and Jean-Claude Perez. To propose a correction, change the record
with the source and locator that shows the error, and open a pull request.

The sources are Zenodo deposits (CC BY 4.0) and one X post. None is
peer reviewed. Several records have many versions under one concept DOI:
cite the version record read, and say which version in the locator. The
two September 2026 papers differ on whether the $\sqrt{13}$ wall makes
space compact: keep both claims, joined by the tension link, rather than
choosing one. The framework makes no claim about mind: do not add one.

## Rules

- One JSON record per file, in the folder named for its type:
  proposition, observation, procedure, link, source, question.
- Every id is a new lowercase UUIDv4. Never reuse or derive one.
- Fields and values are snake_case. File names are kebab-case.
- Every proposition has `kind`, `epistemic_status` and at least one statement.
- Never edit a statement's text. Add a new statement with `previous` set.
- Every claim cites a source in `provenance.sources`, with a locator and a
  short verbatim quote where you can check one. Never invent a DOI, page
  or quote.
- Set `provenance.ai_written` true and `model` when a model wrote it.
  Never set `reviewed` true: only a named person does that.
- State the framework's own claims. A criticism is `voice: "critique"`
  with its source.

## Commands

    form check .            validate. Must print PASS before any commit
    form diff               claim-level difference from the patterns folder
    form propose            suggest a pattern to the patterns folder

From the root of the form repository:

    form check deck/it3
