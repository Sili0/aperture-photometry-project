######
# Makefile
# 
# Style LaTeX pour les rapports des étudiants de la FdS Montpellier
# conçu pour PDFLaTeX
# -- Makefile
# 
# Auteur : Julien Morin <julien.morin@umontpellier.fr>
# Date   : 18/01/2017 
#######

FILE=aaaa-projet_HAP703P_M1CCP_Nom1_Nom2

all: $(FILE).pdf

$(FILE).pdf: $(FILE).tex $(FILE).bib
	pdflatex -interaction=nonstopmode $(FILE); \
	bibtex $(FILE); \
	pdflatex $(FILE); \
	pdflatex $(FILE)

clean:
	-rm -f *~ *.out *.aux *.dvi *.ps *.toc *.lof *.log *.lot *.flg *.bbl *.blg \
	*.idx *.ind *.ilg *.snm *.nav *.fig.bak \
	$(FILE).pdf

# dependencies:
$(FILE).pdf: *.tex
$(FILE).pdf: ./fig/*.*
$(FILE).pdf: ./sty/*
# End of file
