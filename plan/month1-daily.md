# Month 1 daily plan (Nov 11 – Dec 6)

Weekdays are about 1 hour, weekends about 2.5 hours. Every day has the same four parts:

- **Watch/Read**: the input, with rough length
- **Do**: something you produce (this is what makes it stick)
- **Check**: a question you should be able to answer without notes
- **Done when**: the finish line for the day

Video links go to the series playlist; pick the chapter or lecture by number.

## Rules that make this work

1. **Minimum day is 15 minutes.** On a bad day, do only the Watch part. Never zero.
2. **Missed a day? Don't double up.** Move on to today's plan and catch the missed video on the weekend. Items marked *(optional)* are the first to drop.
3. **Always write something.** Notes go in `notes/`, code goes in `exercises/`. A day with no commit is a day that fades.
4. **Sunday review (10 min).** Re-answer that week's Check questions cold. Anything you can't answer goes on next week's list.
5. **Coding practice** is marked ➕ on two days a week: one [NeetCode](https://neetcode.io/) problem, 30 minutes max, in Python.

---

## Week 1: Linear algebra (Nov 11 – 15)

Chapters 1–2 are done. Wed–Fri are slightly compressed to get back on schedule by Saturday.

### Wed Nov 11 — Matrices as transformations
- [ ] **Watch:** [3Blue1Brown](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab) ch 3 (Linear transformations and matrices) and ch 4 (Matrix multiplication as composition), ~20 min total
- [ ] **Do:** On paper: for the matrix [[1, 2], [3, 4]], say where î and ĵ land, then compute where (2, 1) lands. Multiply two 2×2 matrices by hand, then multiply them in the other order.
- [ ] **Check:** Why do the columns of a matrix tell you everything about the transformation? Why is AB ≠ BA in general?
- [ ] **Done when:** you can read a 2×2 matrix and describe the transformation without computing anything.

### Thu Nov 12 — Determinant, inverse, rank ➕
- [ ] **Watch:** [3Blue1Brown](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab) ch 5 (3D transformations, 5 min), ch 6 (The determinant), ch 7 (Inverse matrices, column space, null space), ~30 min total
- [ ] **Do:** Compute det of [[3, 1], [0, 2]] and [[2, 4], [1, 2]] by hand. For the second one, describe its column space and null space.
- [ ] **Check:** What does det = 0 mean geometrically? What is rank, in one sentence?
- [ ] **Done when:** you can explain why a matrix with det = 0 has no inverse.
- [ ] ➕ **Coding:** NeetCode "Contains Duplicate" (Arrays & Hashing)

### Fri Nov 13 — Dot products
- [ ] **Watch:** [3Blue1Brown](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab) ch 8 (Nonsquare matrices, 4 min), ch 9 (Dot products and duality, 14 min)
- [ ] **Watch (optional):** ch 10–11 (Cross products). Skim or skip; rarely used in ML.
- [ ] **Do:** Compute the dot product of (1, 2) and (3, −1). Compute the cosine of the angle between them.
- [ ] **Check:** What does a dot product of 0 mean? Why is a dot product the same as multiplying by a 1×n matrix?
- [ ] **Done when:** you can explain cosine similarity using the dot product.

### Sat Nov 14 — Eigenvectors (2.5 hr)
- [ ] **Watch:** [3Blue1Brown](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab) ch 13 (Change of basis), ch 14 (Eigenvectors and eigenvalues), ~30 min. Ch 12 (Cramer's rule) is *optional*.
- [ ] **Do:** Find the eigenvalues and eigenvectors of [[3, 1], [0, 2]] by hand (solve det(A − λI) = 0). Write half a page of notes on eigenvectors in your own words in `notes/`.
- [ ] **Do:** Install Python + numpy if needed. Check your hand answer with `np.linalg.eig`.
- [ ] **Check:** What is an eigenvector, geometrically? What does an eigenvalue of 1 mean? Of 0?
- [ ] **Done when:** your hand answer matches numpy.

### Sun Nov 15 — Finish linear algebra + numpy (2.5 hr) ➕
- [ ] **Watch:** [3Blue1Brown](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab) ch 15 (Quick trick for eigenvalues), ch 16 (Abstract vector spaces), ~30 min
- [ ] **Do:** Create `exercises/linear-algebra/practice.py` (or a notebook). In numpy: build vectors and matrices, matrix-multiply with `@`, compute det, inverse, rank, eigendecomposition. Show that a rank-1 matrix has det 0. Solve Ax = b with `np.linalg.solve`.
- [ ] **Review:** Re-answer every Check question from this week, cold.
- [ ] **Done when:** the practice file runs and is committed.
- [ ] ➕ **Coding:** NeetCode "Valid Anagram"

---

## Week 2: Calculus and probability (Nov 16 – 22)

### Mon Nov 16 — Derivatives
- [ ] **Watch:** [3Blue1Brown Essence of Calculus](https://www.youtube.com/playlist?list=PLZHQObOWTQDMsr9K-rj53DwVRMYO3t5Yr) ch 1–3 (~45 min)
- [ ] **Do:** Differentiate by hand: x³, 1/x, sin(x)·x². Sketch x² and its derivative.
- [ ] **Check:** What does "derivative" mean without using the word "slope"?
- [ ] **Done when:** the power rule feels obvious, not memorized.

### Tue Nov 17 — Chain rule
- [ ] **Watch:** [Essence of Calculus](https://www.youtube.com/playlist?list=PLZHQObOWTQDMsr9K-rj53DwVRMYO3t5Yr) ch 4 (Chain rule and product rule), ch 5 (Euler's number), ~30 min
- [ ] **Do:** Differentiate (3x + 1)², e^(−x²), and the sigmoid σ(x) = 1 / (1 + e^(−x)). Show that σ′(x) = σ(x)(1 − σ(x)).
- [ ] **Check:** State the chain rule in words. Why is it the heart of backpropagation?
- [ ] **Done when:** you derived the sigmoid derivative yourself. You will use it for years.

### Wed Nov 18 — Partial derivatives and gradients ➕
- [ ] **Watch:** [Khan Academy Multivariable Calculus](https://www.khanacademy.org/math/multivariable-calculus): "Partial derivatives" intro, "Gradient", "Gradient and directional derivatives" (~40 min)
- [ ] **Do:** For f(x, y) = x²y + 3y, compute ∂f/∂x, ∂f/∂y and the gradient at (1, 2).
- [ ] **Check:** Which way does the gradient point? Why does gradient descent subtract it?
- [ ] **Done when:** you can compute a gradient for any simple two-variable function.
- [ ] ➕ **Coding:** NeetCode "Two Sum"

### Thu Nov 19 — Matrix calculus
- [ ] **Read:** [CS229 Linear Algebra Review](https://cs229.stanford.edu/lectures-spring2022/cs229-linear_algebra_review.pdf), section 4 (Matrix calculus): gradient, Hessian, gradients of linear and quadratic forms (~45 min; read slowly)
- [ ] **Do:** Verify by hand, for a 2D example, that ∇ₓ(bᵀx) = b and ∇ₓ(xᵀAx) = 2Ax when A is symmetric.
- [ ] **Check:** What shape is the gradient of a scalar function of a vector? What is the Hessian?
- [ ] **Done when:** those two identities are in your notes. They produce the normal equations next week.

### Fri Nov 20 — Probability, part 1
- [ ] **Read:** [CS229 Probability Review](https://cs229.stanford.edu/lectures-spring2022/cs229-probability_review.pdf), sections 1–2: axioms, conditional probability, Bayes' rule, random variables, PDF/CDF (~45 min)
- [ ] **Do:** A test is 99% accurate and 1% of people have a condition. If you test positive, what is the chance you have it? Work it with Bayes' rule.
- [ ] **Check:** What is the difference between P(A|B) and P(B|A)?
- [ ] **Done when:** you get about 50% on the exercise and can explain why it isn't 99%.

### Sat Nov 21 — Probability, part 2 (2.5 hr)
- [ ] **Read:** [Probability Review](https://cs229.stanford.edu/lectures-spring2022/cs229-probability_review.pdf), rest: expectation, variance, common distributions (Bernoulli, Gaussian), joint distributions, independence, multivariate Gaussian
- [ ] **Do:** Compute the mean and variance of a fair die by hand. In numpy, sample 10,000 values from a Gaussian and plot a histogram; check the sample mean and variance.
- [ ] **Do:** Write the Gaussian PDF from memory and label μ and σ².
- [ ] **Check:** What does independence mean? What do the mean vector and covariance matrix of a multivariate Gaussian control?
- [ ] **Done when:** histogram script committed to `exercises/probability/`.

### Sun Nov 22 — Gradient descent from scratch (2.5 hr) ➕
- [ ] **Setup:** Python environment with numpy, matplotlib, Jupyter
- [ ] **Do (part 1):** Implement gradient descent on f(x) = (x − 3)². Print x each step. Try learning rates 0.01, 0.1, 1.1 and see what happens.
- [ ] **Do (part 2):** Generate noisy data y = 2x + 1 + noise. Fit a line with gradient descent on the least-squares loss, using only numpy. Plot the loss per iteration and the fitted line.
- [ ] **Review:** Re-answer this week's Check questions.
- [ ] **Check:** What happens when the learning rate is too large? Too small?
- [ ] **Done when:** your fit recovers roughly slope 2 and intercept 1, committed to `exercises/gradient-descent/`.
- [ ] ➕ **Coding:** NeetCode "Group Anagrams"

---

## Week 3: CS229 begins (Nov 23 – 29)

CS229 lectures run about 80 minutes. Watch at 1.25–1.5× to fit a weekday hour, and pause to copy down every derivation.

### Mon Nov 23 — Lecture 1: Introduction
- [ ] **Watch:** [CS229 Lecture 1](https://www.youtube.com/playlist?list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU) (skip the course logistics; ~45 min of content)
- [ ] **Do:** Bookmark the course site, download the main notes PDF and Problem Set 1.
- [ ] **Check:** What is the difference between supervised, unsupervised and reinforcement learning? Give one example of each.
- [ ] **Done when:** PS1 is downloaded and you've skimmed its questions.

### Tue Nov 24 — Lecture 2: Linear regression and gradient descent
- [ ] **Watch:** [CS229 Lecture 2](https://www.youtube.com/playlist?list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU)
- [ ] **Do:** Write down, in the course notation: the hypothesis h_θ(x), the cost J(θ), and the batch and stochastic gradient descent update rules.
- [ ] **Check:** When would you choose stochastic over batch gradient descent?
- [ ] **Done when:** you can connect each formula to Sunday's code.

### Wed Nov 25 — Normal equations ➕
- [ ] **Read:** [CS229 main notes](https://cs229.stanford.edu/main_notes.pdf), linear regression chapter (LMS algorithm, normal equations)
- [ ] **Do:** Derive θ = (XᵀX)⁻¹Xᵀy yourself, using Thursday Nov 19's two identities. Then add a normal-equations solution to your gradient descent script and confirm both give the same line.
- [ ] **Check:** Why don't we use the normal equations for neural networks?
- [ ] **Done when:** both methods agree to a few decimal places.
- [ ] ➕ **Coding:** NeetCode "Top K Frequent Elements"

### Thu Nov 26 — Thanksgiving
- [ ] *(optional, 20 min)* Skim your notes from the last two weeks. Rest is fine.

### Fri Nov 27 — Lecture 3: Logistic regression
- [ ] **Watch:** [CS229 Lecture 3](https://www.youtube.com/playlist?list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU) (locally weighted regression, probabilistic interpretation, logistic regression, Newton's method)
- [ ] **Do:** Write the logistic regression log-likelihood and its gradient ascent update. Notice that the update looks the same as linear regression's.
- [ ] **Check:** Why does least squares fall out of assuming Gaussian noise? Why use log-likelihood rather than likelihood?
- [ ] **Done when:** you can explain "maximum likelihood" in two sentences.

### Sat Nov 28 — Lecture 4: Perceptron and GLMs (2.5 hr)
- [ ] **Watch:** [CS229 Lecture 4](https://www.youtube.com/playlist?list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU) (perceptron, exponential family, GLMs, softmax regression)
- [ ] **Read:** [main notes](https://cs229.stanford.edu/main_notes.pdf) sections on logistic regression, Newton's method and GLMs
- [ ] **Do:** Implement logistic regression with gradient ascent in numpy on a toy 2D dataset (two Gaussian blobs). Plot the decision boundary.
- [ ] **Check:** What three things define a GLM? What does softmax do?
- [ ] **Done when:** your classifier separates the blobs, committed to `exercises/cs229/`.

### Sun Nov 29 — Start Problem Set 1 (2.5 hr) ➕
- [ ] **Do:** PS1 question on linear classifiers, logistic regression part: derive the Hessian, then implement Newton's method. (Question numbers follow the Autumn 2018 PS1; if your copy differs, match by topic.)
- [ ] **Review:** Re-answer this week's Check questions.
- [ ] **Done when:** Newton's method converges on the PS1 dataset in under ~10 iterations.
- [ ] ➕ **Coding:** NeetCode "Valid Palindrome" (Two Pointers)

---

## Week 4: Classifiers and Problem Set 1 (Nov 30 – Dec 6)

### Mon Nov 30 — Lecture 5, first half: GDA
- [ ] **Watch:** [CS229 Lecture 5](https://www.youtube.com/playlist?list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU) up to the start of Naive Bayes (~40 min)
- [ ] **Do:** Write down the GDA model: the distributions of y and x|y, and the four parameters it learns.
- [ ] **Check:** What is the difference between a generative and a discriminative model?
- [ ] **Done when:** you can say when GDA beats logistic regression and when it doesn't.

### Tue Dec 1 — Lecture 5, second half: Naive Bayes
- [ ] **Watch:** rest of [Lecture 5](https://www.youtube.com/playlist?list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU)
- [ ] **Read:** [main notes](https://cs229.stanford.edu/main_notes.pdf), generative learning algorithms chapter
- [ ] **Do:** By hand, classify a 3-word message as spam or not from a tiny made-up word-count table using Naive Bayes.
- [ ] **Check:** What is the "naive" assumption? Why is it obviously false, and why does it work anyway?
- [ ] **Done when:** your hand calculation is in your notes.

### Wed Dec 2 — Problem Set 1: GDA ➕
- [ ] **Do:** PS1 linear classifiers question, GDA part: implement GDA and compare its decision boundary with logistic regression on both datasets.
- [ ] **Check:** On which dataset does GDA do worse, and why?
- [ ] **Done when:** both boundaries are plotted on the same figure.
- [ ] ➕ **Coding:** NeetCode "Best Time to Buy and Sell Stock" (Sliding Window)

### Thu Dec 3 — Lecture 6: Naive Bayes wrap-up and SVM intro
- [ ] **Watch:** [CS229 Lecture 6](https://www.youtube.com/playlist?list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU) (Laplace smoothing, event models, start of support vector machines)
- [ ] **Do:** Redo Tuesday's hand example with Laplace smoothing after adding a word that never appeared in training.
- [ ] **Check:** What problem does Laplace smoothing fix? What is the "margin" of a classifier?
- [ ] **Done when:** you can sketch a max-margin boundary and mark the support vectors.

### Fri Dec 4 — Lecture 7: Kernels
- [ ] **Watch:** [CS229 Lecture 7](https://www.youtube.com/playlist?list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU) (kernels, soft-margin SVM)
- [ ] **Do:** For x = (x₁, x₂), show that the kernel K(x, z) = (xᵀz)² equals an inner product of explicit feature vectors, and write out those features.
- [ ] **Check:** What is the kernel trick, in one sentence? Why does it save computation?
- [ ] **Done when:** the expansion is in your notes.

### Sat Dec 5 — Problem Set 1: Poisson regression (2.5 hr)
- [ ] **Do:** PS1 Poisson regression question: show Poisson is in the exponential family, derive the update rule, implement it.
- [ ] **Do (optional):** PS1 locally weighted regression question.
- [ ] **Done when:** your Poisson predictions track the validation data in a plot.

### Sun Dec 6 — Wrap up Month 1 (2.5 hr) ➕
- [ ] **Do:** Finish any open PS1 parts. Compare against the official solutions and note what you got wrong and why.
- [ ] **Review:** Go through `notes/month1-concepts.md`. Mark each concept: solid / shaky / lost. Shaky and lost items carry into Month 2's first week.
- [ ] **Do:** Write a 5-line Month 1 retrospective in `notes/`: what worked, what didn't, real hours per week.
- [ ] **Plan:** Set up the Month 2 daily plan.
- [ ] ➕ **Coding:** NeetCode "Valid Parentheses" (Stack)
