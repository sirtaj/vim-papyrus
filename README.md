vim-papyrus - Syntax highlighting for the TES5 Papyrus language in Vim
======================================================================

A file type plugin for Vim that includes (currently rudimentary) syntax
highlighting for the Papyrus scripting language in TES5: Skyrim.

There is also some quickfix mode support to run the Papyrus compiler and parse
its error messages.


Installation
------------

To use it, copy the included directories into your `.vim/` or `vimfiles/`
directory. The layout is also compatible with pathogen, vundle and similar
plugin bundle management tools.

To enable quickfix compiler support, you must set the `skyrim_install_path`
variable to the path in which Skyrim is installed, eg:

    let g:skyrim_install_path='d:\Steam\SteamApps\Common\Skyrim'

If the variable is set, this will configure the `:make` command to compile the
script in the current buffer using default compiler flags. Any output
(including error messages) will be sent to the quickfix list viewable with
`:copen`.

You can also set the `makeprg` option manually, the error message support will
still be available.


TODO
----

Tighter grammar rules to help catch syntax errors.


License
-------

All parts of this plugin are under the public domain. I request that you drop
me a note if you redistribute this with modifications, but you are under no
legal obligation to do so.
