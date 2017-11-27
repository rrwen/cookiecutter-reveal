# {{cookiecutter.template_name}}

{{cookiecutter.author}}  
{{cookiecutter.email}}  

* [Slides](https://{{cookiecutter.github_user}}.github.io/{{cookiecutter.template_name}})
* [PDF](https://github.com/{{cookiecutter.github_short}}/blob/master/slides/{{cookiecutter.file_name}}.pdf)

{{cookiecutter.template_description}}.

[![Build Status](https://travis-ci.org/{{cookiecutter.github_short}}.svg?branch=master)](https://travis-ci.org/{{cookiecutter.github_short}})
[![GitHub license](https://img.shields.io/github/license/{{cookiecutter.github_short}}.svg)](https://github.com/{{cookiecutter.github_short}}/blob/master/LICENSE)
[![Twitter](https://img.shields.io/twitter/url/https/github.com/{{cookiecutter.github_short}}.svg?style=social)](https://twitter.com/intent/tweet?text={{cookiecutter.template_description.replace(' ','%20')}}:%20https%3A%2F%2Fgithub.com%2F{{cookiecutter.github_user}}%2F{{cookiecutter.template_name}}%20%23revealjs%20%23slides)

## Developer Notes

1. Install [npm](https://www.npmjs.com/)
2. [Clone](https://git-scm.com/docs/git-clone) this repository
3. Generate **{{cookiecutter.reveal_static}}/index.html** (see `script.html`) in [package.json](https://github.com/{{cookiecutter.github_short}}/blob/master/package.json)
4. Generate **slides/{{cookiecutter.file_name}}.pdf** (see `script.pdf`) in [package.json](https://github.com/{{cookiecutter.github_short}}/blob/master/package.json)

```
git clone {{cookiecutter.github_url}}
cd {{cookiecutter.template_name}}
npm install
npm run html
npm run pdf
```

The following can be edited before rendering:

* `slides/{{cookiecutter.file_name}}`: [Markdown](https://daringfireball.net/projects/markdown/) file with slide contents
* `slides/template.html`: [Custom template](https://github.com/webpro/reveal-md#custom-template) for [reveal-md](https://www.npmjs.com/package/reveal-md)
* `{{cookiecutter.reveal_static}}/edit/style.css`: file to adjust styling of slides
* `{{cookiecutter.reveal_static}}/edit/logo.png`: logo image to use
* `reveal.json`: [Reveal.js options](https://github.com/webpro/reveal-md#revealjs-options)
