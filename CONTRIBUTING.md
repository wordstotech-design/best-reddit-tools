# Contributing

This is a vendor neutral list of Reddit tools, grouped by the job each one actually solves rather than by price. Corrections and additions are welcome.

## Edit the data, not the table

1. Edit [tools.yaml](tools.yaml). Fields: `name`, `url` (optional), `reddit_role`, `coverage`, `price_from`, `best_for`.
2. Run `python render_table.py --write` to regenerate the block between the `<!-- TABLE:START -->` and `<!-- TABLE:END -->` markers.
3. Open a PR and link a source for any pricing, coverage, or positioning claim.

## What gets merged

- `reddit_role` stated honestly, as the actual job the tool does for Reddit, not a generic listening label.
- `coverage` naming the real surfaces the tool watches, Reddit alone or Reddit plus other platforms.
- Real pricing, with the currency and tier named. Demo gated pricing stated as demo gated, not guessed at.

## What gets rejected

- Affiliate links. Vendor domain only.
- Duplicate rows. Update the existing entry.
- Adjectives in `best_for`. Name the buyer and the job.

## Setup

```bash
pip install pyyaml
python render_table.py          # preview
python render_table.py --write  # write into README.md
```
