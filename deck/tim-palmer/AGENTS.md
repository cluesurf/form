# Agents working in tim-palmer

This is a form.surf model repository: Invariant set theory. Tim N. Palmer's program in which the geometry of a fractal invariant set in the universe's state space is the primitive law, quantum mechanics is a singular limit, and Bell violation is superdeterministic.
Format: form.surf/1, specified at https://form.surf/guides/developers/format.

This repository is community-written. Its records state Tim N. Palmer's
own claims from public sources. They are AI-extracted and unreviewed
unless a record's `provenance.reviewed` is true. It is not written or
endorsed by Tim N. Palmer. To propose a correction, change the record
with the source and locator that shows the error, and open a pull request.

The sources are peer-reviewed papers (Proceedings of the Royal Society A,
Contemporary Physics, Frontiers in Physics, Entropy, AVS Quantum Science)
and arXiv preprints. Quotes are checked against the arXiv versions.
Palmer uses "superdeterministic" only in the formal sense of violating
Statistical Independence in Bell's theorem, and denies the theory is
conspiratorial or fine tuned: keep that distinction in any rewording.

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

    form check deck/tim-palmer
