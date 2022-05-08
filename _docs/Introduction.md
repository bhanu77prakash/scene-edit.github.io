---
title: Introduction
category:
order: 1
---

Generating images from Scene Graphs is a challenging image generation task, where one wishes to convert a structural information about a scene into an image. In an example provided in the work by Johnson et al. [[cite]](https://arxiv.org/pdf/1804.01622.pdf),  
![example](images/example.png)  
we can clearly observe that traditional text-to-image generation methods struggle to understand complex sentences with many objects. Often, they find it hard to interpret the layout of the scene and the spatial relationships between the objects in the image. This is partly due to the complexity involved in representing the spatial structure through use of natual sentences. On the other hand, scene-graph is a stuctured mode of information with high degrees of information condensed into a format, which encodes the spatial relationships between the objects in form of edges of the graph. By inferring the relationships between any pair of objects in the scene, we can get a global understanding of the placement of the objects w.r.t one another. 
