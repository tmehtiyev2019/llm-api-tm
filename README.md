# LLM-API-TM

## Overview
`llm-api-tm` is an experimental project designed to explore and evaluate the capabilities of Large Language Models (LLMs) in dynamically generating API calls from freeform text inputs. The initiative aims to bridge the gap between natural language processing and API interaction, making it more accessible for users without technical backgrounds in programming or API usage.

## Objectives
- To study the feasibility and effectiveness of using LLMs for interpreting freeform text and translating it into structured API calls.
- To conduct a comparative analysis of multiple LLMs, assessing their performance in the context of API function calling.
- To develop standardized testing and evaluation criteria for comparing different LLMs.
- To investigate the impact of various prompt structures on the performance of LLMs in this specific application.

## Approach
- **LLM Selection and Integration:** Identify and select a range of LLMs for experimentation, including OpenAI's models.
- **Function Calling Schema Development:** Define function calling schemas that the LLMs can use to structure their responses, mimicking the process of API calls.
- **Comparative Analysis Methodology:** Outline the methodology for a comparative analysis of the selected LLMs.
- **Testing and Evaluation Framework:** Develop a framework for standardized testing and evaluation of LLMs.
- **Prompt Structure Experiments:** Design experiments to test the effectiveness of different prompt structures across various LLMs.
## Standardizing Testing and Evaluation Criteria

### Testing Standardization

To ensure a fair and comprehensive comparison of different Large Language Models (LLMs), we follow a standardized testing process:

### GPT-3
- **Description:** GPT-3 is a well-established model known for its wide-ranging language processing capabilities. It is suitable for various applications including text generation, translation, and more.
- **API Integration:** Accessible via OpenAI's API, providing a user-friendly platform for integration.
- **Notable Capabilities:** Impressive linguistic abilities, suitable for a broad spectrum of text-based tasks.

### GPT-4
- **Description:** The latest iteration in the GPT series, offering enhanced performance in understanding and generating text.
- **API Integration:** Similar to GPT-3, GPT-4 is available through OpenAI's API, facilitating ease of use and integration.
- **Notable Capabilities:** Improved accuracy, context comprehension, and detailed response generation compared to its predecessor.

Both models will be evaluated for their effectiveness in interpreting free-form text and generating structured API calls.

#### Test Case Development
- **Diverse Scenarios:** We design a set of standardized test cases that cover a wide range of input scenarios to comprehensively evaluate the LLMs' capabilities.
- **Consistency:** All test cases are crafted to ensure diversity in complexity, length, and subject matter.

#### Testing Environment
- **Uniform Environment:** Tests are conducted in a consistent environment — same hardware, software versions, and network conditions.
- **Consistent LLM Utilization:** Each LLM is accessed and used in a similar manner to ensure uniformity in testing.

#### Automated Testing
- **Framework Utilization:** We use an automated testing framework to execute the test cases, ensuring consistent execution and minimizing manual errors.
- **Metric Recording:** Key metrics like response times and accuracy are recorded systematically.

#### Data Collection
- **Structured Format:** Outputs from each LLM are collected and stored in a structured format for subsequent analysis.

### Evaluation Criteria Standardization

To assess the performance of each LLM, we establish standardized evaluation criteria:

#### Performance Metrics
- **Accuracy:** The precision in translating natural language inputs to the correct API calls.
- **Response Time:** The duration taken by each LLM to process an input and return a response.
- **Robustness:** The ability of the LLM to handle ambiguous or complex queries effectively.
- **Consistency:** The uniformity in performance across various input types.

#### Evaluation Methods
- **Manual Review:** Expert review is used where automated evaluation is not feasible.
- **Statistical Analysis:** Statistical techniques are employed to analyze collected data.
- **Error Analysis:** Types of errors made by each LLM are categorized and examined.

#### Benchmarking
- **Performance Benchmarks:** We establish benchmarks for each metric to classify LLM performance.

#### Feedback Loop
- **Continuous Improvement:** The test cases and evaluation criteria are regularly updated based on new insights and advancements.

### Documentation and Reporting

- **Transparent Documentation:** The methodologies for testing and evaluation are thoroughly documented for clarity and reproducibility.
- **Regular Reporting:** Findings are reported regularly, including both qualitative and quantitative analyses.

This structured approach to testing and evaluation ensures an objective and detailed comparison of the LLMs, providing valuable insights into their suitability for various applications.

### Large Language Models Used

In this project, we are focusing on two of OpenAI's Large Language Models: GPT-3 and GPT-4. Below is a brief overview of each:


