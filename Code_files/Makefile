# This file is for converting .tex file to pdf. 
# - Put this file under the same directory as your target .tex file;
# - Change 'main' to your target file's name; 
# - Using command 'make' to convert target file into pdf version.

I
MAIN=main
SRCS=*.tex

LMK=latexmk
OTYPE=-pdf
TEX=-pdflatex
TEX_OPTS="pdflatex -interaction=nonstopmode -shell-escape"
BIB=-bibtex

ERROR_MSG=Error: cannot find '$(LMK)' in path; try 'pdflatex $(MAIN).tex'

lmk_check =								\
	@which $(LMK) > /dev/null ||		\
		(echo "$(ERROR_MSG)" >& 2 &&	\
			exit 1)

default: $(MAIN).pdf

$(MAIN).pdf: $(MAIN).tex $(SRCS)
	$(call lmk_check)
	@$(LMK) $(OTYPE) $(TEX)=$(TEX_OPTS) $(BIB) $<

.PHONY: watch clean

# Automatically rebuild latex files whenever changes are made.
watch: $(MAIN).tex
	$(call lmk_check)
	@$(LMK) -pvc $(OTYPE) $(TEX)=$(TEX_OPTS) $(BIB) $<

clean:
	@rm -f *.dvi *.aux *.blg *.log *.ps *~ *.bbl $(MAIN).pdf *.out