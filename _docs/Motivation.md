---
title: Motivation
category:
order: 0
---
> What is our motivation and why is this important to solve? 

Image generation is an important problem in the CV domain and has many applications like use scene generation in the animation industry, addressing data scarcity in ML training by creating bigger datasets with more variations, generating adversarial examples for robust training of models, etc.. One approach for image synthesis which has gained popularity in the last few years is the use of scene graphs for image generation. Scene graph is a structured representation of a scene that can clearly express the objects, attributes, and relationships between objects in the scene and is discussed in detail in ([Survey](https://arxiv.org/pdf/2104.01111.pdf)). If we have such a system, a natural next step will be to modify the scene graph to generate more variations of an image. 

> Questions to ponder ..

But will the modification in scene graphs always lead to natural-looking images? If the user describes the image as a scene graph, can we intelligently add more nodes to the defined graph so that the generated image is (more) natural? We wish to explore these questions in our project and work on improving the neural synthesis of images using semantically guided graphical representations.


> But, where would this be helpful? 

Multimodal question answering (MQA) is a fast-evolving domain in the machine learning community and has numerous applications like making better search engines/ chatbots which are capable of handling multimodal inputs, hence improving the interaction and usability of such systems. Most of the current MQA solutions rely on scene-graph image pairs for training their models ([GQA](https://arxiv.org/pdf/1902.09506.pdf)). Hence such systems are bottlenecked by the availability of this scene graph - image information which currently is a manual curation step. In addition to this, the variability of images in existing datasets is very low, which plateaus the generalizability of the models trained from this data. We believe our project will help make this dataset curation process automatic and more robust, allowing the generation of a huge variety of image-scenegraph pairs which could help further the research in the MQA domain.
