# Power Electronic Devices 电力电子器件

## Overview

- Overview of power electronic devices
- Description of different devices
  - Diode
  - Thyristor
  - IGBT/MOSFET

- Devices vs. operating range and applications

## Power Electronic Devices (Switches) 电力电子器件（开关）
- Semiconductor devices in the context of power conversion in electrical systems. Power Electronics plays a very important role in the electrical power conversion and is widely used in transportation, renewable energy and utility applications. 

  电力系统中电力转换背景下的半导体器件。电力电子在电力转换中起着非常重要的作用，广泛应用于交通运输、可再生能源和公用事业应用。

- By 2030, 80% of electrical power will go through power electronics converters somewhere between generation, transmission, distribution and consumption. 

  到2030年，80%的电力将在发电、输电、配电和消费之间通过电力电子转换器。

- High power (e.g. 100W ~ 300 kW), high voltage (e.g. 600V), high current (e.g. 50A) 

  大功率（例如100W~300 kW）、高电压（例如600V）、大电流（例如50A）

## What should a switch do? 开关应该做什么？
- Off-state 关态
  - Switch is turned off and blocks current 开关关闭并阻止电流
  - Large voltage blocked by the switch 开关阻断的大电压
- On-state 开态
  - Switch is turned ON and conducts current 开关接通并导通电流
  - Very small voltage across the switch 开关两端电压非常小
- Switching transition 切换过渡
  - The transitional state between ON and OFF ON和OFF之间的过渡状态
  - Turn-on process and Turn-off process 开启过程和关闭过程

## Power Semiconductor Device Layout 功率半导体器件布局
- Most power devices have a control electrode (C here) as well as the power electrodes (A and B), except for the diode.
大多数功率器件都有一个控制电极(这里是C)以及功率电极(A和B),但二极管除外｡
- A small current or voltage (e.g. 15V) applied to C turns the device either ON or OFF
施加在C上的小电流或电压(例如15V)会打开或关闭设备

## Power Semiconductor Losses 功率半导体损耗
- Losses can be broken down in 3 parts: 损失可以分为三个部分: 
  - On-state (conduction) losses 状态(传导)损失
  - Off-state losses – leakage current 关态损耗 - 泄漏电流
  - Switching losses – turn-on and turn-off transient 开关损耗 - 开启和关闭瞬态
- Off-state losses normally neglected in modern devices 现代设备中通常被忽视的非状态损耗

## Conduction Losses
- The supply voltage is $V_{s}$ and the current conducted in the steady-state when the switch is fully on is given by $LOAD$.
电源电压为$V_{s}$,开关全开时稳态导通的电流I由$LOAD$给出.
- When on, the conduction loss, $P_{c}$ is given by:
打开时,传导损失$P_{c}$为:$P_{c}=I_{L O A D} v_{A B}(o n)$
- A “good” power device is therefore designed to minimise $v_{A B}(o n)$
因此,一个 “好” 的电源开关设备旨在最大限度地减少$v_{AB}(on)$

## Switching Losses
- In a generic power semiconductor device we would try to turn it on and off instantaneously ideally
在通用功率半导体器件中,理想情况下,我们会尝试立即打开和关闭它

- A real power device cannot turn on and off instantaneously
  真正的电源设备不能瞬间打开和关闭
  $$
  E_{o n}=\int_{T_{1}}^{T_{1}+t_{1}} i_{A} v_{A B} d t
  $$
  
  $$
  E_{o f f}=\int_{T_{2}}^{T_{2}+t_{2}} i_{A} v_{A B} d t
  $$
  
- The voltage needs some time to fall and the current takes some time to rise at turn-on
  电压需要一些时间下降,电流需要一些时间在导通时上升

- The instantaneous turn-on power dissipation is: $P_{SWON }=i_{A}(t) v_{A B}(t)$
  瞬时开启功率耗损为:$P_{SWON }=i_{A}(t) v_{A B}(t)$

- The instantaneous turn-off power dissipation is: $P_{SWOFF }=i_{A}(t) v_{A B}(t)$ 
  瞬时关断功率耗损为:$P_{SWOFF }=i_{A}(t) v_{A B}(t)$ 

- Current and voltage rise and fall trajectories are rarely straight lines 

  电流和电压上升和下降轨迹很少是直线

- Turn-on and turn-off losses are not identical
开机和关机损耗不完全相同

## Types of common power devices 常见功率器件的类型
- Passive 被动式的
  - Diode 二极管
