---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
These blogs are dedicated for expressing my personal opinions, ideas and thoughts on various technical issues including but not limited to description of technical features. The thoughts and ideas are mine and mine alone. Therefore, they cannot be attributed to my employer or any other person, living or dead.

Here are my blogs posts under different categories:

{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a>
      {{ post.excerpt }}
     </li>
    {% endfor %}
  </ul>
{% endfor %}
