# Task A: Club files organization

## Scope and checks

- Read only from `input/` and wrote organized copies and this report within `output/`.
- Found 12 input text files and copied each exactly once. The input originals were kept unchanged.
- Compared file contents: `announcement.txt` and `announcement_copy.txt` are identical; `equipment_list.txt` and `equipment_backup.txt` are identical.
- `proposal_final.txt` and `proposal_final2.txt` have different contents. Their filenames do not establish approval, so both are preserved.
- No tools were installed and no internet access was used during file organization.

## Categories

- `communications/`: announcement copies and poster text.
- `planning/`: meeting notes, next steps, rain plan, and both proposal versions.
- `resources/`: budget draft and both equipment-list copies.
- `feedback/`: feedback questions.

## Suspected duplicates

- `announcement.txt` / `announcement_copy.txt`: identical contents; both copies are retained.
- `equipment_list.txt` / `equipment_backup.txt`: identical contents; both copies are retained.

## Unresolved questions

- Which activity proposal, if either, should be selected? The two proposals differ and both say they are undecided.
- Are the duplicate announcement and equipment files intentional backups or redundant copies? Human review is needed before any consolidation.

## Verification performed

- Confirmed the input inventory contained 12 files before copying.
- Verified all 12 manifest entries map an input filename to one output copy.
- Compared source and destination SHA-256 hashes for all 12 copies; all pairs matched.
- Confirmed the input file count remains 12 after copying.

## Still unverified

- No decision was made about which proposal to use or whether any identical files should be consolidated.
