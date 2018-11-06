MAIN=abs
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
