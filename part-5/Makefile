PANDOC := pandoc

.PHONY: all
all: index.html one.html two.html

%.html: %.md
	$(PANDOC) -o $@ $<

.PHONY: clean
clean:
	rm -f *.html
