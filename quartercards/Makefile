all: fliercard.pdf

fliercard.pdf: fliercard.tex tux-bw.pdf
	pdflatex $^

tux-bw.pdf: tux-bw.svg
	inkscape -z -D --file=$^ --export-pdf=$@
