all: fliercard.pdf

fliercard.pdf: fliercard.tex tux-bw.pdf installfest-qr.png
	pdflatex $^

tux-bw.pdf: tux-bw.svg
	inkscape -z -D --file=$^ --export-pdf=$@

installfest-qr.png:
	qrencode -o $@ -t PNG "http://lug.umbc.edu/installfest.html"
