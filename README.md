## Purpose

This repository provides the source of the homepage http://theslinux.org/ .
You need to use `Nanoc` from http://nanoc.ws/ to generate the readable
contents.

## Author

This work belongs to `TheSLinux`.

## License

This work is released under the conditions of the license `CC BY-SA`
that can be found originally from
 http://creativecommons.org/licenses/by-sa/3.0/ .
Some page in this work may need a different license; if that's the case
the license will be mentioned explicitly.

## How to contribute

To contribute to this work you need to create a fork of the Github
repository https://github.com/theslinux/homepage , make some changes
and create your pull request. Remember to fetch the latest updates
from the main repository _(see the address provided)_ by using
`git pull [--rebase]` to avoid some potential conflicts.

Before creating new pull request you need to review your changes locally
by using the `view` or `watch` options provided by `Nanoc`.

## The branches

Normally you would work on the `master` branch where all documentations
of the project are stored. If you have any special feature, please fork
and create a `feature branch` from that.

The `core` branch contains the important `Ruby` code, and that branch
should not be updated by non-privileged developers. Because there are
some mergences that causes very bad and messy logs, please consider to
use `cherry-pick` if you want to use any `core` feature on your branch.

Some important files that are on `core` branch

* Hook scripts in `bin/`
* Layout files in `layouts/`
* Stylesheet files in `content/stylesheet.css`
* All ruby files in any directories
* Nanoc configuration files

This list is not complete. It is always safe to use `master` if you
are working on *real* contents of the site. Any changes to font colors,
font size, layouts, bla bla must be on `core` branch.

*Important notes*: Since 2013 July 28th, the two branches are divergent
and you can't merge them. The only way to get `core` feature is to use
`cherry-pick`. However, you should not do that unless you really mean
what you are going to do.

## Requirements

The following `Ruby` gems are required to build source files with `nanoc`
and to view the output with `nanoc view`.

    adsf coderay git kramdown nanoc kramdown \
    fssm coderay nokogiri guard guard-nanoc

Please note that you need `Ruby-1.9` or higher.

## Example. Other notes

The `guard` gem is an useful to watch your source directory; if there is
any change `guard` will invoke `nanoc compile` to build your source.
Please take a look at the example in

    ./bin/example-start-local-nanoc-stuff.sh

This command normally generates so many output from `Guard` and `nanoc`.
You may skip all or most of them by using some known redirections.
