<h1>AI-Blog-Generation-Using-LLM</h1>

<h2>Importing Libraries</h2>
The code starts by importing the necessary libraries:

- **streamlit (imported as st)**: a Python library for building web applications for machine learning and data science.
- **langchain.prompts and langchain.llms**: libraries for working with large language models (LLMs) and generating text prompts.

<h2>Defining the 'getLLamaresponse' Function</h2>
The getLLamaresponse function takes three inputs:

- **input_text**: the topic of the blog post
- **no_words**: the desired word count of the blog post
- **blog_style**: the target audience for the blog post (Researchers, Data Scientist, or Common People)

The function does the following:

Loading the LLama 2 Model: It loads the LLama 2 model, a large language model that can generate human-like text. The model is configured with specific settings, such as the maximum number of new tokens to generate (256) and the temperature (0.01).

Defining the Prompt Template: It defines a prompt template that will be used to generate the blog post. The template includes placeholders for the blog_style, input_text, and no_words inputs.

- **Formatting the Prompt**: It formats the prompt by replacing the placeholders with the actual input values.
- **Generating the Response**: It uses the LLama 2 model to generate a response based on the formatted prompt.
- **Returning the Response**: It returns the generated response as a string.

<h2>Building the Streamlit Application</h2>
The code then builds a Streamlit application with the following components:

- **Header**: A header that displays the title "Generate Blogs" with a robot icon.
- **Input Fields**: Three input fields:
A text input field for the user to enter the blog topic.
Two columns with text input fields for the number of words and a selectbox for the blog style (Researchers, Data Scientist, or Common People).
- **Generate Button**: A button that triggers the generation of the blog post when clicked.
Response Display: A section that displays the generated blog post when the "Generate" button is clicked.

<h2>Generating the Blog Post</h2>
When the user clicks the "Generate" button, the getLLamaresponse function is called with the input values, and the generated blog post is displayed on the Streamlit application.
