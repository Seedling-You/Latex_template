.PHONY: examples

CC = xelatex

OUTPUT_DIR = out
MID_DIR = midfiles
CV_DIR = cv
RESUME_DIR = resume
COVERLETTER_DIR = coverletter

CV_SRCS = $(shell find $(CV_DIR) -name '*.tex')
RESUME_SRCS = $(shell find $(RESUME_DIR) -name '*.tex')
COVERLETTER_SRCS = $(shell find $(COVERLETTER_DIR) -name '*.tex')

examples: $(foreach x, coverletter cv resume, $x.pdf)

cv.pdf: cv.tex $(CV_SRCS)
	$(CC) -output-directory=$(OUTPUT_DIR)/$(MID_DIR) $<
	mv $(OUTPUT_DIR)/$(MID_DIR)/*.pdf $(OUTPUT_DIR)

resume.pdf: resume.tex $(RESUME_SRCS)
	$(CC) -output-directory=$(OUTPUT_DIR)/$(MID_DIR) $<
	mv $(OUTPUT_DIR)/$(MID_DIR)/*.pdf $(OUTPUT_DIR)

coverletter.pdf: coverletter.tex $(COVERLETTER_SRCS)
	$(CC) -output-directory=$(OUTPUT_DIR)/$(MID_DIR) $<
	mv $(OUTPUT_DIR)/$(MID_DIR)/*.pdf $(OUTPUT_DIR)

clean:
	rm -rf $(OUTPUT_DIR)/*/*

clean-all: clean
	rm -rf $(OUTPUT_DIR)/*.pdf
