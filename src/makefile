OUTPUTDIR = ../out
FILENAME = retroKsiazka

html: $(FILENAME).html
pdf: $(FILENAME).pdf

all: html pdf

%.html : %.md
	mkdir -p $(OUTPUTDIR)
	pandoc --standalone --smart --from markdown --to html5 --toc -o $(OUTPUTDIR)/$@ $^

%.pdf : %.md
	mkdir -p $(OUTPUTDIR)
	pandoc --standalone --smart --from markdown --to latex --toc -o $(OUTPUTDIR)/$@ $^

clean:
	rm -f $(OUTPUTDIR)/*.pdf
	rm -f $(OUTPUTDIR)/*.html
