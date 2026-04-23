# Causal Discovery Prompt Template

This is the standard prompt template used to extract causal prior knowledge from the LLM (Gemini 2.5 Pro). 

## Template
Replace `{Variable 1}` and `{Variable 2}` with the descriptive full names of the variables you wish to evaluate.

---
I want you to act as a causal discovery engine. I will provide a variable pair. You must determine the most likely causal relationship based on the options provided below. 

**Options:** A. Changing {Variable 1} can directly change {Variable 2}. 
B. Changing {Variable 2} can directly change {Variable 1}. 
C. Both A and B are true. 
D. None of the above. No direct relationship exists. 

**Instructions:** Let’s think step-by-step to ensure we get the right answer. After reasoning, provide the final answer within the tags, like this: <Answer>A/B/C/D</Answer>.
---

## Usage Note
In our study, we observed that using descriptive full names (e.g., "Protein Kinase C" instead of "PKC") significantly improves the reasoning performance of the LLM by leveraging its semantic background knowledge.
