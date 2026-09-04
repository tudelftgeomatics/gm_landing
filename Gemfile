source "https://rubygems.org"

# Jekyll 4.3.4+ requires Ruby >= 2.7, but the gems below (csv, logger) need >= 3.0.
# Declaring it here gives a clear error instead of a cryptic "requires ruby >= 3.0"
# when building on old system Rubies (e.g. Ubuntu 20.04's Ruby 2.7).
ruby ">= 3.0"

# Allow any Jekyll 4.x so machines with slightly different installs still build.
# The Gemfile.lock pins the exact version for reproducible builds; run
# `bundle update jekyll` if you want to move that pin deliberately.
gem "jekyll", ">= 4.3.4", "< 5"

# Removed from Ruby's default gems in Ruby 3.4, so Jekyll needs them explicitly
# on newer Rubies. Installing them on older Rubies is harmless.
gem "csv"
gem "base64"
gem "logger"

# Windows and JRuby do not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1", :platforms => [:mingw, :x64_mingw, :mswin]

# Lock `http_parser.rb` gem to `v0.6.x` on JRuby builds since newer versions of the gem
# do not have a Java counterpart.
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]
