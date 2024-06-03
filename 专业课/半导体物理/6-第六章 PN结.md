# 6-第六章 PN结

## 6.1 平衡pn结特性

### 6.1.1 基本结构

pn结是同一块半导体内p型区和n型区的交界面，如下图所示：

![image-20240529185131652](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240529185131652.png)

pn结包括下面几个基本的性质：

结深：上图中的xj对应的位置

结形状，如下图所示结面是一个平面的平面结：

![image-20240529185615172](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240529185615172.png)

结两侧的杂质掺杂浓度分布

### 6.1.2 PN结的杂质浓度分布

pn结的杂质浓度分布的数学表达式比较复杂，通常用突变结和线性缓变结近似实际的杂质分布

**突变结：**

下图是突变结的杂质浓度分布，在结深度xj处也就是结的位置有一个突然的跃变，而杂质浓度在结两侧都是均匀分布的：

![image-20240529185837063](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240529185837063.png)

pn结的杂质浓度函数有：
$$
N(x) = \left\{\begin{matrix}N_A (x < x_j)

 \\N_D(x > x_j)

\end{matrix}\right.
$$
当一边的浓度远大于另一遍的突变结称为单边突变结，标记为$p^+n$或者$n^+p$，上面的角标加号表示一遍的浓度远大于另一边的浓度：
$$
\left\{\begin{matrix} p^+结:N_A >> N_D
\\n^+p结:N_D >> N_A
\end{matrix}\right.
$$


**线性缓变结：**

另外是线性缓变结，杂质浓度在结附近随x线性变化，杂质浓度梯度$a_j$为常数，如下图所示：

![image-20240529190218346](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240529190218346.png)

这时的pn结杂质浓度函数为：
$$
N(x) = a_j(x - x_j)
$$

---

**需要注意的是：**

（1）突变结和线性缓变结是实际杂质浓度分布的两个极端近似

（2）突变结可以给出简单的分析结果，在大多数pn结的分析中，除非特殊说明，一般才用突变结近似

### 6.1.3 平衡pn结的空间电荷区

平衡pn结就是指没有外加电压和光照且内部温度恒定的pn结

pn结的许多重要性质都与空间电荷区有关

对于均匀掺杂的半导体，在热平衡时是电中性的，如下图所示：

![image-20240529191338460](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240529191338460.png)

当两种掺杂的材料发生接触的时候，由于结面处的载流子的浓度差，电子和空穴分别朝结的相反的方向进行扩散，n型半导体的电子浓度大于p型半导体电子浓度，电子向p型半导体扩散，p型半导体的空穴向n型半导体扩散：

![image-20240529191505280](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240529191505280.png)

载流子的扩散会在靠近结的区域留下未被抵消的电离杂质电荷，形成电场：

![image-20240529192003258](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240529192003258.png)

电场会引起载流子的漂移运动，其方向与各自的扩散方向相反，当漂移运动与扩散项抵消时，载流子的净移动为零，在结的两侧就会形成一个稳定的，有一定宽度的空间电荷区；空间电荷区的p型一侧为负电荷，n型一侧为正电荷，正负电荷形成的电场称为自建场，自建场的方向由n区指向p区，如下图所示，空间电荷区基本上就是由电离施主和电离受主构成的：

![image-20240529191231957](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240529191231957.png)

而在热平衡时，空间电荷以外的区域，在特性上与孤立的半导体是完全一样的，是电中性的，称为中性区

### 6.1.4 pn结的能带图

 对于平衡的p型半导体，费米能级靠近价带顶，n型半导体的费米能级靠近导带低如下图所示，Ei是禁带中线：

![image-20240529193322100](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240529193322100.png)

对于电子来说，在宏观下，漂移和扩散的电流强度之和应该为0，也就是：
$$
(J_n)_扩 + (J_n)_漂 = 0
$$
在pn结中因为电子和空穴在不断中和，所以电子浓度应该和位置有关，即$n_0(x)$，我们代入扩散电流和漂移电流的式子得到：
$$
qD_n\frac{dn_0(x)}{dx} + n_0(x)q\mu_n|E| = 0
$$
在热平衡状态下的电子浓度的公式有：$n_0 = N_c exp(-\frac{E_c - E_F}{k_0T})$，其与导带底和费米能级是对应的，因此我们有理由认为当电子浓度随位置x发生变化的时候导带低和费米能级都是随位置变化的变换上式在指数项的分子加上减去Ei加上Ei得到：
$$
n_0 = N_cexp(-\frac{E_c - E_i + E_i - E_F}{k_0T}) = N_cexp(-\frac{E_c - E_i}{k_0T})exp(\frac{E_F - E_i}{k_0T})
$$
$ N_cexp(-\frac{E_c - E_i}{k_0T})$其实就是本征半导体中的载流子浓度$n_i$，因此有：
$$
n_0 = n_iexp(\frac{E_F - E_i}{k_0T})
$$
将ni除到等式左边，并取对数后对x求导，注意ni是本征半导体中的载流子的浓度，是一个常数，所以得到：
$$
\frac{dn_0}{dx} = -n_0\frac{1}{k_0T}\frac{dE_i}{dx} + n_0\frac{1}{k_0T}\frac{dE_F}{dx}
$$
在上式中我们认为Ei和EF都是与x有关的，其中$E_i = \frac{E_c + E_v}{2} = E_c - \frac{E_g}{2}$，而Eg是一个常数，显然有$\frac{dE_i}{dx} = \frac{dE_c}{dx}$：
$$
\frac{dn_0}{dx} = -n_0\frac{1}{k_0T}\frac{dE_c}{dx} + n_0\frac{1}{k_0T}\frac{dE_F}{dx}
$$
因为|E|存在，电子能量下降与位置x有关比Ec下降了$qV(x)$，注意电子从左侧漂移到右侧，能量是下降了，加上左侧p型半导体的导带低是Ec0，那么有：
$$
E_c(x) - E_{C0} = -qV(x)
$$
所以有：
$$
\frac{dE_c}{dx} = -q\frac{dV(x)}{dx}
$$
根据电场的定义：$|E| = - \frac{dV(x)}{dx}$，而电场在平衡状态下为一个定值，所以有：
$$
\frac{dn_0}{dx} = -n_0\frac{qE}{k_0T} + n_0\frac{1}{k_0T}\frac{dE_F}{dx}
$$
将上式代入：$qD_n\frac{dn_0(x)}{dx} + n_0(x)q\mu_n|E| = 0$得到：
$$
J_n = qn_0\mu_nE - qD_nn_0\frac{qE}{k_0T} + n_0\frac{qD_n}{k_0T}\frac{dE_F}{dx} = 0
$$
根据爱因斯坦关系式：$\frac{D_n}{\mu_n} = \frac{k_0T}{q}$，代入上式可以发现前两项可以约掉，所以得到：
$$
\frac{dE_F}{dx} = 0
$$
这就说明费米能级在pn结中是不随位置x发生变化的，因此我们在画能带图的时候应该先画一个费米能级EF，是一条固定的横线

pn结中间有空间电荷区，而在pn结两边仍然是电中性的，因此在n型半导体一侧，导带低Ec靠近费米能级，并且由于电子的漂移向右，能量下降，因此n型半导体中的导带底显然能量是低于p型区的

同理在p型半导体，费米能级应该靠近价带顶，同时空穴的漂移从p型半导体到n型半导体，能量应该上升，n型区相对p型区的价带顶应该向下移动

所以在中间的空间电荷区导带底和价带顶应该是成一个曲线变化的，注意不是直线，如下图所示，禁带中线在导带底和价带顶中间，所以也应该是一个曲线：

<img src="https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240529210232920.png" alt="image-20240529210232920" style="zoom:67%;" />

![image-20240529210253876](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240529210253876.png)

### 6.1.5 pn结接触电势差

注意，如果以pn结左侧的中性p型半导体为电势0的地方，那么由于电场强度从右到左，所以pn结中从左到右应该是电势逐渐上升的，并在n型半导体的边缘处达到一个极大值VD，我们就称这个VD为半导体的接触电势差：

![image-20240530172851041](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240530172851041.png)

很显然n型区的导带底和p型区的导带底的能量的差值就是qVD，称为势垒，如下图所示：

![image-20240530173143301](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240530173143301.png)

下面来分析这个势垒的来源，根据上图可以看到这个势垒也就是p型半导体中导带底到费米能级的距离减去n型半导体中导带底到费米能级的距离：
$$
qV_D = (E_{cp} - E_{Fp}) - (E_{cn} - E_{Fn})
$$
注意到同种材料的p, n两种半导体在接触之前它们的导带底和价带顶的能级是完全一样的，只是费米能级之间有差异，当接触之后两者的费米能级移动到同一位置，但是费米能级与各自的导带底能级的差异是不变的，所以形成pn结之后两者导带底的差距就是形成pn结之前费米能级之间的差异：

![image-20240530173944456](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240530173944456.png)

得到：
$$
qV_D = E_{F(n)} - E_{F(p)}
$$
根据第三章的公式，对于热平衡态非简并半导体在强电离区的费米能级位置公式有：

n型半导体：$E_{F(n)} = E_i + k_0Tln(\frac{N_D}{n_i})$

p型半导体：$E_{F(p)} = E_i - k_0Tln(\frac{N_A}{n_i})$

上式中的ND是n型半导体的掺杂浓度，NA是p型半导体的掺杂浓度，ni是本征半导体的载流子浓度

代入$qV_D = E_{F(n)} - E_{F(p)}$得到接触电势差：
$$
V_D = \frac{k_0T}{q}ln(\frac{N_AN_D}{n_i^2})
$$

> 假如掺杂的受主浓度$N_A = 10^{17}cm^{-3}$，施主浓度是$N_D = 10^{15}cm^{-3}$，那么有：
>
> Si材料的pn结：$V_D \approx   0.7V$
>
> Ge材料的pn结：$V_D \approx 0.3V$

### 6.1.6 pn结的载流子分布

我们先规定一下坐标体系，我们定义pn结的中间为x = 0处，p型区的边界为-xp处，n型区的边界为xn处，那么电势差与x的关系图如下所示：

![image-20240530175731128](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240530175731128.png)

下面我们来求x一点处的载流子浓度

在热平衡态下的导带电子浓度有：$n = N_c exp(-\frac{E_c - E_F}{k_0T})$，这个式子只要是在热平衡非简并情况下都适用，因为导带底是随x变化的，所以我们有：
$$
n(x) = N_c exp(-\frac{E_c(x) - E_F}{k_0T})
$$
我们对指数项的分子部分进行$+E_{cn} - E_{cn}$变换得到：
$$
n(x) = N_c exp(-\frac{E_c(x) + E_{cn} - E_{cn} - E_F}{k_0T}) = N_cexp(-\frac{E_{cn} - E_F}{k_0T})exp(-\frac{E_c(x) - E_{cn}}{k_0T})
$$
对于$N_cexp(-\frac{E_{cn} - E_F}{k_0T})$不就是右侧n区的平衡态下的导带电子浓度吗，这里用$n_{n0} = N_cexp(-\frac{E_{cn} - E_F}{k_0T})$代替，因此得到：
$$
n(x) = n_{n0}exp(-\frac{E_c(x) - E_{cn}}{k_0T})
$$
而对于$E_c(x) - E_{cn}$，根据下图某一点x处的导带能量和n区的导带底的能量差，其实就是qVD减去这一点相对于Ecp降低的能量也就是$qV(x)$，$V(x)$是这一点x处的电势：$E_c(x) - E_{cn} = qV_D - qV(x)$，下图中黑色箭头就是$E_c(x) - E_{cn}$，红色箭头就是$qV(x)$

![image-20240530181513980](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240530181513980.png)

我们将这个关系代入上式得到：
$$
n(x) = n_{n0}exp(-\frac{qV_D - qV(x)}{k_0T})
$$
我们令上式中$x = -x_p$，也就是p区与pn结的结面处的电子浓度有（此时电势为0）：
$$
n(-x_p) =n_{n0}exp(-\frac{qV_D }{k_0T}) = n_{p0}
$$
界面处的导带电子浓度也就是平衡p区的导带电子浓度$n_{p0}$，这就说明平衡n区的电子浓度乘上上式的一个衰减系数就变成了平衡p区的电子浓度！！！

我们如果用平衡p区的电子浓度np0来表达电子浓度式子那么得到：
$$
n(x) = n_{n0}exp(-\frac{qV_D }{k_0T})exp(\frac{qV(x)}{k_0T}) = n_{p0}exp(\frac{qV(x)}{k_0T})
$$
上式也就说明，在空间电荷区的电子浓度，是从p型的边界区从np0按照V(x)，指数增加到$n_{n0}$​的

同理我们可以得到空穴随着x的分布：
$$
p(x) = N_vexp(-\frac{E_F - E_v(x)}{k_0T}) = p_{p0}exp(-\frac{E_{Vp} - E_v(x)}{k_0T})
$$
同上文，得到x = xn处的空穴浓度有：
$$
p(x_n) = p_{p0}exp(-\frac{E_{vp} - E_{vn}}{k_0T}) = p_{p0}exp(-\frac{qV_D}{k_0T}) = p_{n0}
$$
上式中的$p_{p0}, p_{n0}$也就是平衡p区和平衡n区的价带空穴浓度，两者仍然成一个指数系数的关系，同上文我们得到一个p(x)公式：
$$
p(x) = p_{p0}exp(-\frac{qV(x)}{k_0T})
$$
上式就说明空间电荷区的空穴浓度从平衡p区的空穴浓度指数衰减到平衡n区的空穴浓度的

在图像中表示就是：

![image-20240530183548617](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240530183548617.png)

根据载流子的浓度我们写出电导率：$\sigma = qn\mu_n + qp\mu_p$，由于电导率在平衡区是跟多子相关的，但是在空间电荷区多子会迅速衰减，然后另一种载流子数量占上风来决定电导率，所以在空间电荷区的电导率有一个极小值，然后再增加，同理根据电阻率$\rho = \frac{1}{\sigma}$，我们得到电导率和电阻率的图像，下图中的xp，xn分别是两种半导体的边界点：

![image-20240530184033775](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240530184033775.png)

上图的空间电荷的高阻区意味着如果在pn结处加上一个电压的话，**大部分的电压都将降落在高阻区**

> eg：对于Si，在T = 300K，$V_D = 0.7V$的时候求位置x满足$E_c(x) = E_{cn} + 0.1eV$​位置处的载流子浓度
>
> 由于x处的导带底能量比Ecn高了0.1eV，所以x处的电压应该比Ecn处低了0.1V，即$V(x) = V_D - 0.1V = 0.6V$
>
> 得到$n(x) = n_{n0}exp(-\frac{qV_D - qV(x)}{k_0T}) = n_{n0}exp(-\frac{0.1}{0.026}) \approx \frac{N_D}{50}$
>
> $p(x) = p_{p0}exp(-\frac{qV(x)}{k_0T}) = p_{p0}exp(-\frac{0.6}{0.026})\approx 10^{-10}N_A$
>
> 注意上式中平衡区由于是强电离，多子浓度近似等于杂质浓度，可以看到空间电荷区中的载流子浓度远远小于它们在平衡区的多子浓度
>
> 所以在势垒区（空间电荷区）的载流子浓度与掺杂浓度相比是可以忽略的，因此在空间电荷区里的电荷密度其实就是等于电离杂质浓度（杂质电离留下的正电负电中心）
>
> 在空间电荷区忽略了电子和空穴的存在就好像它们全部消失了，因此就称为耗尽层近似

## 6.2 pn结的电流电压特性

### 6.2.1 pn结中的电场和电势分布

#### 电场分布

我们认为电场只存在于空间电荷区的， 空间电荷区以外（耗尽层）是没有电场的

我们需要解出电场和电势的函数，怎么解呢，用泊松方程，电位移矢量的散度等于电荷体密度即$\nabla \vec{D} = \rho$，一维条件下有：
$$
\frac{dD}{dx} = \rho
$$
D是电位移矢量$D = \epsilon E$，因此有：
$$
\frac{dE}{dx} = \frac{\rho}{\epsilon}
$$
而电场强度有$E = \frac{-dV}{dx}$，因此得到：
$$
-\frac{d^2V}{dx^2} = \frac{dE}{dx} = \frac{\rho}{\epsilon}
$$
电势的二阶微分等于电荷浓度除以结点常数，我们想要电场分布，那就必须知道电荷体密度$\rho$，在解泊松方程的前提必须要知道$\rho(x)$，根据上文，电离区的杂质浓度是个常数NA, ND，所以这里解方程就及其简单了

假设在突变的p+/n结中（p型区的掺杂NA >> ND），其杂质浓度图如下所示：

![image-20240529185837063](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240529185837063.png)

电荷体密度有$\rho(x) = q(N_D - N_A + p - n)$，根据耗尽层近似$n = p = 0$

因此在p型区的杂质电荷密度有：$\rho(x) = -qN_A(-x_p \le x \le 0)$（杂质电离留下负电中心），在n型区的杂质电荷密度$\rho(x) = qN_D 0 (\le x \le x_n)$​（杂质电离留下正电中心）

根据泊松方程$\frac{d^2V}{dx^2} = -\frac{\rho(x)}{\epsilon_r \epsilon_0}$得到：
$$
E(x) = -\frac{dV}{dx} = -\int \frac{d^2V}{dx^2}dx
$$
根据边界条件$x = x_n, x = -x_p 处E = 0$，因此得到：

当$-x_p \le x \le 0$​时
$$
E(x) = \int \frac{\rho(x)}{\epsilon_r \epsilon_0}dx = -\int\frac{qN_A}{\epsilon_r \epsilon_0}dx  = -\frac{qN_A}{\epsilon_r \epsilon_0}x + C \rightarrow^{代入边界条件} E_p(x) = -\frac{qN_A}{\epsilon_r \epsilon_0}(x + x_p)
$$
当$0 \le x \le x_n$时
$$
E_n(x) = -\frac{qN_D}{\epsilon_r \epsilon_0}(x_n - x)
$$
在pn结的交界处电场相等，达到最大值：
$$
E_m = -\frac{qN_Ax_p}{\epsilon_r \epsilon_0} = -\frac{qN_Dx_n}{\epsilon_r \epsilon_0}
$$
那么可以得到电场的分布图像如下所示：

<img src="https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240602114736857.png" alt="image-20240602114736857" style="zoom:67%;" />

根据$E_m = -\frac{qN_Ax_p}{\epsilon_r \epsilon_0} = -\frac{qN_Dx_n}{\epsilon_r \epsilon_0}$，我们得到：
$$
qN_Ax_pS = qN_Dx_nS
$$
上式中的S是pn结的截面积，这就说明p型区和n型区的总电荷量是相等的，因此我们得到：
$$
\frac{x_n}{x_p}=\frac{N_A}{N_D}
$$
对于p+n结，由于NA >> ND，所以得到：
$$
x_n >> x_p
$$
这就说明p型区和n型区并不是对称的，耗尽区总是在轻掺杂的一边，浓度低的必须要很厚才能达到和浓度高的相等的电荷量！并且抗压最多的也在低掺杂区，pn结如果坏了，坏的最多的也是在轻掺杂区

当然还有一个方法来求解电势的分布，使用高斯定理：**电场强度在一封闭曲面上的面积分与封闭曲面所包围的电荷量成正比**，什么意思呢？

假如我们有一个带电体，导体带电，只有表面有电，我想要求这个带电体形成的电场强度，假设表面电荷的面密度为$\sigma$，那么我们可以做一个正方体如下图所示蓝色，这个正方体的前后左右都没有电场穿过，下面因为是在导体中，因此没有电场，所以只有上面有电场穿过：

<img src="https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240603163427372.png" alt="image-20240603163427372" style="zoom:67%;" />

那么我们可以得到：
$$
ES = \frac{\sigma S}{\epsilon}
$$
等式左侧就是电通量，也是E对S的面积分，这里的正比系数就是介电常数的倒数，也就是$E = \frac{\sigma}{\epsilon}$，这样就非常简单地求出电场强度了

同理我们看pn结中的电场强度，假设是在n型区，我们同样做一个长方体：

<img src="https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240603163940943.png" alt="image-20240603163940943" style="zoom:67%;" />

假设pn结的横截面积是S，上下前后都没有电场穿过，只有左侧面S有电场穿过，因此我们得到：
$$
ES = \frac{qN_DS(x_n - x)}{\epsilon_r \epsilon_0}
$$
得到：
$$
E =  \frac{qN_D(x_n - x)}{\epsilon_r \epsilon_0}
$$
带个方向就是负值了，这不就是n型区的电场强度公式么：$E =  -\frac{qN_D(x_n - x)}{\epsilon_r \epsilon_0}$，这里如果硬要较真负号的话可以建系

<img src="https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240603171922741.png" alt="image-20240603171922741" style="zoom: 50%;" />

此时$\vec{E} = (0, -E, 0)$，那么$\iint \vec{E}d\vec{S} = -\iint -Edzdy = ES = \frac{qN_DS(x_n - x)}{\epsilon_r \epsilon_0}$，这样解出来的E的大小就是正的了，此时$\vec{E} = -E\vec{i}$

简化为一维就是$E =  -\frac{qN_D(x_n - x)}{\epsilon_r \epsilon_0}$​

#### 电势分布

由电场分布：

当$-x_p \le x \le 0$​时
$$
E_p(x) = -\frac{qN_A}{\epsilon_r \epsilon_0}(x + x_p)
$$
当$0 \le x \le x_n$时
$$
E_n(x) = -\frac{qN_D}{\epsilon_r \epsilon_0}(x_n - x)
$$
电势分布为$V(x) = -\int E(x)dx$，边界条件为：$x = -x_p, V = 0, x  = x_n , V = V_D$所以：

当$-x_p \le x \le 0$时
$$
V(x) = \int \frac{qN_A}{\epsilon_r \epsilon_0}(x + x_p)dx = \frac{qN_A}{2 \epsilon_r \epsilon_0}(x + x_p)^2 + C(C = 0)
$$
当$0 \le x \le x_n$时


$$
V(x) = V_D - \frac{qN_D}{2\epsilon_r \epsilon_0}(x_n - x)^2
$$
所以电势的图像如下所示，其实就是两个抛物线组合起来：

<img src="https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240603172653936.png" alt="image-20240603172653936" style="zoom:67%;" />

根据上面两个电势的关系，在x = 0处有$V_p(x) = V_n(x)$，从而得到：
$$
V_D = \frac{qN_D}{2\epsilon_r \epsilon_0}x_n^2 + \frac{qN_A}{2\epsilon_r \epsilon_0}x_p^2
$$
那么**势垒宽度**有$X_D = x_p + x_n$，并且有$\frac{x_n}{x_p}=\frac{N_A}{N_D}$，因此得到：
$$
\frac{x_p}{x_n + x_p} = \frac{N_D}{N_A + N_D}
$$
于是得到：
$$
x_n = \frac{N_A}{N_A + N_D}X_D, x_p = \frac{N_D}{N_A + N_D}X_D
$$
所以有：
$$
V_D = \frac{q}{2\epsilon_r \epsilon_0}\frac{N_AN_D}{N_A + N_D}X_D^2
$$
所以得到势垒宽度有：
$$
X_D = \sqrt{\frac{2 \epsilon_r \epsilon_0(N_A + N_D)V_D}{qN_AN_D}} = \sqrt{\frac{2 \epsilon_r \epsilon_0V_D}{qN_B}}
$$
上式中的$N_B = \frac{N_AN_D}{N_A + N_D}$称为有效掺杂浓度，当掺杂浓度确定以后，VD, NA, ND都确定了，那么势垒宽度也就确定了，因为是p+n结，所以NA >> ND，因此有：
$$
X_D = \sqrt{\frac{2 \epsilon_r \epsilon_0V_D}{qN_D}} \approx x_n
$$
同理，如果是n+p结，那么有：
$$
X_D = \sqrt{\frac{2 \epsilon_r \epsilon_0V_D}{qN_A}} \approx x_p
$$

#### 线性缓变结的电场电势分布

如果对于线性缓变结，它的杂质浓度分布不是突变的，如果用ND - NA表示杂质分布的话如下图所示：

![image-20240603174614861](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240603174614861.png)

根据耗尽层近似，因此它的电荷分布就是：
$$
\rho(x) = q(N_D - N_A) = q\alpha x
$$
上式中的$\alpha$是杂质浓度梯度

根据泊松方程$-\frac{d^2V}{dx^2} = \frac{dE}{dx} = \frac{\rho}{\epsilon} = \frac{q\alpha x}{\epsilon_r \epsilon_0}$，边界条件为$x = \pm \frac{X_D}{2}, E(x) = 0$，得到电场分布：
$$
E(x) = -\int \frac{d^2V}{dx^2}dx = \frac{q\alpha}{2\epsilon_r \epsilon_0}[x^2 - (\frac{X_D}{2})^2]
$$
因此得到电场的图像为（是一个二次函数）：

![image-20240603175236584](https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240603175236584.png)

同理得到电势分布：
$$
V(x) = -\int E(x)dx = \frac{q\alpha}{2\epsilon_r \epsilon_0}[(\frac{X_D}{2})^2x - \frac{1}{3}x^3]
$$
<img src="https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240603175257608.png" alt="image-20240603175257608" style="zoom:67%;" />

由于$V(\frac{X_D}{2}) - V(-\frac{X_D}{2}) = V_D$，所以得到耗尽层宽度为：
$$
X_D = (\frac{12 \epsilon_r \epsilon_0 V_D}{q\alpha})^{\frac{1}{3}}
$$

### 6.2.2 非平衡p - n结的能带图

非平衡，那就是加上一个电压，大部分电压都降落在势垒区，可以近似认为所有的电压都降落在势垒区

这时外加电压有两种情况

**（1）对于外加电压形成的电场与原来的自建场方向相反的时候（正电压，电场从p指向n，p区接正电压）**

<img src="https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240603190453141.png" alt="image-20240603190453141" style="zoom:67%;" />



自建场被减弱，所以总的势垒降低了，因此电子需要爬坡的电压降低了，平衡区的导带底相比于之前没有下降那么狠了也就是$q(V_D - V_f)$，n型区的整体相对于平衡的来讲需要整体向上平移一段距离

由于自建场的作用是抑制载流子的扩散，那么我们加的电场与其相反，于是载流子就扩散更多了，p型区的空穴扩散更多到n型区，n型区的电子扩散更多到p型区，在平衡的时候扩散的载流子通过自建场漂移拉回去，总体没有电流，但是自建场被削弱之后扩散的载流子拉不回去了

**因此从p区扩散到n区的一部分空穴就注入到了n型区成为了n型区的非平衡少数载流子**

**以及从n区扩散到p区的一部分电子就注入到了p型区成为了p型区的非平衡少数载流子**

这些非平衡少子会一边扩散，一边复合，假设非平衡空穴扩散的长度是Lp，非平衡电子扩散的长度是Ln，扩散长度会形成扩散区：

<img src="https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240603192412612.png" alt="image-20240603192412612" style="zoom:67%;" />

在正向偏压下，PN结的N区和P区都有非平衡少数载流子的注入。在非平衡少数载流子存在的区域内，必须用电子的准费米能级$E_{Fn}$和空穴的准费米能级$E_{Fp}$取代原来平衡时的统一费米能级$E_F$

以n型区为例，根据准费米能级的定义：

导带电子浓度：$n = n_0 + \Delta n = N_cexp(-\frac{E_C - E_F^n}{k_0T})$

价带空穴浓度：$p = p_0 + \Delta p = N_v exp(\frac{E_v - E_F^p}{k_0T})$

在下图nn’位置出现非平横少子空穴（根据第五章的分析，空穴对应的费米能级应该在电子的下面）因为n型区的电子浓度占多数，所以可以忽略电子浓度的变化，电子对应的准费米能级可以看作不变；而价带空穴由于注入所以其浓度变化很大，并且其费米能级位置随着空穴浓度变化而变化，由于空穴一边扩散一边复合，因此其浓度是减小的，根据上面的公式，空穴对应的准费米能级应该是慢慢增大，一直到$\Delta p =\Delta n= 0$​，此时电子空穴对应的费米能级再次重合，而根据载流子的稳态扩散方程，此时的准费米能级应该是成直线增大

由于耗尽层的载流子的浓度很小，根据耗尽层近似，可以认为没有载流子，因为扩散区比势垒区大，因此可以认为此处没有复合产生，所以不管是空穴还是电子对应的费米能级都不发生变化

同理在pp’位置电子向p区进行扩散的过程发生类似的变化

由于加上了一个与自建场相反的电压

<img src="https://typora-1310242472.cos.ap-nanjing.myqcloud.com/typora_img/image-20240603200527120.png" alt="image-20240603200527120" style="zoom:67%;" />









**（2）对于外加电压形成电场与原来的自建场的方向相同的时候（负电压，电场从n指向p，p区接负电压）**

在平衡的时候自建场已经是可以做到p型区扩散多少空穴到n区，自建场给漂移多少空穴从n区到p区回去了，此时n区没有多少空穴，同理p区没有多少电子了

再加上一个与自建场方向相同的电场，其促进p型区的电子向n型区漂移，促进n型区的空穴向p型区漂移，在只有自建场的时候空间电荷区已经没什么了，哪怕再加上一个电场也没有什么可以漂移形成电流了，所以加上一个与自建场方向相同的电场之后pn结中的电流并没有什么变化



