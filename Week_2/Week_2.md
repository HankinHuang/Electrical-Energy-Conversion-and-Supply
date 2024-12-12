# Power Electronic Devices

## Overview

- Overview of power electronic devices
- Description of different devices
  - Diode
  - Thyristor
  - IGBT/MOSFET

- Devices vs. operating range and applications

## Power Electronic Devices (Switches)
- Semiconductor devices in the context of power conversion in electrical systems. Power Electronics plays a very important role in the electrical power conversion and is widely used in transportation, renewable energy and utility applications.
- By 2030, 80% of electrical power will go through power electronics converters somewhere between generation, transmission, distribution and consumption [1].
- High power (e.g. 100W ~ 300 kW), high voltage (e.g. 600V), high current (e.g. 50A)

## What should a switch do?
- Off-state
  - Switch is turned off and blocks current
  - Large voltage blocked by the switch
- On-state
  - Switch is turned ON and conducts current
  - Very small voltage across the switch
- Switching transition
  - The transitional state between ON and OFF
  - Turn-on process and Turn-off process

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
在通用功率半导体器件中,理想情况下,我们会尝试立即打开和关闭它![1](C:\Users\const\Documents\GitHub\Electrical-Energy-Conversion-and-Supply\Week_2\images\1.png)

- A real power device cannot turn on and off instantaneously
  真正的电源设备不能瞬间打开和关闭
- The voltage needs some time to fall and the current takes some time to rise at turn-on
  电压需要一些时间下降,电流需要一些时间在导通时上升

### Switching losses
- The instantaneous turn-on power dissipation is: $P_{SWON }=i_{A}(t) v_{A B}(t)$
瞬时开启功率耗损为:$P_{SWON }=i_{A}(t) v_{A B}(t)$
- The instantaneous turn-off power dissipation is: $P_{SWOFF }=i_{A}(t) v_{A B}(t)$ 
瞬时关断功率耗损为:$P_{SWOFF }=i_{A}(t) v_{A B}(t)$ 
$E_{o n}=\int_{T_{1}}^{T_{1}+t_{1}} i_{A} v_{A B} d t E_{o f f}=\int_{T_{2}}^{T_{2}+t_{2}} i_{A} v_{A B} d t$

### Switching Losses
- Current and voltage rise and fall trajectories are rarely straight lines • Turn-on and turn-off losses are not identical
转换损失 ･电流和电压上升和下降轨迹很少是直线 ･开机和关机损耗不完全相同

### Types of common power devices
- Passive
  - Diode
- Half-controlled
  - Thyristor
- Fully-controlled
  - IGBT MOSFET

### Power Diode
- A power diode is identical to small signal diodes but are designed for higher voltage and current
Anode A Cathode K
- The basic device consists of a p-n junction
ply n-type O
Anode silicon Cathode
Anode Cathode

### Ideal vs. Real diodes
- Ideal diode
  - Reverse biased
  - Forward biased
- Real diode
  - Current
  - Voltage 0.8 – 1 V
  - Higher “turn on” voltage compared to small-signal
  - Reverse leakage current
  - Reverse Breakdown

### Thyristor
- Similar in function to the power diode
- Additional terminal called the gate.
- A thyristor will conduct if
  - forward biased
  - small current is introduced into the gate terminal
- Once the thyristor is conducting, the gate terminal serves no further function
- The device will turn off when the AK current drops below a holding current – no control from gate
晶闸管
- 功能类似于功率二极管 ･称为门的附加终端｡
- 如果晶闸管 - 正向偏置 - 将小电流引入栅极端子 ･一旦晶闸管导通,栅极端子不再起作用
- 当AK电流低于保持电流时,设备将关闭 —— 栅极无法控制

### Thyristor
- The device will turn off when the AK current drops below a holding current
- Commonly in high-power current-source converters (e.g. HVDC systems)
- Thyristors are currently available at ratings up to 5000A, 12000V
･当AK电流低于保持电流时,设备将关闭
･通常用于大功率电流源转换器(例如HVDC系统)
･晶闸管目前的额定电压高达5000A､12000V

### MOSFET
- Metal–Oxide–Semiconductor (MOS) Field-Effect Transistor (FET)
- Resistive on-state characteristic, represented by $R_{D S(o n)}$
- Applications both in digital circuits and power applications due to ability of fast switching
G
S
- $i R = dV di$
- $P_{on }=i_{D}^{2} R_{D S(o n)}$
- $V_{D S}=i_{D} \cdot R_{D S(o n)}$金属氧化物半导体(MOS)场效应晶体管(FET)
电阻导通特性,由$R_{DS (on) }$表示
由于具有快速切换能力,在数字电路和电源应用中的应用

### Insulated Gate Bipolar Transistor (IGBT)
- Most common Silicon-based power device today
- Widely used in
  - Variable Frequency Drives
  - EVs, electrified trains
  - Refrigerators and air conditioners
- $V_{C E}=V_{F W 0}+i \cdot R_{o n}$ 
- $P_{on }=i \cdot V_{C E}$

### Ideal vs. Real active switching devices
- ON-State Characteristics of Ideal Switch
  - Low on-state forward voltage drop and resistance
  - It must have the ability to carry infinite high forward current
- Off-State Characteristics of the Ideal Switch
  - Withstand high reverse & forward voltage
  - Low leakage current (zero leakage current)
  - High off-state resistance (infinite off-state resistance)
- Characteristics during the Transition Process
  - Low delay time approaches to zero
  - Low rise time approaches to zero
  - Low storage time approaches to zero
  - Low fall time approaches to zero
  理想与实际有源开关器件
