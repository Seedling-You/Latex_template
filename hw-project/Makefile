SRC = *.tex
OBJ = *.pdf
tmpfiles = *.aux *.log *.toc *.fls *.nav *.out *.snm *.fdb_latexmk *.vrb *.gz

$(OBJ):$(SRC)
	xelatex $(SRC)

clean:
	rm -rf $(tmpfiles)

