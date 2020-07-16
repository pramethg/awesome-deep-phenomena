# Awesome Deep Phenomena [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

Our understanding of modern neural networks lags behind their practical successes. This growing gap poses a challenge to the pace of progress in machine learning because fewer pillars of knowledge are available to designers of models and algorithms. Inspired by the [ICML 2019 workshop Identifying and Understanding Deep Learning Phenomena](http://deep-phenomena.org/), I collect papers which present interesting empirical study or insight into the nature of deep learning.  

## Table of Contents

- [Deep Learning Theory](#deep-learning-theory)
- [Empirical Study](#empirical-study)
- [Understanding Robustness](#understanding-robustness)
- [Representation Learning](#representation-learning)
- [Interpretability](#interpretability)

## Deep Learning Theory

### 2020

- Double Trouble in Double Descent : Bias and Variance(s) in the Lazy Regime. [[paper]](https://arxiv.org/abs/2003.01054) [[code]](https://github.com/mariaref/Random_Features)
  - Stéphane d'Ascoli, Maria Refinetti, Giulio Biroli, Florent Krzakala. *ICML 2020*
  - Digest:  In this work, we develop a quantitative theory for this phenomenon in the so-called lazy learning regime of neural networks, by considering the problem of learning a high-dimensional function with random features regression. We obtain a precise asymptotic expression for the bias-variance decomposition of the test error, and show that the bias displays a phase transition at the interpolation threshold, beyond which it remains constant.  

- Proving the Lottery Ticket Hypothesis: Pruning is All You Need. [[paper]](https://arxiv.org/abs/2002.00585)
  - Eran Malach, Gilad Yehudai, Shai Shalev-Shwartz, Ohad Shamir. *ICML 2020*
  - Digest: The lottery ticket hypothesis ([Frankle and Carbin, 2018](https://arxiv.org/abs/1803.03635)), states that a randomly-initialized network contains a small subnetwork such that, when trained in isolation, can compete with the performance of the original network. We prove an even stronger hypothesis (as was also conjectured in [Ramanujan et al., 2019](https://arxiv.org/abs/1911.13299)), showing that for every bounded distribution and every target network with bounded weights, a sufficiently over-parameterized neural network with random weights contains a subnetwork with roughly the same accuracy as the target network, without any further training.

### 2019

- Generalization of Two-layer Neural Networks: An Asymptotic Viewpoint. [[paper]](https://openreview.net/forum?id=H1gBsgBYwH)
  - Jimmy Ba, Murat Erdogdu, Taiji Suzuki, Denny Wu, Tianzong Zhang. *ICLR 2020*
  - Digest: This paper focuses on studying the double descent phenomenon in a one layer neural network training in an asymptotic regime where various dimensions go to infinity together with fixed ratios. The authors provide precise asymptotic characterization of the risk and use it to study various phenomena. In particular they characterize the role of various scales of the initialization and their effects.  

- Optimization for deep learning: theory and algorithms. [[paper]](https://arxiv.org/abs/1912.08957)
  - Ruoyu Sun.
  - Digest: When and why can a neural network be successfully trained? This article provides an overview of optimization algorithms and theory for training neural networks.  

- Neural Tangents: Fast and Easy Infinite Neural Networks in Python. [[paper]](https://arxiv.org/abs/1912.02803) [[code]](https://github.com/google/neural-tangents)
  - Roman Novak, Lechao Xiao, Jiri Hron, Jaehoon Lee, Alexander A. Alemi, Jascha Sohl-Dickstein, Samuel S. Schoenholz. *ICLR 2020*
  - Digest: Neural Tangents is a library designed to enable research into infinite-width neural networks. It provides a high-level API for specifying complex and hierarchical neural network architectures. These networks can then be trained and evaluated either at finite-width as usual or in their infinite-width limit.  

- Tensor Programs I: Wide Feedforward or Recurrent Neural Networks of Any Architecture are Gaussian Processes. [[paper]](https://arxiv.org/abs/1910.12478) [[code]](https://github.com/thegregyang/GP4A)
  - Greg Yang. *NeurIPS 2019*
  - Digest: We show that this Neural Network-Gaussian Process correspondence surprisingly extends to all modern feedforward or recurrent neural networks composed of multilayer perceptron, RNNs (e.g. LSTMs, GRUs), (nD or graph) convolution, pooling, skip connection, attention, batch normalization, and/or layer normalization.  

- Why bigger is not always better: on finite and infinite neural networks. [[paper]](https://arxiv.org/abs/1910.08013)
  - Laurence Aitchison. *ICML 2020*
  - Digest: We give analytic results characterising the prior over representations and representation learning in finite deep linear networks. We show empirically that the representations in SOTA architectures such as ResNets trained with SGD are much closer to those suggested by our deep linear results than by the corresponding infinite network.  

- On Robustness of Neural Ordinary Differential Equations. [[paper]](https://arxiv.org/abs/1910.05513)
  - Hanshu Yan, Jiawei Du, Vincent Y. F. Tan, Jiashi Feng. *ICLR 2020*
  - Digest: In this work, we fill this important gap by exploring robustness properties of neural ODEs both empirically and theoretically.  

- Improved Sample Complexities for Deep Networks and Robust Classification via an All-Layer Margin. [[paper]](https://arxiv.org/abs/1910.04284) [[code]](https://github.com/cwein3/all-layer-margin-opt)
  - Colin Wei, Tengyu Ma. *ICLR 2020*
  - Digest:  In this work, we propose to instead analyze a new notion of margin, which we call the "all-layer margin." Our analysis reveals that the all-layer margin has a clear and direct relationship with generalization for deep models.  

- Finite Depth and Width Corrections to the Neural Tangent Kernel. [[paper]](https://arxiv.org/abs/1909.05989)
  - Boris Hanin, Mihai Nica. *ICLR 2020*
  - Digest: We prove the precise scaling, at finite depth and width, for the mean and variance of the neural tangent kernel (NTK) in a randomly initialized ReLU network. The standard deviation is exponential in the ratio of network depth to width. Thus, even in the limit of infinite overparameterization, the NTK is not deterministic if depth and width simultaneously tend to infinity.  

- Towards Explaining the Regularization Effect of Initial Large Learning Rate in Training Neural Networks. [[paper]](https://arxiv.org/abs/1907.04595) [[code]](https://github.com/cwein3/large-lr-code)
  - Yuanzhi Li, Colin Wei, Tengyu Ma. *NeurIPS 2019*
  - Digest: The key insight in our analysis is that the order of learning different types of patterns is crucial: because the small learning rate model first memorizes easy-to-generalize, hard-to-fit patterns, it generalizes worse on hard-to-generalize, easier-to-fit patterns than its large learning rate counterpart.  

- Invariant Risk Minimization. [[paper]](https://arxiv.org/abs/1907.02893) [[code]](https://github.com/facebookresearch/InvariantRiskMinimization)
  - Martin Arjovsky, Léon Bottou, Ishaan Gulrajani, David Lopez-Paz.
  - Digest: We introduce Invariant Risk Minimization (IRM), a learning paradigm to estimate invariant correlations across multiple training distributions. To achieve this goal, IRM learns a data representation such that the optimal classifier, on top of that data representation, matches for all training distributions. Through theory and experiments, we show how the invariances learned by IRM relate to the causal structures governing the data and enable out-of-distribution generalization.  

- Benign Overfitting in Linear Regression. [[paper]](https://arxiv.org/abs/1906.11300)
  - Peter L. Bartlett, Philip M. Long, Gábor Lugosi, Alexander Tsigler. *PNAS*
  - Digest: By studying examples of data covariance properties that this characterization shows are required for benign overfitting, we find an important role for finite-dimensional data: the accuracy of the minimum norm interpolating prediction rule approaches the best possible accuracy for a much narrower range of properties of the data distribution when the data lies in an infinite dimensional space versus when the data lies in a finite dimensional space whose dimension grows faster than the sample size.  

- The Normalization Method for Alleviating Pathological Sharpness in Wide Neural Networks. [[paper]](https://arxiv.org/abs/1906.02926)
  - Ryo Karakida, Shotaro Akaho, Shun-ichi Amari. *NeurIPS 2019*
  - Digest: To theoretically elucidate the effectiveness of normalization, we quantify the geometry of the parameter space determined by the Fisher information matrix (FIM), which also corresponds to the local shape of the loss landscape under certain conditions.  

- Can You Trust Your Model's Uncertainty? Evaluating Predictive Uncertainty Under Dataset Shift. [[paper]](https://arxiv.org/abs/1906.02530) [[code]](https://github.com/google-research/google-research/tree/master/uq_benchmark_2019)
  - Yaniv Ovadia, Emily Fertig, Jie Ren, Zachary Nado, D Sculley, Sebastian Nowozin, Joshua V. Dillon, Balaji Lakshminarayanan, Jasper Snoek. *NeurIPS 2019*
  - Digest: We present a large-scale benchmark of existing state-of-the-art methods on classification problems and investigate the effect of dataset shift on accuracy and calibration. We find that traditional post-hoc calibration does indeed fall short, as do several other previous methods.  

- Implicit Regularization in Deep Matrix Factorization. [[paper]](https://arxiv.org/abs/1905.13655) [[code]](https://github.com/roosephu/deep_matrix_factorization)
  - Sanjeev Arora, Nadav Cohen, Wei Hu, Yuping Luo. *NeurIPS 2019*
  - Digest: We study the implicit regularization of gradient descent over deep linear neural networks for matrix completion and sensing, a model referred to as deep matrix factorization. Our first finding, supported by theory and experiments, is that adding depth to a matrix factorization enhances an implicit tendency towards low-rank solutions, oftentimes leading to more accurate recovery.  

- Lightlike Neuromanifolds, Occam's Razor and Deep Learning. [[paper]](https://arxiv.org/abs/1905.11027)
  - Ke Sun, Frank Nielsen.
  - Digest: We took an information-theoretic approach. We find that the locally varying dimensionality of the parameter space can be studied by the discipline of singular semi-Riemannian geometry. We adapt Fisher information to this singular neuromanifold. We use a new prior to interpolate between Jeffreys' prior and the Gaussian prior. We derive a minimum description length of a deep learning model, where the spectrum of the Fisher information matrix plays a key role to reduce the model complexity.  

- On Exact Computation with an Infinitely Wide Neural Net. [[paper]](https://arxiv.org/abs/1904.11955) [[code]](https://github.com/ruosongwang/cntk)
  - Sanjeev Arora, Simon S. Du, Wei Hu, Zhiyuan Li, Ruslan Salakhutdinov, Ruosong Wang. *NeurIPS 2019*
  - Digest: The current paper gives the first efficient exact algorithm for computing the extension of NTK to convolutional neural nets, which we call Convolutional NTK (CNTK), as well as an efficient GPU implementation of this algorithm.  

- A Mean Field Theory of Batch Normalization. [[paper]](https://arxiv.org/abs/1902.08129)
  - Greg Yang, Jeffrey Pennington, Vinay Rao, Jascha Sohl-Dickstein, Samuel S. Schoenholz. *ICLR 2019*
  - Digest: Our theory shows that gradient signals grow exponentially in depth and that these exploding gradients cannot be eliminated by tuning the initial weight variances or by adjusting the nonlinear activation function. Indeed, batch normalization itself is the cause of gradient explosion.  

- Wide Neural Networks of Any Depth Evolve as Linear Models Under Gradient Descent. [[paper]](https://arxiv.org/abs/1902.06720)
  - Jaehoon Lee, Lechao Xiao, Samuel S. Schoenholz, Yasaman Bahri, Roman Novak, Jascha Sohl-Dickstein, Jeffrey Pennington. *NeurIPS 2019*
  - Digest: In this work, we show that for wide neural networks the learning dynamics simplify considerably and that, in the infinite width limit, they are governed by a linear model obtained from the first-order Taylor expansion of the network around its initial parameters.  

- Scaling Limits of Wide Neural Networks with Weight Sharing: Gaussian Process Behavior, Gradient Independence, and Neural Tangent Kernel Derivation. [[paper]](https://arxiv.org/abs/1902.04760)
  - Greg Yang.
  - Digest: We unify these results by introducing a notion of a tensor program that can express most neural network computations, and we characterize its scaling limit when its tensors are large and randomized.  

- Fine-Grained Analysis of Optimization and Generalization for Overparameterized Two-Layer Neural Networks. [[paper]](https://arxiv.org/abs/1901.08584)
  - Sanjeev Arora, Simon S. Du, Wei Hu, Zhiyuan Li, Ruosong Wang. *ICML 2019*
  - Digest: This paper analyzes training and generalization for a simple 2-layer ReLU net with random initialization. The key idea is to track dynamics of training and generalization via properties of a related kernel.

### 2018

- Gradient Descent Finds Global Minima of Deep Neural Networks. [[paper]](https://arxiv.org/abs/1811.03804)
  - Simon S. Du, Jason D. Lee, Haochuan Li, Liwei Wang, Xiyu Zhai. *ICML 2019*
  - Digest: Our analysis relies on the particular structure of the Gram matrix induced by the neural network architecture. This structure allows us to show the Gram matrix is stable throughout the training process and this stability implies the global optimality of the gradient descent algorithm.  

- Information Geometry of Orthogonal Initializations and Training. [[paper]](https://arxiv.org/abs/1810.03785)
  - Piotr A. Sokol, Il Memming Park. *ICLR 2020*
  - Digest: Here we show a novel connection between the maximum curvature of the optimization landscape (gradient smoothness) as measured by the Fisher information matrix (FIM) and the spectral radius of the input-output Jacobian, which partially explains why more isometric networks can train much faster.  

- Gradient Descent Provably Optimizes Over-parameterized Neural Networks. [[paper]](https://arxiv.org/abs/1810.02054)
  - Simon S. Du, Xiyu Zhai, Barnabas Poczos, Aarti Singh. *ICLR 2019*
  - Digest: One of the mysteries in the success of neural networks is randomly initialized first order methods like gradient descent can achieve zero training loss even though the objective function is non-convex and non-smooth. This paper demystifies this surprising phenomenon for two-layer fully connected ReLU activated neural networks.  

- Gradient descent aligns the layers of deep linear networks. [[paper]](https://arxiv.org/abs/1810.02032)
  - Ziwei Ji, Matus Telgarsky. *ICLR 2019*
  - Digest: This paper establishes risk convergence and asymptotic weight matrix alignment --- a form of implicit regularization --- of gradient flow and gradient descent when applied to deep linear networks on linearly separable data.  

- Dynamical Isometry is Achieved in Residual Networks in a Universal Way for any Activation Function. [[paper]](https://arxiv.org/abs/1809.08848)
  - Wojciech Tarnowski, Piotr Warchoł, Stanisław Jastrzębski, Jacek Tabor, Maciej A. Nowak. *AISTATS 2019*
  - Digest: We demonstrate that in residual neural networks (ResNets) dynamical isometry is achievable irrespectively of the activation function used. We do that by deriving, with the help of Free Probability and Random Matrix Theories, a universal formula for the spectral density of the input-output Jacobian at initialization, in the large network width and depth limit.  

- Neural Tangent Kernel: Convergence and Generalization in Neural Networks. [[paper]](https://arxiv.org/abs/1806.07572)
  - Arthur Jacot, Franck Gabriel, Clément Hongler. *NeurIPS 2018*
  - Digest: We prove that the evolution of an ANN during training can also be described by a kernel: during gradient descent on the parameters of an ANN, the network function (which maps input vectors to output vectors) follows the kernel gradient of the functional cost (which is convex, in contrast to the parameter cost) w.r.t. a new kernel: the Neural Tangent Kernel (NTK).  

- Neural Ordinary Differential Equations. [[paper]](https://arxiv.org/abs/1806.07366) [[code]](https://github.com/rtqichen/torchdiffeq)
  - Ricky T. Q. Chen, Yulia Rubanova, Jesse Bettencourt, David Duvenaud. *NeurIPS 2018*
  - Digest: We introduce a new family of deep neural network models. Instead of specifying a discrete sequence of hidden layers, we parameterize the derivative of the hidden state using a neural network. The output of the network is computed using a black-box differential equation solver.  

- Dynamical Isometry and a Mean Field Theory of RNNs: Gating Enables Signal Propagation in Recurrent Neural Networks. [[paper]](https://arxiv.org/abs/1806.05394)
  - Minmin Chen, Jeffrey Pennington, Samuel S. Schoenholz. *ICML 2018*
  - Digest: We develop a theory for signal propagation in recurrent networks after random initialization using a combination of mean field theory and random matrix theory. To simplify our discussion, we introduce a new RNN cell with a simple gating mechanism that we call the minimalRNN and compare it with vanilla RNNs.  

- Dynamical Isometry and a Mean Field Theory of CNNs: How to Train 10,000-Layer Vanilla Convolutional Neural Networks. [[paper]](https://arxiv.org/abs/1806.05393)
  - Lechao Xiao, Yasaman Bahri, Jascha Sohl-Dickstein, Samuel S. Schoenholz, Jeffrey Pennington. *ICML 2018*
  - Digest: In this work, we demonstrate that it is possible to train vanilla CNNs with ten thousand layers or more simply by using an appropriate initialization scheme. We derive this initialization scheme theoretically by developing a mean field theory for signal propagation and by characterizing the conditions for dynamical isometry, the equilibration of singular values of the input-output Jacobian matrix.  

- Towards Understanding the Role of Over-Parametrization in Generalization of Neural Networks. [[paper]](https://arxiv.org/abs/1805.12076)
  - Behnam Neyshabur, Zhiyuan Li, Srinadh Bhojanapalli, Yann LeCun, Nathan Srebro.  *ICLR 2019*
  - Digest:  In this work we suggest a novel complexity measure based on unit-wise capacities resulting in a tighter generalization bound for two layer ReLU networks. Our capacity bound correlates with the behavior of test error with increasing network sizes, and could potentially explain the improvement in generalization with over-parametrization.  

- How to Start Training: The Effect of Initialization and Architecture. [[paper]](https://arxiv.org/abs/1803.01719)
  - Boris Hanin, David Rolnick. *NeurIPS 2018*
  - Digest: We identify and study two common failure modes for early training in deep ReLU nets. The first failure mode, exploding/vanishing mean activation length, can be avoided by initializing weights from a symmetric distribution with variance 2/fan-in and, for ResNets, by correctly weighting the residual modules. We prove that the second failure mode, exponentially large variance of activation length, never occurs in residual nets once the first failure mode is avoided.  

- Stronger generalization bounds for deep nets via a compression approach. [[paper]](https://arxiv.org/abs/1802.05296)
  - Sanjeev Arora, Rong Ge, Behnam Neyshabur, Yi Zhang. *ICML 2018*
  - Digest: A simple compression framework for proving generalization bounds, perhaps a more explicit and intuitive form of the PAC-Bayes work. It also yields elementary short proofs of recent generalization results.  

- Which Neural Net Architectures Give Rise To Exploding and Vanishing Gradients? [[paper]](https://arxiv.org/abs/1801.03744)
  - Boris Hanin. *NeurIPS 2018*
  - Digest: We give a rigorous analysis of the statistical behavior of gradients in a randomly initialized fully connected network N with ReLU activations. Our results show that the empirical variance of the squares of the entries in the input-output Jacobian of N is exponential in a simple architecture-dependent constant beta, given by the sum of the reciprocals of the hidden layer widths.  

### 2017

- Mean Field Residual Networks: On the Edge of Chaos. [[paper]](https://arxiv.org/abs/1712.08969)
  - Greg Yang, Samuel S. Schoenholz. *NeurIPS 2017*
  - Digest: The exponential forward dynamics causes rapid collapsing of the input space geometry, while the exponential backward dynamics causes drastic vanishing or exploding gradients. We show, in contrast, that by adding skip connections, the network will, depending on the nonlinearity, adopt subexponential forward and backward dynamics, and in many cases in fact polynomial.  

- Resurrecting the sigmoid in deep learning through dynamical isometry: theory and practice. [[paper]](https://arxiv.org/abs/1711.04735)
  - Jeffrey Pennington, Samuel S. Schoenholz, Surya Ganguli. *NeurIPS 2017*
  - Digest: We explore the dependence of the singular value distribution on the depth of the network, the weight initialization, and the choice of nonlinearity. Intriguingly, we find that ReLU networks are incapable of dynamical isometry.  

- Deep Neural Networks as Gaussian Processes. [[paper]](https://arxiv.org/abs/1711.00165)
  - Jaehoon Lee, Yasaman Bahri, Roman Novak, Samuel S. Schoenholz, Jeffrey Pennington, Jascha Sohl-Dickstein. *ICLR 2018*
  - Digest: In this work, we derive the exact equivalence between infinitely wide deep networks and GPs. We further develop a computationally efficient pipeline to compute the covariance function for these GPs.  

- The Implicit Bias of Gradient Descent on Separable Data. [[paper]](https://arxiv.org/abs/1710.10345)
  - Daniel Soudry, Elad Hoffer, Mor Shpigel Nacson, Suriya Gunasekar, Nathan Srebro. *ICLR 2018*
  - Digest: We show the predictor converges to the direction of the max-margin (hard margin SVM) solution. The result also generalizes to other monotone decreasing loss functions with an infimum at infinity, to multi-class problems, and to training a weight layer in a deep network in a certain restricted setting.  

- When is a Convolutional Filter Easy To Learn? [[paper]](https://arxiv.org/abs/1709.06129)
  - Simon S. Du, Jason D. Lee, Yuandong Tian. *ICLR 2018*
  - Digest: We show that (stochastic) gradient descent with random initialization can learn the convolutional filter in polynomial time and the convergence rate depends on the smoothness of the input distribution and the closeness of patches. To the best of our knowledge, this is the first recovery guarantee of gradient-based algorithms for convolutional filter on non-Gaussian input distributions.  

- Understanding Black-box Predictions via Influence Functions. [[paper]](https://arxiv.org/abs/1703.04730)
  - Pang Wei Koh, Percy Liang. *ICML 2017*
  - Digest: In this paper, we use influence functions -- a classic technique from robust statistics -- to trace a model's prediction through the learning algorithm and back to its training data, thereby identifying training points most responsible for a given prediction. To scale up influence functions to modern machine learning settings, we develop a simple, efficient implementation that requires only oracle access to gradients and Hessian-vector products.  

### 2016

- Deep Information Propagation. [[paper]](https://arxiv.org/abs/1611.01232)
  - Samuel S. Schoenholz, Justin Gilmer, Surya Ganguli, Jascha Sohl-Dickstein. *ICLR 2017*
  - Digest: We study the behavior of untrained neural networks whose weights and biases are randomly distributed using mean field theory. We show the existence of depth scales that naturally limit the maximum depth of signal propagation through these random networks. Our main practical result is to show that random networks may be trained precisely when information can travel through them.  

- Exponential expressivity in deep neural networks through transient chaos. [[paper]](https://arxiv.org/abs/1606.05340) [[code]](https://github.com/ganguli-lab/deepchaos)
  - Ben Poole, Subhaneil Lahiri, Maithra Raghu, Jascha Sohl-Dickstein, Surya Ganguli. *NeurIPS 2016*
  - Digest: Our results reveal an order-to-chaos expressivity phase transition, with networks in the chaotic phase computing nonlinear functions whose global curvature grows exponentially with depth but not width.  

### 2015

- Deep Learning and the Information Bottleneck Principle. [[paper]](https://arxiv.org/abs/1503.02406)
  - Naftali Tishby, Noga Zaslavsky. *IEEE ITW 2015*
  - Digest: We first show that any DNN can be quantified by the mutual information between the layers and the input and output variables. Using this representation we can calculate the optimal information theoretic limits of the DNN and obtain finite sample generalization bounds.  

## Empirical Study

### 2020

- On the Generalization Benefit of Noise in Stochastic Gradient Descent. [[paper]](https://arxiv.org/abs/2006.15081)
  - Samuel L. Smith, Erich Elsen, Soham De. *ICML 2020*
  - Digest:  In this paper, we perform carefully designed experiments and rigorous hyperparameter sweeps on a range of popular models, which verify that small or moderately large batch sizes can substantially outperform very large batches on the test set. This occurs even when both models are trained for the same number of iterations and large batches achieve smaller training losses.  

- Finding trainable sparse networks through Neural Tangent Transfer. [[paper]](https://arxiv.org/abs/2006.08228) [[code]](https://github.com/fmi-basel/neural-tangent-transfer)
  - Tianlin Liu, Friedemann Zenke. *ICML 2020*
  - Digest: In this article, we introduce Neural Tangent Transfer, a method that instead finds trainable sparse networks in a label-free manner. Specifically, we find sparse networks whose training dynamics, as characterized by the neural tangent kernel, mimic those of dense networks in function space.  

- Pruning neural networks without any data by iteratively conserving synaptic flow. [[paper]](https://arxiv.org/abs/2006.05467) [[code]](https://github.com/ganguli-lab/Synaptic-Flow)
  - Hidenori Tanaka, Daniel Kunin, Daniel L. K. Yamins, Surya Ganguli.
  - Digest: Recent works have identified, through an expensive sequence of training and pruning cycles, the existence of winning lottery tickets or sparse trainable subnetworks at initialization. This raises a foundational question: can we identify highly sparse trainable subnetworks at initialization, without ever training, or indeed without ever looking at the data? We provide an affirmative answer to this question through theory driven algorithm design.  

- Triple descent and the two kinds of overfitting: Where & why do they appear? [[paper]](https://arxiv.org/abs/2006.03509) [[code]](https://github.com/sdascoli/triple-descent-paper)
  - Stéphane d'Ascoli, Levent Sagun, Giulio Biroli.
  - Digest:  In this paper, we show that despite their apparent similarity, these two scenarios are inherently different. In fact, both peaks can co-exist when neural networks are applied to noisy regression tasks. The relative size of the peaks is governed by the degree of nonlinearity of the activation function. Building on recent developments in the analysis of random feature models, we provide a theoretical ground for this sample-wise triple descent.  

- Comparing Rewinding and Fine-tuning in Neural Network Pruning. [[paper]](https://arxiv.org/abs/2003.02389) [[code]](https://github.com/lottery-ticket/rewinding-iclr20-public)
  - Alex Renda, Jonathan Frankle, Michael Carbin. *ICLR 2020*
  - Digest: Learning rate rewinding (which we propose) trains the unpruned weights from their final values using the same learning rate schedule as weight rewinding. Both rewinding techniques outperform fine-tuning, forming the basis of a network-agnostic pruning algorithm that matches the accuracy and compression ratios of several more network-specific state-of-the-art techniques.  

- Rethinking Bias-Variance Trade-off for Generalization of Neural Networks. [[paper]](https://arxiv.org/abs/2002.11328) [[code]](https://github.com/yaodongyu/Rethink-BiasVariance-Tradeoff)
  - Zitong Yang, Yaodong Yu, Chong You, Jacob Steinhardt, Yi Ma. *ICML 2020*
  - Digest: Recent work calls this into question for neural networks and other over-parameterized models, for which it is often observed that larger models generalize better. We provide a simple explanation for this by measuring the bias and variance of neural networks: while the bias is monotonically decreasing as in the classical theory, the variance is unimodal or bell-shaped: it increases then decreases with the width of the network.  

- The Early Phase of Neural Network Training. [[paper]](https://arxiv.org/abs/2002.10365) [[code]](https://github.com/facebookresearch/open_lth)
  - Jonathan Frankle, David J. Schwab, Ari S. Morcos. *ICLR 2020*
  - Digest:  We find that, within this framework, deep networks are not robust to reinitializing with random weights while maintaining signs, and that weight distributions are highly non-independent even after only a few hundred iterations.  

- Bayesian Deep Learning and a Probabilistic Perspective of Generalization. [[paper]](https://arxiv.org/abs/2002.08791) [[code]](https://github.com/izmailovpavel/understandingbdl)
  - Andrew Gordon Wilson, Pavel Izmailov.
  - Digest: We show that deep ensembles provide an effective mechanism for approximate Bayesian marginalization, and propose a related approach that further improves the predictive distribution by marginalizing within basins of attraction, without significant overhead. We also show that Bayesian model averaging alleviates double descent, resulting in monotonic performance improvements with increased flexibility.  

- Picking Winning Tickets Before Training by Preserving Gradient Flow. [[paper]](https://arxiv.org/abs/2002.07376) [[code]](https://github.com/alecwangcq/GraSP)
  - Chaoqi Wang, Guodong Zhang, Roger Grosse. *ICLR 2020*
  - Digest: We aim to prune networks at initialization, thereby saving resources at training time as well. Specifically, we argue that efficient training requires preserving the gradient flow through the network. This leads to a simple but effective pruning criterion we term Gradient Signal Preservation (GraSP).  

- Understanding Why Neural Networks Generalize Well Through GSNR of Parameters. [[paper]](https://arxiv.org/abs/2001.07384)
  - Jinlong Liu, Guoqing Jiang, Yunzhi Bai, Ting Chen, Huayan Wang. *ICLR 2020*
  - Digest: In this paper, we provide a novel perspective on these issues using the gradient signal to noise ratio (GSNR) of parameters during training process of DNNs. The GSNR of a parameter is defined as the ratio between its gradient's squared mean and variance, over the data distribution.  

### 2019

- White Noise Analysis of Neural Networks. [[paper]](https://arxiv.org/abs/1912.12106) [[code]](https://github.com/aliborji/WhiteNoiseAnalysis)
  - Ali Borji, Sikun Lin. *ICLR 2020*
  - Digest: A white noise analysis of modern deep neural networks is presented to unveil their biases at the whole network level or the single neuron level. Our analysis is based on two popular and related methods in psychophysics and neurophysiology namely classification images and spike triggered analysis.  

- Linear Mode Connectivity and the Lottery Ticket Hypothesis. [[paper]](https://arxiv.org/abs/1912.05671)
  - Jonathan Frankle, Gintare Karolina Dziugaite, Daniel M. Roy, Michael Carbin. *ICML 2020*
  - Digest: We introduce "instability analysis," which assesses whether a neural network optimizes to the same, linearly connected minimum under different samples of SGD noise. We find that standard vision models become "stable" in this way early in training. From then on, the outcome of optimization is determined to within a linearly connected region.  

- Deep Double Descent: Where Bigger Models and More Data Hurt. [[paper]](https://arxiv.org/abs/1912.02292)  
  - Preetum Nakkiran, Gal Kaplun, Yamini Bansal, Tristan Yang, Boaz Barak, Ilya Sutskever. *ICLR 2020*
  - Digest: We show that a variety of modern deep learning tasks exhibit a "double-descent" phenomenon where, as we increase model size, performance first gets worse and then gets better.  

- Fantastic Generalization Measures and Where to Find Them. [[paper]](https://arxiv.org/abs/1912.02178)
  - Yiding Jiang, Behnam Neyshabur, Hossein Mobahi, Dilip Krishnan, Samy Bengio. *ICLR 2020*
  - Digest: We present the first large scale study of generalization bounds and measures in deep networks. We train over two thousand CIFAR-10 networks with systematic changes in important hyper-parameters. We attempt to uncover potential causal relationships between each measure and generalization, by using rank correlation coefficient and its modified forms.  

- What's Hidden in a Randomly Weighted Neural Network? [[paper]](https://arxiv.org/abs/1911.13299) [[code]](https://github.com/allenai/hidden-networks)
  - Vivek Ramanujan, Mitchell Wortsman, Aniruddha Kembhavi, Ali Farhadi, Mohammad Rastegari. *CVPR 2020*
  - Digest: Hidden in a randomly weighted Wide ResNet-50 we show that there is a subnetwork (with random weights) that is smaller than, but matches the performance of a ResNet-34 trained on ImageNet. Not only do these "untrained subnetworks" exist, but we provide an algorithm to effectively find them.  

- Truth or Backpropaganda? An Empirical Investigation of Deep Learning Theory. [[paper]](https://arxiv.org/abs/1910.00359) [[code]](https://github.com/goldblum/TruthOrBackpropaganda)
  - Micah Goldblum, Jonas Geiping, Avi Schwarzschild, Michael Moeller, Tom Goldstein. *ICLR 2020*
  - Digest: The authors take a closer look at widely held beliefs about neural networks. Using a mix of analysis and experiment, they shed some light on the ways these assumptions break down.  

- Data-Independent Neural Pruning via Coresets. [[paper]](https://arxiv.org/abs/1907.04018)
  - Ben Mussay, Margarita Osadchy, Vladimir Braverman, Samson Zhou, Dan Feldman. *ICLR 2020*
  - Digest: We propose the first efficient, data-independent neural pruning algorithm with a provable trade-off between its compression rate and the approximation error for any future test sample. Our method is based on the coreset framework, which finds a small weighted subset of points that provably approximates the original inputs.  

- Finding the Needle in the Haystack with Convolutions: on the benefits of architectural bias. [[paper]](https://arxiv.org/abs/1906.06766) [[code]](https://github.com/sdascoli/anarchitectural-search)
  - Stéphane d'Ascoli, Levent Sagun, Joan Bruna, Giulio Biroli. *NeurIPS 2019*
  - Digest:  In particular, Convolutional Neural Networks (CNNs) are known to perform much better than Fully-Connected Networks (FCNs) on spatially structured data: the architectural structure of CNNs benefits from prior knowledge on the features of the data, for instance their translation invariance. The aim of this work is to understand this fact through the lens of dynamics in the loss landscape.  

- A Signal Propagation Perspective for Pruning Neural Networks at Initialization. [[paper]](https://arxiv.org/abs/1906.06307) [[code]](https://github.com/namhoonlee/spp-public)
  - Namhoon Lee, Thalaiyasingam Ajanthan, Stephen Gould, Philip H. S. Torr. *ICLR 2020*
  - Digest: In this work, by noting connection sensitivity as a form of gradient, we formally characterize initialization conditions to ensure reliable connection sensitivity measurements, which in turn yields effective pruning results. Moreover, we analyze the signal propagation properties of the resulting pruned networks and introduce a simple, data-free method to improve their trainability.  

- One ticket to win them all: generalizing lottery ticket initializations across datasets and optimizers. [[paper]](https://arxiv.org/abs/1906.02773)
  - Ari S. Morcos, Haonan Yu, Michela Paganini, Yuandong Tian. *NeurIPS 2019*
  - Digest:  Perhaps surprisingly, we found that, within the natural images domain, winning ticket initializations generalized across a variety of datasets, including Fashion MNIST, SVHN, CIFAR-10/100, ImageNet, and Places365, often achieving performance close to that of winning tickets generated on the same dataset.  

- Deconstructing Lottery Tickets: Zeros, Signs, and the Supermask. [[paper]](https://arxiv.org/abs/1905.01067) [[code]](https://github.com/uber-research/deconstructing-lottery-tickets)
  - Hattie Zhou, Janice Lan, Rosanne Liu, Jason Yosinski. *NeurIPS 2019*
  - Digest: In this paper, we have studied how three components to LT-style network pruning—mask criterion, treatment of kept weights during retraining (mask-1 action), and treatment of pruned weights during retraining (mask-0 action)—come together to produce sparse and performant subnetworks.

- Are All Layers Created Equal? [[paper]](https://arxiv.org/abs/1902.01996)  
  - Chiyuan Zhang, Samy Bengio, Yoram Singer. *ICML 2019 Workshop*
  - Digest: We show that the layers can be categorized as either "ambient" or "critical". Resetting the ambient layers to their initial values has no negative consequence, and in many cases they barely change throughout training. On the contrary, resetting the critical layers completely destroys the predictor and the performance drops to chance.  

- Identity Crisis: Memorization and Generalization under Extreme Overparameterization. [[paper]](https://arxiv.org/abs/1902.04698)
  - Chiyuan Zhang, Samy Bengio, Moritz Hardt, Michael C. Mozer, Yoram Singer. *ICLR 2020*
  - Digest: We study the interplay between memorization and generalization of overparameterized networks in the extreme case of a single training example and an identity-mapping task.  

### 2018

- On the Information Bottleneck Theory of Deep Learning. [[paper]](https://openreview.net/forum?id=ry_WPG-A-) [[code]](https://github.com/artemyk/ibsgd/tree/iclr2018)
  - Andrew Michael Saxe, Yamini Bansal, Joel Dapello, Madhu Advani, Artemy Kolchinsky, Brendan Daniel Tracey, David Daniel Cox. *ICLR 2018*
  - Digest: This submission explores [recent theoretical work](https://arxiv.org/abs/1703.00810) by Shwartz-Ziv and Tishby on explaining the generalization ability of deep networks. The paper gives counter-examples that suggest aspects of the theory might not be relevant for all neural networks.  

- Reconciling modern machine learning practice and the bias-variance trade-off. [[paper]](https://arxiv.org/abs/1812.11118)
  - Mikhail Belkin, Daniel Hsu, Siyuan Ma, Soumik Mandal. *PNAS*
  - Digest: In this paper, we reconcile the classical understanding and the modern practice within a unified performance curve. This "double descent" curve subsumes the textbook U-shaped bias-variance trade-off curve by showing how increasing model capacity beyond the point of interpolation results in improved performance.  

- Why ReLU networks yield high-confidence predictions far away from the training data and how to mitigate the problem. [[paper]](https://arxiv.org/abs/1812.05720) [[code]](https://github.com/max-andr/relu_networks_overconfident)
  - Matthias Hein, Maksym Andriushchenko, Julian Bitterwolf. *CVPR 2019*
  - Digest: Classifiers used in the wild, in particular for safety-critical systems, should not only have good generalization properties but also should know when they don't know, in particular make low confidence predictions far away from the training data. We show that ReLU type neural networks which yield a piecewise linear classifier function fail in this regard as they produce almost always high confidence predictions far away from the training data.  

- SNIP: Single-shot Network Pruning based on Connection Sensitivity. [[paper]](https://arxiv.org/abs/1810.02340) [[code]](https://github.com/namhoonlee/snip-public)
  - Namhoon Lee, Thalaiyasingam Ajanthan, Philip H. S. Torr. *ICLR 2019*
  - Digest: In this work, we present a new approach that prunes a given network once at initialization prior to training. To achieve this, we introduce a saliency criterion based on connection sensitivity that identifies structurally important connections in the network for the given task.  

- The Lottery Ticket Hypothesis: Finding Sparse, Trainable Neural Networks. [[paper]](https://arxiv.org/abs/1803.03635) [[code]](https://github.com/google-research/lottery-ticket-hypothesis)
  - Jonathan Frankle, Michael Carbin *ICLR 2019*
  - Digest: We find that a standard pruning technique naturally uncovers subnetworks whose initializations made them capable of training effectively. Based on these results, we articulate the "lottery ticket hypothesis:" dense, randomly-initialized, feed-forward networks contain subnetworks ("winning tickets") that - when trained in isolation - reach test accuracy comparable to the original network in a similar number of iterations.  

- Sensitivity and Generalization in Neural Networks: an Empirical Study. [[paper]](https://arxiv.org/abs/1802.08760)
  - Roman Novak, Yasaman Bahri, Daniel A. Abolafia, Jeffrey Pennington, Jascha Sohl-Dickstein. *ICLR 2018*
  - Digest: In this work, we investigate this tension between complexity and generalization through an extensive empirical exploration of two natural metrics of complexity related to sensitivity to input perturbations. We find that trained neural networks are more robust to input perturbations in the vicinity of the training data manifold, as measured by the norm of the input-output Jacobian of the network, and that it correlates well with generalization.  

### 2017

- Deep Image Prior. [[paper]](https://arxiv.org/abs/1711.10925) [[code]](https://dmitryulyanov.github.io/deep_image_prior)
  - Dmitry Ulyanov, Andrea Vedaldi, Victor Lempitsky.
  - Digest: In this paper, we show that, on the contrary, the structure of a generator network is sufficient to capture a great deal of low-level image statistics prior to any learning. In order to do so, we show that a randomly-initialized neural network can be used as a handcrafted prior with excellent results in standard inverse problems such as denoising, super-resolution, and inpainting.  

- Critical Learning Periods in Deep Neural Networks. [[paper]](https://arxiv.org/abs/1711.08856)
  - Alessandro Achille, Matteo Rovere, Stefano Soatto. *ICLR 2019*
  - Digest: Our findings indicate that the early transient is critical in determining the final solution of the optimization associated with training an artificial neural network. In particular, the effects of sensory deficits during a critical period cannot be overcome, no matter how much additional training is performed.  

- A Closer Look at Memorization in Deep Networks. [[paper]](https://arxiv.org/abs/1706.05394)
  - Devansh Arpit, Stanisław Jastrzębski, Nicolas Ballas, David Krueger, Emmanuel Bengio, Maxinder S. Kanwal, Tegan Maharaj, Asja Fischer, Aaron Courville, Yoshua Bengio, Simon Lacoste-Julien. *ICML 2017*
  - Digest: In our experiments, we expose qualitative differences in gradient-based optimization of deep neural networks (DNNs) on noise vs. real data. We also demonstrate that for appropriately tuned explicit regularization (e.g., dropout) we can degrade DNN training performance on noise datasets without compromising generalization on real data.  

- Opening the Black Box of Deep Neural Networks via Information. [[paper]](https://arxiv.org/abs/1703.00810)
  - Ravid Shwartz-Ziv, Naftali Tishby.
  - Digest: [Previous work](https://arxiv.org/abs/1503.02406) proposed to analyze DNNs in the *Information Plane*; i.e., the plane of the Mutual Information values that each layer preserves on the input and output variables. They suggested that the goal of the network is to optimize the Information Bottleneck (IB) tradeoff between compression and prediction, successively, for each layer. In this work we follow up on this idea and demonstrate the effectiveness of the Information-Plane visualization of DNNs.  

### 2016

- Understanding deep learning requires rethinking generalization. [[paper]](https://arxiv.org/abs/1611.03530)
  - Chiyuan Zhang, Samy Bengio, Moritz Hardt, Benjamin Recht, Oriol Vinyals. *ICLR 2017*
  - Digest: Through extensive systematic experiments, we show how these traditional approaches fail to explain why large neural networks generalize well in practice. Specifically, our experiments establish that state-of-the-art convolutional networks for image classification trained with stochastic gradient methods easily fit a random labeling of the training data.  

## Understanding Robustness

### 2020

- Understanding Adversarial Examples from the Mutual Influence of Images and Perturbations. [[paper]](https://arxiv.org/abs/2007.06189)
  - Chaoning Zhang, Philipp Benz, Tooba Imtiaz, In-So Kweon. *CVPR 2020*
  - Digest: Our results suggest a new perspective towards the relationship between images and universal perturbations: Universal perturbations contain dominant features, and images behave like noise to them. We are the first to achieve the challenging task of a targeted universal attack without utilizing original training data. Our approach using a proxy dataset achieves comparable performance to the state-of-the-art baselines which utilize the original training dataset.  

- Understanding and Improving Fast Adversarial Training. [[paper]](https://arxiv.org/abs/2007.02617) [[code]](https://github.com/tml-epfl/understanding-fast-adv-training)
  - Maksym Andriushchenko, Nicolas Flammarion.
  - Digest: We explored the questions of when and why FGSM adversarial training works, and how to improve it by increasing the gradient alignment, and thus the quality of the solution of the inner maximization problem.  

- On Connections between Regularizations for Improving DNN Robustness. [[paper]](https://arxiv.org/abs/2007.02209)
  - Yiwen Guo, Long Chen, Yurong Chen, Changshui Zhang. *TPAMI*
  - Digest: This paper analyzes regularization terms proposed recently for improving the adversarial robustness of deep neural networks (DNNs), from a theoretical point of view.  

- Biologically Inspired Mechanisms for Adversarial Robustness. [[paper]](https://arxiv.org/abs/2006.16427)
  - Manish V. Reddy, Andrzej Banburski, Nishka Pant, Tomaso Poggio.
  - Digest: In this work, we investigate the role of two biologically plausible mechanisms in adversarial robustness. We demonstrate that the non-uniform sampling performed by the primate retina and the presence of multiple receptive fields with a range of receptive field sizes at each eccentricity improve the robustness of neural networks to small adversarial perturbations.  

- Proper Network Interpretability Helps Adversarial Robustness in Classification. [[paper]](https://arxiv.org/abs/2006.14748) [[code]](https://github.com/AkhilanB/Proper-Interpretability)
  - Akhilan Boopathy, Sijia Liu, Gaoyuan Zhang, Cynthia Liu, Pin-Yu Chen, Shiyu Chang, Luca Daniel. *ICML 2020*
  - Digest: In this paper, we theoretically show that with a proper measurement of interpretation, it is actually difficult to prevent prediction-evasion adversarial attacks from causing interpretation discrepancy, as confirmed by experiments on MNIST, CIFAR-10 and Restricted ImageNet.  

- Smooth Adversarial Training. [[paper]](https://arxiv.org/abs/2006.14536)
  - Cihang Xie, Mingxing Tan, Boqing Gong, Alan Yuille, Quoc V. Le.
  - Digest: Hence we propose smooth adversarial training (SAT), in which we replace ReLU with its smooth approximations to strengthen adversarial training. The purpose of smooth activation functions in SAT is to allow it to find harder adversarial examples and compute better gradient updates during adversarial training. Compared to standard adversarial training, SAT improves adversarial robustness for "free", i.e., no drop in accuracy and no increase in computational cost.  

- A Causal View on Robustness of Neural Networks. [[paper]](https://arxiv.org/abs/2005.01095)
  - Cheng Zhang, Kun Zhang, Yingzhen Li.
  - Digest: We present a causal view on the robustness of neural networks against input manipulations, which applies not only to traditional classification tasks but also to general measurement data. Based on this view, we design a deep causal manipulation augmented model (deep CAMA) which explicitly models possible manipulations on certain causes leading to changes in the observed effect.  

- The Notorious Difficulty of Comparing Human and Machine Perception. [[paper]](https://arxiv.org/abs/2004.09406) [[code]](https://github.com/bethgelab/notorious_difficulty_of_comparing_human_and_machine_perception)
  - Christina M. Funke, Judy Borowski, Karolina Stosio, Wieland Brendel, Thomas S. A. Wallis, Matthias Bethge.
  - Digest: We show that, despite their ability to solve closed-contour tasks, our neural networks use different decision-making strategies than humans. We further show that there is no fundamental difference between same-different and spatial tasks for common feed-forward neural networks and finally, that neural networks do experience a "recognition gap" on minimal recognizable images. All in all, care has to be taken to not impose our human systematic bias when comparing human and machine perception.  

- ObjectNet Dataset: Reanalysis and Correction. [[paper]](https://arxiv.org/abs/2004.02042) [[code]](https://github.com/aliborji/ObjectNetReanalysis)
  - Ali Borji.
  - Digest: We highlight a major problem with their work which is applying object recognizers to the scenes containing multiple objects rather than isolated objects. The latter results in around 20-30% performance gain using our code. Compared with the results reported in the ObjectNet paper, we observe that around 10-15 % of the performance loss can be recovered, without any test time data augmentation.

- Overfitting in adversarially robust deep learning. [[paper]](https://arxiv.org/abs/2002.11569) [[code]](https://github.com/locuslab/robust_overfitting)
  - Leslie Rice, Eric Wong, J. Zico Kolter. *ICML 2020*
  - Digest: In this paper, we empirically study this phenomenon in the setting of adversarially trained deep networks, which are trained to minimize the loss under worst-case adversarial perturbations. We find that overfitting to the training set does in fact harm robust performance to a very large degree in adversarially robust training across multiple datasets (SVHN, CIFAR-10, CIFAR-100, and ImageNet) and perturbation models.  

- The Curious Case of Adversarially Robust Models: More Data Can Help, Double Descend, or Hurt Generalization. [[paper]](https://arxiv.org/abs/2002.11080)
  - Yifei Min, Lin Chen, Amin Karbasi.
  - Digest: In the weak adversary regime, more data improves the generalization of adversarially robust models. In the medium adversary regime, with more training data, the generalization loss exhibits a double descent curve, which implies the existence of an intermediate stage where more training data hurts the generalization. In the strong adversary regime, more data almost immediately causes the generalization error to increase.  

- Understanding and Mitigating the Tradeoff Between Robustness and Accuracy. [[paper]](https://arxiv.org/abs/2002.10716)
  - Aditi Raghunathan, Sang Michael Xie, Fanny Yang, John Duchi, Percy Liang. *ICML 2020*
  - Digest: In this work, we precisely characterize the effect of augmentation on the standard error in linear regression when the optimal linear predictor has zero standard and robust error.  

- A Bayes-Optimal View on Adversarial Examples. [[paper]](https://arxiv.org/abs/2002.08859)
  - Eitan Richardson, Yair Weiss.
  - Digest: In this paper, we argue for examining adversarial examples from the perspective of Bayes-Optimal classification. We construct realistic image datasets for which the Bayes-Optimal classifier can be efficiently computed and derive analytic conditions on the distributions so that the optimal classifier is either robust or vulnerable.  

- CEB Improves Model Robustness. [[paper]](https://arxiv.org/abs/2002.05380)
  - Ian Fischer, Alexander A. Alemi.
  - Digest: We demonstrate that the Conditional Entropy Bottleneck (CEB) can improve model robustness. CEB is an easy strategy to implement and works in tandem with data augmentation procedures. We report results of a large scale adversarial robustness study on CIFAR-10, as well as the ImageNet-C Common Corruptions Benchmark, ImageNet-A, and PGD attacks.  

- More Data Can Expand the Generalization Gap Between Adversarially Robust and Standard Models. [[paper]](https://arxiv.org/abs/2002.04725)
  - Lin Chen, Yifei Min, Mingrui Zhang, Amin Karbasi. *ICML 2020*
  - Digest: The conventional wisdom is that more training data should shrink the generalization gap between adversarially-trained models and standard models. However, we study the training of robust classifiers for both Gaussian and Bernoulli models under l-inf attacks, and we prove that more data may actually increase this gap.  

- Fundamental Tradeoffs between Invariance and Sensitivity to Adversarial Perturbations. [[paper]](https://arxiv.org/abs/2002.04599) [[code]](https://github.com/ftramer/Excessive-Invariance)
  - Florian Tramèr, Jens Behrmann, Nicholas Carlini, Nicolas Papernot, Jörn-Henrik Jacobsen. *ICML 2020*
  - Digest:  We demonstrate fundamental tradeoffs between these two types of adversarial examples.
    We show that defenses against sensitivity-based attacks actively harm a model's accuracy on invariance-based attacks, and that new approaches are needed to resist both attack types.  

### 2019

- Adversarial Training and Provable Defenses: Bridging the Gap. [[paper]](https://www.sri.inf.ethz.ch/publications/balunovic2020bridging) [[code]](https://github.com/eth-sri/colt)
  - Mislav Balunovic, Martin Vechev. *ICLR 2020*
  - Digest: The key idea is to model neural network training as a procedure which includes both, the verifier and the adversary. In every iteration, the verifier aims to certify the network using convex relaxation while the adversary tries to find inputs inside that convex relaxation which cause verification to fail.  

- ObjectNet: A large-scale bias-controlled dataset for pushing the limits of object recognition models. [[paper]](https://papers.nips.cc/paper/9142-objectnet-a-large-scale-bias-controlled-dataset-for-pushing-the-limits-of-object-recognition-models.pdf) [[dataset]](https://objectnet.dev/)
  - Barbu, A, Mayo, D, Alverio, J, Luo, W, Wang, C, Gutfreund, D, Tenenabum, JB, Katz, B. *NeurIPS 2019*
  - Digest: A new method, which we refer to as convex layerwise adversarial training (COLT), that can train provably robust neural networks and conceptually bridges the gap between adversarial training and existing provable defense methods.

- Your Classifier is Secretly an Energy Based Model and You Should Treat it Like One. [[paper]](https://arxiv.org/abs/1912.03263)
  - Will Grathwohl, Kuan-Chieh Wang, Jörn-Henrik Jacobsen, David Duvenaud, Mohammad Norouzi, Kevin Swersky. *ICLR 2020*
  - Digest: Within this framework, standard discriminative architectures may beused and the model can also be trained on unlabeled data. We demonstrate that energy based training of the joint distribution improves calibration, robustness, andout-of-distribution detection while also enabling our models to generate samplesrivaling the quality of recent GAN approaches.  

- When NAS Meets Robustness: In Search of Robust Architectures against Adversarial Attacks. [[paper]](https://arxiv.org/abs/1911.10695) [[code]](https://github.com/gmh14/RobNets)
  - Minghao Guo, Yuzhe Yang, Rui Xu, Ziwei Liu, Dahua Lin. *CVPR 2020*
  - Digest: In this work, we take an architectural perspective and investigate the patterns of network architectures that are resilient to adversarial attacks. We discover a family of robust architectures (RobNets).  

- Lower Bounds on Adversarial Robustness from Optimal Transport. [[paper]](https://arxiv.org/abs/1909.12272) [[code]](https://github.com/inspire-group/robustness-via-transport)
  - Arjun Nitin Bhagoji, Daniel Cullina, Prateek Mittal. *NeurIPS 2019*
  - Digest: In this paper, we use optimal transport to characterize the minimum possible loss in an adversarial classification scenario. In this setting, an adversary receives a random labeled example from one of two classes, perturbs the example subject to a neighborhood constraint, and presents the modified example to the classifier.  

- Biologically inspired sleep algorithm for artificial neural networks. [[paper]](https://arxiv.org/abs/1908.02240)
  - Giri P Krishnan, Timothy Tadros, Ramyaa Ramyaa, Maxim Bazhenov. *ICLR 2020*
  - Digest:  We provide a theoretical basis for the beneficial role of the brain-inspired sleep-like phase for the ANNs and present an algorithmic way for future implementations of the various features of sleep in deep learning ANNs.  

- Defense Against Adversarial Attacks Using Feature Scattering-based Adversarial Training. [[paper]](https://arxiv.org/abs/1907.10764) [[code]](https://github.com/Haichao-Zhang/FeatureScatter)
  - Haichao Zhang, Jianyu Wang. *NeurIPS 2019*
  - Digest: We introduce a feature scattering-based adversarial training approach for improving model robustness against adversarial attacks. Conventional adversarial training approaches leverage a supervised scheme (either targeted or non-targeted) in generating attacks for training, which typically suffer from issues such as label leaking as noted in recent works.  

- Natural Adversarial Examples. [[paper]](https://arxiv.org/abs/1907.07174) [[dataset]](https://github.com/hendrycks/natural-adv-examples)
  - Dan Hendrycks, Kevin Zhao, Steven Basart, Jacob Steinhardt, Dawn Song.
  - Digest: We introduce natural adversarial examples–real-world, unmodified, and naturally occurring examples that cause machine learning model performance to substantially degrade.  

- Image Synthesis with a Single (Robust) Classifier. [[paper]](https://arxiv.org/abs/1906.09453) [[code]](https://github.com/MadryLab/robustness_applications?)
  - Shibani Santurkar, Dimitris Tsipras, Brandon Tran, Andrew Ilyas, Logan Engstrom, Aleksander Madry. *NeurIPS 2019*
  - Digest: The crux of our approach is that we train this classifier to be adversarially robust. It turns out that adversarial robustness is precisely what we need to directly manipulate salient features of the input. Overall, our findings demonstrate the utility of robustness in the broader machine learning context.  

- Convergence of Adversarial Training in Overparametrized Neural Networks. [[paper]](https://arxiv.org/abs/1906.07916)
  - Ruiqi Gao, Tianle Cai, Haochuan Li, Liwei Wang, Cho-Jui Hsieh, Jason D. Lee. *NeurIPS 2019*
  - Digest:  This paper provides a partial answer to the success of adversarial training, by showing that it converges to a network where the surrogate loss with respect to the the attack algorithm is within theta of the optimal robust loss.  

- Lower Bounds for Adversarially Robust PAC Learning. [[paper]](https://arxiv.org/abs/1906.05815)
  - Dimitrios I. Diochnos, Saeed Mahloujifar, Mohammad Mahmoody. *ISAIM 2020*
  - Digest: We formalize hybrid attacks in which the evasion attack is preceded by a poisoning attack. This is perhaps reminiscent of "trapdoor attacks" in which a poisoning phase is involved as well, but the evasion phase here uses the error-region definition of risk that aims at misclassifying the perturbed instances.

- Adversarial Robustness as a Prior for Learned Representations. [[paper]](https://arxiv.org/abs/1906.00945) [[code]](https://github.com/MadryLab/robust_representations)
  - Logan Engstrom, Andrew Ilyas, Shibani Santurkar, Dimitris Tsipras, Brandon Tran, Aleksander Madry.
  - Digest: In this work, we show that robust optimization can be re-cast as a tool for enforcing priors on the features learned by deep neural networks. It turns out that representations learned by robust models address the aforementioned shortcomings and make significant progress towards learning a high-level encoding of inputs.  

- Unlabeled Data Improves Adversarial Robustness. [[paper]](https://arxiv.org/abs/1905.13736) [[code]](https://github.com/yaircarmon/semisup-adv)
  - Yair Carmon, Aditi Raghunathan, Ludwig Schmidt, Percy Liang, John C. Duchi. *NeurIPS 2019*
  - Digest: Theoretically, we revisit the simple Gaussian model of [Schmidt et al](https://arxiv.org/abs/1804.11285). that shows a sample complexity gap between standard and robust classification. We prove that unlabeled data bridges this gap: a simple semi-supervised learning procedure (self-training) achieves high robust accuracy using the same number of labels required for achieving high standard accuracy.  

- Are Labels Required for Improving Adversarial Robustness? [[paper]](https://arxiv.org/abs/1905.13725) [[code]](https://github.com/deepmind/deepmind-research/tree/master/unsupervised_adversarial_training)
  - Jonathan Uesato, Jean-Baptiste Alayrac, Po-Sen Huang, Robert Stanforth, Alhussein Fawzi, Pushmeet Kohli. *NeurIPS 2019*
  - Digest: Our main insight is that unlabeled data can be a competitive alternative to labeled data for training adversarially robust models. Theoretically, we show that in a simple statistical setting, the sample complexity for learning an adversarially robust model from unlabeled data matches the fully supervised case up to constant factors.  

- High Frequency Component Helps Explain the Generalization of Convolutional Neural Networks. [[paper]](https://arxiv.org/abs/1905.13545) [[code]](https://github.com/HaohanWang/HFC)
  - Haohan Wang, Xindi Wu, Zeyi Huang, Eric P. Xing. *CVPR 2020*
  - Digest: We investigate the relationship between the frequency spectrum of image data and the generalization behavior of convolutional neural networks (CNN). We first notice CNN's ability in capturing the high-frequency components of images. These high-frequency components are almost imperceptible to a human.  

- Interpreting Adversarially Trained Convolutional Neural Networks. [[paper]](https://arxiv.org/abs/1905.09797) [[code]](https://github.com/PKUAI26/AT-CNN)
  - Tianyuan Zhang, Zhanxing Zhu. *ICML 2019*
  - Digest: Surprisingly, we find that adversarial training alleviates the texture bias of standard CNNs when trained on object recognition tasks, and helps CNNs learn a more shape-biased representation.  

- Adversarial Examples Are Not Bugs, They Are Features. [[paper]](https://arxiv.org/abs/1905.02175) [[dataset]](https://github.com/MadryLab/constructed-datasets)
  - Andrew Ilyas, Shibani Santurkar, Dimitris Tsipras, Logan Engstrom, Brandon Tran, Aleksander Madry. *NeurIPS 2019*
  - Digest: We demonstrate that adversarial examples can be directly attributed to the presence of non-robust features: features derived from patterns in the data distribution that are highly predictive, yet brittle and incomprehensible to humans.  

- You Only Propagate Once: Accelerating Adversarial Training via Maximal Principle. [[paper]](https://arxiv.org/abs/1905.00877) [[code]](https://github.com/a1600012888/YOPO-You-Only-Propagate-Once)
  - Dinghuai Zhang, Tianyuan Zhang, Yiping Lu, Zhanxing Zhu, Bin Dong. *NeurIPS 2019*
  - Digest: In this paper, we show that adversarial training can be cast as a discrete time differential game. Through analyzing the Pontryagin's Maximal Principle (PMP) of the problem, we observe that the adversary update is only coupled with the parameters of the first layer of the network. This inspires us to restrict most of the forward and back propagation within the first layer of the network during adversary updates.  

- NATTACK: Learning the Distributions of Adversarial Examples for an Improved Black-Box Attack on Deep Neural Networks. [[paper]](https://arxiv.org/abs/1905.00441) [[code]](https://github.com/Cold-Winter/Nattack)
  - Yandong Li, Lijun Li, Liqiang Wang, Tong Zhang, Boqing Gong. *ICML 2019*
  - Digest: Instead of searching for an "optimal" adversarial example for a benign input to a targeted DNN, our algorithm finds a probability density distribution over a small region centered around the input, such that a sample drawn from this distribution is likely an adversarial example, without the need of accessing the DNN's internal layers or weights.  

- Benchmarking Neural Network Robustness to Common Corruptions and Perturbations. [[paper]](https://arxiv.org/abs/1903.12261) [[dataset]](https://github.com/hendrycks/robustness)
  - Dan Hendrycks, Thomas Dietterich. *ICLR 2019*
  - Digest: In this paper we establish rigorous benchmarks for image classifier robustness. Our first benchmark, ImageNet-C, standardizes and expands the corruption robustness topic, while showing which classifiers are preferable in safety-critical applications. Then we propose a new dataset called ImageNet-P which enables researchers to benchmark a classifier's robustness to common perturbations.  

- VC Classes are Adversarially Robustly Learnable, but Only Improperly. [[paper]](https://arxiv.org/abs/1902.04217)
  - Omar Montasser, Steve Hanneke, Nathan Srebro. *COLT 2019*
  - Digest: We study the question of learning an adversarially robust predictor. We show that any hypothesis class H with finite VC dimension is robustly PAC learnable with an improper learning rule. The requirement of being improper is necessary as we exhibit examples of hypothesis classes H with finite VC dimension that are not robustly PAC learnable with any proper learning rule.

- Certified Adversarial Robustness via Randomized Smoothing. [[paper]](https://arxiv.org/abs/1902.02918) [[code]](https://github.com/locuslab/smoothing)
  - Jeremy M Cohen, Elan Rosenfeld, J. Zico Kolter. *ICML 2019*
  - Digest: We show how to turn any classifier that classifies well under Gaussian noise into a new classifier that is certifiably robust to adversarial perturbations under the L-2 norm. This "randomized smoothing" technique has been proposed recently in the literature, but existing guarantees are loose. We prove a tight robustness guarantee in L-2 norm for smoothing with Gaussian noise.  

- Theoretically Principled Trade-off between Robustness and Accuracy. [[paper]](https://arxiv.org/abs/1901.08573) [[code]](https://github.com/yaodongyu/TRADES)
  - Hongyang Zhang, Yaodong Yu, Jiantao Jiao, Eric P. Xing, Laurent El Ghaoui, Michael I. Jordan. *ICML 2019*
  - Digest: In this work, we decompose the prediction error for adversarial examples (robust error) as the sum of the natural (classification) error and boundary error, and provide a differentiable upper bound using the theory of classification-calibrated loss, which is shown to be the tightest possible upper bound uniform over all probability distributions and measurable predictors. Inspired by our theoretical analysis, we also design a new defense method, TRADES, to trade adversarial robustness off against accuracy.  

### 2018

- Feature Denoising for Improving Adversarial Robustness. [[paper]](https://arxiv.org/abs/1812.03411) [[code]](https://github.com/facebookresearch/ImageNet-Adversarial-Training)
  - Cihang Xie, Yuxin Wu, Laurens van der Maaten, Alan Yuille, Kaiming He. *CVPR 2019*
  - Digest: This study suggests that adversarial perturbations on images lead to noise in the features constructed by these networks. Motivated by this observation, we develop new network architectures that increase adversarial robustness by performing feature denoising. Specifically, our networks contain blocks that denoise the features using non-local means or other filters; the entire networks are trained end-to-end.  

- ImageNet-trained CNNs are biased towards texture; increasing shape bias improves accuracy and robustness. [[paper]](https://arxiv.org/abs/1811.12231) [[code]](https://github.com/rgeirhos/texture-vs-shape)
  - Robert Geirhos, Patricia Rubisch, Claudio Michaelis, Matthias Bethge, Felix A. Wichmann, Wieland Brendel. *ICLR 2019*
  - Digest: We show that ImageNet-trained CNNs are strongly biased towards recognising textures rather than shapes, which is in stark contrast to human behavioural evidence and reveals fundamentally different classification strategies.  

- Strike (with) a Pose: Neural Networks Are Easily Fooled by Strange Poses of Familiar Objects. [[paper]](https://arxiv.org/abs/1811.11553) [[code]](https://github.com/airalcorn2/strike-with-a-pose)
  - Michael A. Alcorn, Qi Li, Zhitao Gong, Chengfei Wang, Long Mai, Wei-Shinn Ku, Anh Nguyen. *CVPR 2019*
  - Digest: In this paper, we present a framework for discovering DNN failures that harnesses 3D renderers and 3D models. That is, we estimate the parameters of a 3D renderer that cause a target DNN to misbehave in response to the rendered image.  

- Excessive Invariance Causes Adversarial Vulnerability. [[paper]](https://arxiv.org/abs/1811.00401)
  - Jörn-Henrik Jacobsen, Jens Behrmann, Richard Zemel, Matthias Bethge. *ICLR 2019*
  - Digest: We show deep networks are not only too sensitive to task-irrelevant changes of their input, as is well-known from epsilon-adversarial examples, but are also too invariant to a wide range of task-relevant changes, thus making vast regions in input space vulnerable to adversarial attacks. We show such excessive invariance occurs across various tasks and architecture types.  

- Rademacher Complexity for Adversarially Robust Generalization. [[paper]](https://arxiv.org/abs/1810.11914)
  - Dong Yin, Kannan Ramchandran, Peter Bartlett. *ICML 2019*
  - Digest: In this paper, we focus on L-inf attacks, and study the adversarially robust generalization problem through the lens of Rademacher complexity. For binary linear classifiers, we prove tight bounds for the adversarial Rademacher complexity, and show that the adversarial Rademacher complexity is never smaller than its natural counterpart, and it has an unavoidable dimension dependence, unless the weight vector has bounded L-1 norm.  

- Attacks Meet Interpretability: Attribute-steered Detection of Adversarial Samples. [[paper]](https://arxiv.org/abs/1810.11580)
  - Guanhong Tao, Shiqing Ma, Yingqi Liu, Xiangyu Zhang. *NeurIPS 2018*
  - Digest: We argue that adversarial sample attacks are deeply entangled with interpretability of DNN models: while classification results on benign inputs can be reasoned based on the human perceptible features/attributes, results on adversarial samples can hardly be explained. Therefore, we propose a novel adversarial sample detection technique for face recognition models, based on interpretability.  

- Sparse DNNs with Improved Adversarial Robustness. [[paper]](https://arxiv.org/abs/1810.09619)
  - Yiwen Guo, Chao Zhang, Changshui Zhang, Yurong Chen.
  - Digest: Our analyses reveal, both theoretically and empirically, that nonlinear DNN-based classifiers behave differently under l2 attacks from some linear ones. We further demonstrate that an appropriately higher model sparsity implies better robustness of nonlinear DNNs, whereas over-sparsified models can be more difficult to resist adversarial examples.  

- Generalisation in humans and deep neural networks. [[paper]](https://arxiv.org/abs/1808.08750) [[code]](https://github.com/rgeirhos/generalisation-humans-DNNs)
  - Robert Geirhos, Carlos R. Medina Temme, Jonas Rauber, Heiko H. Schütt, Matthias Bethge, Felix A. Wichmann. *NeurIPS 2018*
  - Digest: We compare the robustness of humans and current convolutional deep neural networks (DNNs) on object recognition under twelve different types of image degradations.  

- PAC-learning in the presence of evasion adversaries. [[paper]](https://arxiv.org/abs/1806.01471)
  - Daniel Cullina, Arjun Nitin Bhagoji, Prateek Mittal. *NeurIPS 2018*
  - Digest: In this paper, we step away from the attack-defense arms race and seek to understand the limits of what can be learned in the presence of an evasion adversary. In particular, we extend the Probably Approximately Correct (PAC)-learning framework to account for the presence of an adversary.  

- Why do deep convolutional networks generalize so poorly to small image transformations? [[paper]](https://arxiv.org/abs/1805.12177) [[code]](https://github.com/AzulEye/CNN-Failures)
  - Aharon Azulay, Yair Weiss. *JMLR 2019*
  - Digest: In this paper, we quantify this phenomena and ask why neither the convolutional architecture nor data augmentation are sufficient to achieve the desired invariance. Specifically, we show that the convolutional architecture does not give invariance since architectures ignore the classical sampling theorem, and data augmentation does not give invariance because the CNNs learn to be invariant to transformations only for images that are very similar to typical images from the training set.  

- Robustness May Be at Odds with Accuracy. [[paper]](https://arxiv.org/abs/1805.12152)
  - Dimitris Tsipras, Shibani Santurkar, Logan Engstrom, Alexander Turner, Aleksander Madry. *ICLR 2019*
  - Digest: We show that there may exist an inherent tension between the goal of adversarial robustness and that of standard generalization.  Specifically, training robust models may not only be more resource-consuming, but also lead to a reduction of standard accuracy.  

- Adversarial examples from computational constraints. [[paper]](https://arxiv.org/abs/1805.10204)
  - Sébastien Bubeck, Eric Price, Ilya Razenshteyn. *ICML 2019*
  - Digest: First we prove that, for a broad set of classification tasks, the mere existence of a robust classifier implies that it can be found by a possibly exponential-time algorithm with relatively few training examples. Then we give a particular classification task where learning a robust classifier is computationally intractable.  

- Towards the first adversarially robust neural network model on MNIST. [[paper]](https://arxiv.org/abs/1805.09190)
  - Lukas Schott, Jonas Rauber, Matthias Bethge, Wieland Brendel. *ICLR 2019*
  - Digest: We present a novel robust classification model that performs analysis by synthesis using learned class-conditional data distributions. We demonstrate that most adversarial examples are strongly perturbed towards the perceptual boundary between the original and the adversarial class.

- Adversarially Robust Generalization Requires More Data. [[paper]](https://arxiv.org/abs/1804.11285)
  - Ludwig Schmidt, Shibani Santurkar, Dimitris Tsipras, Kunal Talwar, Aleksander Mądry. *NeurIPS 2018*
  - Digest: We show that already in a simple natural data model, the sample complexity of robust learning can be significantly larger than that of "standard" learning. This gap is information theoretic and holds irrespective of the training algorithm or the model family.  

- Obfuscated Gradients Give a False Sense of Security: Circumventing Defenses to Adversarial Examples. [[paper]](https://arxiv.org/abs/1802.00420) [[code]](https://github.com/anishathalye/obfuscated-gradients)
  - Anish Athalye, Nicholas Carlini, David Wagner. *ICML 2018*
  - Digest: We identify obfuscated gradients, a kind of gradient masking, as a phenomenon that leads to a false sense of security in defenses against adversarial examples. While defenses that cause obfuscated gradients appear to defeat iterative optimization-based attacks, we find defenses relying on this effect can be circumvented.  

- Stochastic Activation Pruning for Robust Adversarial Defense. [[paper]](https://arxiv.org/abs/1803.01442) [[code]](https://github.com/Guneet-Dhillon/Stochastic-Activation-Pruning)
  - Guneet S. Dhillon, Kamyar Azizzadenesheli, Zachary C. Lipton, Jeremy Bernstein, Jean Kossaifi, Aran Khanna, Anima Anandkumar. *ICLR 2018*
  - Digest: We propose Stochastic Activation Pruning (SAP), a mixed strategy for adversarial defense. SAP prunes a random subset of activations (preferentially pruning those with smaller magnitude) and scales up the survivors to compensate.  

- Adversarial vulnerability for any classifier. [[paper]](https://arxiv.org/abs/1802.08686)
  - Alhussein Fawzi, Hamza Fawzi, Omar Fawzi. *NeurIPS 2018*
  - Digest: In this paper, we study the phenomenon of adversarial perturbations under the assumption that the data is generated with a smooth generative model. We derive fundamental upper bounds on the robustness to perturbations of any classification function, and prove the existence of adversarial perturbations that transfer well across different classifiers with small risk.  

### 2017

- Certifying Some Distributional Robustness with Principled Adversarial Training. [[paper]](https://arxiv.org/abs/1710.10571)
  - Aman Sinha, Hongseok Namkoong, Riccardo Volpi, John Duchi. *ICLR 2018*
  - Digest: By considering a Lagrangian penalty formulation of perturbing the underlying data distribution in a Wasserstein ball, we provide a training procedure that augments model parameter updates with worst-case perturbations of training data. For smooth losses, our procedure provably achieves moderate levels of robustness with little computational or statistical cost relative to empirical risk minimization.  

- One pixel attack for fooling deep neural networks. [[paper]](https://arxiv.org/abs/1710.08864)
  - Jiawei Su, Danilo Vasconcellos Vargas, Sakurai Kouichi. *IEEE Transactions on Evolutionary Computation*
  - Digest: In this paper, we analyze an attack in an extremely limited scenario where only one pixel can be modified. For that we propose a novel method for generating one-pixel adversarial perturbations based on differential evolution (DE). It requires less adversarial information (a black-box attack) and can fool more types of networks due to the inherent features of DE.  

### 2016

- Practical Black-Box Attacks against Machine Learning. [[paper]](https://arxiv.org/abs/1602.02697)
  - Nicolas Papernot, Patrick McDaniel, Ian Goodfellow, Somesh Jha, Z. Berkay Celik, Ananthram Swami. *AsiaCCS 2017*
  - Digest: We introduce the first practical demonstration of an attacker controlling a remotely hosted DNN with no such knowledge. Our attack evades a category of defenses, which we call gradient masking, previously proposed to increase resilience to adversarial examples.  

## Representation Learning

### 2020

- Graph Structure of Neural Networks. [[paper]](https://arxiv.org/abs/2007.06559)
  - Jiaxuan You, Jure Leskovec, Kaiming He, Saining Xie. *ICML 2020*
  - Digest:  Here we systematically investigate how does the graph structure of neural networks affect their predictive performance. To this end, we develop a novel graph-based representation of neural networks called relational graph, where layers of neural network computation correspond to rounds of message exchange along the graph structure.  

- Deep Isometric Learning for Visual Recognition. [[paper]](https://arxiv.org/abs/2006.16992) [[code]](https://github.com/HaozhiQi/ISONet)
  - Haozhi Qi, Chong You, Xiaolong Wang, Yi Ma, Jitendra Malik. *ICML 2020*
  - Digest: This paper shows that deep vanilla ConvNets without normalization nor skip connections can also be trained to achieve surprisingly good performance on standard image recognition benchmarks. This is achieved by enforcing the convolution kernels to be near isometric during initialization and training, as well as by using a variant of ReLU that is shifted towards being isometric.  

- Parametric Instance Classification for Unsupervised Visual Feature Learning. [[paper]](https://arxiv.org/abs/2006.14618)
  - Yue Cao, Zhenda Xie, Bin Liu, Yutong Lin, Zheng Zhang, Han Hu.
  - Digest: This paper presents parametric instance classification (PIC) for unsupervised visual feature learning. Unlike the state-of-the-art approaches which do instance discrimination in a dual-branch non-parametric fashion, PIC directly performs a one-branch parametric instance classification, revealing a simple framework similar to supervised classification and without the need to address the information leakage issue.  

- Big Self-Supervised Models are Strong Semi-Supervised Learners. [[paper]](https://arxiv.org/abs/2006.10029) [[code]](https://github.com/google-research/simclr)
  - Ting Chen, Simon Kornblith, Kevin Swersky, Mohammad Norouzi, Geoffrey Hinton.
  - Digest: The proposed semi-supervised learning algorithm can be summarized in three steps: unsupervised pretraining of a big ResNet model using SimCLRv2 (a modification of SimCLR), supervised fine-tuning on a few labeled examples, and distillation with unlabeled examples for refining and transferring the task-specific knowledge.  

- Unsupervised Learning of Visual Features by Contrasting Cluster Assignments. [[paper]](https://arxiv.org/abs/2006.09882)
  - Mathilde Caron, Ishan Misra, Julien Mairal, Priya Goyal, Piotr Bojanowski, Armand Joulin.
  - Digest: In this paper, we propose an online algorithm, SwAV, that takes advantage of contrastive methods without requiring to compute pairwise comparisons. Specifically, our method simultaneously clusters the data while enforcing consistency between cluster assignments produced for different augmentations (or views) of the same image, instead of comparing features directly as in contrastive learning.  

- Bootstrap Your Own Latent: A New Approach to Self-Supervised Learning. [[paper]](https://arxiv.org/abs/2006.07733)
  - Jean-Bastien Grill, Florian Strub, Florent Altché, Corentin Tallec, Pierre H. Richemond, Elena Buchatskaya, Carl Doersch, Bernardo Avila Pires, Zhaohan Daniel Guo, Mohammad Gheshlaghi Azar, Bilal Piot, Koray Kavukcuoglu, Rémi Munos, Michal Valko.
  - Digest: We introduce Bootstrap Your Own Latent (BYOL), a new approach to self-supervised image representation learning. BYOL relies on two neural networks, referred to as online and target networks, that interact and learn from each other. From an augmented view of an image, we train the online network to predict the target network representation of the same image under a different augmented view.  

- What makes for good views for contrastive learning? [[paper]](https://arxiv.org/abs/2005.10243) [[code]](https://github.com/HobbitLong/PyContrast)
  - Yonglong Tian, Chen Sun, Ben Poole, Dilip Krishnan, Cordelia Schmid, Phillip Isola.
  - Digest:  In this paper, we use empirical analysis to better understand the importance of view selection, and argue that we should reduce the mutual information (MI) between views while keeping task-relevant information intact.  

- Understanding Contrastive Representation Learning through Alignment and Uniformity on the Hypersphere. [[paper]](https://arxiv.org/abs/2005.10242) [[code]](https://github.com/SsnL/align_uniform)
  - Tongzhou Wang, Phillip Isola. *ICML 2020*
  - Digest: In this work, we identify two key properties related to the contrastive loss: (1) alignment (closeness) of features from positive pairs, and (2) uniformity of the induced distribution of the (normalized) features on the hypersphere. We prove that, asymptotically, the contrastive loss optimizes these properties, and analyze their positive effects on downstream tasks.  

- Steering Self-Supervised Feature Learning Beyond Local Pixel Statistics. [[paper]](https://arxiv.org/abs/2004.02331) [[code]](https://sjenni.github.io/LCI/)
  - Simon Jenni, Hailin Jin, Paolo Favaro. *CVPR 2020*
  - Digest:  We introduce a novel image transformation that we call limited context inpainting (LCI). This transformation inpaints an image patch conditioned only on a small rectangular pixel boundary (the limited context). Because of the limited boundary information, the inpainter can learn to match local pixel statistics, but is unlikely to match the global statistics of the image.  

- How Useful is Self-Supervised Pretraining for Visual Tasks? [[paper]](https://arxiv.org/abs/2003.14323) [[code]](https://github.com/princeton-vl/selfstudy)
  - Alejandro Newell, Jia Deng. *CVPR 2020*
  - Digest: We evaluate various self-supervised algorithms across a comprehensive array of synthetic datasets and downstream tasks. We prepare a suite of synthetic data that enables an endless supply of annotated images as well as full control over dataset difficulty.  

- Do CNNs Encode Data Augmentations? [[paper]](https://arxiv.org/abs/2003.08773)
  - Eddie Yan, Yanping Huang.
  - Digest: Surprisingly, neural network features not only predict data augmentation transformations, but they predict many transformations with high accuracy. After validating that neural networks encode features corresponding to augmentation transformations, we show that these features are primarily encoded in the early layers of modern CNNs.  

- Automatic Shortcut Removal for Self-Supervised Representation Learning. [[paper]](https://arxiv.org/abs/2002.08822)
  - Matthias Minderer, Olivier Bachem, Neil Houlsby, Michael Tschannen. *ICML 2020*
  - Digest: Here, we propose a general framework for removing shortcut features automatically. Our key assumption is that those features which are the first to be exploited for solving the pretext task may also be the most vulnerable to an adversary trained to make the task harder.  

- A Simple Framework for Contrastive Learning of Visual Representations. [[paper]](https://arxiv.org/abs/2002.05709) [[code]](https://github.com/google-research/simclr)
  - Ting Chen, Simon Kornblith, Mohammad Norouzi, Geoffrey Hinton.
  - Digest: This paper presents SimCLR: a simple framework for contrastive learning of visual representations. We simplify recently proposed contrastive self-supervised learning algorithms without requiring specialized architectures or a memory bank.  

### 2019

- Self-Supervised Learning of Pretext-Invariant Representations. [[paper]](https://arxiv.org/abs/1912.01991)
  - Ishan Misra, Laurens van der Maaten. *CVPR 2020*
  - Digest:  We argue that, instead, semantic representations ought to be invariant under such transformations. Specifically, we develop Pretext-Invariant Representation Learning (PIRL, pronounced as "pearl") that learns invariant representations based on pretext tasks.  

- Momentum Contrast for Unsupervised Visual Representation Learning. [[paper]](https://arxiv.org/abs/1911.05722) [[code]](https://github.com/facebookresearch/moco)
  - Kaiming He, Haoqi Fan, Yuxin Wu, Saining Xie, Ross Girshick. *CVPR 2020*
  - Digest: We present Momentum Contrast (MoCo) for unsupervised visual representation learning. From a perspective on contrastive learning as dictionary look-up, we build a dynamic dictionary with a queue and a moving-averaged encoder. This enables building a large and consistent dictionary on-the-fly that facilitates contrastive unsupervised learning.  

- Self-supervised Label Augmentation via Input Transformations. [[paper]](https://arxiv.org/abs/1910.05872) [[code]](https://github.com/hankook/SLA)
  - Hankook Lee, Sung Ju Hwang, Jinwoo Shin. *ICML 2020*
  - Digest: Our main idea is to learn a single unified task with respect to the joint distribution of the original and self-supervised labels, i.e., we augment original labels via self-supervision of input transformation.  

- A Large-scale Study of Representation Learning with the Visual Task Adaptation Benchmark. [[paper]](https://arxiv.org/abs/1910.04867) [[code]](https://github.com/google-research/task_adaptation)
  - Xiaohua Zhai, Joan Puigcerver, Alexander Kolesnikov, Pierre Ruyssen, Carlos Riquelme, Mario Lucic, Josip Djolonga, Andre Susano Pinto, Maxim Neumann, Alexey Dosovitskiy, Lucas Beyer, Olivier Bachem, Michael Tschannen, Marcin Michalski, Olivier Bousquet, Sylvain Gelly, Neil Houlsby.
  - Digest: We present the Visual Task Adaptation Benchmark (VTAB), which defines good representations as those that adapt to diverse, unseen tasks with few examples. With VTAB, we conduct a large-scale study of many popular publicly-available representation learning algorithms.  

- Building Deep, Equivariant Capsule Networks. [[paper]](https://arxiv.org/abs/1908.01300)
  - Sairaam Venkatraman, S. Balasubramanian, R. Raghunatha Sarma. *ICLR 2020*
  - Digest: This paper combine recent ideas from capsule networks and group-equivariant neural networks to form equivariant capsules.  

- On Mutual Information Maximization for Representation Learning. [[paper]](https://arxiv.org/abs/1907.13625) [[code]](https://github.com/google-research/google-research/tree/master/mutual_information_representation_learning)
  - Michael Tschannen, Josip Djolonga, Paul K. Rubenstein, Sylvain Gelly, Mario Lucic. *ICLR 2020*
  - Digest: In this paper we argue, and provide empirical evidence, that the success of these methods cannot be attributed to the properties of MI alone, and that they strongly depend on the inductive bias in both the choice of feature extractor architectures and the parametrization of the employed MI estimators.  

- Large Scale Adversarial Representation Learning. [[paper]](https://arxiv.org/abs/1907.02544) [[code]](https://colab.research.google.com/github/tensorflow/hub/blob/master/examples/colab/bigbigan_with_tf_hub.ipynb)
  - Jeff Donahue, Karen Simonyan. *NeurIPS 2019*
  - Digest: In this work we show that progress in image generation quality translates to substantially improved representation learning performance. Our approach, BigBiGAN, builds upon the state-of-the-art BigGAN model, extending it to representation learning by adding an encoder and modifying the discriminator.  

- Learning Representations by Maximizing Mutual Information Across Views. [[paper]](https://arxiv.org/abs/1906.00910) [[code]](https://github.com/Philip-Bachman/amdim-public)
  - Philip Bachman, R Devon Hjelm, William Buchwalter. *NeurIPS 2019*
  - Digest: We propose an approach to self-supervised representation learning based on maximizing mutual information between features extracted from multiple views of a shared context.  

- Data-Efficient Image Recognition with Contrastive Predictive Coding. [[paper]](https://arxiv.org/abs/1905.09272)
  - Olivier J. Hénaff, Aravind Srinivas, Jeffrey De Fauw, Ali Razavi, Carl Doersch, S. M. Ali Eslami, Aaron van den Oord. *ICML 2020*
  - Digest: We hypothesize that data-efficient recognition is enabled by representations which make the variability in natural signals more predictable. We therefore revisit and improve Contrastive Predictive Coding, an unsupervised objective for learning such representations.  

- On Variational Bounds of Mutual Information. [[paper]](https://arxiv.org/abs/1905.06922)
  - Ben Poole, Sherjil Ozair, Aaron van den Oord, Alexander A. Alemi, George Tucker. *ICML 2019*
  - Digest:  In this work, we unify these recent developments in a single framework. We find that the existing variational lower bounds degrade when the MI is large, exhibiting either high bias or high variance. To address this problem, we introduce a continuum of lower bounds that encompasses previous bounds and flexibly trades off bias and variance.  

- A critical analysis of self-supervision, or what we can learn from a single image. [[paper]](https://arxiv.org/abs/1904.13132) [[code]](https://github.com/yukimasano/linear-probes)
  - Yuki M. Asano, Christian Rupprecht, Andrea Vedaldi. *ICLR 2020*
  - Digest: We show that three different and representative methods, BiGAN, RotNet and DeepCluster, can learn the first few layers of a convolutional network from a single image as well as using millions of images and manual labels, provided that strong data augmentation is used. However, for deeper layers the gap with manual supervision cannot be closed even if millions of unlabelled images are used for training.  

- Approximating CNNs with Bag-of-local-Features models works surprisingly well on ImageNet. [[paper]](https://arxiv.org/abs/1904.00760) [[code]](https://github.com/wielandbrendel/bag-of-local-features-models)
  - Wieland Brendel, Matthias Bethge. *ICLR 2019*
  - Digest: Our model, a simple variant of the ResNet-50 architecture called BagNet, classifies an image based on the occurrences of small local image features without taking into account their spatial ordering. This strategy is closely related to the bag-of-feature (BoF) models popular before the onset of deep learning and reaches a surprisingly high accuracy on ImageNet.  

- Revisiting Self-Supervised Visual Representation Learning. [[paper]](https://arxiv.org/abs/1901.09005) [[code]](https://github.com/google/revisiting-self-supervised)
  - Alexander Kolesnikov, Xiaohua Zhai, Lucas Beyer. *CVPR 2019*
  - Digest: We challenge a number of common practices in selfsupervised visual representation learning and observe that standard recipes for CNN design do not always translate to self-supervised representation learning.  

- AET vs. AED: Unsupervised Representation Learning by Auto-Encoding Transformations rather than Data. [[paper]](https://arxiv.org/abs/1901.04596) [[code]](https://github.com/maple-research-lab/AET)
  - Liheng Zhang, Guo-Jun Qi, Liqiang Wang, Jiebo Luo. *CVPR 2019*
  - Digest: In this paper, we present a novel paradigm of unsupervised representation learning by Auto-Encoding Transformation (AET) in contrast to the conventional Auto-Encoding Data (AED) approach. Given a randomly sampled transformation, AET seeks to predict it merely from the encoded features as accurately as possible at the output end.  

### 2018

- Challenging Common Assumptions in the Unsupervised Learning of Disentangled Representations. [[paper]](https://arxiv.org/abs/1811.12359) [[code]](https://github.com/google-research/disentanglement_lib)
  - Francesco Locatello, Stefan Bauer, Mario Lucic, Gunnar Rätsch, Sylvain Gelly, Bernhard Schölkopf, Olivier Bachem. *ICML 2019*
  - Digest: Our results suggest that future work on disentanglement learning should be explicit about the role of inductive biases and (implicit) supervision, investigate concrete benefits of enforcing disentanglement of the learned representations, and consider a reproducible experimental setup covering several data sets.  

- Representation Learning with Contrastive Predictive Coding. [[paper]](https://arxiv.org/abs/1807.03748)
  - Aaron van den Oord, Yazhe Li, Oriol Vinyals.
  - Digest: In this work, we propose a universal unsupervised learning approach to extract useful representations from high-dimensional data, which we call Contrastive Predictive Coding. The key insight of our model is to learn such representations by predicting the future in latent space by using powerful autoregressive models.  

## Interpretability

### 2020

- Neural Additive Models: Interpretable Machine Learning with Neural Nets. [[paper]](https://arxiv.org/abs/2004.13912) [[code]](https://github.com/propublica/compas-analysis)
  - Rishabh Agarwal, Nicholas Frosst, Xuezhou Zhang, Rich Caruana, Geoffrey E. Hinton.
  - Digest: We propose Neural Additive Models (NAMs) which combine some of the expressivity of DNNs with the inherent intelligibility of generalized additive models. NAMs learn a linear combination of neural networks that each attend to a single input feature.  

- Restricting the Flow: Information Bottlenecks for Attribution. [[paper]](https://arxiv.org/abs/2001.00396) [[code]](https://github.com/BioroboticsLab/IBA)
  - Karl Schulz, Leon Sixt, Federico Tombari, Tim Landgraf. *ICLR 2020*
  - Digest: By adding noise to intermediate feature maps we restrict the flow of information and can quantify (in bits) how much information image regions provide. We compare our method against ten baselines using three different metrics on VGG-16 and ResNet-50, and find that our methods outperform all baselines in five out of six settings.  

### 2019

- Explaining Classifiers with Causal Concept Effect (CaCE). [[paper]](https://arxiv.org/abs/1907.07165)
  - Yash Goyal, Amir Feder, Uri Shalit, Been Kim.
  - Digest: We define the Causal Concept Effect (CaCE) as the causal effect of (the presence or absence of) a human-interpretable concept on a deep neural net's predictions. We show that the CaCE measure can avoid errors stemming from confounding.

- ML-LOO: Detecting Adversarial Examples with Feature Attribution. [[paper]](https://arxiv.org/abs/1906.03499)
  - Puyudi Yang, Jianbo Chen, Cho-Jui Hsieh, Jane-Ling Wang, Michael I. Jordan.
  - Digest: We observe a significant difference in feature attributions of adversarially crafted examples from those of original ones. Based on this observation, we introduce a new framework to detect adversarial examples through thresholding a scale estimate of feature attribution scores. Furthermore, we extend our method to include multi-layer feature attributions in order to tackle the attacks with mixed confidence levels.  

- Counterfactual Visual Explanations. [[paper]](https://arxiv.org/abs/1904.07451)
  - Yash Goyal, Ziyan Wu, Jan Ernst, Dhruv Batra, Devi Parikh, Stefan Lee. *ICML 2019*
  - Digest: To explore the effectiveness of our explanations in teaching humans, we present machine teaching experiments for the task of fine-grained bird classification. We find that users trained to distinguish bird species fare better when given access to counterfactual explanations in addition to training examples.  

- Interpreting Black Box Models via Hypothesis Testing. [[paper]](https://arxiv.org/abs/1904.00045) [[code]](https://github.com/collin-burns/interpretability-hypothesis-testing)
  - Collin Burns, Jesse Thomason, Wesley Tansey.
  - Digest: We propose two testing methods: one that provably controls the false discovery rate but which is not yet feasible for large-scale applications, and an approximate testing method which can be applied to real-world data sets. In simulation, both tests have high power relative to existing interpretability methods.  

- Explaining Deep Neural Networks with a Polynomial Time Algorithm for Shapley Values Approximation. [[paper]](https://arxiv.org/abs/1903.10992)
  - Marco Ancona, Cengiz Öztireli, Markus Gross. *ICML 2019*
  - Digest: In this work, by leveraging recent results on uncertainty propagation, we propose a novel, polynomial-time approximation of Shapley values in deep neural networks. We show that our method produces significantly better approximations of Shapley values than existing state-of-the-art attribution methods.  

- Unmasking Clever Hans Predictors and Assessing What Machines Really Learn. [[paper]](https://arxiv.org/abs/1902.10178)
  - Sebastian Lapuschkin, Stephan Wäldchen, Alexander Binder, Grégoire Montavon, Wojciech Samek, Klaus-Robert Müller. *Nature Communications*
  - Digest: Here we apply recent techniques for explaining decisions of state-of-the-art learning machines and analyze various tasks from computer vision and arcade games. This showcases a spectrum of problem-solving behaviors ranging from naive and short-sighted, to well-informed and strategic.  

- Towards Automatic Concept-based Explanations. [[paper]](https://arxiv.org/abs/1902.03129) [[code]](https://github.com/amiratag/ACE)
  - Amirata Ghorbani, James Wexler, James Zou, Been Kim. *NeurIPS 2019*
  - Digest: In this work, we propose principles and desiderata for concept based explanation, which goes beyond per-sample features to identify higher-level human-understandable concepts that apply across the entire dataset.

- Global Explanations of Neural Networks: Mapping the Landscape of Predictions. [[paper]](https://arxiv.org/abs/1902.02384) [[code]](https://github.com/capitalone/global-attribution-mapping)
  - Mark Ibrahim, Melissa Louie, Ceena Modarres, John Paisley. *ACM/AAAI AIES 2019*
  - Digest: In response, we present an approach for generating global attributions called GAM, which explains the landscape of neural network predictions across subpopulations. GAM augments global explanations with the proportion of samples that each attribution best explains and specifies which samples are described by each attribution.  

### 2018

- Fooling Network Interpretation in Image Classification. [[paper]](https://arxiv.org/abs/1812.02843)
  - Akshayvarun Subramanya, Vipin Pillai, Hamed Pirsiavash. *ICCV 2019*
  - Digest: We show that it is possible to create adversarial patches which not only fool the prediction, but also change what we interpret regarding the cause of the prediction.  

- Explaining Deep Learning Models - A Bayesian Non-parametric Approach. [[paper]](https://arxiv.org/abs/1811.03422) [[cdoe]](https://github.com/Henrygwb/Explaining-DL)
  - Wenbo Guo, Sui Huang, Yunzhe Tao, Xinyu Xing, Lin Lin. *NeurIPS 2018*
  - Digest: In this work, we propose a novel technical approach that augments a Bayesian non-parametric regression mixture model with multiple elastic nets. Using the enhanced mixture model, we can extract generalizable insights for a target model through a global approximation.  

- This Looks Like That: Deep Learning for Interpretable Image Recognition. [[paper]](https://arxiv.org/abs/1806.10574) [[code]](https://github.com/cfchen-duke/ProtoPNet)
  - Chaofan Chen, Oscar Li, Chaofan Tao, Alina Jade Barnett, Jonathan Su, Cynthia Rudin. *NeurIPS 2019*
  - Digest: In this work, we introduce a deep network architecture -- prototypical part network (ProtoPNet), that reasons in a similar way: the network dissects the image by finding prototypical parts, and combines evidence from the prototypes to make a final classification.  

- RISE: Randomized Input Sampling for Explanation of Black-box Models. [[paper]](https://arxiv.org/abs/1806.07421) [[code]](http://cs-people.bu.edu/vpetsiuk/rise/)
  - Vitali Petsiuk, Abir Das, Kate Saenko. *BMVC 2018*
  - Digest: In this paper, we address the problem of Explainable AI for deep neural networks that take images as input and output a class probability. We propose an approach called RISE that generates an importance map indicating how salient each pixel is for the model's prediction.  

- LEMNA: Explaining Deep Learning based Security Applications. [[paper]](http://xinyuxing.org/pub/ccs18.pdf)
  - Wenbo Guo, Dongliang Mu, Jun Xu, Purui Su, Gang Wang, Xinyu Xing. *CCS 2018*
  - Digest: In this paper, we propose LEMNA, a high-fidelity explanation method dedicated for security applications. Given an input data sample, LEMNA generates a small set of interpretable features to explain how the input sample is classified. The core idea is to approximate a local area of the complex deep learning decision boundary using a simple interpretable model.  

### 2017

- Beyond saliency: understanding convolutional neural networks from saliency prediction on layer-wise relevance propagation. [[paper]](https://arxiv.org/abs/1712.08268) [[code]](https://github.com/Hey1Li/Salient-Relevance-Propagation)
  - Heyi Li, Yunke Tian, Klaus Mueller, Xin Chen. *IVC 2019*
  - Digest: Our proposed method starts out with a layer-wise relevance propagation (LRP) step which estimates a pixel-wise relevance map over the input image. Following, we construct a context-aware saliency map, SR map, from the LRP-generated map which predicts areas close to the foci of attention instead of isolated pixels that LRP reveals.  

- Interpretability Beyond Feature Attribution: Quantitative Testing with Concept Activation Vectors (TCAV). [[paper]](https://arxiv.org/abs/1711.11279)
  - Been Kim, Martin Wattenberg, Justin Gilmer, Carrie Cai, James Wexler, Fernanda Viegas, Rory Sayres. *ICML 2018*
  - Digest: We introduce Concept Activation Vectors (CAVs), which provide an interpretation of a neural net's internal state in terms of human-friendly concepts. The key idea is to view the high-dimensional internal state of a neural net as an aid, not an obstacle.  

- Towards better understanding of gradient-based attribution methods for Deep Neural Networks. [[paper]](https://arxiv.org/abs/1711.06104)
  - Marco Ancona, Enea Ceolini, Cengiz Öztireli, Markus Gross. *ICLR 2018*
  - Digest: In this work, we analyze four gradient-based attribution methods and formally prove conditions of equivalence and approximation between them. By reformulating two of these methods, we construct a unified framework which enables a direct comparison, as well as an easier implementation.  

- Grad-CAM++: Improved Visual Explanations for Deep Convolutional Networks. [[paper]](https://arxiv.org/abs/1710.11063) [[code]](https://github.com/adityac94/Grad_CAM_plus_plus)
  - Aditya Chattopadhyay, Anirban Sarkar, Prantik Howlader, Vineeth N Balasubramanian. *WACV 2018*
  - Digest: Building on a recently proposed method called Grad-CAM, we propose a generalized method called Grad-CAM++ that can provide better visual explanations of CNN model predictions, in terms of better object localization as well as explaining occurrences of multiple object instances in a single image, when compared to state-of-the-art.  

- Interpretation of Neural Networks is Fragile. [[paper]](https://arxiv.org/abs/1710.10547)
  - Amirata Ghorbani, Abubakar Abid, James Zou. *AAAI 2019*
  - Digest: In this paper, we show that interpretation of deep learning predictions is extremely fragile in the following sense: two perceptively indistinguishable inputs with the same predicted label can be assigned very different interpretations.  

- SmoothGrad: removing noise by adding noise. [[paper]](https://arxiv.org/abs/1706.03825) [[code]](https://github.com/hs2k/pytorch-smoothgrad)
  - Daniel Smilkov, Nikhil Thorat, Been Kim, Fernanda Viégas, Martin Wattenberg.
  - Digest:  This paper makes two contributions: it introduces SmoothGrad, a simple method that can help visually sharpen gradient-based sensitivity maps, and it discusses lessons in the visualization of these maps.  

- A Unified Approach to Interpreting Model Predictions. [[paper]](https://arxiv.org/abs/1705.07874) [[code]](https://github.com/slundberg/shap)
  - Scott Lundberg, Su-In Lee. *NeurIPS 2017*
  - Digest: To address this problem, we present a unified framework for interpreting predictions, SHAP (SHapley Additive exPlanations). SHAP assigns each feature an importance value for a particular prediction.  

- Real Time Image Saliency for Black Box Classifiers. [[paper]](https://arxiv.org/abs/1705.07857)
  - Piotr Dabkowski, Yarin Gal. *NeurIPS 2017*
  - Digest: In this work we develop a fast saliency detection method that can be applied to any differentiable image classifier. We train a masking model to manipulate the scores of the classifier by masking salient parts of the input image.  


- Network Dissection: Quantifying Interpretability of Deep Visual Representations. [[paper]](https://arxiv.org/abs/1704.05796) [[code]](http://netdissect.csail.mit.edu/)
  - David Bau, Bolei Zhou, Aditya Khosla, Aude Oliva, Antonio Torralba. *CVPR 2017*
  - Digest: We propose a general framework called Network Dissection for quantifying the interpretability of latent representations of CNNs by evaluating the alignment between individual hidden units and a set of semantic concepts. Given any CNN model, the proposed method draws on a broad data set of visual concepts to score the semantics of hidden units at each intermediate convolutional layer.  

- Learning how to explain neural networks: PatternNet and PatternAttribution. [[paper]](https://arxiv.org/abs/1705.05598)
  - Pieter-Jan Kindermans, Kristof T. Schütt, Maximilian Alber, Klaus-Robert Müller, Dumitru Erhan, Been Kim, Sven Dähne. *ICLR 2018*
  - Digest: DeConvNet, Guided BackProp, LRP, were invented to better understand deep neural networks. Based on our analysis of linear models we propose a generalization that yields two explanation techniques (PatternNet and PatternAttribution) that are theoretically sound for linear models and produce improved explanations for deep networks.  

- Interpretable Explanations of Black Boxes by Meaningful Perturbation. [[paper]](https://arxiv.org/abs/1704.03296)
  - Ruth Fong, Andrea Vedaldi. *ICCV 2017*
  - Digest: In this paper, we make two main contributions: First, we propose a general framework for learning different kinds of explanations for any black box algorithm. Second, we specialise the framework to find the part of an image most responsible for a classifier decision.  

- Learning Important Features Through Propagating Activation Differences. [[paper]](https://arxiv.org/abs/1704.02685) [[code]](https://github.com/kundajelab/deeplift)
  - Avanti Shrikumar, Peyton Greenside, Anshul Kundaje. *ICML 2017*
  - Digest: Here we present DeepLIFT (Deep Learning Important FeaTures), a method for decomposing the output prediction of a neural network on a specific input by backpropagating the contributions of all neurons in the network to every feature of the input. DeepLIFT compares the activation of each neuron to its 'reference activation' and assigns contribution scores according to the difference.  

- Visualizing Deep Neural Network Decisions: Prediction Difference Analysis. [[paper]](https://arxiv.org/abs/1702.04595) [[code]](https://github.com/lmzintgraf/DeepVis-PredDiff)
  - Luisa M Zintgraf, Taco S Cohen, Tameem Adel, Max Welling. *ICLR 2017*
  - Digest: This article presents the prediction difference analysis method for visualizing the response of a deep neural network to a specific input. When classifying images, the method highlights areas in a given input image that provide evidence for or against a certain class. It overcomes several shortcoming of previous methods and provides great additional insight into the decision making process of classifiers.  

- Axiomatic Attribution for Deep Networks. [[paper]](https://arxiv.org/abs/1703.01365) [[code]](https://github.com/ankurtaly/Integrated-Gradients)
  - Mukund Sundararajan, Ankur Taly, Qiqi Yan. *ICML 2017*
  - Digest: We identify two fundamental axioms---Sensitivity and Implementation Invariance that attribution methods ought to satisfy. We show that they are not satisfied by most known attribution methods, which we consider to be a fundamental weakness of those methods.  

### 2016

- Plug & Play Generative Networks: Conditional Iterative Generation of Images in Latent Space. [[paper]](https://arxiv.org/abs/1612.00005)
  - Anh Nguyen, Jeff Clune, Yoshua Bengio, Alexey Dosovitskiy, Jason Yosinski. *CVPR 2017*
  - Digest: Recently, [Nguyen et al. (2016)](https://arxiv.org/abs/1605.09304) showed one interesting way to synthesize novel images by performing gradient ascent in the latent space of a generator network to maximize the activations of one or multiple neurons in a separate classifier network. In this paper we extend this method by introducing an additional prior on the latent code, improving both sample quality and sample diversity, leading to a state-of-the-art generative model that produces high quality images at higher resolutions (227x227) than previous generative models, and does so for all 1000 ImageNet categories.  

- Grad-CAM: Visual Explanations from Deep Networks via Gradient-based Localization. [[paper]](https://arxiv.org/abs/1610.02391) [[code]](https://github.com/ramprs/grad-cam/)
  - Ramprasaath R. Selvaraju, Michael Cogswell, Abhishek Das, Ramakrishna Vedantam, Devi Parikh, Dhruv Batra. *ICCV 2017*
  - Digest: Our approach - Gradient-weighted Class Activation Mapping (Grad-CAM), uses the gradients of any target concept, flowing into the final convolutional layer to produce a coarse localization map highlighting important regions in the image for predicting the concept.  

- Understanding intermediate layers using linear classifier probes. [[paper]](https://arxiv.org/abs/1610.01644)
  - Guillaume Alain, Yoshua Bengio. *ICLR 2017 Workshop*
  - Digest: Neural network models have a reputation for being black boxes. We propose to monitor the features at every layer of a model and measure how suitable they are for classification. We use linear classifiers, which we refer to as "probes", trained entirely independently of the model itself.  

- Synthesizing the preferred inputs for neurons in neural networks via deep generator networks. [[paper]](https://arxiv.org/abs/1605.09304)
  - Anh Nguyen, Alexey Dosovitskiy, Jason Yosinski, Thomas Brox, Jeff Clune. *NeurIPS 2016*
  - Digest:  Here we dramatically improve the qualitative state of the art of activation maximization by harnessing a powerful, learned prior: a deep generator network (DGN).  

- "Why Should I Trust You?": Explaining the Predictions of Any Classifier. [[paper]](https://arxiv.org/abs/1602.04938) [[code]](https://github.com/marcotcr/lime-experiments)
  - Marco Tulio Ribeiro, Sameer Singh, Carlos Guestrin. *KDD 2016*
  - Digest: In this work, we propose LIME, a novel explanation technique that explains the predictions of any classifier in an interpretable and faithful manner, by learning an interpretable model locally around the prediction.  

### 2015

- Learning Deep Features for Discriminative Localization. [[paper]](https://arxiv.org/abs/1512.04150)
  - Bolei Zhou, Aditya Khosla, Agata Lapedriza, Aude Oliva, Antonio Torralba. *CVOR 2016*
  - Digest: In this work, we revisit the global average pooling layer proposed in [13], and shed light on how it explicitly enables the convolutional neural network to have remarkable localization ability despite being trained on image-level labels.  

- Explaining NonLinear Classification Decisions with Deep Taylor Decomposition. [[paper]](https://arxiv.org/abs/1512.02479)
  - Grégoire Montavon, Sebastian Bach, Alexander Binder, Wojciech Samek, Klaus-Robert Müller. *PR 2017*
  - Digest: In this paper we introduce a novel methodology for interpreting generic multilayer neural networks by decomposing the network classification decision into contributions of its input elements.  

- Understanding Neural Networks Through Deep Visualization. [[paper]](https://arxiv.org/abs/1506.06579)  
  - Jason Yosinski, Jeff Clune, Anh Nguyen, Thomas Fuchs, Hod Lipson. *ICML 2015 Workshop*
  - Digest:  We introduce two such tools here. The first is a tool that visualizes the activations produced on each layer of a trained convnet as it processes an image or video (e.g. a live webcam stream). The second tool enables visualizing features at each layer of a DNN via regularized optimization in image space.  

### 2014

- Striving for Simplicity: The All Convolutional Net. [[paper]](https://arxiv.org/abs/1412.6806)
  - Jost Tobias Springenberg, Alexey Dosovitskiy, Thomas Brox, Martin Riedmiller. *ICLR 2015*
  - Digest: We find that max-pooling can simply be replaced by a convolutional layer with increased stride without loss in accuracy on several image recognition benchmarks.  

- Understanding Deep Image Representations by Inverting Them. [[paper]](https://arxiv.org/abs/1412.0035)
  - Aravindh Mahendran, Andrea Vedaldi. *CVPR 2015*
  - Digest: In this paper we conduct a direct analysis of the visual information contained in representations by asking the following question: given an encoding of an image, to which extent is it possible to reconstruct the image itself? To answer this question we contribute a general framework to invert representations.  

- How transferable are features in deep neural networks? [[paper]](https://arxiv.org/abs/1411.1792) [[code]](http://yosinski.com/transfer)
  - Jason Yosinski, Jeff Clune, Yoshua Bengio, Hod Lipson. *NeurIPS 2014*
  - Digest: Features must eventually transition from general to specific by the last layer of the network, but this transition has not been studied extensively. In this paper we experimentally quantify the generality versus specificity of neurons in each layer of a deep convolutional neural network and report a few surprising results.  

### 2013

- Visualizing and Understanding Convolutional Networks. [[paper]](https://arxiv.org/abs/1311.2901)
  - Matthew D Zeiler, Rob Fergus. *ECCV 2014*
  - Digest: We introduce a novel visualization technique that gives insight into the function of intermediate feature layers and the operation of the classifier. We also perform an ablation study to discover the performance contribution from different model layers.  
