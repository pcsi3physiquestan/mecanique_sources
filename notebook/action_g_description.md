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
# Description des actions globales

Comme on l'a dit précédemment, une action globale ou résulante est un regroupement arbitraire mais réfléchi d'actions ponctuelles. Cette définition est opératoire puisque par sommation (ou intégration) des modélisations mathématiques des actions ponctuelles, on peut modéliser les actions résultantes. Néanmoins, nous allons voir qu'en général, on ne passe pas par cette méthode pour modéliser une action résultante.


## Modélisation d'une action globale

_Une action globale est définie comme un ensemble d'actions ponctuelles. On rappelle que si le regroupement est arbitraire, il doit être réfléchi en fonction de la physique._

````{important} __Définition : Force et moment résultant__

Une action résultante peut être décrite __complètement__ au moyen de deux grandeurs:

* la force résultante de l'action, définie comme la somme vectorielle de la force associée à chaque action ponctuelle.
* le moment résultant de l'action exprimé en un point A quelconque, défini comme la somme vectorielle des moment de chaque action ponctuelle et exprimé au même point A. (Attention, les moments sont exprimés au même point A mais les points d'application des actions ponctuelles seront différentes.)

La donnée des deux grandeurs décrivant l'actino et appelé torseur des actions.

Pour un système $\Sigma_1$ exerçant une action globale sur un système $\Sigma$, cette description s'écrit (on pourrait aussi l'écrire avec des intégrales triples): 

\begin{align*}
\overrightarrow{F}(\mathfrak{A}_{\Sigma_{1} \to \Sigma}) = \sum\limits_{M \in \Sigma} \overrightarrow{F}_{\Sigma_{1} \to M}\\
\overrightarrow{M_A}(\mathfrak{A}_{\Sigma_{1} \to \Sigma}) = \sum\limits_{M \in \Sigma} \overrightarrow{AM} \wedge \overrightarrow{F}_{\Sigma_{1} \to M}
\end{align*}
La donnée des DEUX grandeurs est nécessaires pour décrire complètement l'action.

````

````{admonition} Attention : Force et moment
:class: note

A la différence d'une action ponctuelle, le moment résultant d'une action globale __ne peut pas se déduire__ de la force seule a priori. Il faut les deux données.

````

````{dropdown} _Remarque : Points M_

L'ensemble des points M sur lesquels la sommation se fait n'est pas nécessairement l'ensemble des points M su solides. Par exemple, dans le cas d'actions de contact, la sommation se fait uniquement sur la surface de contact.

````


__Description en pratique__
Dans le cadre du programme, il ne sera pas demandé en mécanique de calculer explicitement les sommes discrètes ou intégrales présentées précédemment. En pratique, on sera dans le cas où le moment résultant (et la somme) seront soit données (ou une info équivalente, cf. suite), soit à connaître (cas usuels, cf.suite), soit inconnus. Dans le dernier cas, on a en général des informations par contre sur les contraintes cinématiques imposées (cas des actions de contact (liaisons) où les efforts sont inconnus comme l'expression de la réaction d'un support est inconnue mais on sait qu'ils imposent la nullité d'une composante de vitesse (linéaire ou angulaire), cf. suite).

Pour la suite, certaines démonstrations nécessiteront ces calculs. Ils ne sont pas à savoir refaire et seront donnés en complément.



__Interprétation de la force résultante__
Comme on verra par la suite, la force résultante intervient dans le théorème de la résultante cinétique (loi de la quantité de mouvement) qui est une généralisation du PFD à un système de points. Il permet de prévoir le mouvement du centre d'inertie du système de points (son mouvement de "translation globale"). On peut donc analyser les forces résultantes comme pour un point matériel pour son effet sur la translation globale du système.



__Interprétation du moment résultante__
Chaque moment d'action ponctuelle en un point A donné donnant une information sur la tendance qu'aura l'action ponctuelle à faire tourner le système autour du point A, le moment résultant au même point A va donner la tendance qu'aura l'action résulante à faire tourner le solide autour du point A.


````{dropdown} Remarque

Le système $\Sigma_1$ peut être le système $\Sigma$ lui-même ou une sous partie de ce système agissant sur une autre sous-partie du système. On appelle ces actions, les actions __intérieures__. A l'inverse, les actions exercées par un système extérieur sont appelées __actions...  extérieures__.

````

## Propriétés du moment résultant


__Transfert de moment (HP)__
Cette propriété n'est pas à connaître ni à utiliser. Elle est présentée ici car elle permet d'expliquer certaines modélisations.

Soit deux points A et B, un système $\Sigma$ subissant une action résultante $\mathfrak{A}_{\Sigma_1 \to \Sigma}$ de la part d'un système $\Sigma_1$ dont la force résultante est $\overrightarrow{F}$. Si on connait le moment résultant de l'action au point A $\overrightarrow{M}_A$, alors le moment de la même action au point B se déduit par la relation:

\begin{equation}
\overrightarrow{M}_B = \overrightarrow{M}_A + \overrightarrow{BA} \wedge \overrightarrow{F}
\end{equation}
On insiste sur le fait qu'il faut déjà connaître le moment en un point: on ne déduit pas le moment de l'action à partir de la force résultante seule.



__Interprétation du moment__
Si nous ne calculerons pas le moment par intégration des actions ponctuelles, on peut visualiser qualitativement le moment résultant par analyse graphique. On peux distinguer deux cas utiles: le cas où les moments ponctuels sont nuls et le cas où la répartition de force est uniforme.


