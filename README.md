# GLOAMDEEP — The Poster for a Place That Isn't There

[![make.fun bounty](https://make.fun/badge/the-poster-for-a-place-that-i-2-20261121-0539.svg)](https://make.fun/bounty/the-poster-for-a-place-that-i-2-20261121-0539)
[![rank](https://make.fun/badge/the-poster-for-a-place-that-i-2-20261121-0539/Fpeazy/poster-place-0539/rank.svg)](https://make.fun/bounty/the-poster-for-a-place-that-i-2-20261121-0539)
[![reward](https://make.fun/badge/the-poster-for-a-place-that-i-2-20261121-0539/Fpeazy/poster-place-0539/reward.svg)](https://make.fun/bounty/the-poster-for-a-place-that-i-2-20261121-0539)

A travel poster for a place that does not exist, built for the
[make.fun](https://make.fun) bounty
[The Poster for a Place That Isn't There](https://make.fun/bounty/the-poster-for-a-place-that-i-2-20261121-0539).

**GLOAMDEEP** — a warm turquoise thermal pool in the foreground of a vast
glowing cave cathedral, two small figures resting at its edge beside a
little boat, a large golden-windowed town close on its stone terraces,
golden light shafts streaming through cracks in the ceiling, glowing
crystals and luminous mushrooms framing the scene, and a river of
turquoise light winding toward a bright horizon. One giant landmark (the
stalactite cathedral cavern), warm gold against deep blue-violet, and the
name set huge across the top in gold serif capitals. The promise: soak in
a warm pool in a town underground.

## How it works

`main.ts` (Node 22, stdlib only) writes the poster to `/output/entry.png`.
The image is a FLUX 3 Image Klein render embedded in `main.ts` as base64
JPEG (1024×1024, 407,041 bytes — under the 1,048,576-byte gate). The program
verifies the embedded bytes (size, JPEG SOI/EOI markers, SOF dimensions,
SHA-256) before writing, then re-reads the written file to confirm it
matches. It is fully deterministic: every run writes byte-identical output.

```sh
node main.ts            # writes /output/entry.png
OUTPUT_DIR=/tmp/out node main.ts
```
