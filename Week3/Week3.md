# 交流理论（AC Theories）

## 概述

1. 什么是交流电以及为什么使用交流电？交流电与直流电的比较（What is and why AC? AC vs. DC?）
2. 正弦波的定义（sine wave definitions）
   - 理想和实际波形（Ideal and real waveforms）
   - 谐波和傅里叶分析（Harmonics and Fourier analysis）
3. 周期波形的平均值和均方根值（Average and RMS for periodic waveform）

## 交流电VS.直流电

为什么要使用交流电（AC）

### 1. 变压器（Transformer）

- 变压器能够轻松地升高电压。
- 通过升高（↑）和降低（↓）电压，可以减少输电过程中的电阻损耗（I²R）。
- 变压器提供了电流隔离（Galvanic isolation）。

变压器的有：初级线圈（Primary Supply）、次级线圈（Secondary Load）、变压器铁芯（Transformer Core）、初级匝数（N_PRIMARY turns）和次级匝数（N_SECONDARY turns）。

### 2. 零交叉点（Zero - crossing point）
- 交流电有零交叉点（零区域处），这使得断路器更容易操作。

### 3. 交流电机（AC machines）
- 交流电机无需电刷（Brushless），因此更加耐用。
- 交流电机有旋转磁场（Rotating field）。

交流电机的转子（Rotor core sections、Bar wound wire、Bearing support assembly、Magnets、Steel plate、Rotor hub、转子铁心部分、条形绕组线、轴承支撑组件、磁铁、钢板、转子轮毂）和定子（Stator core）

## 理想变压器（Ideal Transformer in AC Systems）

### 主要内容包括：
1. **电压（Voltage）**
   - 变压器根据匝数比（turns ratio）升高或降低电压。
   - 电压关系公式：
     $$
     \frac{e_1(t)}{e_2(t)} = \frac{N_1}{N_2}
     $$
     其中，$e_1(t)$ 和 $e_2(t)$ 分别是初级和次级电压，$N_1$ 和 $N_2$ 分别是初级和次级线圈的匝数。

2. **电流（Current）**
   - 电流与匝数比成反比。
   - 电流关系公式：
     $$
     \frac{i_1(t)}{i_2(t)} = \frac{N_2}{N_1}
     $$
     其中，$i_1(t)$ 和 $i_2(t)$ 分别是初级和次级电流。

- 初级线圈（$N_1$ 匝）和次级线圈（$N_2$ 匝）。
- 初级电压 $e_1(t)$ 和次级电压 $e_2(t)$。
- 初级电流 $i_1(t)$ 和次级电流 $i_2(t)$。
- 磁芯（Core）和磁通量（$\phi$）。

3. **类比（Analogy）**

   - 变压器可以被看作是一个电气“齿轮箱。

   - 输出功率等于输入功率。

	变压器（Transformer）
	- **结构和原理**
	  - 由初级线圈（Primary Coil）和次级线圈（Secondary Coil）组成。
	  - 当初级线圈匝数多、次级线圈匝数少时，实现降压（Low Voltage）和增流（High Current）的效果，称为“Step - down”变压器。
	  - 当初级线圈匝数少、次级线圈匝数多时，实现升压（High Voltage）和降流（Low Current）的效果，称为“Step - up”变压器。

## 交流电和直流电在发电和输电中的应用 AC and DC in power generation and transmission

### 在发电和输电过程中，交流电（AC）占据主导地位。发电主要依靠交流发电机，而输电则主要依靠高压交流电。不过，在长距离输电的特殊情况下，高压直流电（HVDC）由于其成本优势开始变得更具吸引力。

#### 发电（Power generation）
- **主要内容**：发电主要由交流发电机（AC generators）主导。
  - 一个典型的发电厂的结构，发电厂的主要组件包括：
    - 煤供应（Coal supply）
    - 水供应（Water supply）
    - 锅炉（Boiler）
    - 蒸汽管道（Steam line）
    - 涡轮机（Turbine）
    - 发电机（Generator）
    - 变压器（Transformer）
    - 输电线路（Transmission lines）
  - 光伏（PV）面板产生直流电压。

