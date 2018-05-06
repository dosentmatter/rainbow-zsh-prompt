# *rainbow-zsh-prompt*

**rainbow-zsh-prompt** makes your zsh prompt rainbow by using [dosentmatter/lolcat](https://github.com/dosentmatter/lolcat).

If you are looking for a rainbow prompt for bash, check out [dosentmatter/rainbow-bash-prompt](https://github.com/dosentmatter/rainbow-bash-prompt)

rainbow-zsh-prompt is a zsh port of [dosentmatter/rainbow-bash-prompt](https://github.com/dosentmatter/rainbow-bash-prompt).

This demo is from rainbow-bash-prompt, but they function pretty much the same.
[![demo](https://asciinema.org/a/b5hasvkj9mgoho5ntodffabn0.png)](https://asciinema.org/a/b5hasvkj9mgoho5ntodffabn0?autoplay=1)

## Installation

*Tested on macOS Sierra (Terminal and iTerm2)*

1. Install C implementation of [dosentmatter/lolcat](https://github.com/dosentmatter/lolcat) for speed.
   - That is a fork of [jaseg/lolcat](https://github.com/jaseg/lolcat) with a minor change to make the colors pseudo random.
   - Put the binary in your `$PATH` and name it `lolcat-c`
2. copy `.zsh_prompt` to your `$HOME` directory
3. Add this to your `.zshrc`:
~~~~
if [[ -f ~/.zsh_prompt ]]; then
  . ~/.zsh_prompt
fi
~~~~

## Use

- You can turn on and off debugging by setting `PS1_DEBUG` to `'true'` or `'false'`. Debugging is used to show the non-printing characters and highlight them.
- You can change the command used to colorize `PS1` by setting `PS1_COLORIZE_COMMAND` to a name of a function.
  - Currently, it is set to `'__ps1_lolcat'` which uses `lolcat-c` for speed.
- You can change the command used to format the debug output by setting `PS1_DEBUG_COMMAND` to a name of a function.
  - Currently, it is set to `__ps1_debug` which displays non-printing characters and colors them.
