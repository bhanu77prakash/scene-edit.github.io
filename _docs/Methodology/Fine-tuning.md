---
title: Fine-Tuning
category: Methodology
order: 2
---

After pre-training the Scene Encoding model, we perform task specific fine-tuning for predicting the missing objects and relations. 

> Setup

Given an incomplete scene graph, our objective is to estimate the missing objects and relationships between the objects. The fine-tuning setup is very similar to the [pre-training](../Pre-training) framework. The input is represented in form of the triples available and the missing elements / triples are represented through masks or by *DEL* separated inputs. The architecture used for the fine-tuning is as follows:
<center>
<img src="../../images/fine-tune.png" alt="example" style="width:900px;"/>
<br>
</center>

The layers of the model are initialized with the learnt parameter values from the pre-training setup. The output layers are initialized from scratch. As observed from the figure, there are two setups that we have experimented with. 

<h4>Setup a </h4>
In this setup we assume that a candidate triple is provided to us, which requires us to predict whether it belongs to the input scene or not. 