TEXI2PDF:=texi2pdf
TEXIFLAGS:=--build-dir=build

pres: smart_pres.pdf

hand: smart_hand.pdf

all: hand pres

COMMON:=common_pres.tex c++_stuff.tex cc-zero.pdf

%_img.pdf: %.dot
	neato -n -Tpdf $< > $@
	./pdfcrop.pl $@ $@

SMART_DEPS:=smart.tex $(COMMON) pointer_img.pdf

smart_hand.pdf: $(SMART_DEPS)
	$(TEXI2PDF) $(TEXIFLAGS) -o $@ -t "\PassOptionsToClass{handout}{beamer}" $<

smart_pres.pdf: $(SMART_DEPS)
	$(TEXI2PDF) $(TEXIFLAGS) -o $@ $<
