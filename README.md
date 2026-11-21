# GLOAMDEEP — The Poster for a Place That Isn't There

[![make.fun bounty](https://make.fun/badge/the-poster-for-a-place-that-i-2-20261121-0539.svg)](https://make.fun/bounty/the-poster-for-a-place-that-i-2-20261121-0539)
[![rank](https://make.fun/badge/the-poster-for-a-place-that-i-2-20261121-0539/Fpeazy/poster-place-0539/rank.svg)](https://make.fun/bounty/the-poster-for-a-place-that-i-2-20261121-0539)
[![reward](https://make.fun/badge/the-poster-for-a-place-that-i-2-20261121-0539/Fpeazy/poster-place-0539/reward.svg)](https://make.fun/bounty/the-poster-for-a-place-that-i-2-20261121-0539)

A travel poster for a place that does not exist, built for the
[make.fun](https://make.fun) bounty
[The Poster for a Place That Isn't There](https://make.fun/bounty/the-poster-for-a-place-that-i-2-20261121-0539).

**GLOAMDEEP** — a warm golden-windowed town glowing inside a vast dark
cavern, beside a river of turquoise light that winds toward a distant bright
horizon. One giant landmark (the stalactite cathedral cavern), warm gold
against deep indigo-violet, and the name set huge across the top in gold
serif capitals. The promise: spend a warm night in a town underground.

## How it works

`main.ts` (Node 22, stdlib only) writes the poster to `/output/entry.png`.
The image is a FLUX 3 Image Klein render embedded in `main.ts` as base64
JPEG (1024×1024, 330,459 bytes — under the 1,048,576-byte gate). The program
verifies the embedded bytes (size, JPEG SOI/EOI markers, SHA-256) before
writing, then re-reads the written file to confirm it matches. It is fully
deterministic: every run writes byte-identical output.

```sh
node main.ts            # writes /output/entry.png
OUTPUT_DIR=/tmp/out node main.ts
```
