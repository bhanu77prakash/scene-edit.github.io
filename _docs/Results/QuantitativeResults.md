---
title: Layout Guided Generation - Quantitative Results
category: Results
order: 4
---

In this section, we present the quantitative performance of our proposed scene graph completion technique by evaluating its performance on the layout generation and the image generation modules.

We have reported the results on the following three experimental settings:

- **Missing SG**:
    In this setup, we mask random relations and tail objects of the triplets in the scene graph. This masked scene graph is passed through the layout generation module and the resulting layout is used for generating the final image.

- **Predicted SG**:
    In this setup, we predict the missing relations and objects using our proposed method. This completed scene graph is then used for subsequent layout and image generation.

- **Ground-truth SG**:
    In this setup, the layout and the image are generated using the ground truth scene graphs without any modifications. This setup acts as a baseline for comparing the other settings.

The above experiments are performed on a subset of Visual Genome dataset.





We evaluate the performance of the Image Generation module by calculating the fid score of the generated images. The results are tabulated below:


| Experimental Setting | FID     |
|----------------------|---------|
| Missing SG           | 139.517 |
| Predicted SG         | 138.696 |
| Ground-truth SG      | 138.646 |



As can be seen the fid score (lower the better) for the Ground-truth SG is the better than other settings and the Missing SG fid score is the worst. Though the absolute difference between different fid scores are not significant, the generated images using the Predicted SGs look more natural and coherent when compared to the images generated using Missing SGs. The qualitative results are presented in the [next section](link)............