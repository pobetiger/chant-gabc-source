####################
# Makefile for 
# Alleluia in honor of Fr. Simon Le Moyne
# published by Corpus Christi Watershed
# Makefile by Ben Sung Hsu <pobetiger (at) gmail.com>
#######

################
# Configurations:
# * Edit here for other projects
##########
OUT_FILE = ccwatershed-alleluia-fr-simon-le-moyne
PDF_BUILD = lualatex
SRC := $(wildcard *.gabc)
AUTOGEN_TEX := $(patsubst %.gabc,%.autogen-tex,$(SRC))

###################
### Generic stuff
#######
.PHONEY: $(OUT_FILE)
#ccwatershed-alleluia-fr-simon-le-moyne: $(AUTOGEN_TEX)
$(OUT_FILE): $(AUTOGEN_TEX)
	$(PDF_BUILD) $@.tex

# Debug Use:
#print-source: $(SRC)
#	@echo $(SRC)
#	@echo $(AUTOGEN_TEX)
#

# build rules:
%.autogen-tex : %.gabc
	gregorio $< -o $@

# overall stuff:

clean:
	rm -fr *.autogen-tex

really-clean: clean
	rm -fr *.log *.aux *.gaux
	rm -fr *~

purge: really-clean
	rm -fr $(OUT_FILE).pdf


# end of Makefile
