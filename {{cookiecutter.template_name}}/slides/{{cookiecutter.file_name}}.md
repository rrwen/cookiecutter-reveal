# {{cookiecutter.title}}

<small>{{cookiecutter.author}}</small>  
<small>{{cookiecutter.email}}</small>  
<small>{{cookiecutter.affiliation}}</small>  
  
<small>{{cookiecutter.date}}</small>
  
<small>{{cookiecutter.description}}</small>  

---

# Outline

{{'\n' + '\n'.join([str(i+1) + '. ' + section for i,section in enumerate(cookiecutter.sections.split(','))])}}
{{'\n---\n\n## ' + cookiecutter.sections.replace(',','\n---\n\n## ')}}