- Half-controlled 半控制的
  - Thyristor 半导体晶闸管
- Fully-controlled 完全控制的
  - IGBT 绝缘栅双极晶体管
  - MOSFET 金属氧化物半导体场效应晶体管

## Power Diode 功率二极管
- A power diode is identical to small signal diodes but are designed for higher voltage and current 

  金属氧化物半导体场效应晶体管

  - Anode A 阳极A 
  - Cathode K 阴极K

- The basic device consists of a p-n junction 基本器件由一个 p-n 结组成 

  - Anode -- p-type silicon -- n-type silicon -- Cathode 

    阳极--p型硅--n型硅--阴极

  - Anode -- Cathode

    阳极--阴极


## Ideal vs. Real diodes 理想与实际二极管
### Ideal Diode（理想二极管）

- Anode (A) and Cathode (K)（阳极和阴极）: 

  The ideal diode has two terminals, the anode (A) and the cathode (K). 

  理想二极管有两个端子，阳极（A）和阴极（K）。

- Reverse Biased（反向偏置）: 

  When the diode is reverse - biased, a voltage $V_D$ is applied with the positive terminal connected to the cathode and the negative terminal connected to the anode. In an ideal diode, no current ($I_D = 0$) flows through the diode in the reverse - biased state. 

  当二极管反向偏置时，电压$V_D$，正极连接阴极，负极连接阳极。在理想的二极管中，在反向偏置状态下没有电流（$I_D=0$）流过二极管。 

- Forward Biased（正向偏置）: 

  When the diode is forward - biased, the voltage $V_D$ is applied with the positive terminal connected to the anode and the negative terminal connected to the cathode. In an ideal diode, current ($I_D$) flows through the diode with zero voltage drop across it ($V_D=0$) in the forward - biased state. 

  当二极管正向偏置时，电压$V_D$，正极连接阳极，负极连接阴极。在理想的二极管中，电流（$I_D$）流过二极管，在正向偏置状态下，二极管两端的压降为零（$V_D=0$）。

### Diode with $V_{FWO}$（具有正向导通电压$V_{FWO}$的二极管）

- Anode (A) and Cathode (K)（阳极和阴极）: 

  Similar to the ideal diode, this diode also has an anode (A) and a cathode (K). 

  与理想二极管类似，该二极管也具有阳极（A）和阴极（K）。

- Reverse Biased（反向偏置）: 

  When reverse - biased, a voltage $V_D$ is applied with the positive terminal connected to the cathode and the negative terminal connected to the anode. In this state, a very small leakage current may flow, but it is often negligible. There is a small voltage drop of $0.7V$ across the diode due to the diode's physical properties.  

  当反向偏置时，电压$V_D$，正极连接阴极，负极连接阳极。在这种状态下，可能会流过非常小的漏电流，但通常可以忽略不计。由于二极管的物理特性，二极管两端有0.7V$的小电压降。

- Forward Biased（正向偏置）: 

  When forward - biased, the voltage $V_D$ is applied with the positive terminal connected to the anode and the negative terminal connected to the cathode. In this state, current ($I_D$) flows through the diode, and there is a constant forward voltage drop ($V_{FWO} = 0.7V$) across the diode. 
  
  当正向偏置时，电压$V_D$与阳极连接的正端和阴极连接的负端一起施加。在这种状态下，电流（$I_D$）流过二极管，二极管两端有恒定的正向压降（$V_{FWO}=0.7V$）。

### Diode with $V_{FWO}$ and Loss（具有正向导通电压$V_{FWO}$和损耗的二极管）

- **Anode (A) and Cathode (K)（阳极和阴极）**: 

  This diode also has an anode (A) and a cathode (K). 

  该二极管还具有阳极（A）和阴极（K）。

- **Reverse Biased（反向偏置）**: 

  When reverse - biased, a voltage $V_D$ is applied with the positive terminal connected to the cathode and the negative terminal connected to the anode. Similar to the diode with $V_{FWO}$, there is a small voltage drop of $0.7V$ across the diode due to its physical properties. 

  当反向偏置时，电压$V_D$，正极连接阴极，负极连接阳极。与具有$V_{FWO}$的二极管类似，由于其物理特性，二极管两端有$0.7V$的小电压降。

