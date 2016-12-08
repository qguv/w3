# w3: the wee weechat wrapper

## usage

run `w3` as you would run `weechat`. put it somewhere that's in your `$PATH`
if you want to run it unqualified. it takes all the options weechat does,
except `-d` (use `$XDG_CONFIG_HOME` instead).

## why

weechat vomits configuration defaults all over your config dir. this has
several disadvantages:

  - harder to keep files in version control
  - impossible to tell what options you've set
  - harder to find relevant settings
  - users don't inherit changes in default settings
  - there are defaults all over your config dir

it difficult to keep your preferences in vc. w3 scans for any configuration
options that have changed since the last time weechat was started and saves
them AND ONLY THEM. note that this also has several disadvantages:

  - comments are ripped off without remorse
  - injects -d and -r into weechat command
  - harder to find similar settings (since not all settings are written)
  - config files are re-parsed (spacing is different, for example)
  - bugs?

---

copyright (c) Quint Guvernator, distributed as free software under the GPL3.
see LICENSE file for details.
