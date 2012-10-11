FILENAME=thesis
SOURCES=./$(FILENAME).tex
BIN=./$(FILENAME).pdf
TEMP_FILES= thesis.bbl thesis.blg thesis.brf  thesis.idx thesis.log thesis.aux  thesis.lof  thesis.out thesis.toc
CC=pdflatex -shell-escape
CC_BIB=bibtex

all: tesi
	
tesi: 
	$(CC) $(SOURCES) \
	&& $(CC_BIB) $(FILENAME) \
	&& $(CC) $(SOURCES) \
	&& $(CC) $(SOURCES) \
	&& rm $(TEMP_FILES) \
	&& evince $(BIN)

view:
	evince $(BIN)

clean:
	rm $(TEMP_FILES) 2>&1;

debug:
	$(CC) $(SOURCES)

