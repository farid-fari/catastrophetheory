# Contenu théorique

# Préalable

## Classification des formes quadratiques

### Généralités

Est appelée forme quadratique toute forme $f:\mathbb{R}^n\to\mathbb{R}$ de type $$f(x_1,...,x_n)=\sum_{1\leq i,j\leq n}\lambda_{ij}x_ix_j$$.

Il existe alors $\Lambda\in \mathcal{M}_n(\mathbb{R})$ telle que $f(X)=X^T\cdot\Lambda\cdot X$, avec $X$ vecteur colonne.

$\Lambda$ peut être écrite sous forme de matrice symétrique, en la remplaçant par $\frac{1}{2}(\Lambda+\Lambda^T)$. Or toute matrice symétrique est diagonalisable avec une matrice orthogonale: $$\exists M \in \mathcal{O}(\mathbb{R}) / \Lambda = M^T\cdot D\cdot M$$

Ceci permet donc d'écrire $f(X) = (M\cdot X)^T\cdot D\cdot (M^{-1}\cdot X)$.

*Preuve*: On se ramène au cas où $\lambda_{11} \neq 0$ soit par échange de lignes si un autre terme diagonal est non nul, soit en posant $y_i=\frac{1}{2}(x_i+x_j)$ et $y_j=\frac{1}{2}(x_i-x_j)$ si $\lambda_{ij}\neq 0$. On factorise ensuite l'expression de $f$ par $\lambda_{11}$, et on constate que si l'on note $\mu_{ij}=\frac{\lambda_{ij}}{\lambda_{11}}$, alors les termes en $x_1$ sont exactement:

$$x_1^2+2\sum_{j=2}^n \mu_{1j}x_1x_j=\big(x_1+\sum_{j=2}^n \mu_{1j}x_j\big)^2-\big(\sum_{j=2}^n \mu_{1j}x_j\big)^2$$

En posant $y_1$ égal au premier terme de cette différence, on a une expression du type $f(y)=\lambda_{11}y_1+$ un reste quadratique en $n-1$ variables. Par récurrence, on obtient bien une matrice diagonale.

Par changement de base, on peut donc écrire $f(X) = X\cdot D\cdot X^T$ avec $D$ diagonale. Par un procédé de normalisation de cette base, on peut considérer $D$ diagonale à coefficients dans $\{-1,0,1\}$. Enfin, en changeant l'ordre des vecteurs de la base on se ramène au cas où f est de la forme:

$$f(x_1,...,x_n)=x_1^2+x_2^2+...+x_k^2-x_{k+1}^2-...-x_s^2$$

Par diagonalisation, on sait d'ailleurs que $s=rg(\Lambda)=rg(f)$. De plus, on nomme $2k-s$ la **signature** de la forme quadratique, qui vaut d'ailleurs $\sum_{ij}\lambda_{ij}$ (*loi d'inertie de Sylvester*).

### Cas de $n=2$

On a alors $f(x,y)=ax^2+2bxy+cy^2$, et $0\leq rg(f)\leq 2$ ainsi que $0\leq r\leq rg(f)$. Comme vu ci-dessus, deux formes quadratiques de rang et signature égaux sont équivalentes à changement de base près. On peut donc catégoriser en $1+2+3=6$ classes les formes quadratiques:

 - $Q_{2,2}$: $x^2+y^2$
 - $Q_{2,0}$: $x^2-y^2$
 - $Q_{2,-2}$: $-x^2-y^2$
 - $Q_{1,1}$: $x^2$
 - $Q_{1,-1}$: $-x^2$
 - $Q_{0,0}$: $0$

## Classification des formes cubiques ($n=2$)

### Noyaux de formes cubiques

Une forme cubique de deux variables est une application $$f: (x,y) \mapsto \alpha x^3+\beta x^2y+\gamma xy^2+\delta y^3$$

Ces applications se mettent en cinq catégories en fonction de $(\alpha,\beta,\gamma,\delta)$ (les catégories $Q_{1,-1}$ et $Q_{1,1}$ ``fusionnent" ici car remplacer $(x,y)$ par $-(x,y)$ change le signe de $f$ -- ceci n'est bien entendu pas une démonstration).
Cherchons une classification à partir du noyau de $f$. Ce noyau est stable par $\cdot$ la loi de composition externe, et peut donc être vu comme un ensemble de droites passant par l'origine dans $\mathbb{R}^2$.

En cherchant l'intersection de ces droites avec $x=1$ (en prenant garde à la droite $x=0$), on cherche à résoudre $\alpha+\beta y+\gamma y^3=0$. Si au moins un coefficient est non nul, cette équation admet au plus 3 solutions réelles (et un nombre pair de racines complexes), donc on distingue cinq catégories de noyaux:

 - $C_{3,0}$: Trois droites distinctes
 - $C_{1,0}$: Une droite unique
 - $C_{3,2}$: Trois droites dont deux coïncidantes (racine double)
 - $C_{3,3}$: Trois droites coïncidantes (racine triple)
 - $C_{\infty,0}$: Le plan en entier (cas où $(\alpha,\beta,\gamma,\delta)=(0,0,0,0)$)

Ceci découle du fait que si la droite $x=0$ est solution, alors $\delta=0$ et on se retrouve avec un polynôme du second degré en $y$, et donc bien au plus trois droites. Ces catégories en sont bien, car aucun changement de base ne fera varier le `nombre de droites du noyau' (à voir en termes de déformation du plan, les droites coïncidantes coïncident toujours et celles distinctes restent distinctes).

### Equivalence des classes

Deux fonctions appartenant à la même catégorie de noyeau ont la même expression à changement de coordonées linéaire près. Une analyse de chaque cas donne:

 - $C_{3,0}$: $f(x,y)=x^2y-y^3$
 - $C_{1,0}$: $f(x,y)=x^2y+y^3$
 - $C_{3,2}$: $f(x,y)=x^2y$
 - $C_{3,3}$: $f(x,y)=x^3$
 - $C_{\infty,0}$: $f=0$

*Preuve*: Un changement de base dans le premier cas permet de déformer le plan de manière à obtenir un carré: les trois droites correspondent aux abscisses, ordonées et l'identité. Alors, $f$ est divisible par $xy(x-y)$, et à changement de base supplémentaire ($(x',y')=\frac{1}{2}((x+y),(x-y))$) on obtient $f(x,y)=x^2y-y^3$.

Dans les autres cas, on considère une des droites, d'expression $lx+my=0$. $f$ peut être factorisée par cette expression, et l'on obtient une des quatres premières catégories de formes quadratiques. De plus, les catégories $Q_{1,1}$ et $Q_{1,-1}$ peuvent être fusionées, car le signe peut être compensé par le changement $(x,y)=-(x,y)$.

Par changement de coordonées, on est donc ramené à l'un des cas: $(Lx+My)(x^2-y^2)$ ou $(Lx+My)x^2$ ou $(Lx+My)(x^2+y^2)$. Le premier de ces cas nous ramène soit aux trois droites, soit au second cas (selon si $(Lx+My)$ est multiple de $(x-y)$ ou $(x+y)$ ou non). Le second cas mène soit à $x^3$ (si $M=0$) ou $xy^2$. Le troisième est $(x^2+y^2)y$ (soit $LM=0$, ou on procède à une *rotation des axes*).

