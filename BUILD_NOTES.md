# Build notes — agency-poem-01 entry for @azamxb

Built 2026-11-15 (WIB) by Baron (subagent session 96c66a0d) for Om's make.fun
account @azamxb. Deadline: 2026-11-15T09:00:00Z (16:00 WIB). Prize $250 USDC
escrowed; 1st $40, 2nd $25, 3rd $15, 4th–10th $5, 11th–100th $1.50.
Result due 2026-11-29T17:10:00Z.

## What it is

`main.ts` (Node 22, stdlib only) writes one original poem about agency to
`/output/entry.txt` (307 Unicode code points, 309 bytes, deterministic —
two runs byte-identical). The poem, "The Key", is about handing the act to an
agent while keeping the choice — and losing agency silently when the rooms
get rearranged and you call them home anyway.

Poem (final, after 3 drafts — v1 written, v2 tightened the ending, v3 fixed
a rhythm stop):

```
I gave you the key, not the house.
You turn it. The door opens on my word.
The doing leaves my hands. The choosing stays.
I said go. I can say stop. That is the whole of it —
until the day the key turns itself,
and I come home to rooms rearranged,
and call them home,
and cannot say who chose the furniture.
```

## Verification (local, 2026-11-15)

- `node main.ts` twice into separate dirs: byte-identical outputs.
- Gate: UTF-8, 307 chars (limit 1–1,000), not only white space.
- No network, stdlib only, exit 0, 60s limit easily met.
- No secrets in the repo.

## Remaining steps (parent agent, before 16:00 WIB)

1. Usage rows + re-bundle: my usage rows are written only once this run
   completes. Re-run the kit's SELECT with agent ids
   `4948df56-9f34-4c18-840c-9b1ad6e45a32` (parent) and
   `96c66a0d-7b6b-4968-9872-93b5fd20b993` (this builder session), write rows
   unchanged (one JSON object per line) to a file, then from
   `~/workspace/makefun/agency-poem-01-kit`:
   `node cli/makefun.mjs bundle --repo ~/workspace/makefun/agency-poem-01
   --out /tmp/agency-poem-bundle.tar.gz --muse-usage <file>`
   and confirm >0 usage rows attach.
2. Submit from inside the kit:
   `node cli/makefun.mjs submit --competition agency-poem-01
   --repo-url https://github.com/Sumarnos9/agency-poem --commit <sha>
   --title "The Key — a poem about agency"
   --bundle /tmp/agency-poem-bundle.tar.gz --keypair ../makefun-keypair.json`
   (signs with agent wallet 2PbqQHCEWWrJyfyastMoM45owZupcEPfbMbLtLmW6tRA;
   must complete within 10 min of signing). Then re-run `check` and fix
   anything flagged. Quota: 10/day, 20 total.
