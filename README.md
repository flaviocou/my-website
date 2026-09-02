# my-website

A multipage [Quarto](https://quarto.org) website — a fan tribute to Roger Federer.

## Pages

| File | Page |
|------|------|
| `index.qmd` | Home — overview and headline stats |
| `career.qmd` | Career timeline, rankings, playing style |
| `grand-slams.qmd` | All 20 Grand Slam titles and signature matches |
| `rivalries.qmd` | Nadal, Djokovic, Murray, and earlier rivals |
| `legacy.qmd` | Sportsmanship, philanthropy, business, retirement |

Configuration lives in `_quarto.yml`; custom styling in `styles.css`.

## Build

```sh
quarto preview   # live-reloading local preview
quarto render    # build static site into _site/
```

Statistics reflect Federer's career through his 2022 retirement and are drawn
from public records such as the ATP Tour and Wikipedia.
