chant-gabc-source
=================

Some of my gregorio source code for chant.

ccwatershed-alleluia-fr-simon-le-moyne: added 05/01/2013, compiled a collection based on the generic verse rule, my first gregorio attempt.

Setup:

- install luatex, texlive, texlive-fonts-recommended texlive-fontutils texlive-luatex texlive-music texlive-xetex, and 
  all the extra pckages need to get latex working.
- do a `make clean && make`
- if segfault shows up
-- run `mkluatexfontdb -vvv` and add any segfaulting fonts (full path) to 
  /opt/local/share/texmf-texlive/tex/luatex/luaotfload/luaotfload-blacklist.cnf
-  

