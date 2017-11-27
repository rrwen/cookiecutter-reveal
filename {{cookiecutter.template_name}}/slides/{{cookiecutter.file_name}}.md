# {{cookiecutter.title}}

<small>{{cookiecutter.author}}</small>  
<small>{{cookiecutter.email}}</small>  
<small>{{cookiecutter.affiliation}}</small>  
  
<small>{{cookiecutter.date}}</small>
  
<small>{{cookiecutter.description}}</small>  

---

# Outline

{% for section in cookiecutter.sections.split(',') %}
{{loop.index + '. ' + section + '\n'}}
{% endfor %}
{{'\n---\n\n## ' + cookiecutter.sections.replace(',','\n\n---\n\n## ')}}
