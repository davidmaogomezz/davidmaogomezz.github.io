---
layout: post
title:  "Como agregar disqus a Jekyll"
date:   2023-07-02 13:48:47 -0500
categories: ruby jekyll disqus
comments: true
---
# Nota:
## es necesario tener el sitio online para poder seguir estos pasos.


Tres simples pasos para agregar Disqus a nuestro blog:

El primero es registrarse en [Disqus](https://disqus.com/)

El segundo es en nuestro proyecto:

Debemos crear una carpeta llamada ```_layouts``` dentro de esta carpeta creamos un archivo llamado ```post.html```
en este archivo agregamos el siguiente código:

{% raw %}
```html
---
layout: default
---

<small>{{ page.date | date: "%-d %B %Y" }}</small>
<h1>{{ page.title }}</h1>

{{content}}

{% if page.tags %}
  <small>tags: <em>{{ page.tags | join: "</em> - <em>" }}</em></small>
{% endif %}

{% if page.comments %}
<div id="disqus_thread"></div>
<script>
    (function() {
    var d = document, s = d.createElement('script');
    s.src = 'https://https-davidmaogomezz-github-io.disqus.com/embed.js';
    s.setAttribute('data-timestamp', +new Date());
    (d.head || d.body).appendChild(s);
    })();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
{% endif %}
```
{% endraw %}

En ```YOUR_URL``` va la url de nuestro sitio pero separada por punts. En mi caso [https://davidmaogomezz-github-io/](https://davidmaogomezz.github.io/)

Y por último agregar el setting ```comments: true``` en el post que quieras que aparezca la sesión de comentarios.