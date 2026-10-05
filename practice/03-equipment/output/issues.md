# Equipment record cleaning notes

## Counts

- Input rows: 10
- Valid rows retained: 9
- Rows removed: 1 (source row 6 was entirely empty)

## Normalization performed

- Trimmed surrounding whitespace from text fields (`item_id`, `name`, and `status`).
- Mapped `available`, `可借`, and `可出借` to `available`.
- Mapped `borrowed` and `借出` to `borrowed`.
- Mapped unrecognized statuses to `unknown` and recorded them below.
- Kept every non-empty row, including repeated `item_id` values. Retained each `source_row`.
- Preserved `qty` exactly as supplied; missing or invalid values were not guessed or replaced.

## Quantity issues

- Source row 7 (EQ04, Paper pack / 紙張包): quantity is an empty string. It remains empty; quantity is unknown.
- Source row 8 (EQ05, Tape / 膠帶): quantity is -1, which is outside the accepted nonnegative integer range. It remains -1 and is flagged.

## Unrecognized statuses

- Source row 9 (EQ06, Scissors / 剪刀): original status `待盤點` was normalized to `unknown`.

## Repeated item IDs

- EQ01 appears in source rows 1 and 4. After trimming, both rows have the same name, quantity (4), and normalized status (`available`). Both are retained; their identical fields do not authorize merging.
- EQ02 appears in source rows 2 and 5. Both have the same name and normalized status (`borrowed`), but quantities conflict (2 versus 3). Both are retained for review.

Same names alone were not treated as proof that records represent the same item. No records were merged or deleted except the all-empty source row 6.
