<a id = "matrix"></a>  

# 矩阵总结
---
### 单位矩阵

在矩阵的乘法中，有一种矩阵起着特殊的作用，如同数的乘法中的1，这种矩阵被称为 **单位矩阵** 。它是个方阵，从左上角到右下角的对角线（称为主对角线）上的元素均为1。除此以外全都为0。   

根据 **单位矩阵** 的特点，任何矩阵与 **单位矩阵** 相乘都等于本身，而且 **单位矩阵** 因此独特性在高等数学中也有广泛应用。  

$$
\begin{bmatrix}
1 & 0\\ 
0 & 1
\end{bmatrix}   
\begin{bmatrix}
1 & 0 & 0\\ 
0 & 1 & 0\\ 
0 & 0 & 1
\end{bmatrix}   
\begin{bmatrix}   
1 & 0 & 0 & 0\\ 
0 & 1 & 0 & 0\\ 
0 & 0 & 1 & 0\\
0 & 0 & 0 & 1
\end{bmatrix}   
$$
---
### 方阵

方块矩阵，也称 **方阵**、方矩阵或正方矩阵，是行数及列数皆相同的矩阵。n×n阶矩阵被称为n阶 **方阵** 

---
### 逆矩阵

**逆矩阵** （inverse matrix），又称反矩阵。在线性代数中，给定一个n阶方阵$\mathbf{A}$，若存在一个n阶方阵 $\mathbf{B}$ ，使得$\mathbf{AB}=\mathbf{BA}=\mathbf{I}_n$，其中$\mathbf{I}_n$为n阶单位矩阵，则称$\mathbf{A}$是可逆的，且$\mathbf{B}$是$\mathbf{A}$的 **逆矩阵** ，记作$\mathbf{A} ^{-1}$。

只有方阵（n×n 的矩阵）才可能有 **逆矩阵** 。若方阵$\mathbf{A}$的 **逆矩阵** 存在，则称$\mathbf{A}$为非奇异方阵或可逆方阵。

与行列式类似，**逆矩阵** 一般用于求解联立方程组。

#### ***性质*** 

1. $\left (A^{-1}\right )^{-1}=A$  
2. $(\lambda A)^{-1}=\frac{1}{\lambda}\times A^{-1}$  
3. $(AB)^{-1}=B^{-1}A^{-1}$  
4. $\left (A^\mathrm{T} \right )^{-1}=\left (A^{-1} \right )^{\mathrm{T}}（A^{\mathrm{T}}为A的转置）$  
5. $\det(A^{-1})=\frac{1}{\det(A)}（det为行列式）$  


---
### 内积（点积）

点积（Dot Product）又称数量积或标量积（Scalar Product），是一种接受两个等长的数字序列（通常是坐标向量）、返回单个数字的代数运算。在欧几里得几何中，两个笛卡尔坐标向量的点积常称为 **内积**   

从代数角度看，先对两个数字序列中的每组对应元素求积，再对所有积求和，结果即为点积。从几何角度看，点积则是两个向量的长度与它们夹角余弦的积。这两种定义在笛卡尔坐标系中等价。  

点积的名称源自表示点乘运算的点号（${\displaystyle a\cdot b}$），读作{$\displaystyle a\ dot\ b$}，标量积的叫法则是在强调其运算结果为标量而非向量。向量的另一种乘法是叉乘（${\displaystyle a\times b}$），其结果为向量，称为叉积或向量积。

点积是 **内积** 的一种特殊形式。  

#### ***代数定义***  

两个向量${\displaystyle {\vec {a}}=[a_{1},a_{2},\cdots ,a_{n}]}$和${\displaystyle {\vec {b}}=[b_{1},b_{2},\cdots ,b_{n}]}$的点积定义为：  

$\vec{a}\cdot \vec{b}=\sum\limits_{i=1}^{n} a_ib_i = a_1b_1 + a_2b_2 + \cdots + a_nb_n$
这里的Σ是求和符号，而n是向量空间的维数。

例如，两个三维向量${\displaystyle \left[1,3,-5\right]}和{\displaystyle \left[4,-2,-1\right]}$的点积是

${\displaystyle {\begin{aligned}\ [1,3,-5]\cdot [4,-2,-1]&=(1)(4)+(3)(-2)+(-5)(-1)\\&=4-6+5\\&=3\end{aligned}}}$
点积还可以写为：

${\displaystyle {\vec {a}}\cdot {\vec {b}}={\vec {a}}{\vec {b}}^{T}}$。
这里，${\displaystyle {\vec {b}}^{T}}$是行向量$\vec{b}$的转置。

使用上面的例子，一个1×3矩阵（行向量）乘以一个3×1矩阵（列向量）的行列式就是结果(通过矩阵乘法得到1×1矩阵):

${\displaystyle {\begin{bmatrix}1&3&-5\end{bmatrix}}{\begin{bmatrix}4\\-2\\-1\end{bmatrix}}={\begin{bmatrix}3\end{bmatrix}}=3}$。 


#### ***几何定义*** 

在欧几里得空间中，点积可以直观地定义为  

$\vec{a} \cdot \vec{b} = |\vec{a}| \, |\vec{b}| \cos \theta \;$  

这里 $|\vec{x}|$ 表示$\vec{x}$的模（长度），$\theta$ 表示两个向量之间的角度。  

注意：点积的形式定义和这个定义不同；在形式定义中，$\vec{a}$和$\vec{b}$的夹角是通过上述等式定义的。  

这样，两个互相垂直的向量的点积总是零。若$\vec{a}$和$\vec{b}$都是单位向量（长度为1），它们的点积就是它们的  夹角的余弦。那么，给定两个向量，它们之间的夹角可以通过下列公式得到：

