# LLM-API-TM

## Overview
`llm-api-tm` is an experimental project designed to explore and evaluate the capabilities of Large Language Models (LLMs) in dynamically generating API calls from freeform text inputs. The initiative aims to bridge the gap between natural language processing and API interaction, making it more accessible for users without technical backgrounds in programming or API usage.

## Objectives
- To study the feasibility and effectiveness of using LLMs for interpreting freeform text and translating it into structured API calls.
- To conduct a comparative analysis of multiple LLMs, assessing their performance in the context of API function calling.
- To develop standardized testing and evaluation criteria for comparing different LLMs.

## Approach
- **LLM Selection:** To identify and select a range of LLMs for experimentation, including OpenAI's models.
- **Function Calling Schema Development:** To define function calling schemas that the LLMs, we use to structure their responses, mimicking the process of API calls.
- **Comparative Analysis Methodology:** To outline the methodology for a comparative analysis of the selected LLMs.
- **Testing and Evaluation Framework:** To develop a framework for standardized testing and evaluation of LLMs.

### LLM Selection:
In this project, we have expanded our focus to include three variations of OpenAI's Large Language Models: GPT-3.5-Turbo, GPT-4, and GPT-4-Turbo. Here's an updated overview:

## GPT-3.5-Turbo (gpt-3.5-turbo-1106)
- **Description:** An advanced version of GPT-3, designed for more efficient performance with faster response times.
- **API Integration:** Accessible through the OpenAI API, optimized for quicker and more streamlined interactions.
- **Notable Capabilities:** Enhanced speed and efficiency in processing requests, maintaining the robust language capabilities of GPT-3.

## GPT-4 (gpt-4)
- **Description:** The latest and most sophisticated model in the GPT series, offering superior understanding and text generation abilities.
- **API Integration:** Available via OpenAI's API, it continues the tradition of user-friendly integration with advanced features.
- **Notable Capabilities:** Markedly improved accuracy, deeper context comprehension, and sophisticated response generation, surpassing previous models.

## GPT-4-Turbo (gpt-4-1106-preview)
- **Description:** A turbocharged variant of GPT-4, it combines the advanced capabilities of GPT-4 with the efficiency of turbo models.
- **API Integration:** Integrates seamlessly with existing API setups, providing enhanced speed and performance.
- **Notable Capabilities:** Combines the detailed understanding and output quality of GPT-4 with the rapid response times typical of turbo models.

We will assess their effectiveness in interpreting free-form text and generating structured API calls.


# Function Calling Schema Development

In our project, we have developed a structured JSON schema to facilitate the generation of structured API requests. This schema is specifically designed for creating new products in a catalog system. Below is the detailed description of the schema and its components:

## JSON Schema Overview

- **Title:** APIRequest
- **Description:** Schema for creating a new product in the catalog.
- **Type:** object

## Schema Properties

- **method**
  - **Type:** string
  - **Description:** HTTP method for the API request. 
  - **Allowed Values:** ["POST"]

- **endpoint**
  - **Type:** string
  - **Description:** API endpoint for the request.
  - **Constant Value:** "/products"

- **description**
  - **Type:** string
  - **Description:** Descriptive text about the API request.

- **requestBody**
  - **Type:** object
  - **Description:** Body of the API request containing product details.
  - **Properties:**
    - **name**
      - **Type:** string
      - **Description:** Name of the product.
    - **price**
      - **Type:** number
      - **Description:** Price of the product.
    - **quantity**
      - **Type:** integer
      - **Description:** Quantity of the product in stock.
  - **Required Fields:** name, price, quantity

## Required Fields for Schema

- **method**
- **endpoint**
- **description**
- **requestBody**

This schema is essential for ensuring that the API requests generated are consistent and adhere to the required format for our product catalog microservice. 

## Source of the Schema

The schema is inspired by and adapted from a guided research project by ADA-GWU. For more details and the original schema, please visit the GitHub repository: [ADA-GWU/guidedresearchproject-tmehtiyev2019](https://github.com/ADA-GWU/guidedresearchproject-tmehtiyev2019/tree/main/app/product_catalog_microservice)

---

*Note: The schema is subject to modifications based on project requirements and updates in the API or data structure.*



  
## Standardizing Testing and Evaluation Criteria

### Testing Standardization

#### Overview

The testing involves generating structured API requests from unstructured user inputs using LangChain with three Large Language Models (LLMs) from OpenAI: GPT-3.5-Turbo, GPT-4, and GPT-4-Turbo. Additionally, for generating free-form text prompts, the "text-davinci-003" model is utilized.

#### Key Components

1. **User Input Processing Function (`process_user_input`):**
   - Utilizes "text-davinci-003" model for generating free-form text prompts.
   - Generates a response from the LLM using LangChain with the provided input.

2. **Prompt Template:**
   - Guides the LLMs to generate responses in a structured format.

3. **JSON Schema:**
   - Defines the structure for API request generation.

4. **Structured Output Generation Function (`api_structure_output`):**
   - Structures the LLM response based on the JSON schema.

5. **Testing Loop:**
   - Conducts 100 iterations to test output consistency and accuracy across different LLMs.

## Testing Procedure

1. **Input Generation:**
   - Generate complex product descriptions as user inputs using "text-davinci-003".

2. **LLM Response Generation:**
   - Obtain responses from the LLM using the `process_user_input` function.

3. **Structured API Request Generation:**
   - Generate structured API requests using `api_structure_output` for each LLM model.

4. **Data Collection:**
   - Store LLM responses and structured API results in a DataFrame.

7. **Result Analysis:**
   - Evaluate the structured outputs' accuracy and consistency across models.

## Evaluation Metrics

- **Accuracy:** Alignment of structured outputs with the JSON schema.
- **Consistency:** Uniformity of structured outputs in multiple iterations.
- **Model Performance:** Comparative analysis of LLM models' accuracy and consistency.

## Conclusion

This testing process aims to evaluate the effectiveness of different LLMs in transforming unstructured user inputs into structured API content. The results will inform the selection of the most suitable LLM model for specific project use cases.

---

*Note: The incorporation of the "text-davinci-003" model for free-form text prompt generation is a crucial part of the process, ensuring diverse and complex inputs for testing.*


#### Performance Metrics
- **Accuracy:** The precision in translating natural language inputs to the correct API calls.
- **Consistency:** The uniformity in performance across various input types.

#### Evaluation Methods
- **Manual Review:** Expert review is used where automated evaluation is not feasible.
- **Statistical Analysis:** Statistical techniques are employed to analyze collected data.
- **Error Analysis:** Types of errors made by each LLM are categorized and examined.

### Documentation and Reporting

- **Documentation:** The methodologies for testing and evaluation are thoroughly documented for clarity and reproducibility.
- **Regular Reporting:** Findings are reported regularly, including both qualitative and quantitative analyses.

This structured approach to testing and evaluation ensures an objective and detailed comparison of the LLMs, providing valuable insights into their suitability for various applications.


