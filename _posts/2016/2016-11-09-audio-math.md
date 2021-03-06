---
layout: post
title: "音频的一些性质和数学表示"
description: "音频的一些性质和数学表示"
category: audio
tags: [audio]
---

&#160; &#160; &#160; &#160;最近突然对音频处理感兴趣，看了些文章。现在记录一些音频的特性。

<!-- more -->

* Table of Contents
{:toc}

# 1.声音与声波

## 1.1 声压级与声强级

&#160; &#160; &#160; &#160;声压是指声波震动而产生的空气逾量压强，它等于声波存在时的空气压强减去没有声波时的空气压强，声压的基本单位为帕(Pa)。在声波传播的过程中，媒质中的各质点都要发生震动，因此具有动能，同时媒质还要发生形变，因此具有位能。也因此，声波的传播也是能量的传播。声强是指声波在单位面积上产生的能量，声强的基本单位为$$瓦/米^2$$($$w/m^2$$)。 

> 在声音震动中，声压值和声强值都是声波的客观绝对值

&#160; &#160; &#160; &#160;人耳听觉的能量范围是$$10^{13}:1$$，这是一个极大的范围，人对声音强弱的感觉大体上与声压值或声强值的对数成比例。为了适应人类听觉的这个特性，同时也为了计算方便，科学家把声压值或声强值去对数来表示声音的强弱，这种表示声音强弱的数值称为声压级($$dB$$)或声强级($$dB$$)

声压级：声压级($$dB$$)用两个声压比对数值的20倍来描述

$$
Lp = SPL = 20 \lg(\frac{P1}{P0}) \\\
P1 = 被测声压值 \\\
P0 = 参考声压值 = 0.00002Pa(人耳能听到的最低声压值)
$$



声强级：声强级($$dB$$)用两个声强比对数值的10倍来描述

$$
LI = SIL = 10 \lg(\frac{I1}{I0}) \\\
I1 = 被测声强值 \\\
I2 = 参考声强值 = 10^{-12} w/m^2 (人耳能感受到的最低声强值)
$$

> 声压级和声强级都是以人耳挺阈最低值为参考的客观相对值

## 1.2 声波的基本参数

&#160; &#160; &#160; &#160;对声波的描述主要使用分贝、频率、振幅、波长、周期、相位等物理参数

 **1.2.1 分贝**

&#160; &#160; &#160; &#160;分贝是用来表示声压强度的单位，所谓分贝是指两个相同的物理量(例如A1和A0)之比取以10为底的对数并乘以10(或20)。分贝符号 “dB”，它是无量纲的。A0是基准量(或参考量)，A1是被量度量。被量度量和基准量之比去对数，这对数值成为被量度量的“级”。亦即用对数标度时，所得到的比值，它代表被量度量比基准量高出多少“级”。

 **1.2.2 频率**

&#160; &#160; &#160; &#160;频率是指物体每秒震动的次数，他的测量单位为赫兹(Hz)，上以海因里希·鲁道夫·赫兹的名字命名的。频率越高音调越高。(比如Oatave0音名A（唱名 La）的频率为440Hz)

 **1.2.3 振幅**

&#160; &#160; &#160; &#160;振幅是震动物体离开零点线位置的最大距离，描述了物体震动幅度的大小和震动强弱，较大振幅产生较大声音，较小振幅产生较小声音

 **1.2.4 波长**

&#160; &#160; &#160; &#160;波长是值沿声音传播方向，震动一个周期所传播的距离，或在波形上相同相位的相邻两点间的距离，记为$$\lambda$$，单位为m。它一般用相邻两个波峰或波谷之间的距离来表达，其公式为： 波长=速度/频率。例如，30Hz的声波，其波长为344m/s除以30Hz，约为11.4m

 **1.2.5 周期**

&#160; &#160; &#160; &#160;周期指声源震动一次所经历的时间，即从零点线位置到高压区再到低压区，最后以相同相位返回原点所需要的时间，波形循环一周即为$$360^{\circ}$$。

## 1.3 音色包络

&#160; &#160; &#160; &#160;音色包络是指某一种乐器特有的强度随时间变化的一种形态，一般由四个阶段组成，分为起音、持续、衰弱以及释音

