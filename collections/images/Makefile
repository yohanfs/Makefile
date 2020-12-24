#install imagemagick
SRC:= $(wildcard *.PNG)
OUT:= $(SRC:%.PNG=%.png)

all: $(OUT)

%.png: %.PNG
	convert $< $@
