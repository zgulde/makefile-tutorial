PANDOC := pandoc

SRC_DIR := src
OUTPUT_DIR := out

MD_FILES := $(shell find $(SRC_DIR) -name \*.md)
HTML_FILES := $(patsubst $(SRC_DIR)/%.md, $(OUTPUT_DIR)/%.html, $(MD_FILES))

.PHONY: all
all: $(HTML_FILES)

$(OUTPUT_DIR)/%.html: $(SRC_DIR)/%.md
	@mkdir -p $(dir $@)
	$(PANDOC) -o $@ $<

.PHONY: clean
clean:
	rm -fr $(OUTPUT_DIR)
