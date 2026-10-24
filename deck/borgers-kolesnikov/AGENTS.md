# Agents working in borgers-kolesnikov

This is a form.surf model repository: Causal Recursion Field Theory and BKVS. Brent Borgers's CRFT, reality as information projected from a 9D source at a fixed geometric tax, with the joint Borgers-Kolesnikov Vacuum Spectroscopy (BKVS) and Maxim Kolesnikov's admissibility.
Format: form.surf/1, specified at https://form.surf/guides/developers/format.

This repository is community-written. Its records state Brent Borgers and Maxim Kolesnikov's
own claims from public sources. They are AI-extracted and unreviewed
unless a record's `provenance.reviewed` is true. It is not written or
endorsed by Brent Borgers and Maxim Kolesnikov. To propose a correction, change the record
with the source and locator that shows the error, and open a pull request.

The sources are Zenodo deposits, Substack posts and Academia.edu papers.
None is peer reviewed, though the July 15, 2026 Substack post calls its
archive peer-reviewed: record what the deposit is, not what a post calls
it. Many papers credit language models as co-authors or verifiers. State
that as plain fact, never as a judgment. The numerical claims (the
Borgers Impedance, the fine-structure value $4248/\pi^3$, the Wieferich
anchors) are stated as claimed and labeled `hypothesized`, never more.
Kolesnikov's solo papers are on Academia.edu, which offers no stable
per-paper address that could be checked, so their sources point at his
profile page.

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

    form check deck/borgers-kolesnikov
