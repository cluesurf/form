# Agents working in patterns

This is the form.surf patterns folder: what two or more models have in
common or at issue, pointing at the models' own claims. Format:
form.surf/1, specified at https://form.surf/guides/developers/format.

Every record is AI-written and unreviewed unless its
`provenance.reviewed` is true.

## Rules

- One JSON record per file, in the folder named for its type: question,
  proposition, link, proposal. Never observation, source, procedure or
  paper: evidence and prose live in the models.
- Every id is a new lowercase UUIDv4. Never reuse or derive one.
- Fields and values are snake_case. File names are kebab-case.
- A proposition here is a same idea: a neutral wording of its own, and an
  `origin` naming records in two or more model folders. It has no
  `standing` field.
- A link belongs to the folder that holds both its ends. A link here has
  its ends in different models, and its relation is `contradicts`,
  `is_in_tension_with`, `supports`, `weakens`, `specializes`,
  `generalizes` or `answers`.
- Where two frameworks use a word differently, keep the claims apart,
  joined by `is_in_tension_with`. Never merge whole theories.
- Never a vote, never a ranking. A model's standing stays in its folder.
- Never edit a statement's text. Add a new statement with `previous` set.
- Set `provenance.ai_written` true and `model` when a model wrote it.
  Never set `reviewed` true: only a named person does that.

## Commands

From the root of the form repository:

    form check deck/patterns --with deck
