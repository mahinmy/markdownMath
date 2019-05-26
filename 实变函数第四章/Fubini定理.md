# Fubini定理
## Thm1 可积情形的Fubini定理
设$f(x,y)\in L(R^2)$，则

1. $f_y \in L(R)$ for $x \in R$

2. $\int_R fdy \in L(x)$

3. $\int_R dx\int_R fdy=\iint_{R^2}fdxdy$
### Remark
$f$可积则累次积分可交换次序

## Thm2 非负可测的Tonelli定理
设$f$非负可测
1. $f_y \in M(R)$ for $x \in R$

2. $\int_R fdy \in M(x)$

3. $\int_R dx\int_R fdy=\iint_{R^2}fdxdy$

证明thm2需要以下引理
令$F=\{0 \leq f \in M(R^2)\}$，这里$f$满足上述1，2，3
#### Lemma

1. $f \in F$,$a \geq 0\Rightarrow af\in F$
2. $f,g \in F \Rightarrow f+g\in F$
3. $f,g \in F, f\geq g, g\in L(R^2)\Rightarrow f-g\in F$
4. $\phi_k\in F, \lim_{k\to \infty} \phi_k=f\Rightarrow f \in F$

1,2显然，4用Levi定理可证，看3
$g\in L(R^2)\Rightarrow g$在$R^2$上几乎处处有限，则$f-g+g=f$几乎处处有限，
$\int_R (f-g+g)dy =\int_R (f-g)dy+\int_R gdy\Rightarrow\int_R(f-g)dy=\int_R fdy -\int_R gdy$

### 证明Thm2
只要证明$\forall E \in M,\chi_E \in F$

(i) 若$E=[a,b] \times [c,d]$

$\chi_E(x,y)=\chi_{[a,b]}(x) \chi_{[c,d]}$满足Tonelli的1

$\int_R \chi_E(x,y)dy=(d-c)\chi_{[a,b]}(x)$满足2，这个积分等于$(d-c)(b-a) \geq 0$，满足3

(ii) 若$E$开集
$$E=\bigcup_{k=1}^{\infty} E_k$$
这里$E_k$是$R^2$的互不相交的半开立方体，则有
$$\chi_E(x,y)=\bigcup_{k=1}^{\infty}\chi_{E_k}(x,y)=\lim_{k\to\infty}\sum_{j=1}^k \chi_{E_j}(x,y) \in F$$

(iii) 若$E$为有界闭集，存在开球$B\supset E$，由$E=B\setminus(B\setminus E)$知$\chi_E=\chi_B -\chi_{B\setminus E}$，而这两个集合都是开集，由Lemma的3以及(ii)知$\chi_E \in F$

(iv)  $E$为$G_{\delta}$型
$$E=\bigcap_{k=1}^{\infty} E_K$$
这里$E_K$渐缩，$\chi_{E_k} \in F$，$m(E_1)<+\infty$，则有
$$E_1\setminus E=\bigcup_{k=1}^{\infty}(E_1\setminus E_k)$$
而$E_1\setminus E_k$渐张，
$$\chi_{E_1}(x,y) - \chi_{E}(x,y)=\chi_{E_1\setminus E}(x,y)=\lim_{k\to\infty}\chi_{E_1\setminus E_k}(x,y)$$

(v) $m(E)=0$
这是存在渐缩开集$\{G_k\}$，满足$G_k \supset E$，且$\lim_{k\to\infty}m(G_k)=0$。令$H=\bigcap_{k=1}^{\infty}G_k$，由(ii)和(iv)知$\chi_H\subset F$，因此
$$\int_Rdx\int_R \chi_H(x,y)dy = \int_{R^2}\chi_H(x,y)dxdy=0$$
由$E\subset H$，$m(E)=0$，知$\int_Rdx\int_R \chi_H(x,y)dy=0=\int_{R^2}\chi_E(x,y)dxdy$
即$\chi_E$满足Tonelli的3，同时上式表明$\chi_E(x,y)=0, a.e.x\in R$，从而证明满足Tonelli的1和2

(vi) 对一般可测集$E$
由于$E=(\bigcup_{k=1}^{\infty}F_k)\bigcup Z$，其中$F_k$是有界闭集，$m(Z)=0$，$(\bigcup_{k=1}^{\infty}F_k)\bigcap Z=\emptyset$。
令$K=\bigcup_{k=1}^\infty F_k$，不妨设$F_k$渐张，则$\chi_K\in F$，从而$\chi_E=\chi_K+\chi_Z \in F$