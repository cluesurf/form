# Agents working in predictive-processing

This is a form.surf model repository: Predictive Processing. Perception and selfhood as controlled hallucination, grounded in the predictive regulation of a living body.
Format: form.surf/1, specified at https://form.surf/guides/developers/format.

Community-written from public sources. AI-extracted (claude-opus-5-5) and unreviewed. Not written or endorsed by Anil Seth or his collaborators. This repository is community-written. Its records state Anil Seth's own claims from public sources. They are AI-extracted and unreviewed unless a record's `provenance.reviewed` is true. It is not written or endorsed by Anil Seth. To propose a correction, open a pull request that changes the record and cites the source passage.

## Rules

- One JSON record per file, in the folder named for its type:
  proposition, observation, procedure, link, source, question.
- Every id is a new lowercase UUIDv4. Never reuse or derive one.
- Fields and values are snake_case. File names are kebab-case.
- Every proposition has `kind`, `epistemic_status` and at least one statement.
- Never edit a statement's text. Add a new statement with `previous` set.
- Every claim cites a source in `provenance.sources`, with a locator and a
  short verbatim quote where you can check one. Never invent a DOI, page
  or quote. Page locators marked "accepted manuscript" refer to the open
  author copy linked in the source's `url`, not the journal pagination.
- Set `provenance.ai_written` true and `model` when a model wrote it.
  Never set `reviewed` true: only a named person does that.
- State the framework's own claims. A criticism is `voice: "critique"`
  with its source.
- Clark and Hohwy are related sources only. Claims here are Seth's version.

## Commands

    form check .            validate. Must print PASS before any commit
    form diff               claim-level difference from the patterns folder
    form propose            suggest a pattern to the patterns folder

From the root of the form repository:

    form check deck/predictive-processing
