Vim-Flavored-Markdown
=====================

Add-on to Tim Pope's [`markdown.vim`][mdsyntax] to highlight using Github
Flavored Markdown.

a syntax plugin that extends the Tim Pope's markdown syntax file to recognize
github code blocks like:

    ```yourLanguage
    Some code
    ```

It also colors `markdownCode` blocks and in-lines as String, so they are more
easily differentiable in your code.

Finally, it no longer highlights multiple underscores, i.e.:

```
_this_gets_highlighted_
but_this_does_not
```

Install
-------

### Best way - use Pathogen

If you use Pathogen, you can just clone this into your bundles

```bash
cd ~/.vim/bundle
git clone git://github.com/jtratner/vim-flavored-markdown.git
```

### Otherwise, copy the file to your syntax folder

```bash
wget https://raw.github.com/jtratner/vim-flavored-markdown/master/syntax/ghmarkdown.vim
mv ghmarkdown.vim ~/.vim/syntax/
```

### Use flavored-markdown by default

Add the following `autocmd` to your `.vimrc`:

```viml
augroup markdown
    au!
    au BufNewFile,BufRead *.md,*.markdown setlocal filetype=ghmarkdown
augroup END
```

See it in action
----------------

After installing, open up this readme, and you'll see fenced awesomeness.

License
-------

MIT

Contributors to Vim-Flavored-Markdown
-------------------------------------

Vim-Flavored-Markdown author: Jeff Tratner ([jtratner][jtr])

[markdown.vim][mdsyntax] author: Tim Pope ([tpope][tpope])

Along with all of the various [contributors to markdown.vim][contrib]

[tpope]: https://github.com/tpope
[jtr]: https://github.com/jtratner
[mdsyntax]: https://github.com/tpope/vim-markdown
[contrib]: https://github.com/tpope/vim-markdown/contributors

Thanks to @dankosaur, @knewter, and @Niggler for contributing.


<!--
vim:sw=2 ft=ghmarkdown
-->