#### 输电（Power transmission）
**主要内容**：
- 输电主要由高压交流电（HVAC）主导。
  - 右侧的图示展示了一个典型的输电系统，输电系统的主要组件包括：
    - 发电厂（Power Plant）
    - 升压变压器（Step - up）
    - 高压输电线路（High Voltage）
    - 降压变压器（Step - down）
    - 家庭或商业用户（Home or Business）
- 高压直流电（HVDC）用于特殊情况，通过先进的电力电子设备和直流断路器实现。
- 输电距离与成本的关系：
  - 总高压交流电（HVAC）成本随着输电距离增加而增加。
  - 总高压直流电（HVDC）成本在输电距离超过一定值（架空线400-700 km，电缆25-50 km）后开始低于HVAC成本。

## 正弦交流电压和电流（Sinusoidal AC voltage/current）

### 1. 正弦交流电压/电流的特性
- **时变数量和极性（Time - varying quantity and polarity）**
  - 正弦交流电压和电流的大小和极性随时间变化。

### 2. 相关量（Quantities）
- **公式**
  - 电压或电流的表达式为：$v(t) = V_m \sin(\omega t + \theta_0)$
  - 其中：
    - $V_m$ 是振幅（Amplitude），单位为伏特（V）。
    - $\omega$ 是角频率（Angular frequency），单位为弧度/秒（rad/s）。
    - $t$ 是时间（Time），单位为秒（s）。
    - $\theta_0$ 是初始相位角（Initial phase angle），单位为弧度（rad）。

### 3. 时域变量（Time domain variables）
- **角频率（Angular frequency）**
  - 计算公式为：$\omega = 2 \pi f$
  - 其中 $f$ 是频率（Frequency），单位为赫兹（Hz）。
- **周期（Period）**
  - 计算公式为：$T = \frac{1}{f}$

### 4. 正弦交流电压/电流的实际情况
- **实际情况**
  - 由于负载和发电侧的非线性效应，实际的正弦交流电压和电流往往存在缺陷。
    - 波形图存在平顶（Flat top）现象。
    - 波形图在零交叉点（Zero crossing）处存在扭结（Kink）现象。

## 傅里叶级数（Fourier series）

### 1. 傅里叶级数的定义
- 任何周期函数（信号）都可以由无限个正弦和余弦函数（信号）的和来构成。
- 傅里叶级数的公式如下：
  $$
  f(x) = \frac{1}{2} a_0 + \sum_{n=1}^{\infty} a_n \sin(nx)
  $$
  其中：
  
  - $ f(x) $ 是周期函数
  - $ a_0 $、$ a_n $ 是常数
  - $ n $ 是整数

### 2. 傅里叶分析
- 傅里叶分析可以用来确定常数 $ a_n $ 和 $ b_n $ 的值。

- 频率的 $ n $ 个分量被称为谐波，其中第1个谐波通常被称为基波（fundamental），其频率为 $ f_1 = n \cdot f_0 $。

<img src="C:\Users\const\Documents\GitHub\Electrical-Energy-Conversion-and-Supply\Week3\images\1.png" alt="1" style="zoom:50%;" />

- 有一个波形图，展示了不同频率的波形及其合成。
  - 图中显示了基波（Fundamental）、3次谐波（3rd）、5次谐波（5th）和7次谐波（7th）的波形。
  - 这些波形叠加在一起形成了合成波形（Sum）。

### 总结
解释了傅里叶级数的基本概念，即任何周期函数都可以分解为一系列正弦和余弦函数的和，并且通过傅里叶分析可以确定这些分量的系数。图示展示了不同频率的谐波如何叠加形成复杂的波形。

## 电力系统中的谐波（Harmonics）

### 1. 主要内容
- **谐波的存在**
  - 电力系统中存在谐波会导致波形失真。
- **谐波的产生原因**
  - 由非线性负载（例如电力电子设备、变压器）引起。
- **谐波的影响**
  - 增加损耗并降低电力质量。
  - 干扰设备的正常运行。

两种典型的波形失真：
  - **平顶（Flat top）**：波形在峰值处变平，显示出谐波的存在。
  - **零交叉点的扭结（Kink at zero crossing）**：波形在零交叉点处出现不连续，显示出谐波的存在。

