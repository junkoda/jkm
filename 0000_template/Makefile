.SECONDARY:

LATEX = pdflatex

all:
	make $(addsuffix .pdf, $(basename $(wildcard jk*.tex)))

%.pdf: %.tex
	$(LATEX) $<
	@grep -e 'may have changed' $(basename $<).log && rm $@; $(MAKE) $@ || echo "done."


.PHONY: clean

clean:
	rm -f *.bbl *.blg *.bak *.dvi *.log *.aux
