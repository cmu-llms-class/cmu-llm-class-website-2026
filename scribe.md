---
layout: page
title: Scribe Materials
permalink: /scribe/
---

Scribe notes provide an archive of material covered in advanced technical courses. Each lecture, a designated 1-3 students will take comprehensive notes that capture not just what was said, but also synthesizes the material into a polished document for the entire class. This practice benefits the scribe through deep engagement with the material and simultaneously creates a resource that extends beyond the semester for future students. Unlike personal notes, scribe notes are expected to be technically accurate, comprehensive, and enhanced with additional context: scribes add relevant recent papers, provide worked examples that weren't fully developed in lecture, explain conceptual foundations, and analyze failure modes or edge cases.  Scribe notes also serve as practical references containing tested prompt templates, implementation patterns, and evaluation frameworks that you can directly reference in your projects this semester or beyond.

# Template
You must submit your notes in the template linked [here](https://storage.googleapis.com/cmu-llms/2025/11_766_Scribe_Notes_Template.zip).

# Due Date and Submission
Scribe notes will be due exactly a week after the lecture (e.g. if you are responsible for the January 15 lecture, your notes are due by 11:59 PM on January 22).
The late policy described in the syllabus applies.

Scribe notes should be submitted via Canvas.
Please submit both a pdf file and a .zip or link to your source latex.

# Grading

Scribe notes will be evaluated according to the following criteria, each worth 20 points,
- Correctness
- Coverage
- References
- Depth
- Presentation

## **1\. Correctness (20 points)**

**Definition:** The extent to which the notes accurately represent the technical content about LLM architectures, prompting techniques, evaluation methods, application design patterns, and system implementations without errors in formulas, pseudocode, or conceptual understanding.

### **Grading Scale:**

* **18-20 points (Excellent):** All technical content is accurate with no errors in algorithmic mechanics, prompt engineering, evaluation metrics, or system design patterns  
* **15-17 points (Good):** Minor errors that don't affect overall understanding (e.g., typo in hyperparameter description, small formatting inconsistency in prompt template)  
* **12-14 points (Satisfactory):** A few notable errors that could confuse readers, but core concepts remain sound  
* **8-11 points (Poor):** Multiple significant errors or one critical error that undermines key concepts  
* **0-7 points (Unacceptable):** Pervasive errors throughout; notes are unreliable

### **Good Examples:**

* Accurately representing attention mechanism formulas.  
* Precise prompt templates that match what was demonstrated, including system/user message structure  
* Accurate representation of RAG pipeline steps: retrieval ‚Üí ranking ‚Üí context injection ‚Üí generation  
* Correct evaluation metrics definitions (BLEU, ROUGE, perplexity, human eval rubrics)  
* Proper documentation of few-shot example formats and ordering effects

### **Bad Examples:**

* Confusing encoder-only (BERT) vs decoder-only (GPT) vs encoder-decoder (T5) architectures  
* Stating that higher temperature always produces better results (omitting the diversity/coherence tradeoff)  
* Misrepresenting chain-of-thought as requiring fine-tuning rather than just prompting  
* Claiming ROUGE measures semantic similarity when it measures n-gram overlap  
* Stating that all LLMs have 2048 token context windows when modern models vary widely  
* Confusing hallucination (generating false content) with bias (systematic skew)

---

## **2\. Coverage (20 points)**

**Definition:** The extent to which the notes comprehensively capture all topics including LLM techniques discussed, prompting strategies, evaluation approaches, system design patterns, failure modes, and practical considerations from the lecture.

### **Grading Scale:**

* **18-20 points (Excellent):** All major topics covered; includes prompting techniques, evaluation methods, and failure cases; captures important practical tips and design tradeoffs  
* **15-17 points (Good):** All major topics covered but missing some examples or brief discussions; no significant omissions  
* **12-14 points (Satisfactory):** Missing one minor topic or several examples; overall arc of lecture is preserved  
* **8-11 points (Poor):** Missing multiple topics or one major section; gaps would confuse someone who missed lecture  
* **0-7 points (Unacceptable):** Large sections missing; notes don't represent the full lecture

### **Good Examples:**

* Including all three prompting strategies demonstrated (zero-shot, few-shot, chain-of-thought)  
* Documenting the complete RAG implementation pipeline discussed, from embedding generation to response synthesis  
* Covering both the successful case and the failure modes shown for the agent system  
* Including the comparison table of different embedding models (OpenAI, Cohere, open-source)  
* Capturing the cost-performance tradeoff analysis between GPT-4 and GPT-3.5  
* Recording the debugging strategies discussed for prompt engineering  
* Documenting the specific ethical considerations and bias examples shown

### **Bad Examples:**

* Omitting the entire section on prompt injection vulnerabilities  
* Missing the evaluation framework discussion (only covering model usage)  
* Failing to note the token limit considerations that affect application design  
* Leaving out the comparison between different chunking strategies for RAG  
* Not documenting the failure case examples that illustrated hallucination

---

## **3\. References (20 points)**

**Definition:** The extent to which the notes provide comprehensive references beyond those mentioned in lecture, including recent LLM papers (2023-2025), foundational transformer/prompting papers, technical blog posts from LLM providers, and relevant work from adjacent fields (IR, HCI, NLP evaluation), with contextual discussion.  Each reference should be contextualized by explaining its relevance to lecture content.  Grading will first check for inclusion of references from lecture and, if satisfactory, new references.  References should prioritize published work, although arxiv papers are acceptable if important and unpublished; if a paper is published, you should use its published citation. 

### **Grading Scale:**

* **18-20 points (Excellent):** 5+ high-quality new references spanning recent LLM research, foundational papers, technical documentation, and adjacent fields; good coverage across lecture section  
* **15-17 points (Good):** 3-4 new references; may be weighted toward one category; basic context provided  
* **12-14 points (Satisfactory):** No references beyond lecture  
* **8-11 points (Poor):** missing 1-2 references from lecture  
* **0-7 points (Unacceptable):** No references at all, or references listed without any context

### **Good Examples:**

* **Recent work (2024-2025):** "The Anthropic Constitutional AI paper (Bai et al., 2024\) \[15\] extends the RLHF approach discussed in lecture by adding a second phase where the model critiques its own outputs, reducing the need for human feedback in alignment."  
* **Recent techniques:** "Google's Gemini 1.5 technical report (2024) \[18\] demonstrates the 1M token context window mentioned in lecture, with detailed analysis of how attention patterns change at extreme lengths."  
* **Foundational:** "The original Transformer architecture (Vaswani et al., 2017\) \[3\] introduced the self-attention mechanism we discussed, though modern LLMs like GPT use only the decoder stack."  
* **Adjacent fields \- IR:** "The dense retrieval survey (Zhu et al., 2023\) \[12\] provides comprehensive background on the embedding-based retrieval we use in our RAG pipeline."  
* **Adjacent fields \- HCI:** "The human-AI collaboration framework from Chang et al. (2023) \[9\] offers design patterns relevant to our discussion of chatbot UX."  
* **Evaluation:** "The BIG-bench benchmark suite (Srivastava et al., 2023\) \[7\] includes many of the capability evaluation tasks mentioned, with detailed measurement protocols."

### **Bad Examples:**

* Only citing the attention paper without any LLM-specific references  
* Listing "GPT-4 technical report" without explaining what aspects relate to lecture topics  
* Including papers about traditional NLP without connecting them to LLM applications  
* Citations without explaining whether they introduce a technique, evaluate it, or apply it  
* "See \[1-10\] for more on prompt engineering" without discussing what each contributes  
* Including theoretical papers on transformers without application-relevant content

---

## **4\. Depth (20 points)**

**Definition:** The extent to which the notes expand upon the lecture content through additional prompt examples, deeper explanations of why techniques work, or connections between design patterns.

### **Grading Scale:**

* **18-20 points (Excellent):** Substantial added value through multiple examples, prompt variations with outputs, failure case analysis, or design tradeoff discussions; significantly enriches understanding beyond lecture  
* **15-17 points (Good):** Meaningful additions such as 1-2 complete implementations or deeper analysis of key techniques  
* **12-14 points (Satisfactory):** Some additional content (e.g., one worked example or brief analysis)  
* **8-11 points (Poor):** Minimal additions; notes are essentially a transcript  
* **0-7 points (Unacceptable):** No depth added; possibly even less detail than lecture provided

### **Good Examples:**

* **Extended prompt examples:** Providing 3-5 variations of a prompt template with actual model outputs showing how different phrasings affect results  
* **Failure analysis:** "When we tested this prompt on GPT-3.5, it failed 30% of the time by misinterpreting X as Y. Adding the constraint 'Always format as JSON' reduced failures to 5%."  
* **Comparative evaluation:** Running the same task through GPT-4, Claude, and Llama with cost/quality analysis  
* **Conceptual depth:** Explaining *why* chain-of-thought works by connecting to System 1/System 2 thinking or working memory constraints  
* **Design patterns:** Connecting today's agent pattern to the ReAct framework from lecture 5, showing how they compose  
* **Token analysis:** Breaking down the actual token count for example prompts and showing how it affects costs  
* **Prompt engineering iteration:** Showing the evolution of a prompt through 4-5 versions with explanation of what each change improved

### **Bad Examples:**

* Simply restating the prompt template shown in lecture without variations  
* Adding a "related work" section that doesn't deepen understanding of the specific techniques  
* Including an example so brief it doesn't demonstrate the technique's nuances  
* Providing "depth" through verbose rewording rather than additional insight  
* Adding tangential information about transformer architecture that doesn't help with applications  
* Showing prompt outputs without analysis of what made them succeed or fail

---

## **5\. Presentation (20 points)**

**Definition:** The extent to which the notes are clearly written, well-organized for an LLM applications audience, and readable both at the sentence level (technical writing clarity) and structural level (logical flow through techniques, prompt formatting).

### **Grading Scale:**

* **9-10 points (Excellent):** Professional technical writing; clear organization with logical progression through concepts; minimal errors; reader can implement techniques from notes  
* **7-8 points (Good):** Clear and well-organized with minor issues; a few awkward explanations or formatting choices  
* **5-6 points (Satisfactory):** Readable but has organizational problems or numerous clarity issues  
* **3-4 points (Poor):** Difficult to follow due to poor organization, unclear explanations, or poorly formatted examples  
* **0-2 points (Unacceptable):** Incomprehensible organization; pervasive writing/formatting problems

### **Good Examples:**

* **Structure:** Clear sections like "Technique Overview," "Prompt Design," "Implementation," "Evaluation," "Failure Modes," "Practical Considerations"  
* **Transitions:** "Having established the basic RAG pipeline, we now examine how to optimize retrieval quality through hybrid search..."  
* **Visual hierarchy:** Using headers, blockquotes for prompts, tables for comparisons  
* **Concrete examples:** "For instance, when asked 'What is 2+2?', the model with temperature=0 always responds '4', while temperature=1.5 might produce '4', 'four', or 'two plus two equals four'."

### **Bad Examples:**

* Run-on technical explanations: "The retrieval augmented generation pipeline works by first taking the query and embedding it using a model like text-embedding-ada-002 which produces a 1536 dimensional vector and then..."  
* No visual distinction between different prompting techniques being compared  
* "The thing about temperature is it does stuff to randomness" (imprecise)  
* Tables without headers or unclear column meanings  
* Screenshots of code instead of formatted text  
* Using "it" repeatedly without clear antecedents: "It generates it by sending it to the model"