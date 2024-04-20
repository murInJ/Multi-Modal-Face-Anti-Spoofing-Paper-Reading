# Suppress and Rebalance: Towards Generalized Multi-Modal Face Anti-Spoofing
[[arxiv]](https://arxiv.org/abs/2402.19298)

<div align=center><img src=".\assets\image-20240418233759387.png"></div>


## Problem
> Why using more modalities is not better?  
1. **Modality unreliability** 未知的部署环境和不同类型的传感器在同模态下会有显著的域偏移，这会导致不可靠的特征提取，进而在跨模态融合中相互误导  
2. **Modality imbalance** 多模态场景中模型会倾向于向具有最速收敛曲线的模态进行学习，导致对其他慢速模态的欠学习。在FAS中，当快速模态不可靠或者不能有效侦测目标域的攻击时，模态失衡会让模型无法发挥慢速模态的融合作用。  

  > 关于模态不平衡的这部分感觉参考了很多《[PMR: Prototypical Modal Rebalance for Multimodal Learning](http://arxiv.org/pdf/2211.07089.pdf)》
## Method

<div align=center><img src=".\assets\image-20240418233907671.png"></div>

### Uncertainty Estimation Module (UEM)
token->MCD->计算方差
#### Monte Carlo dropout (MCD)
MCD是确定模型不确定性的主要方法之一，主要是通过开启模型dropout，来对同一输入进行多测采样，再对其输出样本计算其方差等来确定其受扰动程度。  
另一个确定模型不确定性的方法是深度集成法，是通过多个随机初始化权重的同样训练的模型喂入同一输入，再对输出样本进行观测。

###  Uncertainty-Guided Cross-Adapter (U-Adapter)
解决不可靠问题  

<div align=center><img src=".\assets\image-20240418234043152.png"></div>

#### 利用U-Adapter进行微调过程：

<div align=center><img src=".\assets\image-20240418234149494.png"></div>

当前模态与其它模态的调整输出加上当前模态的原本输出  


#### U-Adapter公式

<div align=center><img src=".\assets\image-20240418234244499.png"></div>

估计不确定性来控制不可信特征的融合  
用其它模态的第二层LayerNormal输出特征作为Q  
用当前模态的第二层LayerNormal输出特征作为K,V  
利用Q的不确定性对Q进行调节  

###  Rebalanced Modality Gradient Modulation (ReGrad)
解决不平衡问题

<div align=center><img src=".\assets\image-20240418233610395.png"></div>

#### ReGrad公式

![image-20240418234356022](.\assets\image-20240418234356022.png)

概括来说，就是针对四种收敛情况，去除有问题的方向梯度

在具体实现中，首先利用SSP Loss越低，收敛速度越快，模态越快，从而做到区分四种情况

### Single-Side Prototypical Loss

SSP loss 用于监控每个模态分支的收敛速度，这是通过计算每个模态中样本与其对应域的原型之间的距离来实现的

#### SSP Loss
![image-20240419000948978](.\assets\image-20240419000948978.png)

![image-20240419000932142](.\assets\image-20240419000932142.png)

![image-20240419001003862](.\assets\image-20240419001003862.png)
#### PCE Loss
![alt text](.\assets\image.png)  
改进的部分主要是把$L_{PCE}$中的模态center $c_y^0$ 换成了域的center $p^d_m$    

对比起来，SSP Loss更像是域场景下的PCE Loss。

`如果能做到用同样的公式结构直接模态center换成了域的center，那么模态和域之间是否有什么关系？`

## Performence

![image-20240419004546435](.\assets\image-20240419004546435.png)

## Related

### SSDG

### AMA