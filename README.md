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

- MoE-FFD  Mixture of Experts for Generalized and Parameter-Efficient Face Forgery Detection

  > 本文介绍了一种名为MoE-FFD（Mixture of Experts for Face Forgery Detection）的新型深度伪造检测方法，该方法通过结合轻量级LoRA（Low-Rank Adaptation）和Adapter层，以参数高效的方式更新并保持Vision Transformer（ViT）骨干网络的ImageNet权重固定，同时利用Transformer的表达能力和CNN的局部先验来提取全局和局部伪造线索。MoE-FFD设计了新颖的MoE模块，通过固定激活参数动态选择最优的伪造检测专家，从而提高检测性能，并通过大量实验验证了其在减少参数开销的同时实现最先进的面部伪造检测性能。

- TeG-DG: Textually Guided Domain Generalization for Face Anti-Spoofing

  > 这篇论文提出了一个名为TeG-DG（Textually Guided Domain Generalization）的新框架，旨在提升面部反欺骗（Face Anti-Spoofing, FAS）技术在不同领域中的泛化性能。通过利用文本信息实现跨领域对齐，TeG-DG框架设计了一个分层注意力融合（Hierarchical Attention Fusion, HAF）模块来自适应地聚合不同层级的视觉特征，并引入了一个文本增强视觉鉴别器（Textual-Enhanced Visual Discriminator, TEVD），以改善两种模态间的对齐并使用无偏文本特征来规范分类器。实验结果表明，TeG-DG在各种数据集上均优于现有方法，尤其是在源领域数据极其有限的情况下，展现了出色的小样本（few-shot）性能。

- VL-FAS  Domain Generalization via Vision-Language Model For Face Anti-Spoofing

  > 这篇论文提出了一种名为VL-FAS的面部反欺骗（FAS）新方法，通过结合视觉变换器（ViT）和自然语言描述来提升模型在不同领域间的泛化能力。研究者们利用MiniGPT-4生成细致的面部区域描述作为引导，通过自上而下的注意力调节机制让模型集中学习面部特征，同时引入样本级视觉-文本优化模块（SLVT），借助对比学习加深模型对图像样本内在语义的理解，减少对特定领域信息的依赖。

### Y.2023

- Vision Transformers are Parameter-Efficient  Audio-Visual Learners

  > 这篇论文提出了一个名为LAVISH的新型适配器，它能够使预训练的ViTs在不需要对其原始参数进行微调的情况下，通过注入少量可训练参数来适应音视频任务。LAVISH适配器利用一组小的隐tokens形成注意力瓶颈，有效融合视觉和听觉线索，避免了标准交叉注意力的二次成本。

- Prototypical Modal Rebalance for Multimodal Learning

  > 这篇论文提出了一种名为PMR（Prototypical Modal Rebalance）的新方法，用于解决多模态学习（MML）中的模态不平衡问题。模态不平衡是指在多模态学习过程中，一个表现更好的模态可能会抑制另一个表现较差的模态的学习，从而影响整体性能。PMR的目标是通过特定的策略激发学习速度较慢的模态，并减轻由主导模态带来的抑制效应。

- Efficient Multimodal Fusion via Interactive Prompting

  > 这篇论文提出了一种名为PMF（Prompt-based Multimodal Fusion）的高效多模态融合方法，通过在单模态预训练变换器的深层添加特定类型的提示向量，实现了在显著降低训练内存使用的同时，保持与全参数微调方法可比的性能。PMF方法通过模块化的多模态融合框架和三种不同类型的交互提示，增强了不同模态间的双向交互，展示了在多模态学习任务中的灵活性和高效性。

- Rehearsal-Free Domain Continual Face Anti-Spoofing: Generalize More and Forget Less

  > 这篇论文提出了一种无需重放缓冲区的领域持续学习(DCL)方法，用于面部反欺骗(FAS)任务，通过设计动态中心差分卷积适配器(DCDCA)和代理原型对比正则化(PPCR)来提高模型在未见领域的泛化能力并减少对先验知识的灾难性遗忘。

- FLIP  Cross-domain Face Anti-spoofing with Language Guidance

  > 这篇论文介绍了一种名为FLIP的新型跨域人脸反欺骗（Face Anti-Spoofing, FAS）方法，该方法利用视觉变换器（Vision Transformer, ViT）模型和自然语言指导来提高FAS任务的泛化能力。研究者首先展示了使用多模态（例如CLIP）预训练权重初始化ViTs可以改善FAS任务的泛化性。接着，提出了一种新颖的跨域FAS方法，通过将图像表示与基于自然语言语义的类别描述集合对齐，在数据匮乏的情况下提高FAS的泛化能力。最后，提出了一种多模态对比学习策略，进一步增强特征泛化，并在源域和目标域之间架起桥梁。

### Y.2022

- Balanced multimodal learning via on-the-ﬂy gradient

  > 这篇论文提出了一种新的多模态学习方法，名为“OGM-GE”，旨在解决多模态学习中存在的优化不平衡问题。多模态学习通过整合不同感官的信息来全面理解世界，但现有的多模态判别模型在某些情况下可能无法充分利用多种输入模态，导致某些模态的表示未被充分优化。

### Y.2021

- Attention Bottlenecks for Multimodal Fusion

  > 文章提出了一种新的多模态融合架构MBT，通过在不同层次引入信息融合瓶颈来改善音频和视频的融合效果，降低了计算成本，并在多个音视频分类基准上取得了优异的性能。

- Explaining Face Presentation Attack Detection Using Natural Language

  > 这篇论文提出了一种使用自然语言来解释面部呈现攻击检测（PAD）模型预测的方法。研究者利用轻量级LSTM网络生成描述PAD预测背后逻辑的文本，并研究了不同的损失函数来提高文本质量。通过在含有真实和攻击样本的数据集上的实验，验证了模型生成有效PAD解释的能力。