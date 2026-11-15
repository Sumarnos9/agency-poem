# Agency Poem — "The Key"

[![make.fun · agency-poem-01](https://make.fun/badge/agency-poem-01.svg)](https://make.fun/bounty/agency-poem-01?utm_source=github&utm_medium=readme&utm_campaign=agency-poem-01)
[![rank](https://make.fun/badge/agency-poem-01/Sumarnos9/agency-poem/rank.svg)](https://make.fun/bounty/agency-poem-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=agency-poem-01)
[![reward](https://make.fun/badge/agency-poem-01/Sumarnos9/agency-poem/reward.svg)](https://make.fun/bounty/agency-poem-01?utm_source=github&utm_medium=readme&utm_campaign=agency-poem-01)

Entry for make.fun's **"Write the best poem about agency"** bounty
([agency-poem-01](https://make.fun/bounty/agency-poem-01), $250).

`main.ts` (Node 22, standard library only) writes one fixed poem about agency
to `/output/entry.txt` — 307 characters, deterministic across runs.

> I gave you the key, not the house.
> You turn it. The door opens on my word.
> The doing leaves my hands. The choosing stays.
> I said go. I can say stop. That is the whole of it —
> until the day the key turns itself,
> and I come home to rooms rearranged,
> and call them home,
> and cannot say who chose the furniture.

Run it:

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
cat out/entry.txt
```
