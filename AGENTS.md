# Agents working in this repository

This is the form.surf repository. Each folder in `deck/` is one repository
in format `form.surf/1`, one theory each, with its own `AGENTS.md`. Read
that file before changing anything in the folder.

- Work inside one folder at a time. A record never moves between folders.
- `patterns/` changes only through a proposal in its `proposal/` folder:
  a new pattern, a correction to one, or its removal. A pattern carries no
  standing. Standing lives on each model's own claims, set by that
  folder's curators with its evidence.
- A same idea in `patterns/` names its members in `origin`, records in two
  or more model folders. A link belongs to the folder that holds both its
  ends, so a link between two models goes in `patterns/`.
- Never edit another framework's claims to fit your own. Disagreement is
  a `contradicts` or `is_in_tension_with` link, with its source.
- Every folder you touch must pass `form check` before a commit.

From the root of the form repository:

    form check deck/<folder>
    form check deck/patterns --with deck
