# SoundCLIP Project Webpage - Can Sound Replace Vision in LLaVA?

## Project Overview
This is the official project webpage for "Can Sound Replace Vision in LLaVA With Token Substitution?" featuring an interactive demonstration of our SoundCLIP framework and the fundamental trade-off between cross-modal retrieval and text generation.

## Authors
- **Ali Vosoughi** - University of Rochester ([Website](https://alivosoughi.com/))
- **Jing Bi** - University of Rochester ([Website](https://jing.vision/))
- **Pinxin Liu** - University of Rochester ([Website](https://andypinxinliu.github.io/))
- **Yunlong Tang** - University of Rochester ([Website](https://yunlong10.github.io/))
- **Chenliang Xu** - University of Rochester ([Website](https://www.cs.rochester.edu/~cxu22/index.html))

## Key Contributions

### 1. AVE-2 Dataset
- **580,145 audio-visual clips** with revolutionary 5-dimensional alignment annotations
- Systematic scoring across: Temporal Alignment (7.54), Spatial Coherence (8.35), Contextual Relevance (6.32), Physical Causality (9.02), Sound Source Visibility (8.04)

### 2. SoundCLIP Framework  
- **Token substitution approach**: Replace CLIP's [CLS] token with audio tokens in LLaVA
- **Two alignment strategies**: 
  - Projected: MLP projection to CLIP space (maximizes I(A;V), better retrieval)
  - Raw: Padded audio features (preserves H(A|V), better generation)
- **Lightweight integration**: Only 1.9M parameters for projection layer

### 3. Fundamental Trade-off Discovery
- **Retrieval vs Generation**: y = 0.163x + 11.867 relationship discovered
- Each percentage-point gain in retrieval incurs ~0.163% loss in generation quality

## Interactive Demo Features
- **7 curated examples** from AVE-2 dataset with embedded audio
- **Quality threshold**: ≥42.0/50 (top-performing samples only)
- **Real-time encoder comparison**: Switch between Raw and Projected modes
- **Consistent video display**: Fixed dimensions (400×225px) for uniform presentation

## File Structure
- `index.html`: Main project webpage with interactive demonstration
- `videos/`: Video clips from AVE-2 dataset with embedded audio (7 files)
- `images/`: Fallback frame images (7 files)
- `README.md`: This documentation

## Links
- **Paper**: [ArXiv](https://arxiv.org/abs/2506.10416)
- **Code**: [GitHub Repository](https://github.com/ali-vosoughi/SoundCLIP)
- **Dataset**: AVE-2 (available upon publication)

## Citation
```bibtex
@article{vosoughi2025soundclip,
  title={Can Sound Replace Vision in LLaVA With Token Substitution?},
  author={Vosoughi, Ali and Bi, Jing and Liu, Pinxin and Tang, Yunlong and Xu, Chenliang},
  journal={ArXiv},
  year={2025}
}
```

Generated: 2025-08-05 05:43:07
University of Rochester Computer Science Department