- **Forward Biased（正向偏置）**: 

  When forward - biased, the voltage $V_D$ is applied with the positive terminal connected to the anode and the negative terminal connected to the cathode. In this state, current ($I_D$) flows through the diode, and there is a forward voltage drop ($V_{FWO} = 0.7V$) across the diode. Additionally, there is a series resistance ($R_D$) associated with the diode, which causes a voltage drop ($I_D\times R_D$) in the forward - biased state, contributing to power loss in the diode. 

  当正向偏置时，电压$V_D$与连接阳极的正端子和连接阴极的负端子一起施加。在这种状态下，电流（$I_D$）流过二极管，二极管两端有一个正向压降($V_{FWO} = 0.7V$)。此外，二极管还有一个串联电阻（$R_D$），这会在正向偏置状态下导致压降($I_D\times R_D$)，导致二极管的功率损失。 
  

This diagram illustrates the current - voltage characteristic curve of a real diode. Here are the key elements in the figure: 

这张图展示了实际二极管（Real diode）的电流 - 电压特性曲线。以下是图中的关键元素：

1. **Title**:
   
   - "Real diode", indicating that this is the characteristic curve of an actual diode. 
   - “Real diode”，表示这是实际二极管的特性曲线。
   
2. **Axes**:
   
   - Voltage, measured in volts (V). 电压（Voltage），单位是伏特（V）
   - Current, measured in amperes (A). 电流（Current），单位是安培（A）
   
3. **Curve Features**:
   
   - The curve shows the current characteristics of the diode at different voltages. 
   
     曲线显示了二极管在不同电压下的电流特性

   - In forward bias, when the voltage reaches 0.8 - 1 V, the diode starts to conduct, and the current increases rapidly. This "turn - on voltage" is marked in red in the figure (Higher “turn on” voltage compared to small - signal). 
   
     在正向偏置（Forward bias）时，电压达到0.8 - 1 V时，二极管开始导通，电流迅速增加。图中用红色标注了这个“开启电压”（Higher “turn on” voltage compared to small - signal）。
   
   - In reverse bias, the diode has a small reverse leakage current, marked in green. 
   
     在反向偏置（Reverse bias）时，二极管有一个很小的反向漏电流（Reverse leakage current），用绿色标注。
   
   - When the reverse voltage reaches a certain value, the diode undergoes reverse breakdown, and the reverse breakdown voltage ($V_{rrm}$) is marked in green in the figure. 
   
     当反向电压达到一定值时，二极管会发生反向击穿（Reverse Breakdown），图中用绿色标注了反向击穿电压（$V_{rrm}$）。
   
4. **Annotation Descriptions**:
   
   - The figure uses arrows and text of different colors to annotate several key characteristics of the diode: 
   
     图中用不同颜色的箭头和文字标注了二极管的几个关键特性：
   
     - The red arrow and text mark the turn - on voltage (0.8 - 1 V) in forward bias. 
   
       红色箭头和文字标注了正向偏置时的开启电压（0.8 - 1 V）。
   
     - The green arrow and text mark the reverse leakage current (Reverse leakage current) and the reverse breakdown voltage ($V_{rrm}$). 
   
       绿色箭头和文字标注了反向漏电流（Reverse leakage current）和反向击穿电压（$V_{rrm}$）。

Real diodes are different from ideal diodes. They have a turn - on voltage in forward bias, and there is a possibility of reverse leakage current and reverse breakdown in reverse bias. These characteristics need to be considered when designing and using diodes. 

实际二极管与理想二极管不同，它在正向偏置时有一个开启电压，并且在反向偏置时有反向漏电流和反向击穿的可能性。这些特性在设计和使用二极管时需要考虑。

## Thyristor 晶闸管
- Similar in function to the power diode 功能类似于功率二极管
- Additional terminal called the gate. 称为门的附加终端
- A thyristor will conduct if 如果晶闸管
  - forward biased - 正向偏置
  - small current is introduced into the gate terminal - 将小电流引入栅极端子
- Once the thyristor is conducting, the gate terminal serves no further function 一旦晶闸管导通,栅极端子不再起作用
- The device will turn off when the AK current drops below a holding current – no control from gate 当AK电流低于保持电流时,设备将关闭 —— 栅极无法控制

- The device will turn off when the AK current drops below a holding current 当AK电流低于保持电流时,设备将关闭
- Commonly in high-power current-source converters (e.g. HVDC systems) 通常用于大功率电流源转换器(例如HVDC系统)
- Thyristors are currently available at ratings up to 5000A, 12000V 晶闸管目前的额定电压高达5000A､12000V

## MOSFET

