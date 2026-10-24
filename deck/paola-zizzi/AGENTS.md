# Agents working in paola-zizzi

This is a form.surf model repository: Quantum-computing universe (Zizzi). Paola Zizzi's program in which Planck-scale space-time is a quantum computer whose pixels of area each hold a qubit, the inflationary universe is that computer growing until it self-reduces by Penrose's objective reduction, and that reduction is a conscious event of the same kind as a human one.
Format: form.surf/1, specified at https://form.surf/guides/developers/format.

This repository is community-written. Its records state Paola A. Zizzi's
own claims from public sources. They are AI-extracted and unreviewed
unless a record's `provenance.reviewed` is true. It is not written or
endorsed by Paola A. Zizzi. To propose a correction, change the record
with the source and locator that shows the error, and open a pull request.

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

    form check deck/paola-zizzi
