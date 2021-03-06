# cookiecutter-reveal

Richard Wen  
rrwen.dev@gmail.com  

Personal template for reveal.js presentations with Python cookiecutter.

[![Build Status](https://travis-ci.org/rrwen/cookiecutter-reveal.svg?branch=master)](https://travis-ci.org/rrwen/cookiecutter-reveal)
[![GitHub license](https://img.shields.io/github/license/rrwen/cookiecutter-reveal.svg)](https://github.com/rrwen/cookiecutter-reveal/blob/master/LICENSE)

## Install

1. Install [Python](https://www.python.org/downloads/)
2. Install [cookiecutter](https://pypi.python.org/pypi/cookiecutter) via `pip`

```
pip install cookiecutter
```

## Usage

1. Create a template using [cookiecutter](https://pypi.python.org/pypi/cookiecutter)
2. Change the directory to the folder with the same name as the `template_name` input
3. Install dependencies with [npm](https://www.npmjs.com/)
4. Render HTML slides in the `docs` folder
5. Render PDF slides in the `slides` folder

```
cookiecutter gh:rrwen/cookiecutter-reveal
cd <template_name>
npm install
npm run html
npm run pdf
```

See [Implementation](#implementation) for more details.

## Developer Notes

### Create Github Repository

1. Ensure [git](https://git-scm.com/) is installed
2. Change directory to the generated folder `cd <template_name>`
3. Initialize the repository
4. Add the generated files to commit
5. Create an empty [Github repository](https://help.github.com/articles/create-a-repo/) with the same name as `template_name`
6. Pull any changes if the Github repository is not empty
7. Push the commit from `4.` to your created Github repository

```
git init
git add .
git commit -a -m "Initial commit"
git remote add origin https://github.com/<github_user>/<template_name>.git
git pull origin master --allow-unrelated-histories
git push -u origin master
```

### Implementation

This code creates folders and files for [cookiecutter](https://pypi.python.org/pypi/cookiecutter) templates.

* The main file is [cookiecutter.json](https://github.com/rrwen/cookiecutter-npm/blob/master/cookiecutter.json) which defines the inputs for the command line interface
* The inputs then replace any values surrounded with `{{}}` inside the folder [{{cookiecutter.template_name}}](https://github.com/rrwen/cookiecutter-reveal/tree/master/%7B%7Bcookiecutter.template_name%7D%7D)

```
        cookiecutter              <-- template tool
             |
      cookiecutter.json           <-- template inputs
             |
{{cookiecutter.template_name}}    <-- generated template
```

The following files will be created inside a folder with the same name as the `template_name` input:

File | Description
--- | ---
**docs/edit/logo.png** | Logo image to show on slides
**docs/edit/style.css** | [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) file for styling the slides
**slides/<file_name>.md** | [Markdown](https://daringfireball.net/projects/markdown/) file containing the slide contents
**template.html** | A [reveal-md](https://www.npmjs.com/package/reveal-md) custom template file for generating slides
**.gitignore** | A Node [.gitignore](https://git-scm.com/docs/gitignore) automatically generated from github
**.npmignore** | A file to specify ignoring `docs/*`
**LICENSE** | MIT [license file](https://help.github.com/articles/licensing-a-repository/) automatically created from github
**.travis.yml** | A [.travis.yml](https://docs.travis-ci.com/user/customizing-the-build/) file for automatic builds and tests
**package.json** | The [npm package.json](https://docs.npmjs.com/files/package.json) specifications with [reveal-md](https://www.npmjs.com/package/reveal-md) and [decktape](https://www.npmjs.com/package/decktape) dependencies
**README.md** | a readme [Markdown](https://daringfireball.net/projects/markdown/) file with header section
