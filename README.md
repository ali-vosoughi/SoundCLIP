# SoundCLIP: Can Sound Replace Vision in LLaVA With Token Substitution?

[Code is coming soon.. stay tuned]

🌐 **Live Demo**: [https://ali-vosoughi.github.io/SoundCLIP/](https://ali-vosoughi.github.io/SoundCLIP/)

📄 **Paper**: [Can Sound Replace Vision in LLaVA With Token Substitution? (ArXiv)](https://arxiv.org/abs/2506.10416)

📊 **Dataset**: [AVE-2 on HuggingFace](https://huggingface.co/datasets/ali-vosoughi/ave-2)

## Project Overview
This is the official project webpage for "Can Sound Replace Vision in LLaVA With Token Substitution?" featuring an interactive demonstration of our SoundCLIP framework and the fundamental trade-off between cross-modal retrieval and text generation.

## Authors
- **Ali Vosoughi** - University of Rochester ([Website](https://alivosoughi.com/))
- **Jing Bi** - University of Rochester ([Website](https://jing.vision/))
- **Pinxin Liu** - University of Rochester ([Website](https://andypinxinliu.github.io/))
- **Yunlong Tang** - University of Rochester ([Website](https://yunlong10.github.io/))
- **Chenliang Xu** - University of Rochester ([Website](https://www.cs.rochester.edu/~cxu22/index.html))

## 🔗 Quick Links
- 🌐 **Interactive Demo**: [https://ali-vosoughi.github.io/SoundCLIP/](https://ali-vosoughi.github.io/SoundCLIP/)
- 📄 **Paper**: [ArXiv:2506.10416](https://arxiv.org/abs/2506.10416)
- 💻 **Code**: [GitHub Repository](https://github.com/ali-vosoughi/SoundCLIP)
- 📊 **Dataset**: [AVE-2 on HuggingFace](https://huggingface.co/datasets/ali-vosoughi/ave-2)

## Key Contributions

### 1. AVE-2 Dataset
- **570,138 audio-visual clips** with revolutionary 5-dimensional alignment annotations
- Now available on HuggingFace with comprehensive documentation and usage examples
- Systematic scoring across: Temporal Alignment, Spatial Coherence, Contextual Relevance, Physical Causality, Sound Source Visibility

### 2. SoundCLIP Framework  
- **Token substitution approach**: Replace CLIP's [CLS] token with audio tokens in LLaVA
- **Two alignment strategies**: 
  - Projected: MLP projection to CLIP space (maximizes I(A;V), better retrieval)
  - Raw: Padded audio features (preserves H(A|V), better generation)
- **Lightweight integration**: Only 1.9M parameters for projection layer

### 3. Fundamental Trade-off Discovery
- **Retrieval vs Generation**: y = 0.163x + 11.867 relationship discovered
- Each percentage-point gain in retrieval incurs ~0.163% loss in generation quality


## Citation
If you use SoundCLIP or the AVE-2 dataset in your research, please cite our paper:

```bibtex
@article{vosoughi2025soundclip,
  title={Can Sound Replace Vision in LLaVA With Token Substitution?},
  author={Vosoughi, Ali and Bi, Jing and Liu, Pinxin and Tang, Yunlong and Xu, Chenliang},
  journal={ArXiv},
  year={2025}
}
```
