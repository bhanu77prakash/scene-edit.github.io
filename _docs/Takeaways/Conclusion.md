---
title: Conclusion
category: Takeaways
order: 5
---

In this work we have proposed a multi-staged pipeline for autocompleting incomplete scene graphs and generating the scenes with an explicit intermediate step of generating layout of the scene. We have proposed a method for large scale pretraining of the information encoded in scenes, which we could use for understanding the relationships between objects in the scenes. We also proposed a fine-tuning approach, which when fine-tuned on the pre-trained *Scene Encoder* model could perform the downstream task of automated scene completion with a very good accuracy. 

Owing to the challenges posed in choosing the candidates both in terms of the performance of the auto completion model and the inference overhead, we proposed a candidate selection alorithm. Our qualitative and quantitative analysis of the later two stages of the pipeline layout generation, and image generation prove our hypothesis that completely specified scene graphs lead to better and natural looking images. While quantitatively the IOU scores obtained in the layout generation are a bit on the lower side (due the discrepancy in direct comparison), the qualitative images obtained as the output indicate that the results are much better. 

The qualitative results obtained from the [*sg2im* model](../../Results/Fine-tuning) when we directly provide the scene graph as an input vs the qualitative results obtained from our pipeline of generating the layout first and then peforming the image generation task clearly indicates that the latter setup is more beneficial. Overall, our pipeline of autocomplete -> layout generation -> image generation performs much better both qualitatively and quantitatively when compared to its competitive baselines. 