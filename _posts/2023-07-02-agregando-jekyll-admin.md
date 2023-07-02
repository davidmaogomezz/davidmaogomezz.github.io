---
title: Agregando Jekyll Admin
layout: post
date: '2023-07-02 14:00:00 -0500'
categories:
- jekyll
- ruby
- jekyll-admin
comments: true
---

Para tener un admin en nuestro blog de Jekyll debemos agregar a nuestro Gemfile:

```
gem 'jekyll-admin', group: :jekyll_plugins
```

O si ya tenemos nuestro `group: :jekyll_plugins` entonces lo agregamos allí, asi:

```
group :jekyll_plugins do
  gem 'jekyll-admin'
  gem "jekyll-feed", "~> 0.12"
end
```

Ahora instsalamos la gema con

```
bundle install
```

Y ahora vamos a tener disponible nuestro admin en nuestro [localhost:4000/admin](http://localhost:4000/admin) y de esta forma ya tenemos un poderos panel administrativo desde donde podemos gestionar nuestro blog.

![jekyll-admin](/images/jekyll-admin.png)
