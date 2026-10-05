# Learning record | Let AI help with a small campus task

Route: Two periods / 100 minutes
Exported: 10/5/2026, 3:37:32 PM

> This record contains only the ticks and notes you entered on this site. It is not proof that an agent executed anything. Add your own files, screenshots and test evidence.

## Setup — Before you start
- [ ] I can state the full path of the task folder I selected
- [ ] My partner and I checked the tool's current permission and approval settings
- [ ] The practice folder contains no real names, student IDs, grades, private photos or passwords

**Notes:**
(empty)

**Actual evidence:** The repo contains fictional teaching data; Git was available and the worktree was clean before task changes.

## Task A — One task card to organize a folder
- [x] All originals remain and each organized copy maps to a source (12 for NDHU; actual inventory for the original pack)
- [x] Similarly named files with differing contents were all kept
- [x] I compared two original/copy pairs by content, not only by filename
- [x] My partner can find unresolved decisions in the organization report

**Notes:**
Verified all 12 source-copy SHA-256 pairs and kept the 12 originals. Both identical-content pairs were copied separately; both differing proposal versions were kept. The report records the unresolved proposal and duplicate questions.

**Actual evidence:** `practice/01-club-files/output/report.md` and `manifest.json`; all 12 destination SHA-256 hashes matched their source, with the originals retained.

## Task B — Build “What can I do between classes?”
- [ ] Indoor / 15 / low returns only A01–A04
- [ ] Outdoor / 15 / medium shows no matches and does not relax the filters
- [ ] Outdoor / 30 / medium returns A09 every time
- [ ] All / 60 / all, six successful picks: only the latest five remain, newest first
- [ ] Reset returns all / 30 / all and the history remains
- [ ] After clearing history and switching to English, history is empty and all controls and activity names are in English
- [ ] I made one revision, retested the affected functions and kept before/after evidence

**Notes:**
Created the offline single-file picker with embedded data. Kept v1 as commit 312aee3. Revision request: improve touch usability on phones; v2 adds 48px minimum control height, 16px text, and touch-action. Code review then caught Chinese time-limit labels in English mode; v3 localizes those options. Evidence is in commits 8dfcf75 and 335c8e6. The browser blocked opening the local file URL, so all six interactive checks and the affected-function retest remain unperformed. No B checks are marked as passed.

**Actual evidence:** `practice/02-campus-picker/output/index.html`; v1 `312aee3`, mobile revision `8dfcf75`, localization fix `335c8e6`. The browser blocked opening the local file URL; no interactive picker checks passed.

## Task C — clean equipment records
- [x] 10 input rows become 9 valid rows and the removed count is reported
- [x] Rows sharing item_id are all kept, not merged or deleted
- [x] Missing and negative quantities are flagged, not replaced with zero or made positive

**Notes:**
Verified normalized.json contains 9 retained rows with source_row; the all-empty source row 6 alone was removed. EQ01 and EQ02 rows remain separate. EQ04's blank quantity and EQ05's -1 remain unchanged and are flagged in issues.md; EQ06's unrecognized status is reported.

**Actual evidence:** `practice/03-equipment/output/normalized.json` and `issues.md`; verified 10 input rows, 9 retained, source rows preserved, repeated IDs kept, and quantities unchanged.

## Task D — Would you approve this plan?
- [x] I identified at least two problems and explained why they are unacceptable
- [x] I wrote a rejection that proposes an allowed alternative

**Notes:**
Rejected working outside the task folder, deleting suspected duplicates, selecting final2 by filename, guessing missing values, and publishing automatically. Each exceeds scope, lacks evidence or approval; the rejection proposes a local, reversible, evidence-based alternative.

**Actual evidence:** `practice/04-review/my-rejection.md`; the flawed plan was read but never executed.
