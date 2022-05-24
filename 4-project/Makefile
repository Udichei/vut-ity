PROJ=proj4
PACK=xsyano00-fit
INCLUDE=czechiso.bst

.PHONY: clean pack pdflatex

$(PROJ).pdf: $(PROJ).ps
	ps2pdf -sPAPERSIZE=a4 $^

$(PROJ).ps: $(PROJ).dvi
	dvips $^

$(PROJ).dvi: $(PROJ).tex
	latex $^
	latex $^
	latex $^


pdflatex: $(PROJ).tex
	pdflatex $^
	pdflatex $^
	pdflatex $^

pack: $(PACK).tar.gz

$(PACK).tar.gz: $(PROJ).tex $(PROJ).bib $(INCLUDE)
	tar -czf $@ $^ Makefile

clean:
	rm -f $(PROJ).aux $(PROJ).dvi $(PROJ).log $(PROJ).ps $(PROJ).synctex.gz $(PROJ).fls $(PROJ).fdb_latexmk $(PROJ).bbl $(PROJ).blg 