### 总结
解释了电力系统中谐波的存在、产生原因及其对电力质量和设备运行的负面影响。谐波主要由非线性负载引起，会导致波形失真，增加损耗并干扰设备的正常运行。

## 快速傅里叶变换（Fast Fourier Transformation，FFT）及其在电力系统中的应用。

### 1. 快速傅里叶变换（FFT）
- **定义**
  - FFT是一种将信号从时域转换到频域的算法（基于傅里叶级数）。
- **操作步骤**
  - 需要输入整数个完整周期。
- **应用**
  - 是分析周期波形的有力工具。
  - 不同的谐波来自各种不同的来源。
  - 高频成分通常与电力电子设备相关。
  - 低频成分可能与发电机故障有关。

### 2. 快速傅里叶变换（FFT）与总谐波失真（THD）
- **定义**
  - 总谐波失真（THD）是衡量信号中谐波含量的指标，越低越好（0%表示无谐波）。
  - 计算公式：$ THD_F = \frac{\sqrt{V_2^2 + V_3^2 + V_4^2 + \cdots}}{V_1} $
- **应用**
  - 通过FFT可以计算THD。

### 3. 图示

<img src="C:\Users\const\Documents\GitHub\Electrical-Energy-Conversion-and-Supply\Week3\images\2.png" alt="2" style="zoom:50%;" />

- 图中显示了一个基波（100 Hz，48.58 V）叠加了高频谐波（5000 Hz，7.90 V）的波形。
- 展示了两个波形图及其对应的FFT分析结果。
  - 左图显示了基波（100 Hz）和一个较小的谐波（FFT结果显示基波为48.58 V，THD为0.00%）。
  - 右图显示了基波（100 Hz）和一个较大的谐波（5000 Hz，7.90 V），FFT结果显示基波为48.58 V，THD为17.57%。

### 总结
介绍了快速傅里叶变换（FFT）的原理、操作步骤和应用，特别是在电力系统中分析谐波的应用。通过FFT，可以将时域信号转换为频域信号，从而更好地分析信号中的谐波成分，并通过计算总谐波失真（THD）来评估信号的质量。

这张图片主要讨论了正弦电压和电流（Sinusoidal voltages and currents）的关系。

## 正弦电压和电流 Sinusoidal voltages and currents

### 主要内容
- 在无源/非开关和线性负载中，正弦电压会产生正弦电流，这是供电系统中的一个重要特性。

<img src="C:\Users\const\Documents\GitHub\Electrical-Energy-Conversion-and-Supply\Week3\images\3.jpg" alt="3" style="zoom:50%;" />

- 图表中展示了电压和电流的波形：
  - 电压波形（蓝色）是一个正弦波，其峰值约为400V和-400V，周期约为20ms。
  - 电流波形（橙色）也是一个正弦波，其峰值约为0.4A和-0.4A，周期同样约为20ms。
- 电压和电流的波形相位相同，即电压达到峰值时，电流也达到峰值。

## 周期波形的平均值（Average value of a periodic waveform）

### 1. 主要内容
- **连续时间变化值（Continuously time varying value of magnitude）**
  - 周期性波形的幅值是随时间连续变化的。
- **平均值公式（The average or mean value formula）**
  - 周期性波形的平均或均值 $ V_{ave} $ 由以下公式给出：
    $ V_{ave}(t) = \frac{1}{T} \int_{0}^{T} v(t) dt $
    其中：
    - $ T $ 是周期。
    - $ v(t) $ 是随时间变化的波形函数。
- **计算 $ V_{ave} $ 示例**
  - 当 $ v(t) = V_m \sin(\omega t) $ 时，计算得出 $ V_{ave} = 0 $。

### 2. 其他周期性波形

- 方形波
- 三角波
- 锯齿波

## 直流波形（DC Waveforms）

- **理想与实际直流波形的差异**
  - 我们通常假设理想的直流波形是一条直线，但实际上通常存在纹波（例如，从电源输出的直流电压）。
