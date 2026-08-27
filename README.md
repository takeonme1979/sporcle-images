# sporcle-images

Image hosting for my [Sporcle](https://www.sporcle.com/user/Quiztopia/quizzes/) quizzes,
migrated off imgur/imgbox after both geo-blocked the UK.

## Serving

Use **jsDelivr**, not `raw.githubusercontent.com` — GitHub raw is rate-limited and
not intended as a CDN.

```
https://cdn.jsdelivr.net/gh/takeonme1979/sporcle-images@main/<path>
```

## Layout

Mirrors the source tree, slugified to lowercase-hyphenated:

```
music/top-20-slideshow/<YYYY-MM-DD>/01.jpg .. 20.jpg
```

Slide numbers match both the filename and the chart position burned into each image.

## Manifests

`manifests/*.csv` in the tooling repo map every source file on disk to its repo key
and both URL forms. If a host ever fails again, that mapping makes the next migration
a re-run rather than an investigation.
