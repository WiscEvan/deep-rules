# Output directory containing the formatted manuscript

The [`gh-pages`](https://github.com/Benjamin-Lee/deep-rules/tree/gh-pages) branch hosts the contents of this directory at https://Benjamin-Lee.github.io/deep-rules/.
The permalink for this webpage version is https://Benjamin-Lee.github.io/deep-rules/v/91e04e1953098e22ec5de17f9db20423dd4f749b/.
To redirect to the permalink for the latest manuscript version at anytime, use the link https://Benjamin-Lee.github.io/deep-rules/v/freeze/.

## Files

This directory contains the following files, which are mostly ignored on the `master` branch:

+ [`index.html`](index.html) is an HTML manuscript.
+ [`github-pandoc.css`](github-pandoc.css) sets the display style for `index.html`.
+ [`manuscript.pdf`](manuscript.pdf) is a PDF manuscript.

The `v` directory contains directories for each manuscript version.
In general, a version is identified by the commit hash of the source content that created it.

### Timestamps

The `*.ots` files in version directories are OpenTimestamps which can be used to verify manuscript existence at or before a given time.
[OpenTimestamps](https://opentimestamps.org/) uses the Bitcoin blockchain to attest to file hash existence.
The `deploy.sh` script run during continuous deployment creates the `.ots` files.
However, these files are initially dependent on calendar services and must be upgraded at a later time by running the following in the `gh-pages` branch:

```sh
# Requires a local bitcoin node with JSON-RPC configured
ots upgrade v/*/*.ots
rm v/*/*.ots.bak
git add v/*/*.ots
```

## Source

The manuscripts in this directory were built from
[`91e04e1953098e22ec5de17f9db20423dd4f749b`](https://github.com/Benjamin-Lee/deep-rules/commit/91e04e1953098e22ec5de17f9db20423dd4f749b).
