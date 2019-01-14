all: slides codelab readme


slides:
	cd slides && (make all && cp haskell_102.pdf notes.html .. ; cd ..)

codelab:
	cd codelab && (make clean ; cd ..)
	zip -r codelab.zip codelab/

readme:
	kramdown --template document README.md > README.html


install: slides codelab readme
	cp haskell_102.pdf /google/data/rw/users/ni/nicuveo/www/Haskell102/haskell_102.pdf
	cp codelab.zip     /google/data/rw/users/ni/nicuveo/www/Haskell102/codelab.zip
	cp README.html     /google/data/rw/users/ni/nicuveo/www/Haskell102/README.html
	cp notes.html      /google/data/rw/users/ni/nicuveo/www/Haskell102/notes.html


clean:
	cd slides && (make distclean ; cd ..)
	cd codelab && (make clean ; cd ..)

distclean: clean
	rm -f haskell_102.pdf
	rm -f codelab.zip
	rm -f README.html
	rm -f notes.html


.PHONY: slides codelab readme install clean distclean
