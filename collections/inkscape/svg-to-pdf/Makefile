#change-log
#25-12-2020

SRC:= $(wildcard *.svg)
OUT_pdf:= $(SRC:%.svg=%.pdf)

all: $(OUT_pdf)

%.pdf: %.svg
	inkscape --file=$< --export-pdf=$@ 

