# Optional v3 Research-Group Interface

Load only for a task that actually calls for handoff or consolidated findings. This Skill is standalone otherwise.

- **Owner:** Extract atomic claims and their evidence/logic relations and reconstruct author-approved text.
- **Not responsible for:** Changing the scientific claim or using unsupported evidence to make prose sound convincing.
- **Chinese activation:** 命题图写作、论证结构调整、论文逻辑重组.
- **English activation:** claim graph, academic argument restructure.
- **Avoid triggering for:** unrelated scientific validity review, generic formatting, or an unrequested batch of all specialists.
- **Optional downstream:** ai-paper-editor for language/structure follow-up; ai-strict-reviewer for unresolved scientific claims; requires actual availability and user-authorised action.

## Role-specific safeguard

Do not let structure reconstruction silently increase claim strength. Preserve each claim ID, supporting evidence, uncertainty, and author-approved scientific meaning.

## Shared issue and evidence contract

`ID | owner | document/version/location | issue/claim | located evidence | source status | assessment | local scientific Severity or QA Impact/urgency | next action | author decision | state`.

Source status is `Reported / Documented / Independently checked / Not available`. Assessment `Confirmed / Reasoned inference / Unverified` must specify what was checked. State `Open / Waiting for evidence / Awaiting author / Resolved / Recheck needed`. Do not claim an external call, completed work, a saved ledger or source verification without actual evidence.

## Ledger and efficient routing

If supplied/authorised, reuse Claim ID, Data ID, sources and locations, conditions/baseline, units, dataset or script versions, verification status, and linked issue IDs; this ledger does **not** automatically sync across apps. One issue owner; optional specialist handles a distinct subquestion, not a duplicate full review. Route only when justified. After approved changes, revisit only affected records. Default workflow is literature → approved execution → scientific review → editing → final QA, with feedback loops; do not impose it on narrow requests.
