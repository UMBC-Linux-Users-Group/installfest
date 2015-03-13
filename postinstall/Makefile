all: postinstall.pdf

.PHONY: all git-describe

postinstall.pdf: postinstall.tex tux-bw.pdf site-qr.png git-describe.tex
	pdflatex $^

tux-bw.pdf: ../logos/tux-bw.svg
	inkscape -z -D --file=$^ --export-pdf=$@

# Add a QR code linking to the site.
site-qr.png:
	qrencode -o $@ -t PNG "http://lug.umbc.edu"

git-describe.tex:
	git describe --always --dirty=+ > git-describe.tex
