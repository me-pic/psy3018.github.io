---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Introduction
```{image} site_logo.png
---
width: 200px
align: center
---
```
Ce livre, "Méthodes en neurosciences cognitives", présente les principales techniques de neuroimagerie utilisées pour étudier la cognition chez l'humain (et l'animal) et disposant d'une bonne résolution spatiale:
 * résonance magnétique (anatomique, fonctionnelle, et de diffusion),
 * tomographie par émission de positrons,
 * imagerie optique.

Ce livre est une entrée en matière et est destiné à des lecteurs qui découvrent ces méthodes pour la première fois. Ce livre vous fournira des connaissances théoriques sur les bases physiques et physiologiques de ces techniques de neuroimagerie. De plus, il propose une introduction aux principales techniques de traitement d’image et d’analyse statistique qui leur sont associées. Chaque chapitre comporte une série d'exercices qui incluent des exemples d'applications dans le cadre de projets de recherche en neurosciences cognitives.

```{warning}
Le but de ce livre est d'introduire l'ensemble des techniques les plus conventionnelles en neuroscience cognitive de manière concise, pour que les lecteurs puissent en apprécier les forces et faiblesses, ainsi que comprendre comment choisir la technique la plus adaptée à un type de recherche spécifique. Il ne s'agit pas d'un ouvrage spécialisé dans une technique qui comprend l'ensemble des notions nécessaires pour utiliser cette technique de manière autonome.
```

## Contribuer
Ce projet est développé de manière collaborative. Toute suggestion est la bienvenue! Vous pouvez utiliser la page "[issue](https://github.com/methodes-cogneuro/methodes-cogneuro.github.io/issues)" de Github pour faire une demande à l'équipe, ou décrire un problème. Vous pouvez également proposer directement un changement en effectuant une "pull request" sur la page Github du livre.

## Remerciements
Ce livre est dans une large mesure "reproductible": de nombreuses figures sont générées à l'aide de données ouvertes, avec du code accessible à même le livre. Cette technologie est rendue possible grâce aux projets suivants:
 * [jupyter book](https://jupyterbook.org) est l'outil utilisé pour générer le livre.
 * La librairie [nilearn](https://nilearn.github.io/) en [python](https://www.python.org/), notamment pour la partie sur l'IRM structurelle, l'IRM fonctionnelle et les modèles statistiques.
 * La librairie [Dipy](https://dipy.org), notamment pour la partie sur l'IRM de diffusion.
 * La librairie [MNE python](https://mne.tools/stable/index.html) est utilisée dans le chapitre portant sur l'imagerie optique.
 * Les visualisations d'images cérébrales utilisées dans le cours proviennent en partie de jeux de données publiques. L'origine des données est précisée dans la description de chacune des figures.
 * Certaines images du livre ont été obtenues sous droits illimités pour diffusion web et limités pour impression (500k copies) via [shutterstock](https://www.shutterstock.com) par L. Bellec.
 * Le logo du livre est tiré du site <a href="https://www.vecteezy.com/free-vector/brain">Brain Vectors by Vecteezy</a>


 Les auteurs sont très reconnaissants pour l'énorme travail et la générosité des communautés qui créent et maintiennent tous ces projets!


 ## Contributeurs

 Le développement de ce livre a démarré afin de servir d'outil de référence pour le cours PSY3018, donné au baccalauréat en neurosciences cognitives de l'Université de Montréal. Les contributions générales sont présentées ci-dessous. Des contributions spécifiques sont listées au sein de chaque chapitre.

 🤔 Contenu | 💻 Code | 🧩 Quizz | 👀 révision du texte
 ::::{grid}
 :::{grid-item}
 ![Lune Bellec](https://avatars.githubusercontent.com/u/1670887?v=4?s=100)
 [Lune bellec](https://github.com/lunebellec) 🤔💻🧩👀
 :::

 :::{grid-item}
 ![Julien Cohen-Adad](https://avatars.githubusercontent.com/u/2482071?v=4?s=100)
 [Julien Cohen-Adad](https://github.com/jcohenadad)
 👀
 :::

 :::{grid-item}
 ![Eddy Fortier](https://avatars.githubusercontent.com/u/72314243?v=4?s=100)
 [Eddy Fortier](https://github.com/e-fortier)
 🤔👀
 :::

 :::{grid-item}
 ![Dan J Gale](https://avatars.githubusercontent.com/u/14634382?v=4?s=100)
 [Dan J Gale](https://github.com/danjgale)
 🎨
 :::

 :::{grid-item}
 ![Samuel Guay](https://avatars.githubusercontent.com/u/30598330?v=4?s=100)
 [Samuel Guay](https://github.com/SamGuay)
 👀
 :::

 :::{grid-item}
 [Aline Moussard]()
 👀
 :::

 :::{grid-item}
 ![Xanthy Lajoie](https://avatars.githubusercontent.com/u/90349544?v=4?s=100)
 [Xanthy Lajoie](https://github.com/Xanthylajoie)
 🤔👀
 :::

 :::{grid-item}
 ![Élisabeth Loranger](https://avatars.githubusercontent.com/u/90270981?v=4?s=100)
 [Élisabeth Loranger](https://github.com/elisabethloranger)
 🤔
 :::

 :::{grid-item}
 ![François Lespinasse](https://avatars.githubusercontent.com/u/38385719?v=4?s=100)
 [François Lespinasse](https://github.com/sangfrois)
 🤔👀
 :::

 :::{grid-item}
 ![Marie-Eve Picard](https://avatars.githubusercontent.com/u/77584086?v=4?s=100)
 [Marie-Eve Picard](https://github.com/me-pic)
 🤔👀
 :::

 :::{grid-item}
 ![Andréanne Proulx](https://avatars.githubusercontent.com/u/65092948?v=4?s=100)
 [Andréanne Proulx](https://github.com/anproulx)
 🤔👀
 :::

 :::{grid-item}
 ![Dylan Sutterlin Guindon](https://avatars.githubusercontent.com/u/70554831?v=4?s=100)
 [Dylan Sutterlin Guindon](https://github.com/dylansutterlin)
 👀
 :::

 ::::
