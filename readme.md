### Chatbot for Multiple PDF files

Chatbot for Multiple PDF files is a Python program designed for interacting with multiple PDF documents. Through natural language queries, users can inquire about the PDFs and receive accurate responses based on their content. The app utilizes a language model to generate these answers. It's important to note that the app will only respond to questions pertaining to the loaded PDFs.

There are two options here to use LLM:

1. Use API of OpenAI's GPT-3.5 LLM model (Use python code "Multi_PDF_ChatBot_GPT3.5.py")
OR
2. Use API Falcon 7B model on huggingace Face Hub (Use python code "Multi_PDF_ChatBot_Falcon7B.py")

Similarly there are two options to create embedding as well. (Embeddings of Hugging Face might take huge amount of time for generation. Better to go for Open AI embeddings. We can still use Falcon 7B with OpenAI embeddings)

### How It Works
------------

The ChatBot  follows a series of steps to provide responses to the questions:

1. PDF Inputs: The app reads and extracts the text content from multiple PDF documents.

2. Chunking of text input: The extracted text is divided into smaller, manageable sections for efficient processing.

3. LLM: The app employs a language model to generate vector representations (embeddings) of the text chunks.

4. Similarity Matching: When you ask a question, the app compares it with the text chunks and identifies the most semantically similar ones.

5. Response Generation: The selected text chunks are passed to the language model, which uses the relevant content from the PDFs to generate an appropriate response.

### Installation
----------------------------
To install the MultiPDF Chat App, please follow these steps:

1. Clone the repository to your local machine.

2. Install the required dependencies by running the following command:
   ```
   pip install -r requirements.txt
   ```

3. Obtain an API key from OpenAI and add it to the `.env` file in the project directory.

### Usage
-----
To use the MultiPDF Chat App, follow these steps:

1. Intall requirement.txt and add your OpenAI API key or HugginFace Key (whichever LLM you chose) to the `.env` file.

2. Run following:
   ```
   streamlit run app.py
   ```

3. The application will launch in your default web browser, displaying UI

4. Load multiple PDF documents into the app by following the provided instructions.

5. Ask questions in natural language about the loaded PDFs using the chat interface.

