# SoundCLIP: Can Sound Replace Vision in LLaVA With Token Substitution?

🌐 **Live Demo**: [https://ali-vosoughi.github.io/SoundCLIP/](https://ali-vosoughi.github.io/SoundCLIP/)

📄 **Paper**: [Can Sound Replace Vision in LLaVA With Token Substitution? (ArXiv)](https://arxiv.org/abs/2506.10416)

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
- 📚 **Dataset**: AVE-2 (available upon publication)

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

## 🚀 GitHub Pages Deployment

This repository is configured for GitHub Pages deployment:

1. **Live Site**: [https://ali-vosoughi.github.io/SoundCLIP/](https://ali-vosoughi.github.io/SoundCLIP/)
2. **Source**: The `main` branch serves the GitHub Pages site
3. **Entry Point**: `index.html` in the root directory

### Local Development
```bash
# Clone the repository
git clone https://github.com/ali-vosoughi/SoundCLIP.git
cd SoundCLIP

# Open the demo locally
open index.html  # macOS
# or
start index.html  # Windows
# or
xdg-open index.html  # Linux
```

## File Structure
- `index.html`: Main project webpage with interactive demonstration
- `videos/`: Video clips from AVE-2 dataset with embedded audio (7 files)
- `images/`: Fallback frame images (7 files)
- `README.md`: This documentation

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

## Contact
For questions about this work, please contact:
- Ali Vosoughi: [avosough@ur.rochester.edu](mailto:avosough@ur.rochester.edu)
- Chenliang Xu: [chenliang.xu@rochester.edu](mailto:chenliang.xu@rochester.edu)

---
Generated: 2025-08-05 05:55:23  
University of Rochester Computer Science Department
