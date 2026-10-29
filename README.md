# tmux config

My tmux configuration, exported from a machine running tmux 3.4.
Based on [Oh my tmux!](https://github.com/gpakosz/.tmux), with a custom dark
color palette, mouse scrolling, vi copy mode, OSC 52 clipboard support over SSH,
and 100,000 lines of history.

## Install

Install tmux 3.4 or newer, Git, Perl, sed, and awk using your machine's usual tools.
Back up any existing `~/.tmux`, `~/.tmux.conf`, and `~/.tmux.conf.local` first.
Then run:

```sh
git clone https://github.com/grammy117/tmux-conf.git "$HOME/.tmux"
ln -s "$HOME/.tmux/.tmux.conf" "$HOME/.tmux.conf"
cp -i "$HOME/.tmux/.tmux.conf.local" "$HOME/.tmux.conf.local"
tmux
```

For an existing tmux server, reload with:

```sh
tmux source-file "$HOME/.tmux.conf"
```

Edit `~/.tmux.conf.local` for personal changes. The main `.tmux.conf` contains
the upstream configuration and its embedded helper scripts; keep both files.
OSC 52 copying requires support from your local terminal.

## Useful keys

Both `Ctrl-b` and `Ctrl-a` work as the prefix.

| Keys | Action |
| --- | --- |
| Prefix, `r` | Reload configuration |
| Prefix, `-` | Split top/bottom |
| Prefix, `_` | Split left/right |
| Prefix, `h` / `j` / `k` / `l` | Move between panes |
| Prefix, `Enter` | Enter copy mode |
| `v`, then `y` in copy mode | Select and copy |
| Prefix, `m` | Toggle mouse mode |

## Upstream

The base configuration was exported from gpakosz/.tmux commit
`58a3dcc0d718ec0fa1c0d5a2fddd640a1ad7a5b7`.
The upstream configuration is dual licensed under the MIT license and WTFPL v2;
both license files are included.
