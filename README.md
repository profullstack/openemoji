# OpenEmoji

Every standard emoji, 3,963 of them in Emoji 18.0, drawn by an image model as one family and packed as an [OpenEmoji](https://logicsrc.com/openemoji) set.

**Browse it:** [logicsrc.com/openemoji/catalog](https://logicsrc.com/openemoji/catalog). Search by name or keyword, filter by group, skin tone and Emoji version, then copy an emoji or download its files.

## What is here

```
openemoji.json          the OpenEmoji descriptor: coverage, licence, provenance, every emoji and its files
openemoji.css           @font-face for the fonts, plus an img.openemoji rule
png/<size>/<key>.png    16, 20, 32, 48, 64, 72, 96, 128, 136, 160, 256 and 512 px
webp/<size>/<key>.webp  64 and 128 px, for the web
svg/<key>.svg           a posterised vector trace of each glyph
font/OpenEmoji-CBDT.ttf colour font for Chrome, Android and Linux
font/OpenEmoji-sbix.ttf colour font for Safari, macOS and iOS
style.txt               the art direction every glyph was drawn under
prompts.jsonl           the prompt behind each glyph
```

`<key>` is the fully-qualified codepoint sequence, lowercase and hyphen-joined: `1f600` is 😀, `2764-fe0f` is ❤️ and `1f469-1f3fe-200d-1f4bb` is 👩🏾‍💻.

## Use it

As images, with the character as `alt` so copy, paste and screen readers keep the emoji:

```html
<img class="openemoji" src="png/64/1f602.png" alt="😂" title="face with tears of joy">
```

As a font, with the platform's emoji as the fallback:

```html
<link rel="stylesheet" href="openemoji.css">
<p class="openemoji">Shipped it 🚀🔥</p>
```

## How it was made

Every glyph was drawn by `gpt-image-2` under the art direction in `style.txt`, by [`emoji`](https://github.com/profullstack/cli-tools#emoji) in profullstack/cli-tools. Six anchors were drawn first (😀 🔥 ❤️ 👍 🚀 🐱), and every later glyph was an edit that saw them, so the whole set shares one light and one gloss. Every skin-tone variant is an edit of its base that changes the skin and nothing else. The descriptor records this as `made_by: ai` and `disclosure: ai-generated`, in the W3C AI Content Disclosure vocabulary.

The PNGs and the fonts are the artwork as drawn. The SVGs are traced from the PNGs, which turns the smooth gradients into flat colour steps.

## Licence

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Credit "OpenEmoji by Profullstack, Inc."
