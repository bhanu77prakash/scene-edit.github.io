---
title: Datasets
category:
order: 3
---

Throughout the different stages of our experiments, we have used the following three datasets 
1. COCO-stuff
2. Visual Genome
3. VG-MSDN

Details of the datasets are as follows. 

**COCO-stuff**

The dataset is proposed in the [COCO-stuff](https://arxiv.org/pdf/1612.03716.pdf) paper. This dataset is an augmented dataset on top of the original [COCO](https://arxiv.org/pdf/1405.0312.pdf) dataset with additional stuff catefories. A total of 80 *thing* categories like car, dog, cat, etc.. and 91 *stuff* categories like sky, snow, etc ... are available in the dataset. This dataset is more closer to the VG-MSDN dataset compared to the original COCO dataset. There are a total of 118K annotated training images and 5K validation images. The annotations contain the regions where the objects are present in the corresponding images. In addition to the regions, the relationships are also annotated. The relationships are provided in detail in the [sg2im](https://arxiv.org/pdf/1804.01622.pdf) paper. Instead of the complete relationships provided in the VG dataset, this dataset uses the main 6 geometric relationships that are important for layout description - *left of, right of, above, below, inside*, and *surrounding*. 

The dataset can be downloaded from [here](https://github.com/nightrome/cocostuff). 

**Visual Genome**

The visual genome is a large scale annotated dataset with complete description of the scenes through scene graphs i.e relation triples. It places equal emphasis on the object relationships and attributes as it does on objects themselves. While the relationships mostly capture the actions, properties and spatial information of the objects in the scene, the object attributes encode the aspects of the objects themselves. For example the aspects like *color* (yellow fire hydrant), *orientation* (standing woman), etc. are captured through the attributes and the things like *jumping over*, *is behind*, *wear*, *with* etc.. are captured through the relationships. It also captures image narratives that are non-salient e.g. subplots occurring in the background of images. Each object is defined by a bounding box and object attributes. The relationships between objects are present in form of triples. Each region of the image is present with a subgraph i.e disconnected graphs are possible. It also has QA pairs allowing for VQA tasks, and descriptions useful for captioning the images. In total there are 108,077 images with 5.4 million descriptions (on average 42 per image), and 1.7 million VQA pairs. We use the 3.8 Million object instances, 2.8 million attributes and 2.3 million relationships for the scope of this project. 

The dataset can be found [here](https://visualgenome.org/)

**VG-MSDN**

The original Visual Genome dataset has a very large number of objects and relations. In total we found around 65K object types and 36K relation types in the dataset. While for pre-training task this is useful, for the layout and image generation tasks, learning over such huge space is very difficult. Therefore we use the VG-MSDN dataset which is a proper subset of the Visual Genome dataset. The dataset is proposed in the [Factorizable Net](https://arxiv.org/pdf/1806.11538.pdf) paper. The datset consisits of more than 46K training images and 10K test images. The 46,164 images constists of a total of 507,296 triples and the test 10K images consists of 111,396 triples. The number of objects in both the splits is 150 and the number of different types of relations is set to 50. The objects and the relations are the most frequently occurring classes in the original VG dataset. We use this dataset for finetuning of scene graph autocompletion, layout generation and image generation tasks. 

The dataset can be downloaded from [here](https://drive.google.com/file/d/1WjetLwwH3CptxACrXnc1NCcccWUVDO76/view).