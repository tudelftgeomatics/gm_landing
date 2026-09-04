# gm_landing

Uses [Jekyll](https://jekyllrb.com/) as a builder: `bundle exec jekyll serve`

## Building on any machine

Requires Ruby >= 3.0 (check with `ruby -v`). Then:

```sh
bundle install           # installs the exact versions from Gemfile.lock
bundle exec jekyll build # output in _site/
```

Always run Jekyll through `bundle exec` so the locked version is used, regardless
of what Jekyll version (if any) is installed system-wide. If `bundle install`
complains about the Bundler version, run `gem install bundler:2.5.4` first.

On Linux machines using the **system Ruby** (e.g. Debian/Ubuntu's `ruby3.x`
package), gems cannot be installed into `/var/lib/gems` without root. The
committed `.bundle/config` already avoids this by installing gems into
`vendor/bundle/` inside the project — no `sudo` needed, and it works the same
under rbenv/RVM. Do **not** run `sudo bundle install`.

Built with the [Oat](https://oat.ink/) UI library (`css/oat.min.css` + `js/oat.min.js`), themed with TU Delft cyan.
