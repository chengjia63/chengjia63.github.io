---
layout: default
title: Regularization With Stochastic Transformations and Perturbations for Deep Semi-Supervised Learning
---

# [Regularization With Stochastic Transformations and Perturbations for Deep Semi-Supervised Learning](https://arxiv.org/abs/1606.04586)

#### Mehdi Sajjadi, Mehran Javanmardi, and Tolga Tasdizen

---

## What is the Problem?
Randomized methods improves model generalization and training stability, but it
could cause different predictions of a single data (undergoing different 
transformations) 

## Summary
The authors presented Transformation-stability loss, an unsupervised loss
function to minimize the mean squared difference between different
transformations of tranining samples through the network. The
authors also used Mutual-exclusivity loss to prevent trivial predictions


## Key Insights
- Using Mini-bach that contains replications of a training example to compute a
    single back prop signal avoids gradient bias and does not affect convergence
- TS loss may be combined with any supervised loss function

## Notable Design Details/Strengths
- Easy to implement with small computing cost
- Improves model accuracy regardless of network architecture and implementation

## Limitations/Weaknesses
- These loss functions introduce more hyper-parameters to the training process

## Key Results
- The authors achieved ignificant reduction in error rates when TS loss is
    applied to MNIST, SVHN, NORB, CIFAR10, CIFAR100 and ImageNet data

## Open Questions
- Only address the randomness in transformation of data, but not the randomness
    in the model itself such as random pooling and drop out. The authors tested
    the loss in networks with those techniques but the loss function does not
    address them directly

