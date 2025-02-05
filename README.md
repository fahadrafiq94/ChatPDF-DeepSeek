
# ChatPDF with DeepSeek R1

This project allows users to upload a PDF document, extract its content, and interact with it using the **DeepSeek R1 1.5b model** via a chatbot interface built with Streamlit.

---

## 🚀 Features
- Upload and analyze PDF documents.
- Extract text from PDF using `pdfplumber`.
- Split document text into manageable chunks.
- Use DeepSeek R1 model for chat-based document interaction.

---

## 🛠️ Prerequisites

Before running this project, ensure that you have the following installed:

1. **Python 3.8+**
2. **Ollama** for accessing the DeepSeek R1 1.5b model.

---

## 📦 Setup Instructions

### 1. Clone the Repository

Clone the repository to your local machine:

```bash
git clone https://github.com/fahadrafiq94/ChatPDF-DeepSeek.git
cd ChatPDF-DeepSeek
```

### 2. Create a Virtual Environment

Create a virtual environment to isolate the dependencies:

```bash
python3 -m venv venv
```

Activate the virtual environment:

- **On Windows:**

  ```bash
  .\venv\Scripts\activate
  ```

- **On macOS/Linux:**

  ```bash
  source venv/bin/activate
  ```

### 3. Install Dependencies

Install the required packages from `requirements.txt`:

```bash
pip install -r requirements.txt
```

The `requirements.txt` file contains the following dependencies:

```txt
streamlit
langchain
pdfplumber
langchain-community
langchain-text-splitters
ollama
```

### 4. Install Ollama

Ollama is used to access the **DeepSeek R1 1.5b model**. Follow these steps to install Ollama:

- **On macOS:**

  1. Download the [Ollama CLI](https://ollama.com/download).
  2. Install the app.

- **On Windows:**

  1. Download the [Ollama Installer](https://ollama.com/download) for Windows.
  2. Follow the installation instructions.

After installing, verify that Ollama is installed successfully by running:

```bash
ollama --version
```

### 5. Install the DeepSeek R1 1.5b Model

To install the DeepSeek R1 1.5b model, run the following command:

```bash
ollama pull deepseek-r1:1.5b
```

This will download and install the `deepseek-r1:1.5b` model, which is required for the chat functionality in this project.

---

## 📝 Running the Application

1. **Start the Streamlit app**:

```bash
streamlit run app.py
```

2. **Upload your PDF document**:

   - After launching the app, upload your PDF document via the file upload button.
   - Ask any questions related to the document, and the system will provide answers based on the content of the PDF.

---

## 📂 Directory Structure

- `rag_deep_app.py`: Main Streamlit application file.
- `requirements.txt`: List of required dependencies.
- `document_store/PDFs`: Folder where uploaded PDFs are stored.
- `README.md`: This file.

---

## 🛠️ Troubleshooting

- **Model Not Found**: If you encounter issues with loading the DeepSeek model, ensure that Ollama is correctly installed and the model is pulled successfully with the command `ollama pull deepseek-r1:1.5b`.
- **PDF Text Extraction Issues**: If the text extraction from PDF is not working as expected, make sure you have the necessary dependencies installed (`pdfplumber`).

---

## 💡 Contributing

Feel free to submit issues and pull requests. Contributions to improve the project are welcome!

---

## 📜 License

This project is licensed under the MIT License.
