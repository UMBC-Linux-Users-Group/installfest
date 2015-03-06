all: fliercard.pdf

fliercard.pdf: fliercard.tex tux-bw.pdf archlinux-logo.pdf ubuntu-logo.pdf \
	linuxmint-logo.pdf fedora-logo.pdf installfest-qr.png
	pdflatex $^

tux-bw.pdf: tux-bw.svg
	inkscape -z -D --file=$^ --export-pdf=$@

archlinux-logo.pdf: ../logos/archlinux-bw.svg
	inkscape -z -D --file=$^ --export-pdf=$@
ubuntu-logo.pdf:  ../logos/ubuntu-bw.svg
	inkscape -z -D --file=$^ --export-pdf=$@
linuxmint-logo.pdf: ../logos/linuxmint-bw.svg
	inkscape -z -D --file=$^ --export-pdf=$@
fedora-logo.pdf: ../logos/fedora-bw.svg
	inkscape -z -D --file=$^ --export-pdf=$@

installfest-qr.png:
	qrencode -o $@ -t PNG "http://lug.umbc.edu/installfest.html"
