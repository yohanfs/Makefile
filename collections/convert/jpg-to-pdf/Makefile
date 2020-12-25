#install imagemagick
SRC:= $(wildcard *.jpg)
OUT:= $(SRC:%.jpg=%.pdf)

all: $(OUT)

%.pdf: %.jpg
	convert $< $@
