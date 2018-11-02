PAPER = paper
TEX = $(wildcard *.tex )
BIB = references.bib
FIGS = $(wildcard figures/*.pdf figures/*.png)

.PHONY: all clean

$(PAPER).pdf: $(TEX) $(BIB) $(FIGS)
	pdflatex $(PAPER)
	bibtex $(PAPER)
	pdflatex $(PAPER)
	pdflatex $(PAPER)
	rm -f *.aux *.bbl *.blg *.log *.out 

clean:
	rm -f *.aux *.bbl *.blg *.log *.out $(PAPER).pdf

