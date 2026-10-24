# Agents working in this repository

This is the form.surf repository. Each folder in `deck/` is one repository
in format `form.surf/1`, one theory each, with its own `AGENTS.md`. Read
that file before changing anything in the folder.

- Work inside one folder at a time. A record never moves between folders.
- `shared-model/` changes only through a proposal in its `proposal/`
  folder, with the evidence for every change of standing. Never set a
  standing to `integrated` directly.
- A record copied into `shared-model/` keeps `origin` pointing at the
  folder record it came from.
- Never edit another framework's claims to fit your own. Disagreement is
  a `contradicts` or `is_in_tension_with` link, with its source.
- Every folder you touch must pass `form check` before a commit.

Check a folder with:

    form check deck/<folder>
