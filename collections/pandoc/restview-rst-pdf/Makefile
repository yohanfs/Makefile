watch:
	while true; do \
                inotifywait -qre close_write README.rst; \
                make pdf; \
        done


html:
	restview README.rst
	
pdf:
	pandoc --pdf-engine=pdflatex \
        --variable geometry:"top=3cm, bottom=3cm, left=3cm, right=3cm" \
        --variable geometry:a4paper \
        -o 14-impedancemodel.pdf README.rst
