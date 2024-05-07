# Multi-Modal-Face-Anti-Spoofing-Paper-Reading

一个是记录整理这个领域的论文，阅读笔记，代码等，另外则尝试通过积累梳理出研究方法和思想的脉络

## Contributors

<a href="https://github.com/MurInj/Streaming-Data-Aggregation-Source-Service/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=MurInj/Multi-Modal-Face-Anti-Spoofing-Paper-Reading" />
</a>

## Paper Reading List

### Y.2024

-  Suppress and Rebalance Towards Generalized Multi-Modal Face Anti-Spoofing

   > 为了解决多模态FAS方法应对未见攻击和未见部署条件时泛化能力不足的问题，本文提出了不确定性引导的跨模态adapter来防止不可靠模态的误导，并设计了一种模态梯度平衡调节策略来平衡各个模态的收敛速度。

-  Rethinking Vision Transformer and Masked Autoencoder in Multimodal Face Anti-Spoofing

   > 这篇论文提出了一种改进的视觉变换器（ViT）基础的多模态学习方法，用于提高人脸识别防欺骗系统的性能。研究主要关注三个关键因素：模态感知输入、多模态预训练和微调策略。

-  S-Adapter Generalizing Vision Transformer for Face Anti-Spoofing with Statistical Tokens

   > 这篇文章介绍了一种名为S-Adapter的新型面部反欺骗（Face Anti-Spoofing, FAS）方法，该方法通过在预训练的Vision Transformer（ViT）模型中插入适配器模块来提高面部识别系统的安全性。S-Adapter通过提取局部统计信息和使用Token Style Regularization（TSR）来减少跨域风格差异，从而增强模型在不同领域间的泛化能力。实验结果表明，该方法在零样本和少样本跨域测试以及未见攻击检测方面，相较于现有技术，取得了显著的性能提升。

### Y.2023

- Vision Transformers are Parameter-Efficient  Audio-Visual Learners

  > 这篇论文提出了一个名为LAVISH的新型适配器，它能够使预训练的ViTs在不需要对其原始参数进行微调的情况下，通过注入少量可训练参数来适应音视频任务。LAVISH适配器利用一组小的隐tokens形成注意力瓶颈，有效融合视觉和听觉线索，避免了标准交叉注意力的二次成本。

- Prototypical Modal Rebalance for Multimodal Learning

  > 这篇论文提出了一种名为PMR（Prototypical Modal Rebalance）的新方法，用于解决多模态学习（MML）中的模态不平衡问题。模态不平衡是指在多模态学习过程中，一个表现更好的模态可能会抑制另一个表现较差的模态的学习，从而影响整体性能。PMR的目标是通过特定的策略激发学习速度较慢的模态，并减轻由主导模态带来的抑制效应。

- Efficient Multimodal Fusion via Interactive Prompting

  > 这篇论文提出了一种名为PMF（Prompt-based Multimodal Fusion）的高效多模态融合方法，通过在单模态预训练变换器的深层添加特定类型的提示向量，实现了在显著降低训练内存使用的同时，保持与全参数微调方法可比的性能。PMF方法通过模块化的多模态融合框架和三种不同类型的交互提示，增强了不同模态间的双向交互，展示了在多模态学习任务中的灵活性和高效性。

### Y.2022

- Balanced multimodal learning via on-the-ﬂy gradient

  > 这篇论文提出了一种新的多模态学习方法，名为“OGM-GE”，旨在解决多模态学习中存在的优化不平衡问题。多模态学习通过整合不同感官的信息来全面理解世界，但现有的多模态判别模型在某些情况下可能无法充分利用多种输入模态，导致某些模态的表示未被充分优化。

### Y.2021

- Attention Bottlenecks for Multimodal Fusion

  > 文章提出了一种新的多模态融合架构MBT，通过在不同层次引入信息融合瓶颈来改善音频和视频的融合效果，降低了计算成本，并在多个音视频分类基准上取得了优异的性能。