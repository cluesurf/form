# Agents working in observer-first

This is a form.surf model repository: Algorithmic Idealism. Markus P. Müller's observer-first program, in which universal induction on an observer's present state sets what it sees next and the external world emerges.
Format: form.surf/1, specified at https://form.surf/guides/developers/format.

This repository is community-written. Its records state Markus P. Müller's
own claims from public sources. They are AI-extracted and unreviewed
unless a record's `provenance.reviewed` is true. It is not written or
endorsed by Markus P. Müller. To propose a correction, change the record
with the source and locator that shows the error, and open a pull request.

The main sources are peer-reviewed (Quantum, Foundations of Physics,
Nature Communications, Entropy) and on arXiv. Quotes are checked against
the arXiv versions, which can differ in wording from the published ones.
The 2024 paper renames "observer states" as "self states" and
"probabilistic zombies" as "probabilistic changelings": keep both names
in one record rather than two.

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

    form check deck/observer-first
