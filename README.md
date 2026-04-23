# Causal Discovery from Real-World Educational Data via LLM-Informed Methods

Implementation, prompt templates, and interaction logs for the research paper: **"Causal Discovery from Real-World Educational Data via LLM-Informed Methods"** (Submitted to ICCE 2026).

## 🚀 Overview
Extracting evidence from real-world educational data (RWD) is often hindered by unobserved confounders and limited sample sizes. This study proposes a novel hybrid methodology that integrates the extensive relational knowledge of **Large Language Models (LLMs)** into the **LiNGAM-MMI** framework. By leveraging LLM-based priors to guide the statistical discovery process, we achieve more accurate and stable causal structures in educational settings.

## 📂 Repository Structure
* [cite_start]`/prompts`: Full text of prompt templates used for causal reasoning[cite: 8].
* `/logs`: Detailed interaction logs with Gemini 2.5 Pro, including step-by-step reasoning for each variable pair.
* `/data`: Mapping tables of variable abbreviations to descriptive full names and the resulting prior knowledge matrices ($K$).
* `/scripts`: Python implementation of the integration algorithm and LiNGAM-MMI execution.

## 🤖 LLM Configuration & Reproducibility
[cite_start]To ensure the scientific rigor and reproducibility of our experiments, the following setup was used[cite: 20]:
* **Model:** Gemini 2.5 Pro (via the official Gemini Web Interface)
* **Access Date:** April 2026
* **Hyper-parameters:** System-default settings ($Temperature = 1.0$, $Top\text{-}p = 0.95$, $Top\text{-}k = 64$)
* **Protocol:** To prevent context contamination, the "**New Chat**" function was used to reset the session for every variable-pair evaluation.

## 📝 Prompt Design & Logic
[cite_start]The prompt design follows the methodology proposed by **Lee et al.**[cite: 4].
1. **Role Prompting:** The LLM is tasked to act as a "causal discovery engine."
2. **Multiple-Choice Template:** Causal directions are determined via a four-option format (A, B, C, or D).
3. **Chain-of-Thought (CoT):** The instruction "**Let’s think step-by-step**" is included to enhance logical reasoning and accuracy.

The complete interaction logs for the **Sachs dataset** (11 variables) and the **LEAF dataset** (20 indicators) are provided in the `/logs` directory to demonstrate the LLM's reasoning process.

## 📊 Variable Mapping (LEAF Dataset)
[cite_start]We replaced internal data headers with descriptive full names to maximize the LLM's semantic reasoning capability[cite: 205].

| Original Header | Descriptive Name (Input to LLM) |
| :--- | :--- |
| `Marker_cnt` | Total number of markers used in the digital textbook |
| `Memo_cnt` | Total number of memos recorded by the student |
| `Score_diff` | Improvement in test scores between pre- and post-summer break |
| *(Refer to `/data/variable_mapping.md` for the full list)* |

## 🔗 Citation
If you use this code or these templates in your research, please cite our paper:
```bibtex
@inproceedings{sawada2026causal,
  title={Causal Discovery from Real-World Educational Data via LLM-Informed Methods},
  author={Sawada, Nobuki and Hsu, Chia-Yu and Okumura, Kouki and Ogata, Hiroaki},
  booktitle={Proceedings of the 34th International Conference on Computers in Education (ICCE 2026)},
  year={2026}
}

## 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
