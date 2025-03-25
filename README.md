# Challenges and Applications of Large Language Models

**Authors:**  
- Jean Kaddour<sup>α, †</sup>  
- Joshua Harris<sup>β</sup>  
- Maximilian Mozes<sup>α</sup>  
- Herbie Bradley<sup>γ, δ, ϵ</sup>  
- Roberta Raileanu<sup>ζ</sup>  
- Robert McHardy<sup>η</sup>

**Institutions:**  
- <sup>α</sup> University College London  
- <sup>β</sup> UK Health Security Agency  
- <sup>γ</sup> EleutherAI  
- <sup>δ</sup> University of Cambridge  
- <sup>ϵ</sup> Stability AI  
- <sup>ζ</sup> Meta AI Research  
- <sup>η</sup> InstaDeep

## Overview

The paper aims to provide a structured overview of the current state of large language models (LLMs) by highlighting major unresolved challenges and identifying areas where these models have demonstrated significant success.

**Challenges identified** are grouped into three broad categories:

1. **Design Challenges**  
   Issues related to the technical construction of models, including data quality, tokenization methods, computational costs, fine-tuning requirements, inference speed, and limitations on processing long texts.

2. **Behavioral Challenges**  
   Problems encountered when using LLMs in real-world scenarios, such as sensitivity to prompt wording, generating incorrect information (hallucinations), producing biased outputs, and relying on outdated knowledge.

3. **Scientific Challenges**  
   Fundamental issues affecting the academic advancement of LLMs, such as unreliable evaluation methods, lack of rigorous experimental design, and difficulties with reproducibility of results.

**Applications areas** where LLMs have shown practical value include:

- Conversational AI (Chatbots)
- Computational Biology
- Computer Programming
- Creative Fields (e.g., writing, art)
- Knowledge-Based Tasks (e.g., information retrieval, summarization)
- Legal Domain
- Medical Domain
- Reasoning Tasks (logic and mathematics)
- Robotics and Embodied Agents
- Social Sciences and Psychology
- Synthetic Data Generation

Overall, the paper emphasizes the need to systematically address the outlined challenges to maximize the beneficial applications of LLM technology.

## Challenges

The challenges associated with Large Language Models (LLMs) are broadly divided into three main categories as previously discussed: **Design Challenges**, **Behavioral Challenges**, and **Scientific Challenges**.