- Metal–Oxide–Semiconductor (MOS) Field-Effect Transistor (FET) 金属氧化物半导体(MOS)场效应晶体管(FET)
- Resistive on-state characteristic, represented by $R_{D S(o n)}$ 电阻导通特性,由$R_{DS (on) }$表示
- Applications both in digital circuits and power applications due to ability of fast switching 由于具有快速切换能力,在数字电路和电源应用中的应用
- $R_{DS(on)}= \frac{dV_{DS}}{di_{D}}$
- $P_{on }=i_{D}^{2} R_{D S(o n)}$
- $V_{D S}=i_{D} \cdot R_{D S(o n)}$

## Insulated Gate Bipolar Transistor (IGBT) 绝缘栅双极晶体管（IGBT）

- Most common Silicon-based power device today 当今最常见的硅基电源设备
- Widely used in 广泛用于
  - Variable Frequency Drives 变频驱动器
  - EVs, electrified trains 电动汽车、电气化列车
  - Refrigerators and air conditioners 冰箱和空调
- $V_{C E}=V_{F W 0}+i \cdot R_{o n}$ 
- $P_{on }=i \cdot V_{C E}$

## Ideal vs. Real active switching devices 理想与实际有源开关器件
- ON-State Characteristics of Ideal Switch 理想开关的ON状态特性
  - Low on-state forward voltage drop and resistance 低通态正向压降和电阻
  - It must have the ability to carry infinite high forward current 它必须有能力携带无限高的正向电流
- Off-State Characteristics of the Ideal Switch 理想开关的OFF状态特性
  - Withstand high reverse & forward voltage 承受高反向和正向电压
  - Low leakage current (zero leakage current) 低泄漏电流(零泄漏电流)
  - High off-state resistance (infinite off-state resistance) 高断态电阻(无限断态电阻)
- Characteristics during the Transition Process 转型过程中的特点
  - Low delay time approaches to zero 低延迟时间接近零
  - Low rise time approaches to zero 低上升时间接近零
  - Low storage time approaches to zero 低存储时间接近零
  - Low fall time approaches to zero 低坠落时间接近零

## Gate driving of a power device (e.g. MOSFET) 功率器件（例如 MOSFET）的栅极驱动
CONTROL CIRCUIT 控制电路

Low-power Logic signal 
低功率逻辑信号 

V: e.g. 0/3.3V I: e.g. 200 μA 
电压:例如0/3.3伏 电流:例如200微安

- Switch a high voltage/current 切换高电压/电流 

- Small gate signal 小栅极信号

- Gate Driving Circuit Interface low/high end 栅极驱动电路接口低/高端 

e.g. V: -5/+20V I: 1 A 
例如.  电压-5/+20V 电流1A

Main power circuit
HIGH POWER
Large V: e.g. 800 V
Large I: e.g. 300 A

## Summary – properties of power switches 总结-电源开关的特性
- Rating 评级
  - Max blocking voltage – e.g. 1200 V 最大阻断电压 - 例如1200V
  - Max current (continuous) – e.g. 100A 最大电流(连续)- 例如100A
- Conduction characteristic 导电特性
  - On-state resistance 导通电阻
  - Forward voltage drop 正向压降
- Switching characteristic 开关特性
  - Turn-on and Turn-off loss 开启和关闭损耗
  - Switching speed (e.g. 100 ns to turn on) 开关速度(例如100ns开启)

一个关于MOSFET的最大额定值（Maximum Ratings）和开关损耗（Switching Loss）的图表

**图表数据**

   - 横轴表示漏到源电流（$I_{DS}$），单位为安培（A），范围从0到100 A。
   - 纵轴表示钳位电感开关能量（$E_{sw}$），单位为毫焦耳（mJ），范围从0到12 mJ。
   - 图中有两条曲线，分别标记为 $E_{on}$（开启能量）和 $E_{off}$（关闭能量），随着漏电流的增加，这两条曲线显示出开关能量的增加趋势。

这张图片提供了电子元件在特定条件下的最大额定值和开关损耗特性，对于电路设计和元件选型非常重要。

## Summary – losses in power switches 总结-电源开关的损耗

一个功率器件在开关过程中的能量损耗和功率耗散情况。主要分为三个部分：
开启能量损耗（Turn - on energy loss, $E_{ON}$）、器件功率耗散（Device power dissipation, $P_D$）和关闭能量损耗（Turn - off energy loss, $E_{OFF}$）。

