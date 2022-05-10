---
title: Future Work
category: Takeaways
order: 6
---

To the best of our knowledge, this is one of the first attempts to autocomplete a scene and make use of layout generation as an explicit intermediate step for image generation from scene graphs. While we have achieved much better results in case of missing triples compared to the competitive baselines, we still have some questions unanswered. 

We have assumed that the missing triples in the scene would be mostly one or two common objects and relationships between these objects and the existing ones. However, in real case scenario, it is often possible that the entire background could be missing. While a person is explaining more about the objects of interest such as *boy*, *kite*, *thread*, they might be leaving the details about the background entirely. Though our autocomplete model predicts these to some extent, we hypothesize that a 2 channel framework - one for foreground and one for background - would perform the task of autocompletion much better. This would also help to improve the later stages of the pipeline.

While we have experimented with all stages of the pipeline, currently our stages are individually trained i.e independent from each other. However, we believe that if we train the models end-to-end, we can get additional benefits of choosing missing objects based on the layout possible in the provided image. For example it is possible that a *car* is not sufficient to put in a scene that is describing a *bus* depending on the details surrounding the *bus* object itself. While the scene autocomplete model is trying to complete the scene from a traffic point of view, the actual scene might be describing more about the details of a single bus parked on road.

Finally, while we have used the standard metrics of accuracy for understanding the results of autocompletion, IOU score for layout generation, and FID scores for image generation, we believe that we require a new metric to properly understand the benefits obtained by scene auto completion both in individual stages and the pipeline as a whole. 
