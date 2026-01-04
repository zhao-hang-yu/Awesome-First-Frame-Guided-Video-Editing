<img width="2631" height="193" alt="image" src="https://github.com/user-attachments/assets/0b18f493-2bdf-428f-8ff5-0e42775beb7c" />

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
   > Introduction: A training-free method proposed for object-level editing (insertion, deletion, swapping). Although not purely reliant on the first frame, it solves the fidelity issues of propagation-based methods like GenProp under complex motions by dynamically fusing context information from the original video and the editing target (Adaptive Context Enrichment).

2. **FlowV2V: Consistent Video Editing as Flow-Driven Image-to-Video Generation**, 2025-06, https://arxiv.org/abs/2506.07713
   > Introduction: Explicitly decomposes video editing into "first-frame editing" and "flow-driven I2V generation". It utilizes Optical Flow as a strong geometric constraint to guide the I2V model in propagating the deformation of the first frame precisely to subsequent frames, significantly improving temporal consistency.

3. **LoRA-Edit: Controllable First-Frame-Guided Video Editing via Mask-Aware LoRA Fine-Tuning**, 2025-06, https://arxiv.org/abs/2506.10082
   > Introduction: Proposes a Mask-based LoRA fine-tuning method specifically for first-frame guided video editing. It can precisely control the editing area and protect the background, solving the problem of insufficient flexibility in subsequent frames found in existing methods.

4. **Go-with-the-Flow: Motion-Controllable Video Diffusion Models Using Real-Time Warped Noise**, 2025-01, https://arxiv.org/abs/2501.08331
   > Introduction: Utilizes Optical Flow and Warped Noise techniques to achieve control over video generation and stylization by editing the first frame, possessing extremely high temporal consistency.

5. **GenProp: Propagating Generation for Video Editing (CVPR 2025)**, 2024-12, https://arxiv.org/abs/2412.19761
   > Introduction: A generative video propagation framework proposed by Adobe Research. It leverages the prior knowledge of Image-to-Video (I2V) generation models to intelligently propagate edits on the first frame (including object removal, insertion, and shape changes) to the entire video.

6. **I2VEdit: First-Frame-Guided Video Editing via Image-to-Video Diffusion Models**, 2024-05, https://arxiv.org/abs/2405.16537
   > Introduction: Utilizes pre-trained Image-to-Video models to propagate edits on the first frame to the entire video through coarse motion extraction and appearance refinement, supporting both global and local editing.

7. **ReVideo: Remake a Video with Motion and Content Control**, 2024-05, https://arxiv.org/abs/2405.13865
   > Introduction: Allows users to control video content by modifying the first frame while controlling motion via trajectories, achieving decoupled editing of content and motion.

8. **AnyV2V: A Plug-and-Play Framework For Any Video-to-Video Editing Tasks**, 2024-03, https://arxiv.org/abs/2403.14468
   > Introduction: A plug-and-play framework with the core idea of "edit first frame + I2V generation". Compatible with any image editing tool (such as InstructPix2Pix), it uses I2V models for feature injection to maintain consistency.

9. **CoDeF: Content Deformation Fields for Temporally Consistent Video Processing (CVPR 2024)**, 2023-08, https://arxiv.org/abs/2308.07926
   > Introduction: Proposes "Canonical Content Field", decomposing video into a static panorama and deformation fields. Users only need to edit this static panorama (similar to a keyframe) to automatically propagate changes to the entire video.


---
**else**

It is also guided by the first frame, but not the "model's guidance for subsequent video editing based on the edited first frame uploaded by the user" that we are referring to.
1. **Unified Video Editing with Temporal Reasoner**, 2025-12, https://arxiv.org/abs/2512.07469
    > Introduction: Proposes a unified video editing framework with the core component being a "Temporal Reasoner". This method aims to uniformly handle rigid (e.g., style transfer) and non-rigid (e.g., action change) editing tasks, utilizing the reasoning capability of large models to parse editing instructions and maintain logical consistency over time. [Multi-task Unified Framework]

