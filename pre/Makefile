SRC = *.tex
OBJ = *.pdf
tmpfiles = *.aux *.log *.toc *.fls *.nav *.out *.snm *.fdb_latexmk *.vrb *.gz

$(OBJ):$(SRC)
	# 需要编译两次才能生成目录
	xelatex $(SRC)
	xelatex $(SRC)
	rm -rf $(tmpfiles)

clean:
	rm -rf $(tmpfiles)

clean-all:
	rm -rf *.pdf
	rm -rf $(tmpfiles)