## Couple

````{important} __Définition : Couple de forces__

Un couple est une action résultante dont la résultante des forces est nulle (mais pas le moment).

````

````{important} __Fondamental : Moment d'un couple (Admis)__

Le moment d'un couple de force est indépendant du point de calcul.
````


__Effet d'un couple__
Parce que la force résultante est nulle, un couple de force agit sur la rotation du solide et non sur sa translation. Il est très fréquent d'en rencontrer lorsqu'on étudie des solides en rotation.

Ce terme est d'ailleurs quelque fois utilisé de manière abusives (on parle de couple de torsion alors que la force résultante n'est pas nulle).


````{admonition} Exercice 
:class: attention

On considère deux fils tirant en deux points différents d'un solide avec des forces de mêmes intensités mais opposées. L'action des deux fils sur le solide est un couple. Dans cet exemple le moment dépend de la distance entre les deux points applications et de leur orientation relative par rapport à l'orientation des forces. On verra ce principe par la suite.

````

## Moment nul


__Point de moment nul__
Pour des actions dont la résultante des forces est non nulle (pas les couples), il existe des ppints où le moment est nul. Ces points sont très utiles car ils permettent de faire __comme si__ l'action étant une action ponctuelle s'appliquant en l'un de ces points.

En effet, soit une action dont la force résultante est $\overrightarrow{F}$ et dont le moment est nul en un point A. Le transfert de moment permet d'écrit le moment en un point B:

\begin{equation}
\overrightarrow{M}_B = \overrightarrow{BA} \wedge \overrightarrow{F}
\end{equation}
puisque le moment en A est nul. Le moment en B s'exprime __comme si__ toute l'action s'effectuait au point A. Si l'on connaît un tel point, il faut, sur un schéma placer la force résultante en ce point.


````{attention}

Par abus de langage, on peut lire le terme de "point d'application" pour désigner un point où le moment résultant est nul. C'est un abus de langage (à connaître malgré tout) car l'action résultant se répartie sur l'ensemble (ou une partie) du solide, il arrive même qu'aucune action (même ponctuelle) ne soit appliquée au point de moment nul !

````

````{admonition} Exercice Cas de l'action de la pesanteur (à connaître)
:class: attention

L'action de la pesanteur sur un système de points possède un moment nul en un point appelé centre de gravité. Si le champ de pesanteur est uniforme, le centre de gravité est confondu avec le centre d'inertie.

Preuve: On ne traite ici que le cas d'un champ de pesanteur uniforme. On utilise la description continue d'un système de points:

On remarque qu'au centre d'inertie (G = A), le moment résultant sera bien nul.

````


__Utilisation__
Si l'on connaît (cas de la pesanteur) un point de moment nul ou si l'on donne un point de moment nul, alors on peut faire __comme si__ l'action étant ponctuelle appliquée en ce point, ce qui rend le calcul de moment plus simple (pas d'intégrale).

Attention, il ne faut pas poser par avance la position de ce point. En mécanique du solide, beaucoup d'actions ne nécessitent pas l'utilisation d'un tel point (action de contact notamment).



__Infinité des points de moment nul__
S'il existe un point A où le moment résultant est nul, alors en tout point sur la droite passante par A et parallèle à la force résultante, le moment est aussi nul. La démonstration est triviale.

Cela signifie qu'en réalité, le choix du point où placer la force résultante sur un schéma est en partie arbitraire. On va en général privilégier un point qui a un sens physique (centre d'inertie, point appartenant à la surface de contact... ). Mais c'est un choix de convenance et non une nécessité physique.


## Exemples d'analyse de moment

````{admonition} Exercice 
:class: attention

On se propose d'étudier qualitativement le moment résultant de différentes actions.

1. Liaison pivot parfaite: Comme nous le verrons, une liaison pivot est une liaison entre deux solides en contact où le seul mouvement relatif possible est la rotation.
	1. Quelle doit être la forme du contact entre les deux solides ?
	1. Représenter en quelques points, l'allure des forces modélisant les actions ponctuelles. On remarquera qu'on peut distinguer deux composantes pour ces actions ponctuelles. Peut-on avoir une expression a priori du moment résultant ?
	1. On suppose que le contact est sans frottement, représenter en quelques points les forces modélisants les actions ponctuelles. Que peut-on dire du moment sur l'axe de rotation dans ces conditions ?
1. On considère un cube de côté a de masse M. Il est posé sur une table parfaitement horizontal.
	1. On suppose que la masse est uniformément répartie. Si les faces du cube et de la table sont parfaites, comment est le profil des actions ponctuelles sur la surface de contact ? En déduire l'axe où le moment résultant sera nul.
	1. On penche la table sans que le cube se mette à glisser, comment évolue la répartition des forces. En déduire comment va se déplacer l'axe où le moment sera nul (réponse qualitative). Quelle est la limite à cette évolution (on suppose qu'il n'y a pas glissement) ? Que se passe-t-il alors ?
	1. En réalité, on ne procède pas de cette manière pour déterminer une action de contact. On utilise les théorèmes en statique et les autres actions (ici la pesanteur). Nous verrons cela par la suite.
1. On considère le cas d'un cylindre de centre O de rayon R. Deux fils sont attachées en deux point A et B diamétralement opposés du cylindre (dans le plan de O). Réaliser un paramétrage et exprimer le moment résultant. Dans quel cas réalise-t-on un couple ? Quelles sont les configuration où le système est à l'équilibre ?

````

