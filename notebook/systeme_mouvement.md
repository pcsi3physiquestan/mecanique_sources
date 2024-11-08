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
# Mouvements particuliers

## Translation

_On rappelle que dans une translation, tous les points du système ont la même vitesse dans un référentiel donné. Cette vitesse correspond donc aussi à la vitesse du centre d'inertie._

````{margin}
Ces expressions ne sont valables que pour un mouvement de translation.
````
````{important} __Eléments cinétiques__

L'énergie cinétique du système S dans un référentiel peut alors s'écrire:

$$
E_{c/R}= \frac{1}{2} M v_{G/R}^2
$$

Le moment cinétique du système S par rapport à un point A dans un référentiel donné s'écrit donc:

$$
\overrightarrow{L_{A/\mathfrak{R}}} = \overrightarrow{AG} \wedge M \overrightarrow{v_{G/\mathfrak{R}}}
$$
````

```{topic} Démonstration
\begin{align*}
E_{c/R} &= \sum\limits_{i=1}^{n} \frac{1}{2} m_i v_i^2\\
&= \sum\limits_{i=1}^{n} \frac{1}{2} m_i v_{G/R}^2\\
&= \frac{1}{2} M v_{G/R}^2
\end{align*}

\begin{align*}
\overrightarrow{L_{A/\mathfrak{R}}} &= \sum\limits_{i} \overrightarrow{AM_i} \wedge m_i \overrightarrow{v_{i/\mathfrak{R}}}\\
&= \left(\sum\limits_{i} m_i \overrightarrow{AM_i}\right) \wedge \overrightarrow{v_{G/\mathfrak{R}}}\\
&= \overrightarrow{AG} \wedge M \overrightarrow{v_{G/\mathfrak{R}}}
\end{align*}
```

## Solide en rotation autour d'un axe fixe

### Moment d'inertie

```{topic} Rappel
_On rappelle que le champ de vitesse d'un solide en rotation autour d'un axe fixe s'exprime:_

$$
\overrightarrow{v_{P/R}} = \overrightarrow{\Omega} \wedge \overrightarrow{AP}
$$
_avec A un point de l'axe de rotation._
```

Nous allons d'abord introduire une grandeur très important pour décrire la rotation d'un solide. Nous verrons par la suite qu'elle intervient dans l'expression de l'énergie cinétique et du moment cinétique.


````{important} __Moment d'inertie__

Lorsqu'un solide S est en rotation autour d'un axe fixe, on définit son moment d'inertie $J_{S/\Delta}$ par rapport à l'axe  par la grandeur:

* Cas discret: $J_{S/\Delta} = \sum\limits_{i=1}^{n} m_i d_i^2$ où $d_i$ est la distance entre le point $P_i$ et l'axe.
* Cas continu: $J_{S/\Delta} = \iiint_{P \in S} \rho(P) {d(P)}^2 d \tau(P)$ où $d(P)$ est la distance entre le point P et l'axe.

````

````{topic} Analyse
On remarquera que cette grandeur dépend à la fois de la masse (inertie) et de la distance à l'axe de rotation. On rappelle que plus la masse est loin de l'axe, plus il est difficile de modifier sa rotation depuis l'axe. On a donc bien une grandeur qui reflètre l'inertie du système.

Il est important de pouvoir analyser qualitativement le moment d'inertie d'un solide en fonction de sa répartition de masse. On observe en effet qu'à masse totale égale, __le moment d'inertie sera d'autant plus grand que la répartition de masse est éloignée de l'axe.__
````

### Grandeurs cinétiques

_L'expression de la quantité de mouvement peut toujours s'obtenir par sommation et/ou en utilisant la position du centre d'inertie. Attention, la quantité de mouvement n'est pas nécessairement nulle (cas d'un centre d'inertie qui n'est pas sur l'axe de rotation)._

````{important} __Moment cinétique sur l'axe de rotation__

Pour un solide S en rotation autour d'un axe fixe  dans R, le moment cinétique $\sigma_{S/\Delta}$ du solide S dans le référentiel R s'exprime comme le produit du moment d'inertie $J_{S/\Delta}$ du même système multiplié par la vitesse de rotation $\omega$ __comptée algébriquement en cohérence avec l'orientation de l'axe__ (règle du tire-bouchon par exemple):

$$
\sigma_{S/\Delta} = J_{S/\Delta} \omega
$$
````

````{admonition} Démonstration
:class: note
>__Démonstration__
>\begin{align*}
\sigma_{S/\Delta} &= \iiint_{P \in S} \rho(P)(\overrightarrow{OP} \wedge \overrightarrow{v(P)})\cdot \overrightarrow{u_{\Delta}} d \tau(P)\\
&= \iiint_{P \in S} \rho(P)(\overrightarrow{OP} \wedge (\overrightarrow{\Omega} \wedge \overrightarrow{OP})) \cdot \overrightarrow{u_{\Delta}} d \tau(P)\\
\end{align*}
En utilisant des coordonnées cylindriques d'axe $\Delta$:
>\begin{align*}
&= \iiint_{P \in S} \rho(P)((r(P) \overrightarrow{e_r} + z(P) \overrightarrow{e_z}) \wedge (r(P) \omega \overrightarrow{e_{\theta}})) \cdot \overrightarrow{e_{z}} d \tau(P)\\
&= \iiint_{P \in S} \rho(P) r^2(P) \omega d \tau(P)\\
&= J_{S/\Delta} \omega
\end{align*}
````

````{important} __Energie cinétique d'un solide en rotation autour d'un axe fixe.__

Dans le cas d'une rotation autour d'un axe fixe $\Delta$, l'énergie cinétique du solide peut s'écrire sous la forme:

$$
E_c = \frac{1}{2} J_{S/\Delta} \omega^2
$$
où $J_{S/\Delta}$ est le moment cinétique de S par rapport à l'axe $\Delta$ et $\omega$ la vitesse angulaire de rotation du solide sur le même axe.
````

````{admonition} Démonstration
:class: note
>__Démonstration__
>\begin{align*}
E_{c/R} &= \sum\limits_{i=1}^{n} \frac{1}{2} m_i v_i^2\\
&= \sum\limits_{i=1}^{n} \frac{1}{2} m_i {(r_i \omega)}^2\\
&= \frac{1}{2} J_{S/\Delta} \omega^2
\end{align*}
````

