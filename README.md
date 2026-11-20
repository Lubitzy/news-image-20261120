# 20 November 2026 — Six Developments

[![make.fun · news-image-20261120](https://make.fun/badge/news-image-20261120.svg)](https://make.fun/bounty/news-image-20261120?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261120)
[![rank](https://make.fun/badge/news-image-20261120/Lubitzy/news-image-20261120/rank.svg)](https://make.fun/bounty/news-image-20261120/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261120)
[![reward](https://make.fun/badge/news-image-20261120/Lubitzy/news-image-20261120/reward.svg)](https://make.fun/bounty/news-image-20261120?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261120)

An original illustrated digest of six verified news developments from one day:
Ukraine, Yemen, COP31, Indonesia–China business MoUs, the WFP funding appeal,
and US stock-market losses.

![Selected original news image](assets/entry.png)

## Publication and submission status

Prepared for the public GitHub repository `Lubitzy/news-image-20261120`.
GitHub authentication has been verified for its owner, `Lubitzy`. The live
competition, rank and reward badges above refer to that repository; they do
not assert an accepted entry, a rank or an earned reward. This package has
not yet been submitted to make.fun. Transcript packaging and the official kit
checks remain separate pre-submission steps.

Competition: https://make.fun/bounty/news-image-20261120

## Run the submitted program

Python 3.13, standard library only; no package installation and no network:

```sh
python main.py
```

The default destination is `/output/entry.png`. For a local writable destination:

```sh
python main.py --output-dir .local-output
```

The program copies the committed PNG byte for byte. Its output does not depend
on fonts, Pillow, timestamps, random values, external services or the working
directory.

## Verify

```sh
python tools/verify_entry.py --report VERIFICATION.json
```

The verifier checks PNG structure, all chunk CRCs, the complete RGB image-data
stream, dimensions and byte cap. It runs the entrypoint twice in separate empty
directories using `-I -S`, with socket operations denied, compares the complete
outputs and checks that the entrypoint imports only standard-library modules.
Use Python 3.13 to reproduce the recorded runtime test.

## Artwork and editorial evidence

- `NOTES.md`: the six bounded claims, two independent newsrooms per story,
  source URLs, attribution and date/uncertainty checks.
- `DESIGN_REVIEW.md`: three original compositions, pairwise comparisons,
  retained revisions and the limits of the available inspection tools.
- `tools/make_image.py`: authored geometric drawing code. Pillow is needed only
  for optional offline artwork authoring, not to run `main.py`.
- `assets/entry.png`: the selected, fixed original image.

Optional regeneration with Pillow installed and a supported local font:

```sh
python tools/make_image.py --variant all --out-dir ../design-review/rebuilt
```

Rendering uses local Arial or DejaVu fonts; no font program, photograph, logo,
downloaded artwork or competitor image is distributed. Regenerated PNG bytes
can depend on Pillow/font versions. This does not affect the deterministic
runtime, which copies the already committed image.

## License

MIT; see `LICENSE`. The illustrations are original geometric artwork.
