($[A]_i$ - $i$-ая строка матрицы $A$)

### Упражнение 4.

Для матричных норм $\|A\|_{1}$, $\|A\|_{\infty}$, подчинённых соответствующим векторным нормам $\|x\|_{1}$, $\|x\|_{\infty}$, вывести формулы 

$\|A\|_{1}=\max _{j} \sum_{i}\left|a_{i j}\right|, \quad\|A\|_{\infty}=\max _{i} \sum_{j}\left|a_{i j}\right|​$

#### Решение

$A \in Mat(n\times m, \mathbb C)$ 

1. $\|\cdot\|_{1}$

   $\|A\|_{1} = \underset{\|x\|_{1}\ne 0}{\sup}\dfrac{\|Ax\|_{1}}{\|x\|_{1}} = \underset{\|x\|_{1}=1}{\sup}\|Ax\|_{1} = \underset{\|x\|_{1}=1}{\sup}\sum\limits_{i=1}^n|[Ax]_i| = \underset{\|x\|_{1}=1}{\sup}\sum\limits_{i=1}^n\sum\limits_{j=1}^m|a_{ij}x_{j}| \le \underset{\|x\|_{1}=1}{\sup}\sum\limits_{i=1}^n\sum\limits_{j=1}^m|a_{ij}||x_{j}| = ​$

   $  \underset{\|x\|_{1}=1}{\sup}\sum\limits_{j=1}^m|x_{j}|(\sum\limits_{i=1}^n|a_{ij}|) \le  \underset{\|x\|_{1}=1}{\sup}(\underset{1\le j \le m}{\max}\sum\limits_{i=1}^n|a_{ij}|)\|x\|_{1} = \underset{1\le j \le m}{\max}\sum\limits_{i=1}^n|a_{ij}|​$

   

   Пусть $j^*  = \underset{1\le j\le m}{\arg\max}\sum\limits_{i=1}^n|a_{ij}|$ . Тогда при выборе $x:$  $x_{j^*}=1, ~~x_{k}=0,~k\ne j^*$   $\|x\|_{1}=1$   , и получаем

   $\|Ax\|_{1} =\sum\limits_{i=1}^n\sum\limits_{j=1}^m|a_{ij}x_{j}| = \sum\limits_{i=1}^n|a_{ij^*}|\cdot 1 = \underset{1\le j \le m}{\max}\sum\limits_{i=1}^n|a_{ij}|$ 

   Следовательно $\|A\|_{1} \le \underset{1\le j \le m}{\max}\sum\limits_{i=1}^n|a_{ij}|$ и $\exists~ x:~~\|x\|_{1}=1 , ~~\|Ax\|_{1} =\underset{1\le j \le m}{\max}\sum\limits_{i=1}^n|a_{ij}| $.

   Следовательно $\|A\|_{1} = \underset{1\le j \le m}{\max}\sum\limits_{i=1}^n|a_{ij}|$.

2. $\|\cdot\|_{\infty}​$

   $\|A\|_{\infty} = \underset{\|x\|_{\infty}=1}{\sup}\underset{1\le i \le n}{\max}|[Ax]_i|=\underset{\|x\|_{\infty}=1}{\sup}\underset{1\le i \le n}{\max}|\sum\limits_{j=1}^m a_{ij}x_j|\le  \underset{\|x\|_{\infty}=1}{\sup}\underset{1\le i \le n}{\max}\sum\limits_{j=1}^m |a_{ij}||x_j|\le \underset{1\le i \le n}{\max}\sum\limits_{j=1}^m |a_{ij}|$

   Пусть $i^* = \underset{1\le i \le n}{\arg\max}\sum\limits_{j=1}^m |a_{ij}|​$ 

   Пусть $x_{j} =\mathbb{sign}(a_{i^*j}) ~~~\forall j: ~~1 \le j \le m​$, тогда $\|x\|_{\infty}=1​$ , и получаем

   $\|Ax\|_{\infty} = \underset{1\le i \le n}{\max}|\sum\limits_{j=1}^m a_{ij}x_j|  = \underset{1\le i \le n}{\max}\sum\limits_{j=1}^m a_{ij}\mathbb{sign}(a_{i^*j}) = \underset{1\le i \le n}{\max}\sum\limits_{j=1}^m |a_{ij}|$

   То есть верхняя оценка достигается. $\quad\|A\|_{\infty}=\max _{i} \sum_{j}\left|a_{i j}\right|$

### Упражнение 5

Для матричной норм $\|A\|_2$, подчинённой соответствующей векторной норме $\|x\|_2$ $(x\in \mathbb R^n, A \in \mathbb {Mat} (n, \mathbb R)$, 

$\max _{i, j}\left|a_{i j}\right| \leqslant\|A\|_{2} \leqslant n \max _{i, j}\left|a_{i j}\right|​$

$\|A\|_{2} = \underset{\|x\|_{2}\ne 0}{\sup}\dfrac{\|Ax\|_{1}}{\|x\|_{2}} = \underset{\|x\|_{2}= 1}{\sup}\sqrt{\sum\limits_{i=1}^n|[Ax]_i|^2}=  \underset{\|x\|_{2}= 1}{\sup}\sqrt{\sum\limits_{i=1}^n|\sum\limits_{j=1}^n a_{ij}x_j|^2}​$

Пусть $i^*, j^* = \underset{i, j}{\arg\max}|a_{ij}|$ и $x: ~~x_{j^*}=1,~x_k=0,~~k\ne j^*$. Тогда $\|x\|_2 = 1$ и 

$\|Ax\|_2 = \sqrt{\sum\limits_{i=1}^n|a_{ij^*}|^2}​$

Заметим, во-первых, что $\sqrt{\sum\limits_{i=1}^n|a_{ij^*}|^2} \ge \sqrt{|a_{i^*j^*}|^2} = |a_{i^*j^*}| = \underset{i,j}{\max}|a_{ij}|​$

Следовательно $\|A\|_2 \ge \|Ax\|_2 \ge \underset{i,j}{\max}|a_{ij}|$.



С другой стороны, используя неравенство Коши-Буняковского, 

$\|A\|_2 =  \underset{\|x\|_{2}= 1}{\sup}\sqrt{\sum\limits_{i=1}^n|\sum\limits_{j=1}^n a_{ij}x_j|^2} =  \underset{\|x\|_{2}= 1}{\sup}\sqrt{\sum\limits_{i=1}^n\langle [A]_i,x\rangle^2} \le  \underset{\|x\|_{2}= 1}{\sup}\sqrt{\sum\limits_{i=1}^n\|[A]_i\|^2\|x\|_2^2} = \sqrt{\sum\limits_{i=1}^n\|[A]_i\|^2} = \sqrt{\sum\limits_{i=1}^n\sum\limits_{j=1}^n|a_{ij}|^2}$

$\le n \underset{i,j}{\max}|a_{ij}|$











