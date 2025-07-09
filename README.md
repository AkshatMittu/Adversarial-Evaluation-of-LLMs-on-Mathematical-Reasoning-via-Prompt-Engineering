# Adversarial-Evaluation-of-LLMs-on-Mathematical-Reasoning-via-Prompt-Engineering

This project has two lightweight LLMs, Phi 4-mini-instruct and Qwen 3-4b, competing against each other to solve some mathematical reasoning tasks. This project solely works on prompt engineering. In each round, prompts are optimized automatically via another LLM, Mistral 7B instruct, based on their scores in the previous round. This LLM-as-judge approach also gives suggestions to optimize prompts and improve components of the scoring function, as given below.


