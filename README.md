## Overview

This is a slightly modified version of the [Textpattern CMS default theme](https://github.com/textpattern/textpattern-default-theme). It aims to be visually identical to the original but replace all remote assets with locally-available versions.

## Modifications

This modified theme is more suited for offline or firewalled servers, and also where [Content Security Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) directives restrict access to remote servers.

The associated font files ([PT Serif](https://en.wikipedia.org/wiki/PT_Fonts), weights 400 & 700 in `EOT`, `SVG`, `TTF`, `WOFF` and `WOFF2` formats) are included in the theme download. Textpattern page and form scaffolds have been updated to serve fonts from the Textpattern site and are _not_ served from [Google Fonts](https://fonts.google.com):

```
<!-- Localised font stylesheet (replaces Google font API below) -->
<link rel="stylesheet" href="<txp:page_url type="theme_path" />/styles/fonts.css">

<!-- Original Google font API -->
<!-- <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=PT+Serif:400,400i,700,700i&amp;subset=latin-ext"> -->
```

## Font loading preference

If the font is installed on the user's device, it will be used in preference to the font file included in the theme and the user's browser will not download a font file.

If the font is _not_ installed on the user's device, it will be served from the Textpattern site in the most appropriate format for the user's browser.

## Legal

PT Serif is included with an SIL Open Font License.
