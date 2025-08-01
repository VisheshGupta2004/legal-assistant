# AI-Powered Legal Assistant for Indian Law

![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
[![GitHub stars](https://img.shields.io/github/stars/yourusername/legal-assistant?style=social)](https://github.com/VisheshGupta2004/legal-assistant)

An intelligent legal assistant that provides accurate and reliable information based on Indian legal documents using state-of-the-art natural language processing.

## 🌟 Features

- **AI-Powered Legal Queries**: Get precise answers to legal questions based on Indian legal documents
- **Document Analysis**: Process and analyze legal PDFs with ease
- **Context-Aware Responses**: Responses include relevant legal provisions, section numbers, and citations
- **User-Friendly Web Interface**: Simple and intuitive chat interface
- **Privacy Focused**: Runs locally on your machine after initial setup

## 🚀 Quick Start

### Prerequisites
- Python 3.8 or higher
- Pinecone account and API key
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/legal-assistant.git
   cd legal-assistant
   ```

2. **Set up virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment**
   ```bash
   cp .env.example .env
   # Edit .env with your Pinecone API key
   ```

5. **Add legal documents**
   - Place your PDF files in the `data/` directory
   - Process documents:
     ```bash
     python store_index.py
     ```

6. **Run the application**
   ```bash
   python app.py
   ```
   Open http://localhost:8080 in your browser

## 🛠️ Project Structure

```
legal-assistant/
├── data/                  # Legal PDFs storage
├── model/                 # LLM model files
├── src/                   # Source code
│   ├── helper.py          # Document processing utilities
│   └── prompt.py          # AI prompt templates
├── static/                # Static assets
├── templates/             # Web interface
├── .env                   # Configuration
├── app.py                 # Main application
└── requirements.txt        # Dependencies
```

## 🤖 How It Works

1. **Document Processing**:
   - Legal PDFs are loaded and split into manageable chunks
   - Text chunks are converted to vector embeddings using HuggingFace's sentence-transformers

2. **Vector Storage**:
   - Vectors are stored in Pinecone for efficient similarity search
   - Enables quick retrieval of relevant legal information

3. **Query Processing**:
   - User questions are converted to vectors
   - System finds the most relevant document chunks
   - LLaMA-2 generates accurate, context-aware responses

## 📚 Example Queries

- "What are the penalties for cybercrime under IT Act 2000?"
- "Explain the process of filing an RTI application in India."
- "What are the legal rights of tenants in India?"

## ⚠️ Important Disclaimer

This application is for informational purposes only and does not constitute legal advice. The responses are generated based on available legal documents and may not be fully accurate or up-to-date. Always consult with a qualified legal professional for specific legal advice.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

Distributed under the MIT License. See `LICENSE` for more information.

## 🙏 Acknowledgments

- [LangChain](https://python.langchain.com/) - LLM framework
- [HuggingFace](https://huggingface.co/) - Sentence transformers
- [Pinecone](https://www.pinecone.io/) - Vector database
- [LLaMA-2](https://ai.meta.com/llama/) - Language model
