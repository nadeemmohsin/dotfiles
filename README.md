# Usage

This is a dotfiles repo meant for use with GNU Stow. Each top-level folder in this repo is what Stow
considers a _package_. The names don't matter, as long as they don't conflict.

The way I use this is to clone this folder into `$HOME`. From inside `$HOME/dotfiles`, running `stow
package_name` will symlink the contents of the package folder into `$HOME`. This reflects the
internal folder structure. 

As an example, I need to have an `init.el` file in `.emacs.d`. I've got a package named `emacs`
here, and inside it is an `.emacs.d` folder that contains `init.el`. On a new system, I can simply
run `stow` from `$HOME/dotfiles` and this `init.el` will now be symlinked to
`$HOME/.emacs.d/init.el`.
