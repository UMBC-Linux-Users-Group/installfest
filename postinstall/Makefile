all: postinstall.pdf

postinstall.pdf: postinstall.tex tux-bw.pdf
	pdflatex $^

tux-bw.pdf: ../logos/tux-bw.svg
	inkscape -z -D --file=$^ --export-pdf=$@
