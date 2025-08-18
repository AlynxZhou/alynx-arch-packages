noto-fonts-cjk-alynx
====================

Noto Sans/Serif CJK fonts have larger vertical metrics in 'hhea' table, because it contains some tall glphys (<https://github.com/notofonts/noto-cjk/issues/144#issuecomment-478968910>). This makes it hard to align those fonts with other fonts when apps handle line height. They already have correct vertical metrics in 'OS/2' table, but because `USE_TYPO_METRICS` bit is not set in `fsSelection`, harfbuzz won't use those correct metrics (<https://github.com/harfbuzz/harfbuzz/blob/main/src/hb-ot-metrics.cc#L82>).

This package patches fonts to set `USE_TYPO_METRICS` of `fsSelection`. To make it easier to patch, I choose the `.otf` files instead of `.ttc` files.
