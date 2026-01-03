# Awesome-First-Frame-Guided-Video-Editing 🎬

> This repository catalogs cutting-edge research papers, practical tools, and open source projects for First-Frame Guided Video Editing, where edits on the first frame are propagated to the entire video.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📋 Table of Contents

- [📚 Papers](#-papers)
- [🛠️ Tools](#️-tools)
- [🚀 Open Source Projects](#-open-source-projects)

---

## 📚 Papers

> All papers are in chronological order, from newest to oldest
1. **ContextFlow: Training-Free Video Object Editing via Adaptive Context Enrichment**, 2025-09, https://arxiv.org/abs/2509.17818
   > 简介: 针对对象级编辑（插入、删除、交换）提出的免训练方法。虽然不纯粹依赖首帧，但它通过动态融合原始视频和编辑目标的上下文信息（Adaptive Context Enrichment），解决了 GenProp 等传播类方法在复杂运动下的保真度问题。

2. **FlowV2V: Consistent Video Editing as Flow-Driven Image-to-Video Generation**, 2025-06, https://arxiv.org/abs/2506.07713
   > 简介: 将视频编辑明确分解为“首帧编辑”和“流驱动的 I2V 生成”。利用光流（Optical Flow）作为强几何约束，指导 I2V 模型将首帧的形变精确传播到后续帧，显著提升了时序一致性。

3. **LoRA-Edit: Controllable First-Frame-Guided Video Editing via Mask-Aware LoRA Fine-Tuning**, 2025-06, https://arxiv.org/abs/2506.10082
   > 简介: 提出了一种基于 Mask 的 LoRA 微调方法，专门用于首帧引导的视频编辑。它可以精确控制编辑区域并保护背景，解决了现有方法在后续帧中灵活性不足的问题。

4. **Go-with-the-Flow: Motion-Controllable Video Diffusion Models Using Real-Time Warped Noise**, 2025-01, https://arxiv.org/abs/2501.08331
   > 简介: 利用光流（Optical Flow）和噪声变形（Warped Noise）技术，实现通过编辑第一帧来控制视频的生成和风格化，具有极高的时序一致性。

5. **GenProp: Propagating Generation for Video Editing (CVPR 2025)**, 2024-12, https://arxiv.org/abs/2412.19761
   > 简介: Adobe Research 提出的生成式视频传播框架。利用图像到视频（I2V）生成模型的先验知识，将首帧的编辑（包括对象移除、插入、形状改变）智能传播到全视频。

6. **I2VEdit: First-Frame-Guided Video Editing via Image-to-Video Diffusion Models**, 2024-05, https://arxiv.org/abs/2405.16537
   > 简介: 利用预训练的 Image-to-Video 模型，通过粗略运动提取和外观细化，将首帧的编辑传播到整个视频，支持全局和局部编辑。

7. **ReVideo: Remake a Video with Motion and Content Control**, 2024-05, https://arxiv.org/abs/2405.13865
   > 简介: 允许用户通过修改第一帧来控制视频内容，同时通过轨迹控制运动，实现了内容和运动的解耦编辑。

8. **AnyV2V: A Plug-and-Play Framework For Any Video-to-Video Editing Tasks**, 2024-03, https://arxiv.org/abs/2403.14468
   > 简介: 一个即插即用的框架，核心思想是“编辑第一帧 + I2V 生成”。兼容任何图像编辑工具（如 InstructPix2Pix），通过 I2V 模型进行特征注入以保持一致性。

9. **CoDeF: Content Deformation Fields for Temporally Consistent Video Processing (CVPR 2024)**, 2023-08, https://arxiv.org/abs/2308.07926
   > 简介: 提出“规范内容场”（Canonical Content Field），将视频分解为静态全景图和变形场。用户只需编辑这张静态全景图（类似于关键帧），即可自动传播到整个视频。


---
else:
6. **InsViE-1M: Effective Instruction-based Video Editing with Elaborate Dataset Construction (InsV2V)**, 2024-12, https://openaccess.thecvf.com/content/ICCV2025/html/Wu_InsViE-1M_Effective_Instruction-based_Video_Editing_with_Elaborate_Dataset_Construction_ICCV_2025_paper.html
   > 简介: 虽然主打指令编辑，但相关工作 InsV2V 探讨了视频生成模型在编辑中的应用，并构建了大规模数据集，常与 AnyV2V 等首帧方法进行对比。

11. **TokenFlow: Consistent Diffusion Features for Consistent Video Editing**, 2023-07, https://arxiv.org/abs/2307.10373
   > 简介: 通过在扩散特征空间中强制特征一致性来实现视频编辑。支持关键帧编辑模式，确保编辑后的特征能够基于对应关系传播。

12. **Text2Video-Zero: Text-to-Image Diffusion Models are Zero-Shot Video Editors**, 2023-03, https://arxiv.org/abs/2303.13439
    > 简介: 无需训练，通过重编程注意力机制（Cross-Frame Attention），让后续帧参考第一帧的生成特征，实现风格迁移和编辑。

13. **FateZero: Fusing Attentions for Zero-shot Text-based Video Editing**, 2023-03, https://arxiv.org/abs/2303.09535
    > 简介: 零样本视频编辑方法，通过在反演过程中融合注意力图来保持结构和运动，虽然主打文字编辑，但其注意力控制机制是后续很多传播方法的基础。




---

## 🛠️ Tools

### Commercial & Web Tools
- **[Pika](https://pika.art/)** - 著名的 AI 视频生成工具。其 "Modify Region" 或 "Pikaframes" 功能允许用户控制首尾帧或特定区域来进行视频编辑和扩展。
- **[Runway Gen-1/Gen-2](https://runwayml.com/)** - 提供 "Video to Video" 模式，允许通过参考图像（第一帧风格）来驱动视频生成。
- **[EbSynth (Software)](https://ebsynth.com/)** - 免费且强大的工具，专门用于将关键帧的绘画风格传播到视频中，被广泛用于动画制作。
---

## 🚀 Open Source Projects
- **[LoRA-Edit](https://github.com/cjeen/LoRAEdit)** - 实现了基于 Mask 的 LoRA 首帧编辑传播。
- **[AnyV2V](https://github.com/TIGER-AI-Lab/AnyV2V)** - 一个通用的视频编辑框架，支持将任何图像编辑工具扩展到视频。
- **[Go-with-the-Flow](https://github.com/Eyeline-Research/Go-with-the-Flow)** - 使用光流引导的视频扩散模型编辑。
- **[CoDeF](https://github.com/QiangZhou/CoDeF)** - 官方实现的 Content Deformation Fields，支持高质量的视频重绘和编辑。
- **[TokenFlow](https://github.com/omerbt/TokenFlow)** - 官方实现，支持基于文本和关键帧的一致性编辑。
- **[I2VEdit](https://github.com/Vicky0522/I2VEdit)** - 首帧引导的 I2V 编辑代码。
---

## 🤝 Contributing

Contributions are welcome! If you know of any great resources related to First-Frame Video Editing that should be included, please feel free to share them.

### How to Contribute

Simply **open an issue** with the following information:

- **Resource Name**: The name of the tool/paper/dataset/etc.
- **Category**: Which section it belongs to (Papers, Tools, Datasets, etc.)
- **Link**: URL to the resource
- **Description**: Brief description of what it is and why it's useful
- **Tags** (optional): Year, conference, keywords, etc.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<div align="center">

**⭐ Star this repository if you found it helpful!**

</div>