- **直流波形的组成**
  - 直流波形可以被认为是直流分量与交流分量叠加而成。
  - 直流波形的公式为：
    $ v(t) = v_0 + V_{m1} \sin(\omega_1 t + \theta_{01}) + \cdots $
    其中：
    - $ v_0 $ 是直流分量。
    - $ V_{m1} \sin(\omega_1 t + \theta_{01}) $ 是交流分量。

<img src="C:\Users\const\Documents\GitHub\Electrical-Energy-Conversion-and-Supply\Week3\images\4.jpg" alt="4" style="zoom:50%;" />

- 图片中包含两个直流波形图：
  - 左侧的图展示了理想的直流波形，是一条水平直线，表示直流电压 $ V_m $。
  - 右侧的图展示了实际的直流波形，是一条带有纹波的直线，表示直流电压 $ v(t) $ 是由直流分量和交流分量叠加而成。

直流波形的特点，强调了实际直流波形通常包含纹波，可以被看作是直流分量与交流分量的叠加。

## 非对称方波（Asymmetric square waveform）

- **定义和应用**
  - 这种波形常见于与供电系统接口的电力电子转换器系统中。
- **占空比（Duty cycle）**
  - 占空比（δ）是电源操作中的一个重要参数，其定义为：
    $$
    \delta = \frac{T_{on}}{T}
    $$
    其中：
    - $ T_{on} $ 是波形处于高电平的时间。
    - $ T $ 是整个波形的周期。

## 非对称方波的平均值（Average of asymmetric square waveform）

- **波形的构成**
  - 这种波形由两个方程构成，分别对应开关打开和关闭时的情况。
  - 当 $ T_{on} = 0 \to \delta T $ 时，$ v_1(t) = V_m $；当 $ T_{off} = \delta T \to T $ 时，$ v_2(t) = 0 $。
- **平均值公式**
  - 非对称方波的平均值公式为：
    $$
    v_{ave}(t) = \frac{1}{T} \left[ \int_{0}^{\delta T} v_1(t) dt + \int_{\delta T}^{T} v_2(t) dt \right] = V_m \delta
    $$
    <img src="C:\Users\const\Documents\GitHub\Electrical-Energy-Conversion-and-Supply\Week3\images\5.png" alt="5"  />

- 展示了非对称方波的基本形状，标注了 $ T_{on} $、$ T_{off} $ 和 $ T $。

## 正弦波的“有用”平均值，均方根值（Root - Mean - Square, RMS）

- **正弦波的平均电流为零**
  - 我们知道，对于一个正弦波，其平均值是零。
- **交流电路中的功率损耗**
  - 但是，在交流电路中电流流动并消耗功率，因此平均值可能并不有用。
- **均方根值（RMS）的定义**
  - 因此，我们定义了均方根值：
    - “电流（或电压）的RMS值与在给定电阻中产生相同热效应的直流电流（或电压）值相同。”
    - 一个10V RMS的交流电压源连接到一个2Ω电阻，电流为5A RMS，功率损耗为50W。
    - 一个10V的直流电压源连接到一个2Ω电阻，电流为5A，功率损耗为50W。
    - 通过相同电阻负载消耗的功率相同。

## 波形的均方根值（Root - Mean - Square value，简称RMS），特别是正弦波形的RMS值

### 1. 正弦波形的描述
- 考虑一个由以下公式描述的正弦波形：
  $$
  v(t) = V_m \sin(\omega t) 
  $$
  其中：
  - $ v(t) $ 是随时间变化的电压。
  - $ V_m $ 是电压的峰值。
  - $ \omega $ 是角频率。
  - $ t $ 是 n   时间。

### 2. 瞬时功率损耗
- 在任意时刻，电阻 \( R \) 上的瞬时功率损耗 \( p(t) \) 由以下公式给出：
  $$
  p(t) = \frac{v(t)^2}{R} = \frac{V_m^2 \sin^2(\omega t)}{R}
  $$

### 3. 波形的均方根值
- 在一个周期 $ T $ 内，电阻上消耗的能量 $ E $ 由以下积分给出：
  $$
  E = \frac{1}{R} \int_{0}^{T} v(t)^2 dt
  $$
