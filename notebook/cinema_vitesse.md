---
jupytext:
  encoding: '# -*- coding: utf-8 -*-'
  formats: ipynb,md:myst
  split_at_heading: true
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.10.3
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---
# Vecteur vitesse

## Vecteur vitesse: Définition

````{margin}
Il est important de préciser le référentiel d'étude: il définit les vecteurs qu'on considère fixe. Dans un premier temps, il n'y aura qu'un seul référentiel.
````
````{important} __Vecteur vitesse__

Soit O un point fixe du référentiel R et M un point mobile. La vitesse du point M dans le référentiel R est définit comme la dérivée temporelle du vecteur position dans le référentiel R.

$$
\overrightarrow{V_{M/R}} = {(\frac{d \overrightarrow{OM}}{dt})}_{R}
$$
````


## Expression du vecteur vitesse

````{important} __Expressions du vecteur vitesse__

Le vecteur vitesse s'exprime.

En coordonnées cartésiennes:

$$
\overrightarrow{v_{M/\mathfrak{R}}} = \dot x \overrightarrow{e_x} + \dot y \overrightarrow{e_y} + \dot z \overrightarrow{e_z}
$$

En coordonnées cyindriques:

$$
\overrightarrow{v_{M/\mathfrak{R}}} = \dot r \overrightarrow{e_r} +r \dot \theta \overrightarrow{e_\theta} + \dot z \overrightarrow{e_z}
$$

En coordonnées spheriques:

$$
\overrightarrow{v_{M/\mathfrak{R}}} = \dot r \overrightarrow{e_r} + r \dot \theta \overrightarrow{e_\theta} + r \sin{\theta} \dot \varphi \overrightarrow{e_\varphi}
$$
````

````{topic} Démonstration
> On peut démontrer ces expressions de deux manières: soit en dérivant le vecteur position (il faut tenir compte des dérivées des vecteurs des bases locales, nous le verrons en traitant le cas du vecteur accélération) ou en utilisant l'expression du vecteur déplacement élémentaire. Nous présentons ce dernier cas. On rappelle que le déplacement élémentaire s'exprime (respectivement en coordonnées cartésiennes, cylindriques, sphériques):
> 
> \begin{equation}
\overrightarrow{dOM} = dx \overrightarrow{e_x} + dy \overrightarrow{e_y} + dz \overrightarrow{e_z}
\end{equation}
> \begin{equation}
\overrightarrow{dOM} = dr \overrightarrow{e_r} + r d \theta \overrightarrow{e_{\theta}} + dz \overrightarrow{e_z}
\end{equation}
> \begin{equation}
\overrightarrow{dOM} = dr \overrightarrow{e_r} + r d \theta \overrightarrow{e_{\theta}} + r \sin \theta d\varphi \overrightarrow{e_{\varphi}}
\end{equation}
> Ici, on rapport le déplacement élémentaire à la variation temporelle dt pendant lequel le déplacement se fait, ce qui revient à rapporter chaque différentielle ($dx, dy, d\theta, dr...$) par dt, c'est-à-dire les remplacer par les dérivées. On obtient bien les expressions données.
````