- 理想开关的ON状态特性
  - 低通态正向压降和电阻
  - 它必须有能力携带无限高的正向电流 -
- 理想开关的OFF状态特性
  - 承受高反向和正向电压
  - 低泄漏电流(零泄漏电流)
  - 高断态电阻(无限断态电阻)
- 转型过程中的特点
  - 低延迟时间接近零
  - 低上升时间接近零
  - 低存储时间接近零
  - 低坠落时间接近零

### Gate driving of a power device (e.g. MOSFET)
- CONTROL CIRCUIT Low-power Logic signal V: e.g. 0/3.3V I: e.g. 200 μA
控制电路 低功率逻辑 信号 电压:例如0/3.3伏 电流:例如200微安
- Switch a high voltage/current
Small gate signal
- Gate Driving Circuit Interface low/high end V: e.g. -5/+20V I: e.g. 1 A栅极驱动电路 高低端接口 电压:例如 -5/+20伏 电流:例如1安培
- $V = 800V$
Main power circuit
HIGH POWER
Large V: e.g. 800 V
Large I: e.g. 300 A
$V$
+20V
$V$
3.3V
−5 V
D
0 V
$V$
+800V
G
0 V
S

### Summary
- Passive
  - Diode
- Half-controlled
  - Thyristor
- Fully-controlled
  - MOSFET IGBT

### Summary – properties of power switches
- Rating
  - Max blocking voltage – e.g. 1200 V
  - Max current (continuous) – e.g. 100A
- Conduction characteristic
  - On-state resistance • Forward voltage drop
- Switching characteristic
  - Turn-on and Turn-off loss • Switching speed (e.g. 100 ns to turn on)
- 评级 ･最大阻断电压 - 例如1200 V ･最大电流(连续)- 例如100A - 导电特性 ･导通电阻 ･正向压降 - 开关特性 ･开启和关闭损耗 ･开关速度(例如100 ns开启)

### Maximum Ratings (T.=25Cunles otherwise)
| Symbol | Parameter | Value | Unit |
| --- | --- | --- | --- |
| Vm | Drain-Source Votage | 1200 | V |
| Vc | Gate-Source Voltage (dymamic) | -8/+19 | V |
| Vbe | Gate-Source Voltage (static) | -4/+15 | V |
|  | Continuous Drain Current | 81 | A |
| 56 |
|  | Pulsed Drain Current | 200 |  |

### Summary – losses in power switches
- Turn-on energy loss, EON Device power dissipation,PD Turn-offenergy loss,EoFF
v(t) ILOAD ·Voc
OFF ON OFF
0 i(t)
Turn-on Conduction Energy Turn-off

### Third generation semiconductors – GaN and SiC
- Switch faster
- Lower switching loss
- Higher thermal conductivity and operating temperature
第三代半导体 - GaN和SiC
- 切换更快
- 降低开关损耗
- 更高的导热系数和工作温度

### Gallium Nitride (GaN) FETs
- GON

### Silicon Carbide (SiC) FETs

### Switching power device application space
- HC-supplier HVDC Application 1G1 Power by application (W) Future Scenario Power Electronics ULTRA HIGH POWER
  - >Large drives >Locomotives Ships 100M 10M HIGH POWER
  - >Large solar plants >Trams,buses 1M IGBT
  - >Electric cars >On-roof PV >Small drives >Air conditioner 100k 10k SiC MID POWER
  - >Robotics GaN
  - >Washing machine 1k
  - SMPS Chargers/Adapters 100 "Degree of adoption depends strongly on Cost 10 10 BJT 100 1k MOSFET 10k 100k 1M Reduced size 10M Frequency (Hz) LOW POWER 100M

### Task
- In which cases below it leads to higher switching loss
  - A. Higher switching speed - switch faster
  - B. Higher switching frequency – switch more times per second
  - C. Switch a higher voltage
  - D. Switch a higher current
  在哪些情况下,会导致更高的开关损耗
  - A. 更高的切换速度 - 切换更快
  - B. 更高的开关频率 - 每秒切换更多次
  - C. 切换更高的电压
  - D. 切换更高的电流
- How is a diode turned off?
  - A. A current is applied to the gate terminal
  - B. The device is forward biased
  - C. A positive voltage is applied across the gate-emitter terminals
  - D. The device is reverse biased
  - E. A current is drawn from the gate terminal
  二极管如何关闭?
  - A. 电流施加到栅极端子
  - B. 装置正偏
  - C. 在栅极发射极端子上施加正电压
  - D. 装置反向偏置
  - E. 从栅极端子引出电流
- Which of these is not a requirement for a power electronic device?
  - A. Able to switch between on and off states easily
  - B. Be able to withstand the applied voltage when in blocking mode
  - C. Store energy in the device control terminal
  - D. Ensure minimal power dissipation in both on and off states
  - E. Handle a high power in the gate terminal
  哪些不是电力电子设备的要求?
  - A. 能够轻松地在打开和关闭状态之间切换
  - B. 在阻塞模式下能够承受施加的电压
  - C. 将能量存储在设备控制终端中
  - D. 确保开启和关闭状态下的功率耗损最小
  - E. 处理栅极端子中的大功率

### Further reading
- PN Junction Diode https://www.electronics-tutorials.ws/diode/diode_3.html
- Thyristor https://www.electronics-tutorials.ws/power/thyristor.html
- IGBT https://www.electronics-tutorials.ws/power/insulated-gate-bipolartransistor.html
- MOSFET https://www.electronics-tutorials.ws/transistor/tran_6.html