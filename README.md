Vim Plugin for the Papyrus scripting language
=============================================

A file type plugin for Vim that includes (currently rudimentary) syntax
highlighting for the Papyrus scripting language used in TES5: Skyrim.

There is also some quickfix mode support to run the Papyrus compiler and parse
its error messages.

For information on the Papyrus language, visit the Creation Kit website at
http://www.creationkit.com/

Installation
------------

Copy the included directories into your personal `.vim/` or `vimfiles/`
directory. The layout is also compatible with pathogen, vundle and similar
plugin bundle management tools.

To enable quickfix compiler support, you must set the `skyrim_install_path`
variable to the path in which Skyrim is installed, eg (in your `.vimrc`):

    let g:skyrim_install_path='D:\Steam\SteamApps\Common\Skyrim'

If the variable is set, this will configure the `:make` command to compile the
script in the current buffer using default compiler flags. Any output
(including error messages) will be sent to the quickfix list viewable via
`:copen`.

*Note* while Vim will usually accept forward slash as a path separator on
Windows, it is recommended that you use backslash in this variable. The path is
used to set the input, output and flag arguments to the compiler on the command
line and forward slashes may confuse it.

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


Author/Maintainer
-----------------

Sirtaj Singh Kang
