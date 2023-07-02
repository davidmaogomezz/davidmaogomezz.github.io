---
layout: post
title:  "Como crear un blog en Jekyll"
date:   2023-07-02 13:02:47 -0500
categories: jekyll update
comments: true
---
Debemos asegurarnos de tener instalado ```Ruby``` en nuestra maquina ya que usaremos ```Jekyll``` el cual usa ruby.

A continuación los pasos para crear nuestro blog

# Paso 1. Instalar Jekyll

```
gem install jekyll bundler
```

# Paso 2. Crear el blog

```
jekyll new blog
```

# Paso 3. Entrar al blog y ejecutar el server

```
cd blog && jekyll serve
```

o pode lanzar el servidor con la bandera ```--livereload```

```
jekyll serve --livereload
```



Lo siguiente que haremos sera inicializar nuestro repositorio de git con

```
git init
```

Crear un repositorio en github de la forma:

```
<username>.github.io
```

Seguir los pasos para enlazar el repositorio local con el remoto y listo, ya se podría visitar la url <username>.github.io en caso [https://davidmaogomezz.github.io/](https://davidmaogomezz.github.io/)

Ahora lo que debemos hacer es inicializar nuestro proyecto con

```
git init
```

y seguir las instrucciones de github para enlazar nuestro proyecto local con nuestro repositorio Github. Para mi caso:

```
echo "# davidmaogomezz.github.io" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:davidmaogomezz/davidmaogomezz.github.io.git
git push -u origin main
```