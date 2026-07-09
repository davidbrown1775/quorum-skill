# Output Structure

Quorum writes everything to disk so the user can navigate the work and act on it. Create this tree in the working folder. Checkpoint after each artifact, and commit if the workspace is a git repo. Never push or deploy.

```
quorum-review/
  00_OVERVIEW.md            # headline findings, status, and the summary to read first
  01_CURRENT-STATE.md       # what exists, what is thin, what is missing (the audit map)
  02_PANEL-FINDINGS/        # one file per panel: strengths, gaps, recommendations
  03_SYNTHESIS.md           # convergence, tension, and the ranked master list
  BACKLOG.md                # the prioritized backlog, scored
  ROADMAP.md                # the sequenced roadmap
  PRIORITIZATION-FRAMEWORK.md  # the durable, overrulable framework (see prioritization-framework.md)
  PRD.md                    # business-general PRD, or a handoff note to prd-taskmaster
  proposed/                 # drafts for any missing building blocks the board proposed
    vision-mission-values.md
    icp.md
    metrics-model.md
  _meta/
    ROSTER.md               # each seat, its lens, and its representation confidence
    INTERVIEW.md            # the user's answers
    ASSUMPTIONS.md          # defaults taken where the user did not answer
    SOURCES.md              # external claims with source and date
    PROGRESS.md             # updated after every artifact
    RESUME.md               # the exact next step if interrupted
    BUDGET.md               # any spend against the ceiling
    DECISIONS.md            # open decisions for the user
```

## Rules for the tree

- Create only what the run produces. If the user already has a roadmap, `ROADMAP.md` holds the review and the proposed changes, not a blank rewrite.
- `proposed/` holds only the building blocks that were missing. Do not propose blocks the user already has in good shape.
- Every draft asset starts with a "draft, for review" header and a note on which goal and which lens produced it.
- `00_OVERVIEW.md` is written last and read first. Lead with the headline, then the five things to look at, then what needs a decision.

## If there is no git repo

Still write the full tree. Skip the commits, keep `PROGRESS.md` and `RESUME.md` current, and tell the user the outputs are staged in `quorum-review/` for their review.
