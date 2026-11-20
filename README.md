# 20 November 2026 — Six Developments

An original illustrated digest of six verified news developments from one day:
Ukraine, Yemen, COP31, Indonesia–China business MoUs, the WFP funding appeal,
and US stock-market losses.

![Selected original news image](assets/entry.png)

## Local status

The image and entrypoint are local build artifacts, not a submitted make.fun
entry. GitHub authentication and the repository owner have not been verified.
The official competition/rank/reward badges and GitHub About must be finalized
from the current requirements after the real GitHub owner and public repository
are known. No owner, repository URL, entry ID or server score is invented here.

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
