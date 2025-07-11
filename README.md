# Adversarial-Evaluation-of-LLMs-on-Mathematical-Reasoning-via-Prompt-Engineering

This project has two lightweight LLMs, Phi 4-mini-instruct and Qwen 3-4b, competing against each other to solve some mathematical reasoning tasks. This project solely works on prompt engineering. 

In each round, prompts are optimized automatically via another LLM, Mistral 7B instruct, based on their scores in the previous round. This LLM-as-judge approach gives suggestions to optimize prompts and improve components of the scoring function, as given below.


Score = (0.05 × (1 / log(number_of_tokens_generated + 2)))
      + (0.10 × context_length_utilized)
      + (0.15 × (explanation_score / 100))
      + (0.15 × (1 / log(generation_time + 2)))
      + (0.40 × correct_answer)
      + (0.15 × log(token_speed + 1))


![Score Equation](https://latex.codecogs.com/svg.image?\text{Score}=0.05\cdot\left(\frac{1}{\log(\text{tokens}+2)}\right)%2B0.10\cdot\text{context}%2B0.15\cdot\left(\frac{\text{explanation}}{100}\right)%2B0.15\cdot\left(\frac{1}{\log(\text{time}+2)}\right)%2B0.40\cdot\text{correct}%2B0.15\cdot\log(\text{speed}%2B1))



