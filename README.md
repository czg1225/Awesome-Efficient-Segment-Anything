<div align="center">
<img src="assets/title.png" width="100%">
</div>



# Efficient-Segment-Anything-Model
[Segment Anything Model (SAM)](https://github.com/facebookresearch/segment-anything) has attracted considerable attention from the community since its inception. However, the formidable model size and demanding computational requirements of SAM have rendered it cumbersome for deployment on resource-constrained devices. To mitigate these constraints, many efforts have been made to effectively make SAM more efficient and lightweight. 
This repository provides a summary of those efficient segment anything models.

If you find this repository helpful, please consider Stars ⭐ or Sharing ⬆️. Thanks.

## Updates
* 🚀 **August 7, 2024**: Updated new related works before 07/08/2024 in this GitHub. 
* 🚀 **March 22, 2024**: Updated new related works before 20/03/2024 in this GitHub. 

## Contents

- [Scratch Training Methods](#scratch-training-methods)
  - [FastSAM](#fastsam)
  - [Lite-SAM](#lite-sam)
- [Knowledge Distillation Methods](#knowledge-distillation-methods)
  - [MobileSAM](#mobilesam)
  - [EdgeSAM](#edgesam)
  - [EfficientSAM](#efficientsam)
  - [EfficientViT-SAM](#efficientvit-sam)
  - [RepViT-SAM](#repvit-sam)
  - [SAM-LIGHTENING](#sam-lightening)
  - [TinySAM](#tinysam)
- [Model Pruning Methods](#sam-lightening)
  - [SlimSAM](#slimsam)
- [Training Free Methods](#training-free-methods)
  - [Expedit-SAM](#expedit-sam)

## Scratch Training Methods

### FastSAM
> **Fast Segment Anything**   
> Xu Zhao, Wenchao Ding, Yongqi An, Yinglong Du, Tao Yu, Min Li, Ming Tang,
Jinqiao Wang \
> Institute of Automation, Chinese Academy of Sciences, Beijing, China   
> Paper: [[Arxiv]](https://arxiv.org/pdf/2306.12156.pdf?trk=public_post_comment-text)
> Code: [![Stars](https://img.shields.io/github/stars/CASIA-IVA-Lab/FastSAM.svg?style=social&label=Star)](https://github.com/CASIA-IVA-Lab/FastSAM)

**Description:** The Fast Segment Anything Model(FastSAM) is a CNN Segment Anything Model trained using only 2% of the SA-1B dataset published by SAM authors.
![FastSAM](assets/fastsam.png)


### Lite-SAM
> **Lite-SAM Is Actually What You Need for Segment Everything**   
> Jianhai Fu, Yuanjie Yu, Ningchuan Li, Yi Zhang, Qichao Chen, Jianping Xiong, Jun Yin, and Zhiyu Xiang\
> Zhejiang Dahua Technology, Zhejiang University, Hangzhou, China   
> Paper: [[Arxiv]](https://arxiv.org/pdf/2407.08965)

**Description:** Lite-SAM is an efficient end-to-end solution for the SegEvery task designed to reduce computational costs and redundancy.
![litesam](assets/litesam.png)



## Knowledge Distillation Methods

### MobileSAM
> **FASTER SEGMENT ANYTHING: TOWARDS LIGHTWEIGHT SAM FOR MOBILE APPLICATIONS**   
> Chaoning Zhang, Dongshen Han, Sheng Zheng, Jinwoo Choi, Tae-Ho Kim, Choong Seon Hong \
> Kyung Hee University \
> Paper: [[Arxiv]](https://arxiv.org/pdf/2306.14289.pdf)
> Code: [![Stars](https://img.shields.io/github/stars/ChaoningZhang/MobileSAM.svg?style=social&label=Star)](https://github.com/ChaoningZhang/MobileSAM)

**Description:** MobileSAM is a lightweight SAM suitable for resource-constrained mobile devices.
![MobileSAM](assets/mobilesam.jpg)


### EdgeSAM
> **EdgeSAM: Prompt-In-the-Loop Distillation for On-Device Deployment of SAM**   
> Chong Zhou, Xiangtai Li, Chen Change Loy, Bo Dai \
> S-Lab, Nanyang Technological University, Shanghai Artificial Intelligence Laborator \
> Paper: [[Arxiv]](https://arxiv.org/pdf/2312.06660.pdf)
> Code: [![Stars](https://img.shields.io/github/stars/chongzhou96/EdgeSAM.svg?style=social&label=Star)](https://github.com/chongzhou96/EdgeSAM)

**Description:** EdgeSAM is an accelerated variant of the Segment Anything Model (SAM), optimized for efficient execution on edge devices with minimal compromise in performance.
![MobileSAM](assets/edgesam.png)


### EfficientSAM
> **EfficientSAM: Leveraged Masked Image Pretraining for Efficient Segment Anything**   
> Yunyang Xiong et al.\
> Meta AI Research \
> Paper: [[Arxiv]](https://arxiv.org/pdf/2312.00863.pdf)
> Code: [![Stars](https://img.shields.io/github/stars/yformer/EfficientSAM.svg?style=social&label=Star)](https://github.com/yformer/EfficientSAM)

**Description:** EfficientSAMs is lightweight SAM model that exhibits decent performance with largely reduced complexity. The idea is based on leveraging masked image pretraining, SAMI, which learns to reconstruct features from SAM image encoder for effective visual representation learning.
![EfficientSAM](assets/efficientsam.png)


### EfficientViT-SAM
> **EfficientViT-SAM: Accelerated Segment Anything Model Without Performance Loss**   
> Zhuoyang Zhang, Han Cai, Song Han\
> Tsinghua University, MIT, NVIDIA\
> Paper: [[Arxiv]](https://arxiv.org/pdf/2402.05008.pdf)
> Code: [![Stars](https://img.shields.io/github/stars/mit-han-lab/efficientvit.svg?style=social&label=Star)](https://github.com/mit-han-lab/efficientvit)

**Description:** EfficientViT-SAM is a new family of accelerated segment anything models. It retain SAM’s lightweight prompt encoder and mask decoder while replacing the heavy image encoder with EfficientViT
![EfficientViT-SAM](assets/efficientvit.png)

### RepViT-SAM
> **RepViT-SAM: Towards Real-Time Segmenting Anythings**   
> Ao Wang, Hui Chen, Zijia Lin, Jungong Han, Guiguang Ding\
> Tsinghua University, The University of Sheffield\
> Paper: [[Arxiv]](https://arxiv.org/pdf/2312.05760.pdf)
> Code: [![Stars](https://img.shields.io/github/stars/THU-MIG/RepViT.svg?style=social&label=Star)](https://github.com/THU-MIG/RepViT)

**Description:** RepViT achieves the state-of-the-art performance and latency trade-off on mobile devices by incorporating efficient architectural designs of ViTs into CNNs. Here, to achieve real-time segmenting anything on mobile devices, following [27], this work replace the heavyweight image encoder in SAM with RepViT model, ending up with the RepViT-SAM model.
![RepViT-SAM](assets/repvit.png)


### SAM-LIGHTENING
> **SAM-LIGHTENING: A LIGHTWEIGHT SEGMENT ANYTHING MODEL WITHIN DILATED FLASH ATTENTION TO ACHIEVE 30× ACCELERATION**   
> Yanfei Song, Bangzheng Pu, Peng Wang, Dong Dong, Hongxu Jiang, Yiqing Shen\
> Beihang University, Beihang Hangzhou Innovation Institute, Johns Hopkins University\
> Paper: [[Arxiv]](https://arxiv.org/pdf/2403.09195v1.pdf)
> Code: [[Anonymous Github]](https://anonymous.4open.science/r/SAM-LIGHTENING-BC25/readme.md)

**Description:** SAM-Lightening revolutionizes image segmentation by introducing a highly efficient, lightweight model. This model features an innovative Dilated Flash Attention mechanism, enabling rapid inference and minimal memory usage, ideal for applications in real-time environments and resource-constrained devices.
![SAM-LIGHTENING](assets/samlighten.png)


### TinySAM
> **TinySAM: Pushing the Envelope for Efficient Segment Anything Model**   
> Han Shu, Wenshuo Li, Yehui Tang, Yiman Zhang, Yihao Chen, Houqiang Li, Yunhe Wang,  Xinghao Che\
> University of Science and Technology of China, Huawei Noah’s Ark Lab\
> Paper: [[Arxiv]](https://arxiv.org/pdf/2312.13789)
> Code: [![Stars](https://img.shields.io/github/stars/xinghaochen/TinySAM.svg?style=social&label=Star)](https://github.com/xinghaochen/TinySAM)

**Description:** TinySAM is a framework can obtain a tiny segment anything model while maintaining the strong zero-shot performance.
![TinySAM](assets/tinysam.png)



## Model Pruning Methods
### SlimSAM
> **SlimSAM: 0.1% Data Makes Segment Anything Slim**   
> [Zigeng Chen](https://github.com/czg1225), [Gongfan Fang](https://fangggf.github.io/), [Xinyin Ma](https://horseee.github.io/), [Xinchao Wang](https://sites.google.com/site/sitexinchaowang/)   
> [Learning and Vision Lab](http://lv-nus.org/), National University of Singapore  
> Paper: [[Arxiv]](https://arxiv.org/abs/2312.05284)
> Code: [![Stars](https://img.shields.io/github/stars/czg1225/SlimSAM.svg?style=social&label=Star)](https://github.com/czg1225/SlimSAM)

**Description:** SlimSAM is a novel data-efficient SAM compression method that achieves superior performance with extremely less training data. The essence of SlimSAM is encapsulated in the alternate slimming framework which effectively enhances knowledge inheritance under severely limited training data availability and exceptional pruning ratio. 

![SlimSAM](assets/slimsam.png)



## Training Free Methods
### Expedit-SAM
> **Expediting Large-Scale Vision Transformer for Dense Prediction without Fine-tuning**   
> Weicong Liang et al.\
> Key Laboratory of Machine Perception, Peking University, ETH Zurich\
> Paper: [[Arxiv]](https://arxiv.org/pdf/2210.01035.pdf)
> Code: [![Stars](https://img.shields.io/github/stars/Expedit-LargeScale-Vision-Transformer/Expedit-SAM.svg?style=social&label=Star)](https://github.com/Expedit-LargeScale-Vision-Transformer/Expedit-SAM)

**Description:** Expedit-SAM is a method can speed up SAM without any training. This is achieved by a novel token clustering algorithm.
![SAM-LIGHTENING1](assets/Hourglass_transformer_framework.png)
![SAM-LIGHTENING2](assets/TokenClusterReconstruct_Details.png)
