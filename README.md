# LearningVLMProgressTracker

8-Week Plan: Zero to vLLM Contributor
Time commitment: 10-15 hours/week (2 hours weekdays + 5-10 hours weekend)

WEEK 1: Transformer Fundamentals
Goal: Understand how transformers work at a conceptual level 
Monday-Tuesday (2 hours):

Watch: Andrej Karpathy "Intro to Large Language Models" (1 hour) : https://www.youtube.com/watch?v=XfpMkf4rD6E - watched for 30 min
Read: "The Illustrated Transformer" by Jay Alammar (1 hour) - https://jalammar.github.io/illustrated-transformer/
Output: Write 1-page summary in your own words

Wednesday-Thursday (2 hours):

Watch: Andrej Karpathy "Let's build GPT from scratch" (2 hours, can speed up)
Focus on: attention mechanism, self-attention, multi-head attention

Friday (2 hours):

Read: "Attention Is All You Need" paper - just sections 3.1-3.2 (skip the math details)
Understand: Q, K, V matrices and what they do

Weekend (6-8 hours):

HANDS-ON: Implement tiny transformer from scratch

Follow Karpathy's code but type it yourself
Use PyTorch
Train on tiny dataset (Shakespeare text or similar)
Deliverable: Working character-level transformer



Key concepts to internalize:

What is attention computing? (similarity between query and keys)
Why self-attention? (tokens attending to other tokens)
What's in the KV cache? (why it matters for inference)


WEEK 2: LLM Inference & Memory
Goal: Understand how LLM inference works and why it's memory-intensive
Monday-Tuesday (2 hours):

Read: "LLM Inference Performance Engineering" blog posts
Google: "KV cache in transformers" - read top 3 results
Understand: Autoregressive generation (generate token by token)

Wednesday-Thursday (2 hours):

HANDS-ON: Profile your transformer from Week 1

Add code to track memory usage
Measure: KV cache size as sequence length increases
See: Why memory grows linearly with sequence length



Friday (2 hours):

Read: "Making Deep Learning Go Brrrr From First Principles" (Horace He)
Focus on: GPU memory hierarchy, why memory bandwidth matters

Weekend (6-8 hours):

PROJECT: Build naive LLM serving API

Download Llama 3.2 1B model (small enough to run locally)
Use Hugging Face transformers library
Build simple Flask API: POST /generate
Measure: Latency, memory usage, throughput
Deliverable: Working API + performance measurements



Key insights to gain:

Memory is the bottleneck (not compute)
KV cache dominates memory for long sequences
Batching is hard (sequences have different lengths)


WEEK 3: vLLM Architecture Study
Goal: Understand vLLM's key innovations
Monday-Tuesday (2 hours):

Read: vLLM paper - "Efficient Memory Management for Large Language Model Serving with PagedAttention"
Focus on: Problem statement, PagedAttention concept

Wednesday-Thursday (2 hours):

Watch: vLLM presentation videos (search YouTube)
Read: vLLM blog posts on their website

Friday (2 hours):

Read: vLLM GitHub README thoroughly
Browse: Architecture docs
Understand: Continuous batching concept

Weekend (8-10 hours):

HANDS-ON: Install and run vLLM
