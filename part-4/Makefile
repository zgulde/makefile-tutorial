PANDOC_FLAGS := --self-contained --section-divs
PANDOC := pandoc $(PANDOC_FLAGS)

%.html: %.md
	$(PANDOC) -o $@ $<
