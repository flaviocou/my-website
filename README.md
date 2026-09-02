# my-website

A single-page [Quarto](https://quarto.org) website — a fan tribute to Roger Federer.

## Structure

All content lives in `index.qmd`, organised into four top-level sections:

| Section | Contents |
|---------|----------|
| Career | Timeline, career totals, weeks at No. 1, ATP titles since 2018, playing style |
| Grand Slam titles | The record, all 20 major titles, signature matches, Olympic and team results |
| Rivalries | Nadal, Djokovic, Murray, and earlier rivals |
| Legacy | Sportsmanship, philanthropy, business, retirement, honours |

Configuration lives in `_quarto.yml`; custom styling in `styles.css`. The navbar
links jump to the sections within the single page.

## Build

```sh
quarto preview   # live-reloading local preview
quarto render    # build static site into _site/
```

Statistics reflect Federer's career through his 2022 retirement and are drawn
from public records such as the ATP Tour and Wikipedia.
