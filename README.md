
# A Review of Indic Language LLM Benchmarks: Comparing with Industry-Trusted Benchmarks

This repository contains a literature review on the current state of benchmarks for evaluating Indic Large Language Models (LLMs). It compares existing Indic benchmarks to established industry-trusted benchmarks and suggests potential directions for creating a new, more comprehensive benchmark for Indic LLMs.

## Current Status of Indic LLM Benchmarks

Several benchmarks have emerged to evaluate Indic LLMs, each with its own strengths and limitations:

- **IndicGLUE** (Kakwani et al., 2020): This benchmark includes a variety of tasks like sentiment analysis, natural language inference, and question answering, covering 11 Indic languages. However, the number of tasks and languages covered is still limited compared to industry-trusted benchmarks.
- **IndicXTREME** (Doddapaneni et al., 2023): This benchmark expands upon IndicGLUE by including nine diverse NLU tasks and covering 20 languages. Notably, it focuses on testing the multilingual zero-shot capabilities of pretrained language models, a crucial aspect for low-resource languages.
- **IN22** (Gala et al., 2023): This benchmark focuses on machine translation for all 22 scheduled Indic languages, offering both general-purpose and conversational domain subsets. However, it only assesses translation quality and doesn't cover other NLU tasks.

While these benchmarks represent significant progress, they still have limitations:

- **Limited task and language coverage**: Compared to HellaSwag (57 tasks, 70 languages), MMLU (57 tasks, 100 languages), and ARC (7,787 questions), Indic benchmarks cover fewer tasks and languages. This limits the ability to comprehensively assess the capabilities of Indic LLMs.
- **Data quality and bias**: Some Indic benchmarks rely on automatically translated or generated data, which can introduce noise and bias. Additionally, the data may not be representative of the diversity of language use in the real world.
- **Lack of focus on specific capabilities**: Existing benchmarks often focus on general NLU tasks but may not adequately test specific capabilities like commonsense reasoning, factual consistency, or dialogue coherence.

## Creating a New Indic LLM Benchmark: Filling the Gaps

To create a new benchmark that addresses these limitations and advances Indic LLM evaluation, consider the following:

1. **Expanding Task and Language Coverage**:
    - Include a wider range of NLU tasks, such as commonsense reasoning (e.g., HellaSwag), factual consistency checking, and dialogue coherence evaluation.
    - Cover more languages, including lesser-resourced languages and dialects, to ensure inclusivity and representativeness.
    
2. **Ensuring Data Quality and Reducing Bias**:
    - Use human-annotated data as much as possible, especially for tasks where subtle linguistic nuances are crucial.
    - Employ techniques like adversarial filtering (Zellers et al., 2018) and AFLITE (Sakaguchi et al., 2019) to systematically reduce bias and identify spurious correlations in the data.
    - Collect data from diverse sources to ensure the benchmark reflects real-world language use.
    
3. **Focusing on Specific Capabilities**:
    - Design tasks that specifically test commonsense reasoning, factual consistency, and dialogue coherence, as these are crucial for real-world applications of LLMs.
    - Consider incorporating human evaluation to assess aspects of LLM performance that are difficult to capture with automatic metrics.
    
4. **Addressing Data Contamination**:
    - Be mindful of potential test data contamination and take steps to mitigate it, such as carefully curating the training data and using techniques like data augmentation.
    - Be transparent about the data sources and collection process to facilitate research on contamination detection and prevention.

## Expanding the Scope: Beyond the Basics

Building upon the suggestions above, here are additional considerations for creating a new, state-of-the-art Indic LLM benchmark:

1. **Incorporating Multimodality**:
    - Include tasks that require reasoning over multiple modalities, such as visual question answering, image captioning, and audio-visual speech recognition. This will assess the ability of Indic LLMs to understand and reason about the world in a more holistic way.
    
2. **Evaluating Explainability and Interpretability**:
    - Include tasks that assess the explainability and interpretability of Indic LLMs, such as rationale generation, attention visualization, and counterfactual generation. This will encourage the development of transparent and understandable models.
    
3. **Assessing Robustness and Fairness**:
    - Include tasks that assess the robustness and fairness of Indic LLMs, such as adversarial robustness, bias detection and mitigation, and domain generalization. This will encourage the development of reliable, unbiased, and generalizable models.
    
4. **Continuously Evolving Benchmark**:
    - Design the benchmark to be modular and extensible, allowing for the addition of new tasks and languages over time. This will ensure its long-term relevance and usefulness.

## Conclusion

While Indic LLM benchmarks are making progress, there is still much room for improvement. Addressing the challenges and incorporating the suggestions outlined in this review can lead to the creation of a comprehensive, robust, and informative benchmark that accurately assesses the capabilities of Indic LLMs and drives further progress in the field.

## Citations

- Aggarwal, D., Gupta, V., & Kunchukuttan, A. (2022). IndicXNLI: Evaluating multilingual inference for Indian languages. arXiv preprint arXiv:2204.08776.
- Ahuja, S., Aggarwal, D., Gumma, V., Watts, I., Sathe, A., Ochieng, M., ... & Sitaram, S. (2023). MEGAVERSE: Benchmarking large language models across languages, modalities, models and tasks. arXiv preprint arXiv:2311.07463.
- Clark, P., Cowhey, I., Etzioni, O., Khot, T., Sabharwal, A., Schoenick, C., & Tafjord, O. (2018). Think you have solved question answering? Try ARC, the AI2 reasoning challenge. arXiv preprint arXiv:1803.05457.
- Doddapaneni, S., Aralikatte, R., Ramesh, G., Goyal, S., Khapra, M. M., Kunchukuttan, A., & Kumar, P. (2023). Towards leaving no Indic language behind: Building monolingual corpora, benchmark and models for Indic languages. In Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers) (pp. 12402-12426). https://doi.org/10.18653/v1/2023.acl-long.574
- Gala, J., Chitale, P. A., Raghavan, A. K., Doddapaneni, S., Gumma, V., Kumar, A., ... & Khapra, M. M. (2023). IndicTrans2: Towards high-quality and accessible machine translation models for all 22 scheduled Indian languages
