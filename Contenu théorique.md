# Contenu théorique

# Préalable

## Classification des formes quadratiques

### Généralités

Est appelée forme quadratique toute forme $f:\mathbb{R}^n\to\mathbb{R}$ de type $$f(x_1,...,x_n)=\sum_{1\leq i,j\leq n}\lambda_{ij}x_ix_j$$

On associe alors à $f$ une matrice diagonale symmétrique $\Lambda$. Or toute matrice symétrique est diagonalisable en une matrice orthogonale: $\exists M \in \mathcal{O}(\mathbb{R}) / \Lambda = M^T\cdot D\cdot M$. Ceci permet donc d'écrire $f(X) = (M\cdot X)^T\cdot D\cdot (M^{-1}\cdot X)$.

*Preuve*: On se ramène au cas où $\lambda_{11} \neq 0$ soit par échange de lignes si un autre terme diagonal est non nul, soit en posant $y_i=\frac{1}{2}(x_i+x_j)$ et $y_j=\frac{1}{2}(x_i-x_j)$ si $\lambda_{ij}\neq 0$. On factorise ensuite l'expression de $f$ par $\lambda_{11}$, et on constate que si l'on note $\mu_{ij}=\frac{\lambda_{ij}}{\lambda_{11}}$, alors les termes en $x_1$ sont exactement:

$$x_1^2+2\sum_{j=2}^n \mu_{1j}x_1x_j=\big(x_1+\sum_{j=2}^n \mu_{1j}x_j\big)^2-\big(\sum_{j=2}^n \mu_{1j}x_j\big)^2$$

En posant $y_1$ égal au premier terme de cette différence, on a une expression du type $f(y)=\lambda_{11}y_1+$ un reste quadratique en $n-1$ variables. Par récurrence, on obtient bien une matrice diagonale.

Par changement de base, on peut donc écrire $f(X) = X\cdot D\cdot X^T$ avec $D$ diagonale. En normalisant, on peut considérer $D$ diagonale à coefficients dans $\{-1,0,1\}$. Enfin, en changeant l'ordre des vecteurs de la base on se ramène au cas où f est de la forme:

$$f(x_1,...,x_n)=x_1^2+x_2^2+...+x_k^2-x_{k+1}^2-...-x_s^2$$

On constate par ailleurs que $s=rg(\Lambda)=rg(f)$ et $sgn(\Lambda)=k-(s-k)=2k-s$.

### Cas de $n=2$

On a alors $f(x,y)=ax^2+2bxy+cy^2$, et $0\leq rg(f)\leq 2$ ainsi que $0\leq k\leq rg(f)$. Comme vu ci-dessus, deux formes quadratiques de rang et signature égaux sont équivalentes à changement de base près. On peut donc catégoriser en $1+2+3=6$ classes les formes quadratiques:

 - $Q_{2,2}$: $x^2+y^2$
 - $Q_{2,0}$: $x^2-y^2$
 - $Q_{2,-2}$: $-x^2-y^2$
 - $Q_{1,1}$: $x^2$
 - $Q_{1,-1}$: $-x^2$
 - $Q_{0,0}$: $0$

## Classification des formes cubiques ($n=2$)

### Noyaux de formes cubiques

Une forme cubique de deux variables est une application $$f: (x,y) \mapsto \alpha x^3+\beta x^2y+\gamma xy^2+\delta y^3$$

Ces applications se divisent en cinq catégories en fonction de $(\alpha,\beta,\gamma,\delta)$. Cherchons une classification à partir du noyau de $f$. Ce noyau est stable par $\cdot$ la loi de composition externe, et peut donc être vu comme un ensemble de droites passant par l'origine dans $\mathbb{R}^2$.

En cherchant l'intersection de ces droites avec $x=1$ (en prenant garde à la droite $x=0$), on cherche à résoudre $\alpha+\beta y+\gamma y^3=0$. Si au moins un coefficient est non nul, cette équation admet au plus 3 solutions réelles (et un nombre pair de racines complexes), donc on distingue cinq catégories de noyaux:

 - $C_{3,0}$: Trois droites distinctes
 - $C_{1,0}$: Une droite unique
 - $C_{3,2}$: Trois droites dont deux coïncidantes (racine double)
 - $C_{3,3}$: Trois droites coïncidantes (racine triple)
 - $C_{\infty,0}$: Le plan en entier (cas où $(\alpha,\beta,\gamma,\delta)=(0,0,0,0)$)