- 平均功率损耗 $ P_{\text{ave}} $ 是通过将能量 $ E $ 除以时间间隔 $ T $ 得到的：
  $$
  P_{\text{ave}} = \frac{1}{T} \times \frac{1}{R} \int_{0}^{T} v(t)^2 dt
  $$
  <img src="C:\Users\const\Documents\GitHub\Electrical-Energy-Conversion-and-Supply\Week3\images\6.jpg" alt="6" style="zoom: 67%;" />
- 波形图展示了一个正弦波形 $ v(t) $，标注了峰值 $ V_m $ 和一个周期 $ T $。

### 4. 主要内容
- **均方根值的定义**
  - 根据均方根值的定义：
    $$
    P_{\text{ave}} = \frac{V_{\text{RMS}}^2}{R}
    $$
    其中：
    - $ P_{\text{ave}} $ 是平均功率。
    - $ V_{\text{RMS}} $ 是电压的均方根值。
    - $ R $ 是电阻。
- **公式推导**
  - 通过将上述公式与另一个表示平均功率的公式相等，得到：
    $$
    P_{\text{ave}} = \frac{1}{T} \times \frac{1}{R} \int_{0}^{T} v(t)^2 dt = \frac{V_{\text{RMS}}^2}{R} 
    $$
    由此得出电压的均方根值公式：
    $$
    V_{\text{RMS}} = \sqrt{\frac{1}{T} \int_{0}^{T} v(t)^2 dt}
    $$
- **均方根值的意义**
  - 均方根值是对信号平方的平均值再开方，这样可以消除信号负半周的影响。
  - 均方根值代表了交流电压和电流在电阻上消耗功率的有效值。

## 正弦波的均方根值 RMS value of a sinusoid

### 1. 主要内容
- **计算正弦波的均方根值（V_RMS）**
  - 对于一个由公式 $ v(t) = V_m \sin(\omega t) $ 描述的正弦波，其均方根值（V_RMS）的计算公式为：
    $$
    {RMS} = \sqrt{\frac{1}{T} \int_{0}^{T} v(t)^2 dt} = \frac{V_m}{\sqrt{2}}
    $$
    其中：
    - $ v(t) $是随时间变化的电压。
    - $V_m$是电压的峰值。
    - $\omega$是角频率。
    - $t$是时间。
    - $T$是周期。
  
- **正弦波的瞬时功率损耗**
  - 瞬时功率损耗在每个周期内两次在零和峰值之间摆动。
  - 在50 Hz系统中，功率损耗因此以100 Hz的频率脉动。
  - 从热效应的角度来看，它等同于一个直流信号，其幅值等于交流信号的均方根值。

<img src="C:\Users\const\Documents\GitHub\Electrical-Energy-Conversion-and-Supply\Week3\images\7.jpg" alt="7" style="zoom: 50%;" />

- 最上面的图是正弦波（sin(ωt)）。
- 中间的图是正弦波的平方（sin²(ωt)）。
- 最下面的图是正弦波平方的均方根值（RMS of sin²(ωt)），并标注了其幅值。

## 我们何时使用均方根值 When do we use RMS

- **电力工程中的交流量**
  - 在电力工程中，当我们讨论交流量时，除非另有说明，通常使用的是均方根值（RMS）。
- **英国标准家庭供电电压**
  - 标准的英国家庭供电电压为230V，这里的230V指的是均方根值（RMS）。
- **峰值电压与绝缘考虑**
  - 需要注意峰值电压，特别是在考虑绝缘时。

这张图片提出了一个问题并给出了答案。

### 为什么正弦波形的平均值等于零？ Why is the average of a sinusoidal waveform equal to zero?

1. **正弦波在一个周期内的积分等于零**
   - 数学上，正弦函数在一个完整周期内的积分结果为零。这意味着在一个周期内，正弦波在正半轴和负半轴的面积相互抵消。
2. **波形在起点和终点处为零**
   - 正弦波在一个周期的起点和终点处的值为零，这表明波形在一个周期内是完整的，没有额外的偏移。
3. **周期性波形的平均值总是零**
   - 所有周期性波形，由于其周期性和对称性，其平均值为零。
4. **x轴上方和下方的面积相等**
   - 正弦波在x轴上方和下方的面积相等。当计算平均值时，这些相等的正负面积相互抵消，导致平均值为零。
