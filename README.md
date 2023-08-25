# Electronic Store Customer Service Assistance with OpenAI CHATGPT

## Introduction
This Jupyter Notebook showcases an implementation of an automated customer service assistant for an electronic store. The assistant is designed to address customer queries regarding products using OpenAI's CHATGPT. Through a series of modularized instructions, the code demonstrates how to extract product or category information from user queries, fetch relevant product details, and provide structured and friendly responses to users.

## Requirements

### Prerequisites
1. **Python Environment**: Ensure you have a Python 3.x environment.
2. **Python Libraries**: Ensure you have the following libraries installed in your system:
   - `os`
   - `openai`
   - `dotenv`
   - `json`
3. **OpenAI API Key**: You'll need an API key from OpenAI to interact with the service. Store it securely in an `.env` file or another secure location and make sure it's accessible to the notebook

## Code Explanation
### Setup and Initialization
- **Library Imports:** Essential Python libraries are imported.
- **Environment Variable Loading:** The OpenAI API key is loaded from the local .env file using `dotenv`.

### Function Definitions

- `get_completion_from_messages():` Sends a series of messages to the OpenAI model to retrieve a response.
- `get_product_by_name():` Fetches product details by product name.
- `get_products_by_category():` Fetches all products within a specified category.
- `read_string_to_list():` Converts a string representation of a list to an actual Python list.
- `generate_output_string():` Processes the list of products or categories extracted from user queries to generate a structured response string.

### Chain of Reasoning Implementation
- **Category and Product Recognition:** The code provides detailed instructions to the model to extract product or category information from user queries.
- **User Queries:** Example user queries are demonstrated, such as inquiries about specific products and categories. For each query, the model identifies the products or categories and fetches their details.

### User-Friendly Response Generation
After extracting product details based on user queries, the model is instructed to generate a friendly and concise response while also prompting the user with relevant follow-up questions.

## Usage Tips
- The `system_message` is pivotal in guiding the model's behavior. It provides context, ensuring the model understands its role as a customer service assistant.
- The `delimiter` is used for structuring queries to the model. Ensure that user queries and system messages follow the specified delimiter pattern.
- The notebook contains a comprehensive database of electronic products, offering flexibility to handle various user queries. Adjustments can be made to this database to fit different retail scenarios.
