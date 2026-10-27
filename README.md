# zbrad.github.io

Source for <https://zbrad.github.io/>, built with [Hugo](https://gohugo.io/)
and the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme
(a git submodule under `themes/PaperMod`).

## Local preview

```sh
git submodule update --init
hugo server
```

## Writing a post

Add `content/posts/<slug>.md`. Images go under `static/images/` and are
referenced as `/images/...`.

Posts imported from the old Jekyll site set `url:` in front matter so their
original URLs keep working; new posts don't need it.