Here is a diagram clearly representing the different challenges within each category:
![Challenges Diagram](https://github.com/user-attachments/assets/b094513b-f802-4899-8f88-61cf29b006e9)


Now, let's dive deeper into each of the individual challenges listed above to gain a better understanding of their implications and complexities.

### **1. Unfathomable Datasets**

Modern large language models are trained on enormous and diverse datasets, which makes comprehensive manual inspection or quality checks impractical. This issue creates several critical problems, including:

- **Duplicate and near-duplicate data**: The presence of similar or repeated information negatively impacts model training and overall performance.
- **Benchmark contamination**: Overlap between training data and test benchmarks can unintentionally inflate evaluation metrics, leading to misleading conclusions about model accuracy.
- **Privacy concerns**: Training data often unintentionally includes personally identifiable information (PII), posing serious privacy risks.
- **Optimal data mixtures**: It becomes challenging to determine the best combination of diverse data sources and domain-specific datasets for effective model training and fine-tuning.

  ![Pre-Training Datasets](https://github.com/user-attachments/assets/cb301c03-e741-40ce-8f9a-765dfb658f36)

### **2. Tokenizer-Reliance**

Tokenizers split text into smaller pieces (tokens) for models to process. Initially, simple methods like splitting words by spaces or punctuation were used. However, to better handle language complexities, modern tokenizers are often trained on large datasets. This trained approach introduces several problems, such as:

- **Language bias**
- **Limited vocabulary for novel words**
- **Loss of linguistic nuance after splitting**
  
![Tokenization variations](https://github.com/user-attachments/assets/66cd85ed-159b-415a-ae5b-2f4025470e4d)


### **3,4 and 5. High Pre-Training, Fine-Tuning, and Inference Costs**

Large language models require extensive resources at multiple stages: initial training (pre-training), adapting them to specific tasks (fine-tuning), and generating outputs (inference). This results in:

- **Significant financial and environmental costs** due to heavy computational requirements.
- **High memory and storage demands** when storing multiple fine-tuned models.
- **Slow inference speeds (latency)** making real-time or resource-constrained applications challenging.
- **Limited accessibility** for researchers or practitioners without powerful computing resources.


![H100 Owners](https://github.com/user-attachments/assets/f3036506-27f6-4248-a944-ac80f9062842)


Source: [this link](https://www.visualcapitalist.com/which-companies-own-the-most-nvidia-h100-gpus/).

### **6. Limited Context Length**

Large language models have restrictions on how much text they can process at once (context length). This limitation makes it challenging to handle tasks requiring longer texts or extended discussions. Specific problems include:

- **Inability to effectively understand lengthy documents or conversations.**
- **Reduced performance on tasks like long document summarization or extended dialogue understanding.**
- **Increased computational costs** when attempting to process longer contexts.

![Screenshot 2025-03-24 at 5 05 47 PM](https://github.com/user-attachments/assets/e893d252-a985-4b59-abe2-63a22047613d)


Source: [this link](https://support.netdocuments.com/s/article/Maximum-Length).


### **7, 8 and 9. Prompt Brittleness,Brittle Evaluations  and Lack of Reproducibility**

Large language models are highly sensitive to small changes in the wording or structure of input prompts. Slight variations in prompts can lead to significantly different outputs, causing problems such as:

- **Causes Brittle Evaluations** (Slight modifications of the benchmark prompt or evaluation protocol can give drastically different results.)
- **Lack of Reproducibility** (Not just modified prompts but also same prompts result in different results due to the stochasticity of the models)

![Prompt Brittleness](https://github.com/user-attachments/assets/aef0e684-413f-4b3a-bee2-574ae23fff82)

  
> ### **Question1:** Before moving on to the next challenge, consider this: What do you think is the most significant limitation of deep learning models (including LLMs) compared to human cognition?   
> **Hint:** Think about what humans and LLMs do differently when they encounter something they don't know.
> \
> \
> \
> \
> \
> **Answer:** The core limitation is that deep learning models lack metacognition—they do not know when they don't know. Unlike humans, who can acknowledge uncertainty and seek additional information or guidance, these models will always produce an output even if it's incorrect, because they don't have a proper mechanism to detect or flag uncertainty.

### **10. Hallucinations**

Large language models sometimes generate text that seems plausible but contains incorrect or entirely fabricated information. This issue leads to critical challenges, such as:

- **Reduced trust and reliability** in model-generated content.
- **Potential harm** if used in sensitive applications like medical diagnosis, legal advice, or factual reporting.
- **Increased need for human oversight and verification**.

![Hallucination](https://github.com/user-attachments/assets/34c7c810-eba5-48aa-946b-08f14543b0a2)


### **11. Misaligned Behavior**

Large language models may generate outputs that are biased, inappropriate, or harmful, reflecting problematic content learned from training data. This misalignment causes serious issues such as:

- **Reinforcing harmful stereotypes or biases.**
- **Generating offensive or unsafe responses.**
- **Difficulty in aligning models with ethical standards and human values.**

![Misaligned Behavior](https://github.com/user-attachments/assets/7eb8248d-76ea-4735-a03d-799d4a65f754)

Source: [this link](https://www.cnn.com/2024/10/30/tech/teen-suicide-character-ai-lawsuit/index.html).

### **12. Outdated Knowledge**

Large language models rely on static training datasets, meaning they often contain information that is outdated or incomplete. This limitation causes:

- **Incorrect or obsolete responses**, especially regarding recent events or fast-changing information.
- **Reduced usefulness in real-time or dynamic applications.**
- **Frequent need for retraining or updating models to maintain accuracy.**

![Outdated Knowledge](https://github.com/user-attachments/assets/a69d8711-6b12-48c1-aea8-7e4e9036c1fc)



> ### **Question:** What are some of the approaches currently used to supress the issue of outdated knowledge in large language models without having to retrain or fine tune the models?
> \
> \
> \
> \
> \
> **Answer:** Modern implementations often use retrieval-augmented generation (RAG) techniques, where a language model is combined with a real-time retrieval system to fetch current data. Additionally, integrating direct web search capabilities helps models access up-to-date information, reducing reliance on static training data.

### **13. Evaluations Based on Static, Human-Written Ground Truth**

Evaluations often depend on human annotations, which can be costly, biased, or may not always accurately reflect reality.

![Approximate Human Annotations Cost](https://github.com/user-attachments/assets/db54534b-b471-45a3-861f-47be6b84d611)


Source: [this link](https://aidatalabelers.com/how-much-do-ai-data-annotation-services-cost-in-2025-the-complete-guide/).

### **14. Indistinguishability between Generated and Human-Written Text**

It’s increasingly challenging to differentiate AI-generated text from human-written content, causing verification issues.

![AI Written - 1](https://github.com/user-attachments/assets/eb18396e-3551-4f0f-82de-c93bf70d2eaf)

![AI Written - 2](https://github.com/user-attachments/assets/9d8def8e-a907-48ab-808e-ebd9dee2a41f)


### **15. Tasks Not Solvable By Scale**

Simply increasing model size or data isn't sufficient to address certain new or complex problems if information about the problems or related problems is missing in the training data.

### **16. Lacking Experimental Designs**

Papers presenting novel LLMs often lack controlled experiments, likely due to the prohibitive costs of training enough models.

