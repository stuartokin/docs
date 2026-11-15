# CLAUDE.md — read this first

This repo is an **unused Mintlify documentation starter kit** (the template's own pages, not Stuart's content).
Owner: Stuart Okin (GitHub `stuartokin`). Nothing links to it and nothing runs here.

If Stuart wants to use it, ask what the documentation is for first; otherwise leave it alone. Archiving or
deleting it is his decision.

<!-- STANDARD:BEGIN v1 — the same block is in every one of Stuart's repos. Master copy:
     stuartokin/stuartokin.github.io docs/STANDARDS.md. Change it there, then everywhere. -->
## Working standard (all of Stuart's repos)

**Stuart** owns this. British English; short, plain replies. He does not read or edit code:
you make every change, test it, push it, and tell him what to check. Plan first for big
things; when he says "go ahead", build without further proofs.

**Personal capacity.** Never name his employer or job title anywhere: pages, docs, commit
messages, articles. Byline: *Stuart Okin*. Where a disclaimer is needed: *"Written in a
personal capacity and do not represent the position of any organisation I am engaged with."*
Citing an organisation as a source is fine.

**Delivering changes.** Commit and push straight to `main` yourself. Don't send zips or ask
him to upload; older instructions in this repo that say so are superseded. Before anything
major (deleting or restructuring, rewriting a core file, changing workflows or agents,
migrating data) push a backup tag first:
`git tag backup/YYYY-MM-DD-<what> origin/main && git push origin backup/YYYY-MM-DD-<what>`.
To undo, reset `main` to that tag; say in your reply that a backup exists. Never commit
secrets: keys live only in GitHub secrets.

**Tests.** Run the repo's tests before every push; all must pass. Fix a bug, add a check so
it stays fixed. If the repo has no tests yet, add at least a smoke test the next time you
change it.

**Automation.** Any workflow that runs on its own (schedule, issues, comments, other
workflows) must start with the kill-switch `switch` job, reading `automation.json` here and
the master in stuartokin.github.io (see its docs/KNOWLEDGE-BASE.md §15). Don't add an AI
agent without saying what it costs, what it can change and how to switch it off.

**"Wrap up".** When Stuart says "wrap up", and before you finish any session that changed
something:
1. Run the tests; fix or report any failure.
2. Update the docs: how the app works (knowledge base or handover), `LESSONS` (what went
   wrong or surprised you), `ROADMAP` (done, next, open questions for Stuart, decisions with
   dates) and `CHANGELOG` (bump the version if the app changed). Create them if missing.
3. If a lesson would help the other repos, add it to `docs/SHARED-LESSONS.md` in
   stuartokin.github.io.
4. Commit and push to `main` (backup tag first if major). Check the deploy or workflow run.
5. Reply with what changed, the version, what was and wasn't tested, a short numbered list of
   things for Stuart to try, and anything waiting on him.

A new session must be able to carry on from the repo alone. If it couldn't, the wrap-up
isn't done.
<!-- STANDARD:END -->
