---
id: img_proc
title: Image Processing
---


# Welcome

This site features documentation on the image processing and optimization routines available in SPIDAL. 

A basic philosophy underlying SPIDAL is that *many problems in AI-related domains* 
(including machine learning, image understanding,  computer vision, etc) *can be posed and solved using
one of a relatively small number of general techniques.* Instead of re-inventing algorithms that are
customized for a particular application, we advocate posing new problems in terms of  general and abstract
techniques. For example, many problems involving analyzing sequences can be posed as Hidden Markov Models,
whether the sequences are sentences, positions of objects across time, audio signals, or protein sequences.

This view encourages separating applications, models,  algorithms, and implementations to maximize generalization and
code reuse. An *application* involves solving a particular domain-specific problem. Many such domain-specific tasks
can be posed in terms of a *model* that precisely defines a mathematical problem to be solved.
Different models may make different assumptions, trading off between
simplicity and faithfulness to the original problem. 
An *algorithm* is a particular strategy for solving for unknown variables in that model. 
Different algorithms can be used to solve a given model, often with different trade-offs
between accuracy and speed.
An *implementation* is one particular set of source codes for executing an algorithm. Implementations
may use heuristics or simplifications to improve practical results or decrease running time of an algorithm. 

# Contents

The goal of this site is to help choose the right model and algorithm abstractions for a given novel problem,
and then apply SPIDAL codes to these new problems.
Thus in addition to information about how to use the libraries themselves, we include background information about what these routines do, how they work, and when to use them, and show examples of their use on real problems.

You can use this resource in several different ways:

* If you'd like to see how to apply SPIDAL algorithms to real problems, see [Exemplar Applications](#exemplar-applications).

* If you'd like to learn more about a particular model, see [Models](#models).

* If you'd like to learn more about a particular algorithm, see [Algorithms](#algorithms).

<!--- [](If you have a problem to solve and need to choose a model or algorithm see Documentation by Problem Type.) -->




---


# Exemplar applications

## 3D Reconstruction of Polar Ice

