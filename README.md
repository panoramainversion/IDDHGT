基于有限欧拉乘积的黎曼 Zeta 函数动态切分理论

摘要 (Abstract)

本文提出了一种针对黎曼 Zeta 函数 $\zeta(s)$ 的动态切分框架。通过引入截断参数 $N$，我们将全体正整数划分为三个互斥的算术子集，从而将 $\zeta(s)$ 分解为三个区域函数：核心项 $R_1$、平滑项 $R_2$ 与全局余项 $R_3$。本文进一步定义了差分扩张算子 $\Phi$，用以描述系统随截断规模 $N$ 增大时的演化行为。该框架揭示了非平凡零点从虚轴 $\mathrm{Re}(s)=0$ 向临界线 $\mathrm{Re}(s)=\frac{1}{2}$ 迁移的动力学机制。



1. 预备知识与符号说明 (Preliminaries)

设 $s = \sigma + it \in \mathbb{C}$。令 $\mathbb{P}$ 为全体质数集合。针对任意正整数截断 $N \in \mathbb{Z}^+$，定义以下算术量：



截断质子集： $\mathbb{P}_N = { p \in \mathbb{P} \mid p \leq N }$

$p$ 进赋值指数： $a_p = v_p(N) = \max { k \in \mathbb{Z}_{\geq 0} : p^k \mid N }$

$N$-光滑数集： $S_N = { n \in \mathbb{Z}^+ \mid p \mid n \implies p \leq N }$
该集合包含所有质因子均不超过 $N$ 的正整数。



2. 三个区域函数的解析分解 (Regional Functions)

基于算术基本定理，我们将 $\zeta(s)$ 在 $\mathrm{Re}(s) > 1$ 处的狄利克雷级数展开式划分为三个具有明确算术意义的子级数。


2.1 核心区域 $R_1$ (约数生成函数)

定义 $R_1(s; N)$ 为 $N$ 的全体正约数构成的有限级数：
$$R_1(s; N) = \sum_{d \mid N} \frac{1}{d^s} = \prod_{p \in \mathbb{P}_N} \frac{1 - p^{-s(a_p+1)}}{1 - p^{-s}}$$
该区域代表了系统在当前“语法深度” $N$ 下完全确定的已知部分。


2.2 过渡区域 $R_2$ (光滑非约数项)

定义 $R_2(s; N)$ 为所有质因子 $\leq N$ 但不整除 $N$ 的数构成的级数：
$$R_2(s; N) = \sum_{\substack{n \in S_N \ n \nmid N}} \frac{1}{n^s} = \prod_{p \in \mathbb{P}N} \frac{1}{1 - p^{-s}} - \prod{p \in \mathbb{P}_N} \frac{1 - p^{-s(a_p+1)}}{1 - p^{-s}}$$
该区域代表了基于已知质数生成的潜能项，但由于幂次超标而未进入核心区域。


2.3 全局余项区域 $R_3$ (高维质数项)

定义 $R_3(s; N)$ 为所有包含至少一个大于 $N$ 的质因子的数构成的级数：
$$R_3(s; N) = \sum_{n \notin S_N} \frac{1}{n^s} = \zeta(s) - \prod_{p \in \mathbb{P}_N} \frac{1}{1 - p^{-s}}$$


2.4 全局分解恒等式

定理 2.1. 对于任何 $N \geq 1$ 且 $\mathrm{Re}(s) > 1$，$\zeta(s)$ 存在如下唯一分解：
$$\zeta(s) = R_1(s; N) + R_2(s; N) + R_3(s; N)$$



3. 差分扩张算子 $\Phi$ (Evolution Operator)

定义系统从截断规模 $N$ 跃迁至 $N'$ 的扩张算子 $\Phi$：
$$\Phi_{N \to N'}(s) = \frac{R_1(s; N')}{R_1(s; N)}$$


演化通过以下两种路径实现：



维度激活 (Path A)： 引入新质数 $q > N$。

深度演化 (Path B)： 提升已有质数 $p \leq N$ 的赋值 $a_p$。


系统的生长由乘性方程驱动：$R_1(s; N') = R_1(s; N) \cdot \Phi_{N \to N'}(s)$。



4. 渐近极限与收敛性 (Convergence)

定理 4.1. 在 $N \to \infty$ 且满足 $\min(a_p) \to \infty$ 的条件下：



$\lim_{N \to \infty} R_2(s; N) = 0$

$\lim_{N \to \infty} R_3(s; N) = 0$

$\lim_{N \to \infty} R_1(s; N) = \zeta(s)$


这表明有限的算术结构在极限状态下与无限的 Zeta 函数实现精准同构。



5. 零点迁移理论 (Zero-Migration)

5.1 原始零点位置

命题 5.1. $R_1(s; N)$ 的所有根（原始零点）均分布在虚轴 $\mathrm{Re}(s) = 0$ 上。


5.2 动力学迁移机制

全局零点 $\zeta(s)=0$ 满足平衡方程：
$$R_1(s; N) = - [R_2(s; N) + R_3(s; N)]$$


结论： 随着系统的语法扩张（$N$ 增大），区域三 $R_3$ 产生的高频随机相位与 $R_1$ 在复平面上进行非线性干涉。受函数方程对称性的约束，这种干涉在 $\sigma = \frac{1}{2}$ 处形成稳定的吸引子，迫使零点离开虚轴向临界线迁移。



6. 数值验证建议 (Computation)

研究者可通过观察前若干个质数生成的 $R_1+R_2$ 级数在临界带内的局部极小值点，追踪其随 $N$ 增加而向 $\sigma=0.5$ 靠拢的轨迹。

