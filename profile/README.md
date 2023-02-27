
<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->


# 🚀🚀🚀 🔥🔥🔥DETRs with Hybrid Matching, arXiv 2022

[![arXiv](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/abs/2207.13080)
![visitors](https://visitor-badge.glitch.me/badge?page_id=HDETR&left_color=blue&right_color=green)

## News

⛽⛽⛽ [MSRA-VC-Group] is hiring research interns to push the frontier cutting-edge technology of object detection and segmentation. Contact: [yuhui.yuan@microsoft.com](yuhui.yuan@microsoft.com)

**2023.02.28** HDETR has been accepted by CVPR 2023 😉😉😉

**2022.11.25** Optimized implementation for hybrid matching is released at [pull-request](https://github.com/HDETR/H-Deformable-DETR/pull/12), which parallelizes the matching/loss computations of one2one branch and one2many branch. 🍺🍺🍺 credits to [Ding Jia](https://github.com/JiaDingCN) 🍺🍺🍺

**2022.11.17** Code for [H-Detic-LVIS](https://github.com/HDETR/H-Detic-LVIS) is released. 🍺🍺🍺 credits to [Haodi He](https://github.com/hardyho) 🍺🍺🍺

**2022.11.10** Code for [H-TransTrack](https://github.com/HDETR/H-TransTrack) is released. 🍺🍺🍺 credits to [Haojun Yu](https://github.com/HaojunYuPKU) 🍺🍺🍺

**2022.10.20** 🎉🎉🎉[Detrex](https://github.com/IDEA-Research/detrex) have supported our [H-Deformable-DETR](https://github.com/IDEA-Research/detrex/blob/main/projects/h_deformable_detr/README.md) 🍺🍺🍺 credits to [Ding Jia](https://github.com/JiaDingCN) and [Tianhe Ren](https://github.com/rentainhe) 🍺🍺🍺

**2022.09.12** Our [H-Deformable-DETR w/ Swin-L]() achieves **58.2** AP on COCO val with **4-scale feature maps**, thus achieving comparable (slightly better) results then the very recent [DINO-DETR w/ Swin-L](https://github.com/IDEACVR/DINO#36-epoch-setting) equipped with **4-scale feature maps**.

**2022.08.31** Code for [H-Deformable-DETR-mmdet](https://github.com/HDETR/H-Deformable-DETR-mmdet) (**support mmdetection2d**) is released. We will also release the code for [H-Mask-Deformable-DETR](https://github.com/HDETR/H-Mask-Deformable-DETR) soon (**strong results on both instance segmentation and panoptic segmentation**).

**2022.08.07** Code for [H-PETR-3D](https://github.com/HDETR/H-PETR-3D) (**strong results on nuScenes**) and [H-PETR-Pose](https://github.com/HDETR/H-PETR-Pose) (**strong results on COCO pose estimation**) is released.

**2022.08.01** Code for [H-Deformable-DETR](https://github.com/HDETR/H-Deformable-DETR) (**strong results on COCO object detection**) is released.

**2022.07.27** HDETRs has been released to arXiv. The code will be released soon, please stay tuned. 


## Introduction
One-to-one set matching is a key design for DETR to establish its end-to-end capability, so that object detection does not require a hand-crafted NMS (non-maximum suppression) method to remove duplicate detections. This end-to-end signature is important for the versatility of DETR, and it has been generalized to a wide range of visual problems, including instance/semantic segmentation, human pose estimation, and point cloud/multi-view-images based detection, etc. However, we note that because there are too few queries assigned as positive samples, the one-to-one set matching significantly reduces the training efficiency of positive samples. This paper proposes a simple yet effective method based on a hybrid matching scheme that combines the original one-to-one matching branch with auxiliary queries that use one-to-many matching loss during training. This hybrid strategy has been shown to significantly improve training efficiency and improve accuracy. In inference, only the original one-to-one match branch is used, thus maintaining the end-to-end merit and the same inference efficiency of DETR. The method is named H-DETR, and it shows that a wide range of representative DETR methods can be consistently improved across a wide range of visual tasks, including Deformable-DETR, 3DETR/PETRv2, PETR, and TransTrack, among others.

- The HDETR architecture:

![teaser](profile/HDETR_framework.png)

## Experiments

![teaser](profile/HDETR_main_results.png)


## Citing H-DETR
If you find H-DETR useful in your research, please consider citing:
```bibtex
@article{jia2022detrs,
  title={DETRs with Hybrid Matching},
  author={Jia, Ding and Yuan, Yuhui and He, Haodi and Wu, Xiaopei and Yu, Haojun and Lin, Weihong and Sun, Lei and Zhang, Chao and Hu, Han},
  journal={arXiv preprint arXiv:2207.13080},
  year={2022}
}
```

