
docs/index.html: slides/{{cookiecutter.file_name}}.md
	npm run html

slides/{{cookiecutter.file_name}}.pdf: slides/{{cookiecutter.file_name}}.md
	npm run pdf

install:
	npm install

html: docs/index.html	

pdf: slides/{{cookiecutter.file_name}}.pdf
	
watch:
	npm run watch