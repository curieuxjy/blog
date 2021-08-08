---
toc: true
layout: post
description: GNN introduction
categories: [gnn]
title: Hello GNN
---

GNN에 관심을 가지게 된 계기는 [RoboGrammar](https://cdfg.mit.edu/publications/robogrammar-graph-grammar-for-terrain-optimized-robot-design)라는 [paper](https://cdfg.mit.edu/assets/files/robogrammar.pdf)였다. 예전부터 하고 싶었던 Robot design 아이디어를 GNN을 가지고 실현시킨 것이 너무 신기해서 공부해보고 싶었다. 이번 포스팅에서는 GNN과 첫만남인 만큼 공부할 자료들을 정리해보려 한다.

## Materials
- [Tobigs Graph Study](https://tobigs.gitbook.io/tobigs-graph-study)

- [CS224W: Machine Learning with Graphs](http://web.stanford.edu/class/cs224w) / [Videos](https://youtube.com/playlist?list=PL-Y8zK4dwCrQyASidb2mjj_itW2-YYx6-)

- [Graph Neural Networks - Penn Engineering](https://gnn.seas.upenn.edu/)

- [TF Graph Neural Network Samples](https://github.com/microsoft/tf-gnn-samples)

- [Graph Neural Networks in TF2](https://github.com/microsoft/tf2-gnn)

- [Graph Representation Learning(Pytorch)](https://github.com/dsgiitr/graph_nets)

- [A Gentle Introduction to Graph Neural Networks (Basics, DeepWalk, and GraphSage)](https://towardsdatascience.com/a-gentle-introduction-to-graph-neural-network-basics-deepwalk-and-graphsage-db5d540d50b3)

- [Invariant Graph Networks](https://slideslive.com/38917604) :  invariance, equivariance, k-WL GNN 관련 주제

- [End-to-End, Transferable Deep RL for Graph Optimization](https://ai.googleblog.com/2020/12/end-to-end-transferable-deep-rl-for.html) : RL + GNN

### Tutorials & Workshops

- [WWW 18 Tutorial : Representation Learning on Networks](http://snap.stanford.edu/proj/embeddings-www/)

- [CIKM 19 Tutorial : Recent Developments of Deep Heterogeneous Information Network Analysis](http://shichuan.org/CIKM19_Tutorial.html)

- [WSDM 19 Tutorial : Learning and Reasoning on Graph for Recommendation](https://next-nus.github.io/)

- [KDD 19 Tutorial : Learning From Networks](https://learningnets.github.io/KDD19_Tutorial/)

- [AAAI 20 Tutorial : Graph Neural Networks: Models and Applications](http://cse.msu.edu/~mayao4/tutorials/aaai2020/)

- [ICML2020 GNN Workshop GRL+](https://grlplus.github.io/)

- [WWW 20 Hands on Tutorial](https://github.com/dglai/WWW20-Hands-on-Tutorial) - [Videos](https://youtu.be/bD6S3xUXNds)

- [Graph Neural Networks for Natural Language Processing](https://github.com/svjan5/GNNs-for-NLP) / [PPT](https://shikhar-vashishth.github.io/assets/pdf/emnlp19_tutorial.pdf)

- [Tutorial on Spectral and Graph ConvNets](http://www.ipam.ucla.edu/abstract/?tid=15786&pcode=GLTUT)


### Papers & Survey
- [Graph Neural Networks: Taxonomy, Advances and Trends](https://arxiv.org/abs/2012.08752)

- [A Comprehensive Survey on Graph Neural Networks](https://arxiv.org/pdf/1901.00596.pdf)

- [Directional Graph Networks](https://arxiv.org/abs/2010.02863)

- GNN KR [Paper List](https://github.com/GNN-KR/paper_list)

- [Graph Meta Learning via Local Sub-graphs](https://zitniklab.hms.harvard.edu/projects/G-Meta/)
    - Meta-GNN: On Few-shot Node Classification in Graph Meta-learning
    - Few-shot Learning with Graph Neural Networks
    - Learning to Propagate for Graph Meta-Learning

- [Self-supervised Training of Graph Convolutional Networks](https://arxiv.org/pdf/2006.02380v1.pdf)

- [XGNN: Towards Model-Level Explanations of Graph Neural Networks](https://arxiv.org/pdf/2006.02587v1.pdf)

- [L2-GCN: Layer-Wise and Learned Efficient Training of Graph Convolutional Networks, 2020 CVPR](https://arxiv.org/pdf/2003.13606v5.pdf)

### Videos 

#### An Introduction to Graph Neural Networks: Models and Applications

{{< youtube zCEYiCxrL_0 >}}

#### Graph Convolutional Networks using only NumPy

{{< youtube 8qTnNXdkF1Q >}}

#### Geometric Deep Learning on Graphs and Manifolds

{{< youtube LvmjbXZyoP0 >}}

#### Graph Nets: The Next Generation
* [Link](https://www.ias.edu/video/machinelearning/2020/0721-MaxWelling)

{{< youtube Wx8J-Kw3fTA >}}

#### Recent Developments of Graph Network Architectures
* [Slide](https://rb.gy/quo3n6)
* 2019-2020에 발표된 GNN 방법론들을 정리
* GNN의 expressiveness, 그중에서도 invariance and equvariance

{{< youtube M60huxIvKbE >}}

#### Deep learning on graphs: successes, challenges, and next steps

{{< youtube PLGcx65MhCc >}}

#### Graph Representation Learning for Algorithmic Reasoning
- [Slide](https://petar-v.com/talks/Algo-WWW.pdf)

{{< youtube IPQ6CPoluok >}}

#### How Uber uses Graph Neural Networks to recommend you food
- [Post](https://eng.uber.com/uber-eats-graph-learning/)

{{< youtube 9O9osybNvyY >}}