# {{cookiecutter.title}}
  
<small>
{{cookiecutter.author}}  
{{cookiecutter.email}}  
{{cookiecutter.affiliation}}  
</small>
  
<small>
{{cookiecutter.date}}  
</small>
  
<small>
{{cookiecutter.description}}
</small>

---

# Overview

{{'* ' + cookiecutter.sections.replace(',','\n* ')}}
{{'\n---\n\n## ' + cookiecutter.sections.replace(',','\n---\n\n## ')}}
