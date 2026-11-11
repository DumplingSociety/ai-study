# AI Study

A self-study path into AI/ML systems engineering, using free resources. About 10 hours a week (weekdays ~1 hr, weekends ~2.5 hr), starting November 2026.

**Focus:** ML infrastructure — inference, GPU programming, and LLM systems — building on a C/systems programming background.

- [Study materials](materials.md): every resource, with links
- [Notes](notes/): concept summaries per month
- [Exercises](exercises/): problem sets and practice code
- [Projects](projects/): larger builds

## Plan

### Month 1 (Nov 9 – Dec 6): Math refresh + start CS229

- [ ] Week 1: 3Blue1Brown *Essence of Linear Algebra* (all chapters) + numpy practice
- [ ] Week 2: 3Blue1Brown *Essence of Calculus*, partial derivatives & gradients, CS229 probability review, gradient descent from scratch in numpy
- [ ] Week 3: CS229 (Autumn 2018) Lectures 1–4, start Problem Set 1
- [ ] Week 4: CS229 Lectures 5–7, finish Problem Set 1 (focus on code, go light on proofs)

Key concepts: [notes/month1-concepts.md](notes/month1-concepts.md)

### Month 2 (Dec): Neural nets + build from scratch

- [ ] CS229, lightly: neural networks, backprop, bias/variance lectures only
- [ ] Karpathy *Neural Networks: Zero to Hero*: micrograd
- [ ] Karpathy *Zero to Hero*: makemore series

### Month 3 (Jan): Transformers + C/CUDA

- [ ] Karpathy "Let's build GPT" and the tokenizer video
- [ ] Read Karpathy's **llm.c** (GPT-2 training in plain C/CUDA)
- [ ] Get comfortable with PyTorch

### Month 4 (Feb): Systems for LLMs

- [ ] Stanford **CS336** (Language Modeling from Scratch) lectures
- [ ] CS336 Assignment 1 (tokenizer + transformer from scratch)
- [ ] CUDA basics: **GPU MODE** lecture series
- [ ] Start the main project

### Month 5 (Mar): Inference + main project

- [ ] KV cache, batching, quantization
- [ ] vLLM (PagedAttention) paper and parts of the llama.cpp source
- [ ] **Main project:** small LLM inference engine in C — profile, optimize, write up before/after numbers

### Month 6+ (Apr onward): Agent infrastructure

- [ ] Second project: agent tracing/evaluation tool (log tool calls, latency, failures; replay runs)
- [ ] ML system design practice (e.g. "design an LLM serving system")

## Ongoing: coding practice

- Now – Month 3: 2–3 problems a week ([NeetCode 150](https://neetcode.io/), solved on LeetCode, in Python)
- Month 4: 4–5 a week, plus systems-style problems (LRU cache, rate limiter, thread-safe queue, allocator)
- Month 5+: about 1 a day, timed
