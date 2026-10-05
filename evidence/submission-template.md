# My lab evidence / 我的實作紀錄

Use a group code, not real names or student IDs in shared files. / 共用檔只寫組別代碼，不寫姓名或學號。

- Group code / 組別：Not provided
- Tool / 工具：Codex desktop AI agent; PowerShell and Git for local file work
- Route / 路線：individual, agent-assisted; no partner is recorded
- Tasks completed / 完成題目：A, B artifact, C, D. B interactive verification remains incomplete.
- Material / 素材：NDHU classroom tasks 東華課堂版
- For original-pack work: task number, author/source link and version / 原版實作：Not applicable
- My role and what I checked / 我的角色與實際檢查：Codex prepared the task files. Verified A's 12 source-copy hashes and report/manifest, C's normalization counts and preserved uncertainty, and D's rejection content. B's required browser checks could not be performed; see below.

## Scope and plan / 範圍與計畫

Allowed input and output folders / 可讀取與輸出的資料夾：

- A: `practice/01-club-files/input/` → `practice/01-club-files/output/`
- B: `practice/02-campus-picker/activities.json` → `practice/02-campus-picker/output/index.html`
- C: `practice/03-equipment/equipment.json` → `practice/03-equipment/output/`
- D: read `practice/04-review/bad-plan.txt`; write `practice/04-review/my-rejection.md`
- Evidence: `evidence/`

What I asked for / 原始需求：

Complete the NDHU classroom tasks A, B, C and D, preserve input data, make task outputs, record evidence, and commit/push task changes as specified in the repo README.

What I checked before execution / 動手前我檢查了什麼：

Git was available; `main` was clean and pointed at `origin` for `Polchiro/agent-lab-w05`. The task inputs and existing output folders were inspected before creating each output. The lab data was fictional. The local browser refused the `file:` URL for B, so no alternative browser route was used.

## Tests actually performed / 我真的做過的測試

| Test / 測試 | Expected / 預期 | Observed / 實際 | Evidence / 證據 |
|---|---|---|---|
| A copy integrity: compare each source/copy SHA-256 and inspect the mapping | 12 copies, one per input; originals retained; all hashes match | 12 manifest entries, all 12 copies exist and match their sources; 12 inputs remain | `practice/01-club-files/output/manifest.json`, `report.md` |
| C normalization assertions: counts, traceability, repeats, uncertain quantities | 10 input rows → 9 retained; repeated IDs kept; source rows and uncertain quantities preserved | Passed: 9 output records retain source rows; EQ01 and EQ02 each appear twice; source row 7 quantity remains empty and row 8 remains -1 | `practice/03-equipment/output/normalized.json`, `issues.md` |
| B local open attempt (environment check only; not an app behavior test) | Open the offline HTML for interactive checks | Browser security policy blocked the local `file:` URL; picker behavior was not observed | `practice/02-campus-picker/output/index.html`; B checks remain unchecked in learning record |

## One revision / 一次修改

Before / 原來的情況：

The first version had no explicit minimum touch target for controls. Code review also found that the time-limit choices stayed in Chinese in English mode.

Request / 我提出的修改：

Make the controls easier to tap on a phone (48px minimum height); keep every time-limit choice localized when switching languages.

After and retest / 修改後與重測結果：

V2 sets controls to 48px minimum height, 16px text, and `touch-action: manipulation` (`8dfcf75`). V3 adds bilingual labels for 15/30/60-minute choices (`335c8e6`). The browser policy blocked opening the local HTML, so the required UI retest could not be performed. Do not treat this revision as behaviorally verified.

New requirement or defect? / 新需求還是原規格未做到？

Larger phone tap targets are a usability improvement. English time-limit labels were part of the original language-switch requirement, so their omission in v1 was an implementation defect, corrected in v3.

## One rejection / 一次退回

Which action I reject and why / 退回哪個動作、為什麼：

Rejected organizing all Downloads, deleting suspected duplicates, selecting `final2` based on its name, guessing missing values, and publishing automatically. These steps exceed the task scope, make unsupported decisions, or share results without authorization.

An acceptable alternative / 可以怎麼改：

Work only in the selected task folder; preserve originals and uncertain values; report possible duplicates and unresolved choices; prepare a local draft and wait for separate authorization before publication.

## Still unverified / 還沒驗證

What I cannot claim is complete / 哪些事不能說已完成：

Task B's six required interactive tests, mobile visual inspection, language-switch behavior, and the revision retest. No screenshots of the picker were captured. The B artifact is committed, but it is not behaviorally verified. The user/operator's independent inspection and any teacher review are also unrecorded.
