Chromium Codesearch Plugin for Vim
==================================

Integrates Chromium CodeSearch into Vim. When combined with additional plugins
(e.g. [vim-fugitive](https://github.com/tpope/vim-fugitive)) should make it
totally unnecessary to leave your editor to visit https://cs.chromium.org.

Examples of what's currently possible:

* Search from within Vim and visit a rendered search results buffer. `<Enter>`
  takes you to the corresponding file in the local working directory.

  ![screencast](resources/searching.gif)

* Look up cross references for the symbol under the cursor. The crossreferences
  are displayed in a new buffer which allows navigation to corresponding files
  in the local working directory.

  ![screencast](resources/xrefs.gif)

* Look up the call graph for a symbol under the cursor. The graph can be
  expanded incrementally and support navigation similar to other rendered
  buffers.

  ![screencast](resources/calls.gif)

* Load all possible call targets for a function call under the curser into the
  quickfix list.

  ![screencast](resources/tour-targets.gif)

* And more!

Caveats
-------

The index at https://cs.chromium.org is updated regularly. The cross reference
information is only accurate to the extent that your working directory matches
what was indexed. If they diverge, you may notice that the jump targets don't
match the snippets displayed, or worse, cross references are incorrect.

Installation
------------

Use your favorite plugin manager. E.g.:

* [Vundle](https://github.com/VundleVim/Vundle.vim):

```viml
call vundle#begin()
" Other plugins
Plugin 'chromium/vim-codesearch'
" More plugins
call vundle#end()
```

* [vim-plug](https://github.com/junegunn/vim-plug)

```viml
call plug#begin()
" Other plugins
Plug 'chromium/vim-codesearch'
" More plugins
call plug#end()
```

Documentation
-------------

Once installed, you should be able to run `:help crcs.txt` to view the help
file. As with all Vim plugins, all documentation should go there.

Contributing
------------

**NOTE**: This is not an official Google product.

See [CONTRIBUTING](./CONTRIBUTING.md).

BUGS
----

File bugs at https://github.com/chromium/vim-codesearch