Ceci découle du fait que si la droite $x=0$ est dans le noyau, alors $\delta=0$ et on se retrouve avec un polynôme du second degré en $y$, et donc bien au plus trois droites.

Ces catégories en sont bien, car aucun changement de base ne fera varier le `nombre de droites du noyau' (à voir en termes de déformation du plan, les droites coïncidantes coïncident toujours et celles distinctes restent distinctes).

### Equivalence des classes

Deux fonctions appartenant à la même catégorie de noyau ont la même expression à changement de coordonées linéaire près. Une analyse de chaque cas donne:

 - $C_{3,0}$: $f(x,y)=x^2y-y^3$
 - $C_{1,0}$: $f(x,y)=x^2y+y^3$
 - $C_{3,2}$: $f(x,y)=x^2y$
 - $C_{3,3}$: $f(x,y)=x^3$
 - $C_{\infty,0}$: $f=0$

*Preuve*: Un changement de base dans le premier cas permet de déformer le plan de manière à obtenir un carré: les trois droites correspondent aux abscisses, ordonées et l'identité. Alors, $f$ est divisible par $xy(x-y)$, et à changement de base supplémentaire ($(x',y')=\frac{1}{2}((x+y),(x-y))$) on obtient $f(x,y)=x^2y-y^3$.

Dans les autres cas, on considère une des droites, d'expression $lx+my=0$. $f$ peut être factorisée par cette expression, et l'on obtient une de trois catégories de formes quadratiques: $Q_{1,1}$ et $Q_{1,-1}$ ainsi que $Q_{2,2}$ et $Q_{2,-2}$ peuvent être fusionées, car le signe peut être compensé par le changement $(x,y)=-(x,y)$.

Par changement de coordonées, on est donc ramené à l'un des cas: $(Lx+My)(x^2-y^2)$ ou $(Lx+My)x^2$ ou $(Lx+My)(x^2+y^2)$. Le premier de ces cas nous ramène soit aux trois droites, soit au second cas (selon si $(Lx+My)$ est multiple de $(x-y)$ ou $(x+y)$ ou non). Le second cas mène soit à $x^3$ (si $M=0$) ou $xy^2$. Le troisième est $(x^2+y^2)y$ (soit $LM=0$, ou on procède à une *rotation des axes* $(x',y')=\frac{1}{\sqrt{L^2+M^2}}(Ly-Mx,Lx+My)$).

## Fonctions inverses et implicites

### Développement limités

On introduit la notion de *k-jet*, la fonction polynomiale formée par les $k$ premiers termes du développement de Taylor d'une fonction en un point $y$, noté: $$(j^k_y f)(y+x) = f(y) + xf'(y)+...+\frac{x^n f^{(n)}(y)}{n!}$$

Pour une fonction à $n$ variables, on définit son dévelopmmeent de Taylor et son *k-jet* par: $$(j^k_y f)(y+x) = f(y) + df_y(x)+...+\frac{(df^{(k)}_y)(x)(x)...(x)}{k!}$$

On peut réecrire le terme d'ordre $k$ sous la forme $$\frac{1}{k!}\sum_{i_1,...,i_k} \frac{\partial^k f}{\partial x_{i_1}...x_{i_k}} x_{i_1}...x_{i_k}$$

### Théorème des fonctions inverses

Si $f\in\mathcal{C}^{\infty}(U,\mathbb{R}^m)$, et que $df_x$ est bijective (ou de déterminant non nul), alors f est un **difféomorphisme local** (ou localement bijective).

\bigskip

*Preuve*: On se ramène à un voisinage de 0 où $df_0=Id_E$ (et donc $F=E$) en prenant pour fonction $df_a^{-1}(f(a+x)-f(a))$. Sur $B_r$, on a $\Vert df_x-Id_E \Vert < \frac{1}{2}$. On peut alors écrire $df_x=Id_E-u$ et donc avoir $df_x^{-1}=Id_E+u+u^2+...$ (voir chapitre sur les *suites de fonctions*).

On pose, pour y fixé de $B_{\frac{r}{2}}$, $h:x\mapsto x+y-f(x)$. On a par les acroissements finis sur $B_r, \Vert h(x) - h(x')\Vert\leq\frac{\Vert x-x' \Vert}{2}$, donc h contractante. Elle est de plus à images dans $B_r$ et y admet un unique point fixe: $y$ admet un antécédent unique par $f$ dans $B_r$. Elle est donc bijective $f^{-1}(B_\frac{r}{2}) \cap B_r \to B_{\frac{r}{2}}$.

Quant à la continuité de la réciproque, on pose $h:x\mapsto x-f(x)$. On a $\Vert x-x' \Vert\leq 2\Vert f(x) - f(x')\Vert$ et donc en appliquant à $f^{-1}(y)$ et $f^{-1}(y')$ on obtient g 2-lipschitzienne.

### Théorème des fonctions implicites

Si $f\in\mathcal{C}^{\infty}(\mathbb{R}^n\times\mathbb{R}^m,\mathbb{R}^p)$, et que le noyau de $df_{(x,y)}$ est localement le graphe d'une fonction $y=g(x)$, alors le noyau de $f$ est localement le graphe d'une application $y=h(x)$.

Plus formellement, si l'on note $f_2(y) = f(x_0, y)$, et que $df_{2,y_0}$ est difféomorphisme local (donc $f_2$ est localement inversible), alors on a une application $\phi$ telle que $f(x,\phi(x))=c$ sur un voisinage de $(x_0,y_0)$, et ce pour tout $c$ au voisinage de $f(x_0,y_0)$.

Cela signifie que $c$ admet un unique antécédent par $y\mapsto f(x,y)$ pour $x$ suffisament proche de $x_0$.

\bigskip

On notera que ces deux théorèmes restent valables sous des hypothèses moins fortes de régularité, et que ces hypothèses sont héritées par $\phi$ dans ce cas. De plus, le lien entre ceux-ci est fort: l'un peut se déduire de l'autre.

## Points critiques

Un point critique est dit non dégénéré si $\forall x, rg(d^2f_a(x))=n$ (c'est à dire que $x\mapsto(y\mapsto d^2f_a(x,y))$ est isomorphisme), ou de manière équivalente si le déterminant Hessien de $f$ est non nul.

Par ailleurs, si $f(0)=0$ et $f$ est de infiniment différentiable, alors il existe un voisinage de 0 sur lequel $f$ peut s'écrire: $f(x)=g_1(x)x_1+...+g_n(x)x_n$ avec $g_i(0) = \frac{\partial f}{\partial x_i}(0)$.

### Lemme de Morse

Si $f\in\mathcal{C}^\infty(\mathbb{R}^n,\mathbb{R})$ admet un point critique non dégénéré en $u$, alors il existe un voisinage de $u$ et un $\mathcal{C}^\infty$-difféomorphisme $y=(y_1,...,y_n)$ tel que: $$f=f(u)-y_1^2-...-y_l^2+y_{l+1}^2+...+y_n^2$$

Une application du type $a+y_1^2+...+y_k^2-y_{k+1}^2-...-y_n^2$ est appelée *l-saddle de Morse*. De plus, on note que si $f$ est *0-saddle* alors $u$ est minimum local, et si $f$ est *n-saddle*, alors $u$ est maximum local.

$u$ est alors un point critique isolé (il existe un voisinage sans autre points critiques), et puisque le changement de coordonées conserve l'isolation, on en déduit que tout point critique non dégénéré est isolé. De plus, $l$ est invariant de base.

### Cas de $n=1$

Si $f(0)=f'(0)=...=f^{(k-1)}=0$ et $f^{(k)}(0)\neq 0$ alors, il existe un voisinage de 0 et un changement de coordonées pour lesquels $f(x)=\pm x^k$ (et un $+$ si $k$ est impair).
