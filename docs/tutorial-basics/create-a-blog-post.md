---
sidebar_position: 3
---

# Crie um Post no Blog

O Docusaurus cria uma **página para cada post**, além de uma **página índice do blog**, **sistema de tags** e feed **RSS**...

## Crie seu primeiro post

Crie um arquivo em `blog/2021-02-28-greetings.md`:

```md title="blog/2021-02-28-greetings.md"
---
slug: greetings
title: Greetings!
authors:
  - name: Joel Marcey
    title: Co-creator of Docusaurus 1
    url: https://github.com/JoelMarcey
    image_url: https://github.com/JoelMarcey.png
  - name: Sébastien Lorber
    title: Docusaurus maintainer
    url: https://sebastienlorber.com
    image_url: https://github.com/slorber.png
tags: [greetings]
---

Parabéns, você criou seu primeiro post!

Sinta-se à vontade para experimentar e editar este post como quiser.
```

Um novo post do blog estará disponível em [http://localhost:3000/blog/greetings](http://localhost:3000/blog/greetings).
