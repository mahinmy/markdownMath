# Fubini����
## Thm1 �ɻ����ε�Fubini����
��$f(x,y)\in L(R^2)$����

1. $f_y \in L(R)$ for $x \in R$

2. $\int_R fdy \in L(x)$

3. $\int_R dx\int_R fdy=\iint_{R^2}fdxdy$
### Remark
$f$�ɻ����۴λ��ֿɽ�������

## Thm2 �Ǹ��ɲ��Tonelli����
��$f$�Ǹ��ɲ�
1. $f_y \in M(R)$ for $x \in R$

2. $\int_R fdy \in M(x)$

3. $\int_R dx\int_R fdy=\iint_{R^2}fdxdy$

֤��thm2��Ҫ��������
��$F=\{0 \leq f \in M(R^2)\}$������$f$��������1��2��3
#### Lemma

1. $f \in F$,$a \geq 0\Rightarrow af\in F$
2. $f,g \in F \Rightarrow f+g\in F$
3. $f,g \in F, f\geq g, g\in L(R^2)\Rightarrow f-g\in F$
4. $\phi_k\in F, \lim_{k\to \infty} \phi_k=f\Rightarrow f \in F$

1,2��Ȼ��4��Levi�����֤����3
$g\in L(R^2)\Rightarrow g$��$R^2$�ϼ����������ޣ���$f-g+g=f$�����������ޣ�
$\int_R (f-g+g)dy =\int_R (f-g)dy+\int_R gdy\Rightarrow\int_R(f-g)dy=\int_R fdy -\int_R gdy$

### ֤��Thm2
ֻҪ֤��$\forall E \in M,\chi_E \in F$

(i) ��$E=[a,b] \times [c,d]$

$\chi_E(x,y)=\chi_{[a,b]}(x) \chi_{[c,d]}$����Tonelli��1

$\int_R \chi_E(x,y)dy=(d-c)\chi_{[a,b]}(x)$����2��������ֵ���$(d-c)(b-a) \geq 0$������3

(ii) ��$E$����
$$E=\bigcup_{k=1}^{\infty} E_k$$
����$E_k$��$R^2$�Ļ����ཻ�İ뿪�����壬����
$$\chi_E(x,y)=\bigcup_{k=1}^{\infty}\chi_{E_k}(x,y)=\lim_{k\to\infty}\sum_{j=1}^k \chi_{E_j}(x,y) \in F$$

(iii) ��$E$Ϊ�н�ռ������ڿ���$B\supset E$����$E=B\setminus(B\setminus E)$֪$\chi_E=\chi_B -\chi_{B\setminus E}$�������������϶��ǿ�������Lemma��3�Լ�(ii)֪$\chi_E \in F$

(iv)  $E$Ϊ$G_{\delta}$��
$$E=\bigcap_{k=1}^{\infty} E_K$$
����$E_K$������$\chi_{E_k} \in F$��$m(E_1)<+\infty$������
$$E_1\setminus E=\bigcup_{k=1}^{\infty}(E_1\setminus E_k)$$
��$E_1\setminus E_k$���ţ�
$$\chi_{E_1}(x,y) - \chi_{E}(x,y)=\chi_{E_1\setminus E}(x,y)=\lim_{k\to\infty}\chi_{E_1\setminus E_k}(x,y)$$

(v) $m(E)=0$
���Ǵ��ڽ�������$\{G_k\}$������$G_k \supset E$����$\lim_{k\to\infty}m(G_k)=0$����$H=\bigcap_{k=1}^{\infty}G_k$����(ii)��(iv)֪$\chi_H\subset F$�����
$$\int_Rdx\int_R \chi_H(x,y)dy = \int_{R^2}\chi_H(x,y)dxdy=0$$
��$E\subset H$��$m(E)=0$��֪$\int_Rdx\int_R \chi_H(x,y)dy=0=\int_{R^2}\chi_E(x,y)dxdy$
��$\chi_E$����Tonelli��3��ͬʱ��ʽ����$\chi_E(x,y)=0, a.e.x\in R$���Ӷ�֤������Tonelli��1��2

(vi) ��һ��ɲ⼯$E$
����$E=(\bigcup_{k=1}^{\infty}F_k)\bigcup Z$������$F_k$���н�ռ���$m(Z)=0$��$(\bigcup_{k=1}^{\infty}F_k)\bigcap Z=\emptyset$��
��$K=\bigcup_{k=1}^\infty F_k$��������$F_k$���ţ���$\chi_K\in F$���Ӷ�$\chi_E=\chi_K+\chi_Z \in F$