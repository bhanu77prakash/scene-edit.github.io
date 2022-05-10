---
title: Related Work
category:
order: 2
---

[Scene Graphs](https://arxiv.org/pdf/2104.01111.pdf), are graphical structures that represent scenes as directed graphs where the nodes are the different objects present in the scene and the edges are the relationships that exist between these objects. There are several works that utilize scene graphs for a variety of [vision](https://openaccess.thecvf.com/content_cvpr_2015/papers/Johnson_Image_Retrieval_Using_2015_CVPR_paper.pdf) and [language tasks.](https://arxiv.org/pdf/1607.08822.pdf)

In this project we focus on generating natural images from incomplete scene graphs. Existing works that generate images from scene graphs can be broadly categorized into two approaches. Methods in the  first approach directly generates images from scene graphs in a single stage while the works using the second approach first generates the image layout from the scene graph and then generates the image from the layout. The following subsections outlines varies works that falls under all these categories.

> Scene Graph to Image generation
<center>
<img src="../images/sg_img.png" alt="example" style="width:500px;"/>
<br>
</center>
> Scene Graph to Layout generation
<center>
<img src="../images/sg_lt.png" alt="example" style="width:500px;"/>
<br>
</center>

> Layout to Image generation
<center>
<img src="../images/lt_img.png" alt="example" style="width:500px;"/>
<br>
</center>

> Interactive Image generation
<center>
<img src="../images/int_sg.png" alt="example" style="width:500px;"/>
<br>
</center>