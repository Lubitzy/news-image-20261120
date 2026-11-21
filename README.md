# 20 November 2026 — Fifteen Developments

[![make.fun · news-image-20261120](https://make.fun/badge/news-image-20261120.svg)](https://make.fun/bounty/news-image-20261120?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261120)
[![rank](https://make.fun/badge/news-image-20261120/Lubitzy/news-image-20261120/rank.svg)](https://make.fun/bounty/news-image-20261120/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261120)
[![reward](https://make.fun/badge/news-image-20261120/Lubitzy/news-image-20261120/reward.svg)](https://make.fun/bounty/news-image-20261120?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261120)

An original illustrated digest of fifteen sourced developments from one day,
covering Europe, Asia, Africa, Oceania, the Americas, the Middle East and global
events. Three lead stories, six supporting panels and six attributed briefs
balance geographic breadth with a clear editorial hierarchy.

![Selected original news image](assets/entry.png)

## Publication and submission status

The public repository is `Lubitzy/news-image-20261120`. An earlier six-story
version was submitted as `01a1fb98-1a10-774d-9076-e316e284a5fe` and passed the
server's validity checks. This is the broader editorial revision, not a claim
that it has a better official score or has won a prize. Live badges refer to
this repository and may change as judging progresses.

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

- `stories.json`: fifteen concise claims with source URLs, date qualifications
  and a structural editorial check. Not every story has two independent newsrooms;
  single-source claims are clearly attributed.
- `NOTES.md`: the earlier six-story research, retained as development history.
- `DESIGN_REVIEW.md`: original review and the appended three-way revision comparison.
- `tools/render_revision.py`: current layout and new original drawing code;
  `tools/make_image.py` supplies shared geometry and retains the earlier layout.
  Pillow is needed only to author artwork, not to run `main.py`.
- `assets/entry.png`: the selected fixed original image.

Optional regeneration with Pillow installed and a supported local font:

```sh
python tools/check_editorial.py stories.json
python tools/render_revision.py --stories stories.json --variant all --out ../revision-review/rebuilt
```

Rendering uses local Arial or DejaVu fonts; no font program, photograph, logo,
downloaded artwork or competitor image is distributed. Regenerated PNG bytes
can depend on Pillow/font versions. This does not affect the deterministic
runtime, which copies the already committed image.

## License

MIT; see `LICENSE`. The illustrations are original geometric artwork.
