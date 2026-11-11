# Month 1 key concepts

The core idea: a model is a matrix of numbers, and training uses gradients to adjust those numbers until a probability-based loss is small.

**If you remember only three:** matrix = linear transformation (every layer), chain rule (backprop), gradient descent (training).

## Linear algebra

| Concept | Key idea | Why it matters for AI |
| --- | --- | --- |
| Vector | A list of numbers, or an arrow in space | Every data point, feature set and embedding is a vector |
| Linear combination & span | All vectors reachable as av + bw | What a linear model can and can't represent |
| Linear independence & basis | A minimal set of vectors that spans the space, no redundancy | Redundant features add no information; dimension = number of basis vectors |
| Matrix = linear transformation | A matrix records where the basis vectors land | Every neural network layer is Wx + b |
| Matrix multiplication = composition | AB means apply B, then A | Stacked linear layers collapse into one; that's why activations are needed |
| Determinant | How much a transformation scales area or volume; 0 = space gets squished | det = 0 means not invertible |
| Rank, column space, null space | Rank = number of output dimensions; null space = inputs mapped to zero | Low-rank ideas power LoRA fine-tuning and compression |
| Inverse | Undoes a transformation | Used in the normal equations |
| Dot product | Projection; how aligned two vectors are | Cosine similarity, attention scores |
| Eigenvectors & eigenvalues | Directions only stretched, not rotated | PCA, training stability |
| Change of basis | Same vector, different coordinates | PCA and embeddings |

## Calculus

| Concept | Key idea | Why it matters for AI |
| --- | --- | --- |
| Derivative | Rate of change, or slope | Which way to nudge a parameter to lower the loss |
| Chain rule | d/dx f(g(x)) = f′(g(x)) · g′(x) | This is backpropagation |
| Gradient | Vector of partial derivatives; points uphill | Gradient descent steps the opposite way |
| Hessian | Matrix of second derivatives (curvature) | Used by Newton's method |

## Probability

| Concept | Key idea | Why it matters for AI |
| --- | --- | --- |
| Conditional probability & Bayes' rule | P(A\|B) = P(B\|A) P(A) / P(B) | Basis of Naive Bayes and GDA |
| Expectation & variance | Average value and spread | Loss is an average error |
| Gaussian distribution | Bell curve set by mean and variance | Assumed noise in linear regression; GDA |
| Maximum likelihood (MLE) | Parameters that make the data most probable | Derives least squares and cross-entropy loss |

## CS229 lectures 1–7

| Concept | Key idea | Why it matters for AI |
| --- | --- | --- |
| Supervised learning | Learn x → y from labeled examples | The setup for most practical ML |
| Linear regression & least squares | Minimize J(θ) = ½ Σ (hθ(x) − y)² | The template for all other models |
| Gradient descent (batch vs stochastic) | θ := θ − α∇J; α = learning rate | How every neural network is trained |
| Normal equations | θ = (XᵀX)⁻¹Xᵀy | Exact answer for small linear problems |
| Locally weighted regression | Weight nearby points more | Example of a non-parametric model |
| Logistic regression & sigmoid | σ(z) = 1 / (1 + e⁻ᶻ) outputs a probability | The basic classifier; a single neuron |
| Newton's method | Uses the Hessian; fewer steps | Too expensive for large models |
| Perceptron | Hard 0/1 threshold | Ancestor of neural networks |
| GLMs & exponential family | One framework for linear, logistic, softmax | Explains the form of common losses |
| Softmax | Scores → probabilities over many classes | An LLM's final layer picking the next token |
| Generative vs discriminative | p(x\|y) (GDA, Naive Bayes) vs p(y\|x) (logistic) | Two ways to build a classifier |
| Laplace smoothing | Add 1 to counts so nothing is zero | Handles unseen words or events |
| SVM & margin | Boundary with the widest gap | Strong classic classifier |
| Kernel trick | Inner products in high dimensions without building them | Non-linear boundaries from linear methods |
