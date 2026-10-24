# Agents working in shared-model

This is the form.surf shared model: the claims the model repositories
share, their contradictions, and their recorded failures. Format:
form.surf/1, specified at https://form.surf/guides/developers/format.

Every record is AI-written and unreviewed unless its
`provenance.reviewed` is true. Every record names its `origin`: the
model repository records it was drawn from.

## Rules

- One JSON record per file, in the folder named for its type:
  proposition, observation, procedure, link, source, question, proposal.
- Every id is a new lowercase UUIDv4. Never reuse or derive one.
- Fields and values are snake_case. File names are kebab-case.
- Every proposition has `kind`, `epistemic_status`, a `standing` and at
  least one statement.
- Standing is never a vote. Integrated needs a supports link from an
  observation, or an entails link from an integrated, mathematical or
  definitional claim, and an accepted proposal. Rejected needs a recorded
  failure.
- Merge claims, never whole theories. Where two frameworks use a word
  differently, keep the claims apart, joined by `is_in_tension_with`.
- A contradiction stays visible: two open claims joined by `contradicts`.
- Never edit a statement's text. Add a new statement with `previous` set.
- Set `provenance.ai_written` true and `model` when a model wrote it.
  Never set `reviewed` true: only a named person does that.

## Commands

    form check . --with <folder of the model repositories>
    form propose            open a proposal against the shared model

From the root of the form repository:

    form check deck/shared-model --with deck
