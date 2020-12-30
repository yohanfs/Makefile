Filename = plot.py

watch:
	while true; do \
		inotifywait -qre close_write $(Filename); \
		make compile; \
	done 

compile:
	python3 $(Filename)
