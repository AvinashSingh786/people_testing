BUILD_PRINT = \e[1;32m Completed $<\e[0m
def:
	pdflatex *.tex
	rm -f *.toc
	rm -f *.out
	rm -f *.aux
	rm -f *.log
	evince *.pdf &
	clear
	@echo -e "$(BUILD_PRINT)\n"

push:
	read -p "Enter commit message:" msg; 
	git commit *.tex -m echo $$msg
	git push origin master
