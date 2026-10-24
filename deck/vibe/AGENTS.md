# Agents working in vibe

This is a form.surf model repository: Vibe Theory. Vibe explores whether
physics and experience could both emerge from a relatively simple rule
on a structured space. Its work so far leans toward one reversible rule
on the four-dimensional hyperbolic honeycomb {3,4,3,4}.
Format: form.surf/1, specified at https://form.surf/guides/developers/format.

This repository is written by the framework's originator, Lance Pollard.
Its records are generated from the vibe research database. Never edit a
record here: propose the change as a pull request, and it is carried
into the research database and the next generation.

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
- Set `supported` only with a basis link into the claim: `supports`
  from an observation, or `entails` from a supported, mathematical or
  definitional claim. A negative result stays, `rejected`, with the
  observation that failed it.

## Commands

    form check .            validate. Must print PASS before any commit
    form diff               claim-level difference from the patterns folder
    form propose            suggest a pattern to the patterns folder

From the root of the form repository:

    form check deck/vibe