![音色包络](http://7xqrar.com1.z0.glb.clouddn.com/69609d2ab4474a40fa5f44ea3d808eb9.gif)

1. 起音：起音也称声建立，是指声音起始阶段迅速曾强的变化形态
2. 持续：持续是描述声建立期之后声音的周期性增减形态
3. 衰弱：衰弱是指声音收到空气阻尼强度开始衰落的变化形态
4. 释音：释音是指声音消失过程中的变化形态

# 2. 声音的类别

&#160; &#160; &#160; &#160;随着物理声学研究的深入和技术手段的完善，科学家发现人的主管听觉与声音的物理特性是有差异的，并由此发展出生理声学、心里声学和音乐声学

## 2.1响度级与响度

&#160; &#160; &#160; &#160;在前面介绍的声压与声强，他们表达了声音的客观参量。但是研究证明，声音信号在人的听觉系统中会被非线性“加工”。为了表达人的听觉系统对声音强弱的感受特点，需要引入听觉感受的半主观量“响度级”与主观量“响度”两个概念。这样，就把声音强弱的客观尺度与在此声音刺激下的主观感受的强弱联系起来

  **2.1.1 响度**

&#160; &#160; &#160; &#160;响度是人耳判别声音由轻到响的强度等级概念，它不仅取决于声音的强度（如声压级），还与它的频率以及波形有关。响度的单位为“宋”，1宋的定义：声压级为40dB，频率为1000Hz，且来自听者正前方的平面波形的强度。如果另一个声音听起来比1宋的声音大N倍，即该声音的响度为N宋

  **2.1.2 响度级**

&#160; &#160; &#160; &#160;响度级是建立在两个声音主管比较的基础上，选择1000Hz的纯音作基准音，若某一噪音听起来与该纯音一样响，则该噪声的响度级在数值上就等于这个纯音的声压级(dB)。响度级用LN表示，单位是“方”。如果某噪声听起来与声压级为80dB、频率为1000Hz的纯音一样响，则该噪声的响度级就是80方

  **2.1.3 响度与响度级**

&#160; &#160; &#160; &#160;根据大量实验表面，响度级每改变10方，响度加倍或减半。他们的关系可用数学式表示：

$$
N = 2[\frac{LN - 40}{10}]
$$

或

$$
LN = 40 + 33\lg N
$$

> 注意：响度级的合成不能直接相加，而响度可以相加。应先将各响度级换算成响度进行合成，再换算成响度级

## 2.2 频率与音高

&#160; &#160; &#160; &#160;人的听觉对声音频率的感觉为音调的高低，在音乐中简称“音高”。研究证明，当两个不同频率的声音进行比较时，具有决定意义的是他们的比值，而不是他们的差值。音高与声音频率大致上承对数关系。音阶频率对照表如下表所示

<table>
	<tr>
		<th colspan="2">音阶</th>
		<th colspan="4">频率(Hz)</th>
	</tr>
	
	<tr>
		<td>唱名</td>
		<td>音名</td>
		<td>Octave0</td>
		<td>Octave1</td>
		<td>Octave2</td>
		<td>Octave3</td>
	</tr>
	
	<tr>
		<td>Do</td>
		<td>C</td>
		<td>262</td>
		<td>523</td>
		<td>1047</td>
		<td>2093</td>
	</tr>
	
	<tr>
		<td></td>
		<td>Db</td>
		<td>277</td>
		<td>554</td>
		<td>1109</td>
		<td>2217</td>
	</tr>
	
	<tr>
		<td>Re</td>
		<td>D</td>
		<td>294</td>
		<td>587</td>
		<td>1175</td>
		<td>2349</td>
	</tr>
	
	<tr>
		<td></td>
		<td>Eb</td>
		<td>311</td>
		<td>622</td>
		<td>1245</td>
		<td>2489</td>
	</tr>
	
	<tr>
		<td>Mi</td>
		<td>E</td>
		<td>330</td>
		<td>659</td>
		<td>1329</td>
		<td>2639</td>
	</tr>
	
	<tr>
		<td>Fa</td>
		<td>F</td>
		<td>349</td>
		<td>698</td>
		<td>1397</td>
		<td>2794</td>
	</tr>
	
	<tr>
		<td></td>
		<td>Gb</td>
		<td>370</td>
		<td>740</td>
		<td>1480</td>
		<td>2960</td>
	</tr>
	
	<tr>
		<td>Sol</td>
		<td>G</td>
		<td>392</td>
		<td>784</td>
		<td>1568</td>
		<td>3136</td>
	</tr>
	
	<tr>
		<td></td>
		<td>Ab</td>
		<td>415</td>
		<td>831</td>
		<td>1661</td>
		<td>3322</td>
	</tr>
	
	<tr>
		<td>La</td>
		<td>A</td>
		<td>440</td>
		<td>880</td>
		<td>1760</td>
		<td>3520</td>
	</tr>
	
	<tr>
		<td></td>
		<td>Bb</td>
		<td>466</td>
		<td>923</td>
		<td>1865</td>
		<td>3729</td>
	</tr>
	
	<tr>
		<td>Xi</td>
		<td>B</td>
		<td>494</td>
		<td>988</td>
		<td>1976</td>
		<td>3951</td>
	</tr>
</table>

> 虽然声音的频率是决定音高的主要因素，但声强对音高也起一定的作用。为了表征音高这一主观心理物理量，需要引入音高的单位——美(Mel)。主观音量高的单位美(Mel)的定义为：响度级为40方、频率为1000Hz的标准音，其音高为1000美。

## 2.3 谐波与泛音

&#160; &#160; &#160; &#160;谐波和泛音所指的是同一种声学现象，因为分支科学的不同，物理声学中的“谐波”在音乐中称为“泛音”。

&#160; &#160; &#160; &#160;简单来说，同城乐器在发音时，其弦或空气柱的整体震动会发出较强的音，即基音。同时，还会在弦长或空气柱长的1/2、1/3、1/4、1/5······等处发出较弱的音，即泛音。泛音是基音的2倍、3倍、4倍、5倍······等各次谐波，并由此构成了一个泛音列。

## 2.4 音色与音质

&#160; &#160; &#160; &#160;音色的不同取决于不同的泛音、不用种类的乐器、不同的人以及所有能发声的物体发出的声音，除了一个基音外，还有许多不同频率（震动速度）的泛音伴随，正是这些泛音决定了其不同的音色，使人能辨别出事不同的乐器甚至不同的人发出的声音。不同的人即使说相同的话也是不同的音色，因此可以根据其音色辨别出是不同的人。

&#160; &#160; &#160; &#160;音色是音乐中能直接吸引人、触动听觉感官的重要表现手段。音乐中的音色分为现实性音色和非现实性虚拟音色两种。人声音色和乐器音色即是现实性音色，它是人们所熟知的客观音色。MIDI电子乐器可以创造出各种非现实性虚拟音色，给人耳目一新的感觉。

&#160; &#160; &#160; &#160;音质是指广播、电视、动画、音乐CD和MP3等音像产品中音频质量客观指标和主观感受，主要指声音的信噪比、清晰度、方位感、空间感、频率均衡和温暖度等回放效果等，从这些基本的信息中感官体验出音质的好与坏。