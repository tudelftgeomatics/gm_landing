# gm_landing

Uses [Jekyll](https://jekyllrb.com/) as a builder: `jekyll serve`

Built with the [Oat](https://oat.ink/) UI library (`css/oat.min.css` + `js/oat.min.js`), themed with TU Delft cyan.

## Building on any machine

Requires Jekyll 4.x (check with `jekyll -v`; the site was built with 4.3.4).
There is no Gemfile — just install Jekyll once:

```sh
gem install jekyll -v 4.3.4     # add `sudo` on Linux system Ruby
jekyll build                    # output in _site/
```

CI (`.github/workflows/jekyll-build.yml`) installs Jekyll 4.3.4 the same way.
