# Readme: mmd.js
A [multimarkdown](https://github.com/fletcher/MultiMarkdown-4) JavaScript lib generated by ["emscripten"](http://kripken.github.io/emscripten-site/index.html). You can use Following to reproduce:
```.sh
cd <checked_out_root_of_multimarkdown-4>
git submodule init
git submodule update
git submodule update --init --recursive
make clean # maybe
make
<absolute_path_to>emcc -O2 beamer.c critic.c GLibFacade.c html.c latex.c \
lyxbeamer.c lyx.c memoir.c multimarkdown.c odf.c opml.c \
parse_utilities.c rng.c rtf.c text.c toc.c transclude.c writer.c parser.c \
-s "EXPORTED_FUNCTIONS=['_mmd_version', '_markdown_to_string']" \
-s OUTLINING_LIMIT=10000 -s TOTAL_MEMORY=268435456 -o mmd.min.js
```

## Example
The example makes use of some ideas of [plaintext.js](https://github.com/dtjm/plaintext.js)

## Copyright
See licences of projects used. Everything else is CC0.
