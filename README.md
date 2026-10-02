# Projected Audio Tokens Gain Retrieval and Lose Grounded Generation in Multimodal LLMs

Ali Vosoughi, Jing Bi, Pinxin Liu, Yolo Y. Tang, Chenliang Xu

Preprint; submitted to ICASSP 2027

🌐 **Project Page**: [https://ali-vosoughi.github.io/SoundCLIP/](https://ali-vosoughi.github.io/SoundCLIP/)

📄 **Paper**: [Frozen ICASSP 2027 submission](paper/main.pdf)

📊 **Dataset**: [AVE-2 on HuggingFace](https://huggingface.co/datasets/ali-vosoughi/ave-2)

## Project Overview
This is the official project webpage for "Projected Audio Tokens Gain Retrieval and Lose Grounded Generation in Multimodal LLMs". SoundCLIP compares raw and projected audio tokens in frozen LLaVA-1.6 with a Mistral-7B language backbone. The study measures audio-to-video retrieval, grounded caption generation, and representation geometry. These comparisons do not identify a causal mechanism.

## Authors
- **Ali Vosoughi** - University of Rochester ([Website](https://alivosoughi.com/))
- **Jing Bi** - University of Rochester ([Website](https://jing.vision/))
- **Pinxin Liu** - University of Rochester ([Website](https://andypinxinliu.github.io/))
- **Yolo Y. Tang** - University of Rochester ([Website](https://yoloytang.me/))
- **Chenliang Xu** - University of Rochester ([Website](https://www.cs.rochester.edu/~cxu22/index.html))

## 🔗 Quick Links
- 🌐 **Project Page**: [https://ali-vosoughi.github.io/SoundCLIP/](https://ali-vosoughi.github.io/SoundCLIP/)
- 📄 **Paper**: [Frozen ICASSP 2027 submission](paper/main.pdf)
- 💻 **Code**: [GitHub Repository](https://github.com/ali-vosoughi/SoundCLIP)
- 📊 **Dataset**: [AVE-2 on HuggingFace](https://huggingface.co/datasets/ali-vosoughi/ave-2)

## Key Contributions

### 1. AVE-2 Dataset
- The corrected local rebuild contains **570,138 three-second audio-video segments** sourced from AudioSet.
- AVE-2 provides visible and invisible active-source fields. The study uses AVE-2 for evaluation and geometry analysis.
- The evaluation pool contains **1,006 clips**, yielding **1,010 clip-segments** for generation scoring; geometry is measured on **3,568 disjoint paired clips**.

### 2. SoundCLIP Framework
- **Token substitution**: Replace the visual class token in frozen LLaVA-1.6-Mistral-7B with an audio token, retaining selected visual patch tokens.
- **Two token constructions**:
  - Projected: A three-layer MLP maps frozen audio-encoder features into CLIP's visual space.
  - Raw: Audio-encoder features are padded or truncated to 1,024 dimensions without the learned visual mapping.
- The study compares **five frozen audio encoders** at visual patch-token budgets **k = 15** and **k = 150**.

### 3. Retrieval and Grounded Generation
- Projection raises audio-to-video R@1 for every encoder on the evaluation pool, including ImageBind from **0.10% to 15.7%**. CLAP and Whisper R@1 values are lower bounds for their original encoder configurations.
- At **k = 150**, the caption-to-audio grounding score B1 decreases by **23–53%** and source recall B3 by **31–48%** relative to raw tokens. Interpret CLAP B1 with B3 because the encoder and scorer share a checkpoint family.
- Projection increases alignment with visual embeddings while orthogonal residual and nearest-neighbor overlap with the raw audio graph decrease. These are associations, not evidence of a causal mechanism.
- Raw-over-projected generation scores predominate across **five frozen backbones from 7B to 34B** wherever raw-token generation is stable.

## Citation
If you use SoundCLIP or the AVE-2 dataset in your research, please cite our paper:

```bibtex
@unpublished{vosoughi2026soundclip,
  title={{Projected Audio Tokens Gain Retrieval and Lose Grounded Generation in Multimodal LLMs}},
  author={Vosoughi, Ali and Bi, Jing and Liu, Pinxin and Tang, Yolo Y. and Xu, Chenliang},
  note={Preprint; submitted to ICASSP 2027},
  year={2026},
  url={https://ali-vosoughi.github.io/SoundCLIP/paper/main.pdf}
}
```
