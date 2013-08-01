Vimotheque
==========

Vimotheque (henceforth, Vtq) is meant to make Vim deployments easy.

A Vim deployment will set up Vim for a particular user on a particular
system. It mostly consists of a generated Vim configuration, and a number of
plugins. The first of these plugins is usually Pathogen, the rest are managed 
by Pathogen.

Vim Configuration
-----------------

Vim is usually configured via the vimrc file. Vtq supports generating the
vimrc file out of reusable fragments (or just one fragment, if you just want to
copy your vimrc over).

Vim can also be configured with files in the .vim/plugin directory. Vtq aims to
support this as well. Note that not everything from the vimrc file can be 
converted to plugin files; Pathogen must still be invoked from vimrc, for
example.

Vimrc generation
~~~~~~~~~~~~~~~~
Vtq can be provided a list of files (snippets). These files will then be copied
over (to .vim/snippets) and concatenated into the vimrc file. The files will be
concatenated in alphabetical order.
