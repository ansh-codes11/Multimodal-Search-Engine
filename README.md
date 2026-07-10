# Lens Pro Max

Lens Pro Max is an advanced image analysis and web search tool that combines computer vision and natural language processing to generate accurate web queries based on user input and image content.

## Features

- Multi-modal image and text processing
- Accurate web query generation
- Integration with Yahoo Search for web results

## Technologies Used

- Python
- PyTorch
- Transformers library (Hugging Face)
- Qwen2VL model for image-text processing
- Llama 3.2 3B Instruct model for query generation
- Anvil for web application interface
- Yahoo Search API for web results

## Installation and Usage

1. **Open the Notebook**
   - Access Google Colab and open the file named `Lens_pro_max_finalproj.ipynb`.

2. **Configure GPU**
   - In Colab, navigate to Runtime > Change runtime type.
   - Set the Hardware accelerator to T4 GPU to enable GPU support.

3. **Generate Access Token for Llama-3.2-3B-Instruct Model**
   - Log in to your Hugging Face account.
   - Search for Llama-3.2-3B-Instruct in the model hub.
   - Input your contact information on the model page to request access and generate an access token.

4. **Update the Notebook**
   - In the fifth code block of the Colab notebook, locate the `access_token` variable.
   - Replace the placeholder value with the access token you generated from Hugging Face.

5. **Execute the Notebook**
   - Run all the code blocks in the notebook sequentially.
   - Note that the last code block will remain running continuously and will not terminate automatically.

6. **Access the Application**
   - Open the following link: https://anchored-harmless-swan.anvil.app/
   - On the app interface, input text and images as required and click Submit to process the data.

## How It Works

1. **Image and Query Processing**: 
   - The user uploads an image and enters a query through the Anvil web interface.
   - The image is preprocessed and, along with the query, fed into the Qwen2VL-2B-Instruct model to generate a descriptive caption.

2. **Web Query Generation**:
   - The user query and generated caption are passed to the Llama-3.2-3B-Instruct model to produce an accurate web query.

3. **Web Search**:
   - The generated web query is used to perform a search using the Yahoo Search API.

4. **Result Display**:
   - The web query and search results are returned to the user interface for display.

## Limitations and Future Work

- The current setup is optimized for T4 GPUs. More powerful GPUs could enable the use of larger, more accurate models.
- Future iterations could explore alternative multi-modal models or fine-tuning existing models for improved performance, and eliminating the need for two Models.
- The Anvil server setup might need to be replaced with a different web framework for production use.