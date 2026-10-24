# Agents working in matter-as-machine

This is a form.surf model repository: Matter As Machine. The matterasmachine.com framework: everything is execution, particles are cyclic machines, and evolution is slow creation by simple machines steered by instincts.
Format: form.surf/1, specified at https://form.surf/guides/developers/format.

This repository is community-written. Its records state the claims of the author of matterasmachine.com
from the site's public pages. They are AI-extracted and unreviewed
unless a record's `provenance.reviewed` is true. It is not written or
endorsed by the author of matterasmachine.com. To propose a correction, change the record
with the page and locator that shows the error, and open a pull request.

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
- Use only the pages the site marks free to read. The site has no open
  license: restate its ideas in new words and keep quotes to one or two
  sentences. Record nothing about the author beyond the site's own name.

## Commands

    form check .            validate. Must print PASS before any commit
    form diff <shared>      claim-level difference from the shared model
    form propose            open a proposal against the shared model

From the root of the form repository:

    form check deck/matter-as-machine
