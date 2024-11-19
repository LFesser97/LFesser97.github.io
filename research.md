---
layout: default
title: "Research"
---

# Research

Welcome to my research page. Below are selected projects and publications. Please refer to my [CV](https://lfesser97.github.io/assets/pdfs/Resume_2024.pdf) or [Google Scholar](https://scholar.google.co.uk/citations?user=c1wgSpMAAAAJ&hl=en) for a complete list.

## Geometric Deep Learning Foundations

### Unitary Convolutions for Learning on Graphs and Groups

<img src="/assets/images/unitary_message_passing.png" alt="Unitary Graph Convolutions" style="float: left; margin-right: 20px; width: 400px;">

Group-convolutional architectures, which encode symmetries as inductive bias, have shown great success in applications, but can suffer from instabilities as their depth increases and often struggle to learn long range dependencies in data. For instance, graph neural networks experience instability due to the convergence of node representations (over-smoothing), which can occur after only a few iterations of message-passing, reducing their effectiveness in downstream tasks. Here, we propose and study unitary group convolutions, which allow for deeper networks that are more stable during training. The main focus of the paper are graph neural networks, where we show that unitary graph convolutions provably avoid over-smoothing. Our experimental results confirm that unitary graph convolutional networks achieve competitive performance on benchmark datasets compared to state-of-the-art graph neural networks. 

- **Authors**: Bobak Kiani, Lukas Fesser, Melanie Weber.
- **Venue**: Advances in Neural Information Processing Systems 37 (NeurIPS 2024), Spotlight.
- **Links**: [Paper](https://arxiv.org/abs/2410.05499), [GitHub Repository](https://github.com/Weber-GeoML/Unitary_Convolutions).

## Curvature in Graph Machine Learning

### Effective Structural Encodings via Local Curvature Profiles

Structural and Positional Encodings can significantly improve the performance of Graph Neural Networks in downstream tasks. Recent literature has begun to systematically investigate differences in the structural properties that these approaches encode, as well as performance trade-offs between them. However, the question of which structural properties yield the most effective encoding remains open. In this paper, we investigate this question from a geometric perspective. We propose a novel structural encoding based on discrete Ricci curvature (Local Curvature Profiles, short LCP) and show that it significantly outperforms existing encoding approaches. We further show that combining local structural encodings, such as LCP, with global positional encodings improves downstream performance, suggesting that they capture complementary geometric information. Finally, we compare different encoding types with (curvature-based) rewiring techniques. Rewiring has recently received a surge of interest due to its ability to improve the performance of Graph Neural Networks by mitigating over-smoothing and over-squashing effects. Our results suggest that utilizing curvature information for structural encodings delivers significantly larger performance increases than rewiring.

### Mitigating Over-Smoothing and Over-Squashing Using Augmentations of Forman-Ricci Curvature

While Graph Neural Networks (GNNs) have been successfully leveraged for learning on graph-structured data across domains, several potential pitfalls have been described recently. Those include the inability to accurately leverage information encoded in long-range connections (over-squashing), as well as difficulties distinguishing the learned representations of nearby nodes with growing network depth (over-smoothing). An effective way to characterize both effects is discrete curvature: Long-range connections that underlie over-squashing effects have low curvature, whereas edges that contribute to over-smoothing have high curvature. This observation has given rise to rewiring techniques, which add or remove edges to mitigate over-smoothing and over-squashing. Several rewiring approaches utilizing graph characteristics, such as curvature or the spectrum of the graph Laplacian, have been proposed. However, existing methods, especially those based on curvature, often require expensive subroutines and careful hyperparameter tuning, which limits their applicability to large-scale graphs. Here we propose a rewiring technique based on Augmented Forman-Ricci curvature (AFRC), a scalable curvature notation, which can be computed in linear time. We prove that AFRC effectively characterizes over-smoothing and over-squashing effects in message-passing GNNs. We complement our theoretical results with experiments, which demonstrate that the proposed approach achieves state-of-the-art performance while significantly reducing the computational cost in comparison with other methods. Utilizing fundamental properties of discrete curvature, we propose effective heuristics for hyperparameters in curvature-based rewiring, which avoids expensive hyperparameter searches, further improving the scalability of the proposed approach.

### Augmentations of Forman's Ricci Curvature and their Applications in Community Detection

The notion of curvature on graphs has recently gained traction in the networks community, with the Ollivier–Ricci curvature (ORC) in particular being used for several tasks in network analysis, such as community detection. In this work, we choose a different approach and study augmentations of the discretization of the Ricci curvature proposed by Forman (AFRC). We empirically and theoretically investigate its relation to the ORC and the un-augmented Forman–Ricci curvature. In particular, we provide evidence that the AFRC frequently gives sufficient insight into the structure of a network to be used for community detection, and therefore provides a computationally cheaper alternative to previous ORC-based methods. Our novel AFRC-based community detection algorithm is competitive with an ORC-based approach.
