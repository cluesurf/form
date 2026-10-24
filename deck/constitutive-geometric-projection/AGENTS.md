# Agents working in constitutive-geometric-projection

This is a form.surf model repository: Constitutive Geometric Projection. The metaphysical position of the MetaCortex Dynamics research program: an entity exists only when its constitutive activity satisfies a genealogical, a structural and a functional projection of one geometric structure at once, and consciousness is what being that entity is.
Format: form.surf/1, specified at https://form.surf/guides/developers/format.

Community-written from public sources, AI-extracted, unreviewed. Not written or endorsed by Devon Generally. To propose a correction, open an issue or pull request that changes the record and cites the source.

This repository is community-written. Its records state Devon Generally's own claims from public sources. They are AI-extracted and unreviewed unless a record's `provenance.reviewed` is true. It is not written or endorsed by Devon Generally.

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

    form check deck/constitutive-geometric-projection