2. **In-Context Sync-LoRA for Portrait Video Editing**, 2025-12, https://arxiv.org/abs/2512.03013
    > Introduction: An editing method designed specifically for portrait/talking head videos. Adopts the In-Context LoRA paradigm, inputting the "source video" and "edited first frame" as context conditions into the model, rather than traditional feature injection. The core advantage lies in training with data filtered for synchronization, achieving frame-level precise synchronization of lip-sync, blinking, and gaze while significantly changing appearance. [Portrait Specific / In-Context Learning]

3. **First Frame Is the Place to Go for Video Content Customization**, 2025-11, https://arxiv.org/abs/2511.15700
    > Introduction: The starting point of the paper is to revisit the role of the "First Frame" in video generation models. Different perspective: video models implicitly view the first frame as a conceptual memory buffer. [Multi-object Editing into One Video]

4. **Edit-Your-Interest: Efficient Video Editing via Feature Most-Similar Propagation**, 2025-10, https://arxiv.org/pdf/2510.13084
    > Introduction: Utilizes Spatiotemporal Feature Memory (SFM) and Feature Most-Similar Propagation (FMP) to ensure lightweight and high definition, and uses cross-attention maps to automatically extract masks of objects of interest to achieve background preservation. [Text-Guided Video Editing]

5. **InsViE-1M: Effective Instruction-based Video Editing with Elaborate Dataset Construction (InsV2V)**, 2024-12, https://openaccess.thecvf.com/content/ICCV2025/html/Wu_InsViE-1M_Effective_Instruction-based_Video_Editing_with_Elaborate_Dataset_Construction_ICCV_2025_paper.html
    > Introduction: Although focused on instruction-based editing, the related work InsV2V explores the application of video generation models in editing and constructs a large-scale dataset, often compared with first-frame methods like AnyV2V.

6. **TokenFlow: Consistent Diffusion Features for Consistent Video Editing**, 2023-07, https://arxiv.org/abs/2307.10373
    > Introduction: Achieves video editing by enforcing feature consistency in the diffusion feature space. Supports keyframe editing mode, ensuring that edited features can propagate based on correspondences.

7. **Text2Video-Zero: Text-to-Image Diffusion Models are Zero-Shot Video Editors**, 2023-03, https://arxiv.org/abs/2303.13439
    > Introduction: Training-free, by reprogramming the attention mechanism (Cross-Frame Attention), it allows subsequent frames to reference the generation features of the first frame, achieving style transfer and editing.

8. **FateZero: Fusing Attentions for Zero-shot Text-based Video Editing**, 2023-03, https://arxiv.org/abs/2303.09535
    > Introduction: Zero-shot video editing method that maintains structure and motion by fusing attention maps during the inversion process. Although focused on text editing, its attention control mechanism is the foundation for many subsequent propagation methods.




---

## 🛠️ Tools

### Commercial & Web Tools
- **[Pika](https://pika.art/)** - Famous AI video generation tool. Its "Modify Region" or "Pikaframes" features allow users to control the first/last frames or specific regions for video editing and extension.
- **[Runway Gen-1/Gen-2](https://runwayml.com/)** - Offers "Video to Video" mode, allowing video generation driven by a reference image (first frame style).
- **[EbSynth (Software)](https://ebsynth.com/)** - Free and powerful tool, specifically used to propagate the painting style of keyframes to the video, widely used in animation production.

---

## 🚀 Open Source Projects
- **[LoRA-Edit](https://github.com/cjeen/LoRAEdit)** - Implements Mask-based LoRA first-frame edit propagation.
- **[Go-with-the-Flow](https://github.com/Eyeline-Research/Go-with-the-Flow)** - Video diffusion model editing guided by optical flow.
- **[I2VEdit](https://github.com/Vicky0522/I2VEdit)** - First-frame guided I2V editing code.
- **[ReVideo](https://github.com/MC-E/ReVideo)** - Aims to solve local video editing problems. Editing targets include modification of visual content and motion trajectories.
- **[AnyV2V](https://github.com/TIGER-AI-Lab/AnyV2V)** - A universal video editing framework supporting the extension of any image editing tool to video.
- **[CoDeF](https://github.com/ant-research/CoDeF)** - Decomposes video into a static panorama and deformation fields; editing just this static panorama automatically propagates to the entire video.
- The aforementioned ContextFlow, FlowV2V, and GenProp are not yet open source.



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