$\cos{\theta} = \frac{\mathbf{a \cdot b}}{|\vec{a}| \, |\vec{b}|}$  

这个运算可以简单地理解为：在点积运算中，第一个向量投影到第二个向量上（这里，向量的顺序是不重要的，点积运算是可交换的），然后通过除以它们的标量长度来“标准化”。这样，这个分数一定是小于等于1的，可以简单地转化成一个角度值。  

#### ***性质***

点积具有以下性质。  

* 满足交换律：  

    ${\displaystyle {\vec {a}}\cdot {\vec {b}}={\vec {b}}\cdot {\vec {a}}}$  

    从定义即可证明（$\theta$  为a与b的夹角）：  

    ${\displaystyle {\vec {a}}\cdot {\vec {b}}=\left\|{\vec {a}}\right\|\left\|{\vec {b}}\right\|\cos \theta =\left\|{\vec {b}}\right\|\left\|{\vec {a}}\right\|\cos \theta ={\vec {b}}\cdot {\vec {a}}}$  
<br />  

* 对向量加法满足分配律：  

    $\vec{a} \cdot (\vec{b} + \vec{c}) = \vec{a} \cdot \vec{b} + \vec{a} \cdot \vec{c}$  
<br />  

* 点积是双线性算子：  

    ${\displaystyle {\vec {a}}\cdot (r{\vec {b}}+{\vec {c}})=r({\vec {a}}\cdot {\vec {b}})+({\vec {a}}\cdot {\vec {c}})}$  
<br />  

* 在乘以标量时满足：  

    $(c_1\vec{a}) \cdot (c_2\vec{b}) = (c_1c_2) (\vec{a} \cdot \vec{b})$  
<br />  

* 不满足结合律。
    因为标量（${\displaystyle {\vec {a}}\cdot {\vec {b}}}$）与向量（$\vec{c}$）的点积没有定义，所以结合律相关的表达式${\displaystyle ({\vec {a}}\cdot {\vec {b}})\cdot {\vec {c}}}$ 和 ${\displaystyle {\vec {a}}\cdot ({\vec {b}}\cdot {\vec {c}})}$ 都没有良好的定义  
<br />  

---
### 外积（叉积）

在数学和向量代数领域，叉积（Cross product）又称向量积（Vector product），是对三维空间中的两个向量的二元运算，使用符号 $\times$。与点积不同，它的运算结果是向量。  

对于线性无关的两个向量 $\mathbf {a}$  和 $\mathbf {b}$ ，它们的叉积写作 ${\displaystyle \mathbf {a} \times \mathbf {b} }$，是 $\mathbf {a}$  和 $\mathbf {b}$  所在平面的法线向量，与 $\mathbf {a}$  和 $\mathbf {b}$  都垂直。  

#### ***代数性质***

对于任意三个向量 $\mathbf {a}$ 、$\mathbf {b}$ 、$\mathbf {c}$ ，  

* ${\displaystyle \mathbf {a} \times \mathbf {a} =\mathbf {0} }$  
<br />  

* ${\displaystyle \mathbf {a} \times \mathbf {0} =\mathbf {0} }$  
<br />  

* ${\displaystyle \mathbf {a} \times \mathbf {b} =-\mathbf {b} \times \mathbf {a} }$（反交换律）  
<br />  

* ${\displaystyle \mathbf {a} \times (\mathbf {b} +\mathbf {c} )=\mathbf {a} \times \mathbf {b} +\mathbf {a} \times \mathbf {c} }$（加法的左分配律）  
<br />  

* ${\displaystyle (\mathbf {a} +\mathbf {b} )\times \mathbf {c} =\mathbf {a} \times \mathbf {c} +\mathbf {b} \times \mathbf {c} }$（加法的右分配律）  
<br />  

* ${\displaystyle (\lambda \mathbf {a} )\times \mathbf {b} =\lambda (\mathbf {a} \times \mathbf {b} )=\mathbf {a} \times (\lambda \mathbf {b} )}$  
<br />  

* ${\displaystyle \mathbf {a} \times \mathbf {b} +\mathbf {c} \times \mathbf {d} =(\mathbf {a} -\mathbf {c} )\times (\mathbf {b} -\mathbf {d} )+\mathbf {a} \times \mathbf {d} +\mathbf {c} \times \mathbf {b} }$  
<br />  

* ${\displaystyle |\mathbf {a} \times \mathbf {b} |=|\mathbf {b} \times \mathbf {a} |}$  
<br />  

* ${\displaystyle |\mathbf {a} \times \mathbf {b} |^{2}=|\mathbf {a} |^{2}|\mathbf {b} |^{2}-(\mathbf {a} \cdot \mathbf {b} )^{2}={\begin{vmatrix}\mathbf {a} \cdot \mathbf {a} &\mathbf {a} \cdot \mathbf {b} \\\mathbf {a} \cdot \mathbf {b} &\mathbf {b} \cdot \mathbf {b} \\\end{vmatrix}}}$（拉格朗日恒等式）  
<br />  

一般来说，向量叉积不遵守约简律，即 ${\displaystyle \mathbf {a} \times \mathbf {b} =\mathbf {a} \times \mathbf {c} }$ 不表示${\displaystyle \mathbf {b} =\mathbf {c} }$。此外，${\displaystyle \mathbf {a} \times \mathbf {b} =\mathbf {0} }$ 不表示 ${\displaystyle \mathbf {a} =\mathbf {0} }$ 或 ${\displaystyle \mathbf {b} =\mathbf {0} }$。  

但对于两个非零向量 $\mathbf {a}$  和 $\mathbf {b}$:

* ${\displaystyle \mathbf {a} \times \mathbf {b} =\mathbf {0} }$ 当且仅当 $\mathbf {a}$  平行于 $\mathbf {b}$  









