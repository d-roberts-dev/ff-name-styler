# FF Name Styler

FF Name Styler is a stylish nickname generator for Free Fire. It restyles plain text into decorative Unicode lettering — small caps, bubble text, symbol frames and more — using styles that have been tested inside the actual game, and it checks every result against Free Fire's 12-character nickname limit before you copy it into the game.

## What it does

- Restyles a name with 10 in-game-tested Unicode styles, including `crown` (꧁Name꧂) and `small_caps` (ɴᴀᴍᴇ).
- Counts characters the way the game does — every symbol counts as one — so a styled nickname never overruns the 12-character limit.
- Works as a Python library and as a command-line tool.
- Has no third-party dependencies: it is pure Python 3.8+.

## Installation

Install FF Name Styler from PyPI:

```bash
pip install ff-name-styler
```

## Basic usage

Style a name in Python:

```python
from ff_name_styler import style, all_styles, fits_game_limit

print(style("Ali", "crown"))       # ꧁Ali꧂
print(style("Ali", "small_caps"))  # ᴀʟɪ

# Check a styled name against the game's 12-character limit:
print(fits_game_limit("꧁Ali꧂"))     # True

# Preview every available style at once:
for style_name, styled in all_styles("Ali").items():
    print(style_name, styled)
```

Or style a name from the command line:

```bash
python -m ff_name_styler Ali
```

## The 12-character rule

Free Fire nicknames must be 3–12 characters long, and decorative symbols count towards that limit just like ordinary letters. FF Name Styler is built around that rule: `fits_game_limit()` reports whether a styled name still fits, so you never waste a rename card on a nickname the game will reject.

## Prefer a web version?

A fuller version runs in any browser as a [Free Fire name styler](https://ffnamegenerator.com/), with 100+ styles, a one-tap symbol crate and guild name ideas.

## Licence

FF Name Styler is released under the MIT Licence. It is an unofficial community tool and is not affiliated with Garena.

