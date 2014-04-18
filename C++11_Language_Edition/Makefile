TEXI2PDF:=texi2pdf
TEXIFLAGS:=--build-dir=build

pres: C++11lang_pres.pdf

hand: C++11lang_hand.pdf

all: hand pres

COMMON:=common_pres.tex c++_stuff.tex cc-zero.pdf

%_hand.pdf: %.tex $(COMMON)
	$(TEXI2PDF) $(TEXIFLAGS) -o $@ -t "\PassOptionsToClass{handout}{beamer}" $<

%_pres.pdf: %.tex $(COMMON)
	$(TEXI2PDF) $(TEXIFLAGS) -o $@ $<
