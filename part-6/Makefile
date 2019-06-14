
PANDOC := pandoc
MD_FILES := $(shell find . -name \*.md)
HTML_FILES := $(patsubst %.md, %.html, $(MD_FILES))

.PHONY: all
all: $(HTML_FILES)

%.html: %.md
	$(PANDOC) -o $@ $<

.PHONY: clean
clean:
	rm -f *.html
