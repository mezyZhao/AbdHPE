# AbdHPE🧠
Learning Abductive Relationships for Human Pose Estimation via Syntactic Holistic Perception 
## 🔍 Overview

Human pose estimation becomes especially challenging when target joints are occluded, visually ambiguous, or confused with background distractors. In such cases, local texture evidence alone is often insufficient. AbdHPE addresses this limitation by introducing abductive anatomical reasoning into deep pose estimation.

## 📌 Abstract

Robustly estimating human pose under severe occlusion and visual ambiguity has attracted significant attention in computer vision. Previous studies largely rely on explicit visual matching, which often fails when visual evidence is missing or incomplete.

Our study shows that human pose estimation is governed by multi-level abductive anatomical relationships, while only a sparse subset of visual evidence is truly informative for localizing a target keypoint. Motivated by this observation, we propose a novel abductive human pose estimation network, **AbdHPE**, which infers global structure by jointly modeling local observations and logical reasoning.

Specifically, we design an abductive relationship mining module to reconstruct fractured texture evidence chains within deep networks. Then, we construct a syntactic holistic perception module based on an abductive agent, which adaptively focuses on keypoint-relevant evidence and enforces skeletal topological constraints in the feature space.

AbdHPE is evaluated on multiple pose estimation benchmarks, including COCO, MPII, CrowdPose, OCHuman, and AP-10K. Extensive quantitative and qualitative experiments demonstrate that AbdHPE yields robust estimation results and achieves state-of-the-art performance.

## 🚀 Main Contributions

1. **Unified Abductive Modeling Framework**

   We propose a unified framework to explicitly characterize hierarchical dependencies across keypoints, limbs, and holistic pose. This enables ambiguous joints to be inferred from multi-level anatomical constraints in an evidence-driven manner.

   An abductive agent is further introduced to prioritize informative body-centric cues while suppressing distractors, reconciling fine-grained local precision with global structural coherence.

2. **ARM and SHP for Global Consistency**

   Two complementary modules are designed to enforce global consistency.

   - The **ARM module** excavates latent correlations across feature hierarchies to guide multi-level relational reasoning among keypoints and limbs.
   - The **SHP module**, built around an abductive agent, actively selects and aggregates torso-relevant evidence to infer a coherent holistic configuration.

   This design enables plausible pose completion when local visual cues are limited.

3. **Strong Benchmark Performance and Generalization**

   AbdHPE demonstrates competitive performance on the MS COCO, MPII, CrowdPose, OCHuman, and AP-10K datasets. It effectively handles varied poses, occlusion, and complex backgrounds by mitigating visual biases and reducing structural errors.

   AbdHPE also shows encouraging zero-shot generalization under unseen poses, imaging conditions, and moderate domain shifts without additional fine-tuning.

## 🧩 Method

AbdHPE follows an abductive reasoning paradigm for pose estimation:

1. Extract local and hierarchical visual features from the input image.
2. Mine abductive relationships among fragmented visual evidence, keypoints, and limbs.
3. Use an abductive agent to select informative skeletal evidence while suppressing irrelevant distractors.
4. Enforce holistic skeletal topology in feature space.
5. Predict keypoint heatmaps with improved local accuracy and global structural consistency.

## 📊 Benchmarks

AbdHPE is evaluated on standard pose estimation benchmarks:

- **MS COCO**
- **MPII Human Pose**
- **CrowdPose**
- **OCHuman**
- **AP-10K**

  
## 📝 Citation

If this work is helpful for your research, please cite AbdHPE. The BibTeX entry will be provided after publication.

```bibtex
@article{abdhpe,
  title   = {AbdHPE: Learning Abductive Relationships for Human Pose Estimation via Syntactic Holistic Perception},
  author  = {Hai Liu and Ziyi Zhao and Chongxin Zheng and Tingting Liu and Zhaoli Zhang and You-Fu Li},
  journal = {IEEE Transactions on Circuits and Systems for Video Technology},
  year    = {2026},
}
```

## 🏷️ Keywords

Human pose estimation, abductive relationships, syntactic holistic perception, image understanding, computer vision.

## 📄 License

The license will be specified when the code is released.
