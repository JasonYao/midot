# midot
By [Jason Yao](https://github.com/JasonYao)

## Description
`midot` is a dotfiles interface built to
make dotfiles easier to build, maintain,
and upgrade via global commands.

By complying with the `midot` interface,
you gain for free simple, yet powerful,
global commands to control your dotfiles
from anywhere.

To jump-start this process, you can take
a look at a basic `midot`-compliant dotfile
[here](https://github.com/JasonYao/midot-base.git),
or simply run `midot generate` and follow the
given instructions.

## Setup
For now:
```sh
mkdir -p ~/.bin
git clone https://github.com/JasonYao/midot.git ~/.bin/midot
echo "PATH=$PATH:$HOME/.bin" >> ~/.bashrc
midot GITHUB_SSH_URL
# e.g.
midot git@github.com:JasonYao/dotfiles.git
```

In the future with homebrew*:
```sh
brew install midot
midot GITHUB_SSH_URL
# e.g.
midot git@github.com:JasonYao/dotfiles.git
```

\* Note: We first target the `homebrew`
package manager for `v1.0`, and then
expand to general *nix afterwards.

## Commands
Update dotfiles
```sh
midot update
```

Upgrade dotfiles
```sh
midot upgrade
```

Show midot commands
```sh
midot help
```

Installs the dotfiles
```sh
midot GITHUB_SSH_URL
# e.g.
midot git@github.com:JasonYao/dotfiles.git
```

Uninstalls & cleans up the dotfiles
```sh
midot uninstall
```

Generate base midot-compliant dotfiles (defaults to ~/.dotfiles)
```sh
midot generate
```

Checks for midot-compliance
```sh
midot check
```

Shows the current version
```sh
midot version
```

## Dependencies
git:
```sh
brew install git
```

## How to build `midot`-compliant dotfiles
Building `midot`-compliant dotfiles is a relatively
simple matter. You can use the built in `generate`
command to download a basic `midot`-compliant set of dotfiles, 
or manually do the following:
- Have a `bin` folder inside of your dotfiles
	- If you want to have scripts run pre/post commands, place them here. e.g. `bin/pre-update`
	- Have an `upgrade` script. This should be your "start" script, able to be run consecutively.
	- Have an `uninstall` script. This should cleanly remove all traces of your dotfiles

## License
This repo is licensed under the terms of the MIT license,
a copy of which may be found [here](LICENSE)
