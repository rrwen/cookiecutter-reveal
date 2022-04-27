# {{cookiecutter.directory_name}}

{{cookiecutter.author}}
{{cookiecutter.email}}

* [Slides](https://{{cookiecutter.github_user}}.github.io/{{cookiecutter.directory_name}})
* [PDF](https://github.com/{{cookiecutter.github_short}}/blob/master/slides/{{cookiecutter.file_name}}.pdf)

{{cookiecutter.template_description}}.

[![Build Status](https://travis-ci.org/{{cookiecutter.github_short}}.svg?branch=master)](https://travis-ci.org/{{cookiecutter.github_short}})
[![GitHub license](https://img.shields.io/github/license/{{cookiecutter.github_short}}.svg)](https://github.com/{{cookiecutter.github_short}}/blob/master/LICENSE)
[![Twitter](https://img.shields.io/twitter/url/https/github.com/{{cookiecutter.github_short}}.svg?style=social)](https://twitter.com/intent/tweet?text={{cookiecutter.template_description.replace(' ','%20')}}:%20https%3A%2F%2Fgithub.com%2F{{cookiecutter.github_user}}%2F{{cookiecutter.directory_name}}%20%23revealjs%20%23slides)

## Install

1. Install [npm](https://www.npmjs.com/)
2. [Clone](https://git-scm.com/docs/git-clone) this repository
3. Install dependencies with `npm`

```
git clone {{cookiecutter.github_url}}
cd {{cookiecutter.directory_name}}
npm install
```

See [Edits](#edits) and [Implementation](#implementation) for more details.

## Usage

1. Generate `{{cookiecutter.reveal_static}}/index.html` (see `script.html` in [package.json](https://github.com/{{cookiecutter.github_short}}/blob/master/package.json))
2. Generate `slides/{{cookiecutter.file_name}}.pdf` (see `script.pdf` in [package.json](https://github.com/{{cookiecutter.github_short}}/blob/master/package.json))

```
npm run html
npm run pdf
```

## Developer Notes

### Edits

The following can be edited before generating:

* `slides/{{cookiecutter.file_name}}.md`: [Markdown](https://daringfireball.net/projects/markdown/) file with slide contents
* `slides/template.html`: Custom [reveal-md](https://github.com/webpro/reveal-md) template to generate slides with
* `{{cookiecutter.reveal_static}}/edit/style.css`: [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) file to adjust styling of slides
* `{{cookiecutter.reveal_static}}/edit/logo.png`: logo image to use

### Implementation


The slides [{{cookiecutter.directory_name}}]({{cookiecutter.github_url}}) uses the following [npm](https://www.npmjs.com/) packages for its implementation:

npm | Purpose
--- | ---
[reveal-md](https://www.npmjs.com/package/reveal-md) | Converting `slides/{{cookiecutter.file_name}}.md` to `{{cookiecutter.reveal_static}}/index.html`
[decktape](https://www.npmjs.com/package/decktape) | Converting `slides/{{cookiecutter.file_name}}.md` to `slides/{{cookiecutter.file_name}}.pdf`
[windows-build-tools](https://www.npmjs.com/package/windows-build-tools) | Compiling dependencies for decktape on Windows Operating System (OS)

```
       reveal-md            <-- Convert markdown  slides to html

       decktape             <-- Convert markdown slides to pdf
          |
  windows-build-tools       <-- Compile decktape on Windows OS
```