![](http://vision.soic.indiana.edu/papers/thumbs/icesurface2017icip-thumb.png)

#### Reconstructs the three-dimensional surface of bedrock under polar ice using tomographic slices from ground-penetrating radar echograms.


* [Research paper (IEEE International Conference on Image Processing 2017)](http://vision.soic.indiana.edu/papers/icesurface2017icip.pdf)
* [Research project website](http://vision.soic.indiana.edu/projects/icelayers/)
* Technologies: Image reconstruction, image recognition, discrete optimization, probabilistic inference
* Models: [Markov Random Fields](#spatial-models)
* Algorithms: [Loopy Belief Propagation](#discrete-optimization), [Tree-reweighted Message Passing](#discrete-optimization)


## Segmentation of Radar Echograms

![](http://vision.soic.indiana.edu/papers/thumbs/icelayers2014icip-thumb.png)

#### Segments location bedrock, ice, and air in radar echograms of polar ice.

* [Research paper (IEEE International Conference on Pattern Recognition 2012)](http://vision.soic.indiana.edu/papers/icesheets2012icpr.pdf)
* [Research project website](http://vision.soic.indiana.edu/projects/icelayers/)
* Technologies: Image segmentation, discrete optimization, probabilistic inference
* Models: [Hidden Markov Models](#sequence-models)
* Algorithms: [Viterbi](#sequence-model-inference)

#### Identifies layer boundaries in radar echograms, including "soft" confidence bounds on layer locations.

* [Research paper (IEEE International Conference on Image Processing 2014)](http://vision.soic.indiana.edu/papers/icelayers2014icip.pdf)
* [Research project website](http://vision.soic.indiana.edu/projects/icelayers/)
* Technologies: Image segmentation, discrete optimization, probabilistic inference
* Models: [Hidden Markov Models](#sequence-models), [Markov Random Fields](#spatial-models)
* Algorithms: [Markov Chain Monte Carlo](#sequence-model-inference)

## 3D Reconstruction of Landmarks from Social Media images


![](http://vision.soic.indiana.edu/papers/thumbs/sfm2011cvpr-thumb.png)


#### Creates three-dimensional reconstructions of buildings and other landmarks from images downloaded from social media.

* [Research paper (IEEE Transactions on Pattern Analysis and Machine Intelligence 2013)](http://vision.soic.indiana.edu/papers/disco2013pami.pdf)
* [Research project website](http://vision.soic.indiana.edu/disco/)
* Technologies: Discrete optimization, continuous optimization, image feature point extraction
* Models: [Markov Random Fields](#spatial-models), [Non-linear Least Squares](#regression-models)
* Algorithms: [Loopy Belief Propagation](#discrete-optimization), [Levenberg-Marquardt](#continuous-optimization), [Scale Invariant Feature Transforms](#image-processing-and-computer-vision)

## Multi-modal Photo Clustering

![](http://vision.soic.indiana.edu/papers/thumbs/multimodal2014cvpr-thumb.png)

#### Clusters large-scale collections of images by combining visual, temporal, spatial, and textual features.

* [Research paper (IEEE Computer Vision and Pattern Recognition 2014)](http://vision.soic.indiana.edu/papers/multimodal2014cvpr.pdf)
* Technologies: Clustering, discrete optimization, image feature  extraction
* Models: [Markov Random Fields](#spatial-models), [Bag-of-words](#image-features)
* Algorithms: [Tree-reweighted Message Passing](#discrete-optimization), [K-means](#clustering-and-grouping), [Scale Invariant Feature Transforms](#image-processing-and-computer-vision)

#### Organizes and visualizes social media images using multimodal features.

* [Research paper (World Wide Web Conference 2009)](http://vision.soic.indiana.edu/papers/mapping2009www.pdf)
* [Research project website](http://www.cs.indiana.edu/~djcran/photomap/)
* Technologies: Clustering, image feature extraction
* Models: [Bag-of-words](#image-features), [Support vector machines](#classification-models)
* Algorithms: [K-means](#clustering-and-grouping), [Mean shift](#clustering-and-grouping)

## Photo segmentation

![](http://vision.soic.indiana.edu/papers/thumbs/mcl2016nips-thumb.png)

#### Produces multiple diverse candidate solutions for pixel-level semantic photo labeling.

* [Research paper (Neural Information Processing Systems 2016)](http://vision.soic.indiana.edu/papers/mcl2016nips.pdf)
* Technologies: Segmentation, deep learning, discrete optimization
* Models: [Markov Random Fields](#spatial-models), [Deep Neural Networks](#regression-models)
* Algorithms:  [Gradient Descent](#continuous-optimization), [Tree-reweighted Message Passing](#discrete-optimization)


## Image recognition

![](http://vision.soic.indiana.edu/papers/thumbs/landmarks2015book-thumb.png)

#### Estimates where on Earth a photo was taken using visual, textual, and temporal features.

* [Research paper (Book Chapter)](http://vision.soic.indiana.edu/papers/landmarks2015book.pdf)
* Technologies: Recognition, deep learning, discrete optimization, continuous optimization, image feature extraction
* Models: [Hidden Markov Models](#sequence-models), [Deep Neural Networks](#regression-models), [Support Vector Machines](#classification-models), [Bag-of-words](#image-features)
* Algorithms: [Viterbi](#sequence-model-inference),  [Gradient Descent](#continuous-optimization), [K-means](#clustering-and-grouping), [k-nearest neighbors](#clustering-and-grouping)


## Image captioning

![](http://vision.soic.indiana.edu/papers/thumbs/deepdiary2016eccvw-thumb.png)

#### Automatically produces diverse captions to describe an image.

* [Research paper (ECCV Workshop 2016)](http://vision.soic.indiana.edu/papers/deepdiary2016eccvw.pdf)
* [Research project website](http://vision.soic.indiana.edu/projects/deepdiary/)
* Technologies: Deep learning, discrete optimization
* Models: [Hidden Markov Models](#sequence-models), [Deep Neural Networks](#regression-models), [Long-short Term Memories](#sequence-models)
* Algorithms: [Viterbi](#sequence-model-inference), [Gradient Descent](#continuous-optimization)



---

# Algorithms

SPIDAL implementations are available for algorithms that solve various models and problems. The links below lead
to more information about the algorithms, as well as source code and documentation.

## Sequence model inference

* [Viterbi algorithm](https://github.com/hpcanalytics/Hidden-Markov-Model/tree/master/algorithm.viterbi) for exact Maximum A Posteriori (MAP) inference
* [Forward-Backward algorithm](https://github.com/hpcanalytics/Hidden-Markov-Model/tree/master/algorithm.forward-backward) for exact marginal inference
* [Markov Chain Monte Carlo (MCMC)](https://github.com/hpcanalytics/Hidden-Markov-Model/tree/master/algorithm.mcmc) for approximate MAP inference 
 

## Discrete optimization

* [Loopy Belief Propagation](https://github.com/hpcanalytics/Markov-Random-Field/tree/master/algorithm.Loopy-Belief-Propoagation) for approximate optimization of [Markov Random Fields](#spatial-models) 
* [Tree Reweighted Message Passing (TRW-S)](https://github.com/hpcanalytics/Markov-Random-Field/tree/master/algorithm.TRW-S) for approximate optimization of [Markov Random Fields](#spatial-models) 
* Gibbs Sampling for approximate inference on [Markov Random Fields](#spatial-models) 
 

## Continuous optimization

* Levenberg-Marquardt - non-linear least squares
* Gradient descent
 


## Clustering and grouping

* [K-means clustering](https://github.com/hpcanalytics/Clustering-and-Grouping/tree/master/algorithm.k-means)
* [Mean shift clustering](https://github.com/hpcanalytics/Clustering-and-Grouping/tree/master/algorithm.mean-shift)
* Approximate all-pairs similarity search
* Deterministic Annealing 

## Dimensionality reduction

* Multidimensional Scaling (MDS) 
 

## Image processing and computer vision

* Unsupervised image segmentation
* Image alignment
* Edge detection
* Scale Invariant Feature Transform

---

# Models

## Sequence models
* [Hidden Markov Models](https://github.com/hpcanalytics/Hidden-Markov-Model)
* Long-short Term Memory models

## Spatial models
* [Markov Random Fields](https://github.com/hpcanalytics/Markov-Random-Field)

## Classification models
* Nearest neighbor
* Support Vector Machines


## Regression models
* Non-linear least squares
* Deep Neural Networks

## Image features
* Edges
* Interest points
* Bag of words models


<iframe width="420" height="315" src="https://www.youtube.com/embed/oGqp_fAv5S8" frameborder="0" allowfullscreen></iframe>