1. **电压和电流波形**
   - 在图的上方，有两条波形图，分别表示电压（v(t)）和电流（i(t)）随时间的变化。
   - 电压波形（v(t)）在开启和关闭过程中有明显的变化，而在导通（ON）期间保持相对稳定。
   - 电流波形（i(t)）在开启和关闭过程中也有明显的变化，而在导通（ON）期间保持相对稳定。
2. **开启能量损耗（$E_{ON}$）**
   - 在图的左侧，有一个三角形区域，表示开启能量损耗（$E_{ON}$）。
   - 这个区域由电压和电流波形在开启过程中的变化所围成。
3. **器件功率耗散（$P_D$）**
   - 在图的中间，有一个矩形区域，表示器件功率耗散（$P_D$）。
   - 这个区域由电压和电流波形在导通期间的稳定值所围成。
4. **关闭能量损耗（$E_{OFF}$）**
   - 在图的右侧，有一个三角形区域，表示关闭能量损耗（$E_{OFF}$）。
   - 这个区域由电压和电流波形在关闭过程中的变化所围成。

通过电压和电流波形以及相应的能量损耗区域，直观地展示了功率器件在开启、导通和关闭过程中的能量损耗和功率耗散情况。这些信息对于设计和分析功率电子电路非常重要。

## Third generation semiconductors – GaN and SiC 第三代半导体 - GaN和SiC
- Switch faster 切换更快
- Lower switching loss 降低开关损耗
- Higher thermal conductivity and operating temperature 更高的导热系数和工作温度

Gallium Nitride (GaN) FETs 氮化镓（GaN）FET 

Silicon Carbide (SiC) FETs碳化硅（SiC）FET

## Switching power device application space 开关功率器件应用空间

不同功率电子器件在未来各种应用中的使用场景。

1. **应用（Application）**
   - 列出了各种应用场景，包括：
     - 高压直流输电（HVDC）
     - 大容量供电（HC - supplier）
     - 大型驱动器（Large drives）
     - 船舶（Ships）
     - 机车（Locomotives）
     - 大型太阳能电站（Large solar plants）
     - 有轨电车和公交车（Trams, buses）
     - 电动汽车（Electric cars）
     - 屋顶光伏发电（On - roof PV）
     - 小型驱动器（Small drives）
     - 空调（Air conditioner）
     - 机器人（Robotics）
     - 洗衣机（Washing machine）
     - 开关电源（SMPS）
     - 充电器/适配器（Chargers/Adapters）

### 具体功率电子场景
- 将不同功率范围分为几个区间：
  - 超高压（ULTRA HIGH POWER）：>100M W
  - 高压（HIGH POWER）：10M - 100M W
  - 中压（MID POWER）：100k - 10M W
  - 低压（LOW POWER）：100 - 100k W

- 以及频率（Frequency），范围从10 Hz到100M Hz。

**不同器件的应用区域**

- **晶闸管（Thyristor）**：主要应用于超高压和高压范围，频率较低。
- **绝缘栅双极晶体管（IGBT）**：适用于高压和中压范围，频率适中。
- **碳化硅（SiC）**：主要应用于中压和低压范围，频率较高。
- **氮化镓（GaN）**：适用于低压范围，频率较高，且标注有“减小尺寸（Reduced size）”。
- **双极结型晶体管（BJT）**：主要应用于低压范围，频率较低。
- **金属 - 氧化物 - 半导体场效应晶体管（MOSFET）**：适用于低压和中压范围，频率较高。

### 总结
不同功率电子器件在未来各种应用中的适用范围，考虑了功率需求和频率需求，并强调了成本对这些器件采用程度的影响。

## Task
- In which cases below it leads to higher switching loss 在哪些情况下,会导致更高的开关损耗
  
  Higher switching frequency – switch more times per second 更高的开关频率 - 每秒切换更多次
  
- How is a diode turned off? 二极管如何关闭？
  
  - The device is reverse biased 装置反向偏置
  
- Which of these is not a requirement for a power electronic device? 哪些不是电力电子设备的要求?
  - Store energy in the device control terminal 将能量存储在设备控制终端中
  - Handle a high power in the gate terminal 处理栅极端子中的大功率

## Further reading
- PN Junction Diode https://www.electronics-tutorials.ws/diode/diode_3.html
- Thyristor https://www.electronics-tutorials.ws/power/thyristor.html
- IGBT https://www.electronics-tutorials.ws/power/insulated-gate-bipolartransistor.html
- MOSFET https://www.electronics-tutorials.ws/transistor/tran_6.html