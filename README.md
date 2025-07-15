# Research Paper Analysis Tool

A comprehensive AI-powered research paper analysis application that provides intelligent insights, visualizations, and multi-language support for academic documents.

## 🚀 Features

### 📄 Document Processing
- **PDF Upload**: Support for multiple PDF files
- **Text Extraction**: Advanced parsing with PyPDF2 and pdfplumber
- **Smart Chunking**: Intelligent document segmentation for better analysis
- **Vector Search**: FAISS-powered semantic search capabilities

### 🤖 AI-Powered Analysis
- **Document Summarization**: Generate concise, accurate summaries
- **Research Gap Analysis**: Identify limitations and future research opportunities
- **Idea Generation**: Suggest original research directions and questions
- **Debate Simulation**: Create structured academic discussions
- **Citation Generation**: Automatic APA-style citation formatting
- **Interactive Q&A**: Ask specific questions about uploaded papers

### 📊 Data Visualization
- **Automatic Data Extraction**: Find tables and numerical data in PDFs
- **Interactive Charts**: Plotly-powered dynamic visualizations
- **Statistical Analysis**: Extract percentages, measurements, and metrics
- **Visual Insights**: AI-generated analysis of extracted data

### 🌍 Multi-Language Support
- **Translation Services**: Convert analysis results to multiple languages
- **Supported Languages**: Spanish, French, German, Chinese, Urdu, and custom languages
- **Academic Tone Preservation**: Maintains scholarly language in translations

## 🛠️ Installation

### Prerequisites
- Python 3.8 or higher
- Groq API key (free tier available)

### Setup Steps

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd research-paper-analyzer
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables**
   Create a `.env` file in the root directory:
   ```env
   GROQ_API_KEY=your_groq_api_key_here
   ```

4. **Run the application**
   ```bash
   streamlit run streamlit_application/app.py
   ```

5. **Access the application**
   Open your browser to `http://localhost:8501`

## 📋 Requirements

```
streamlit
langchain
langchain-community
langchain-core
langchain-groq
python-dotenv
PyPDF2
pdfplumber
faiss-cpu
huggingface-hub
sentence-transformers
plotly
matplotlib
pandas
numpy
```

## 🔧 Configuration

### API Setup
1. **Get Groq API Key**: Visit [Groq Console](https://console.groq.com/) and create a free account
2. **Add to Environment**: Place your API key in the `.env` file
3. **Model Selection**: Currently uses Llama3-8b-8192 (configurable in `app.py`)

### Customization Options
- **Embedding Model**: Change in `app.py` (default: all-MiniLM-L6-v2)
- **Chunk Size**: Modify in `document_processor.py` (default: 1000 characters)
- **Language Options**: Add more languages in `app.py` translation section

## 🖥️ Usage

### Basic Workflow
1. **Upload PDF(s)**: Click "Upload one or more PDF files" and select your research papers
2. **Process Documents**: Click "Process Documents" to create the vector database
3. **Select Analysis**: Choose from the available analysis options:
   - Summarize document
   - Identify research gaps
   - Suggest research ideas
   - Simulate a debate
   - Generate citation
   - Generate visual insights
   - Chat with paper
4. **Run Analysis**: Click "Run Agent" to generate insights
5. **Optional Translation**: Toggle translation and select your preferred language

### Advanced Features
- **Interactive Q&A**: Use "Chat with paper" to ask specific questions
- **Visual Analysis**: Select "Generate visual insights" to extract and chart data
- **Multi-document Analysis**: Upload multiple papers for comprehensive analysis
- **Export Results**: Copy analysis results for use in your research

## 🏗️ Architecture

### Project Structure
```
streamlit_application/
├── app.py                 # Main Streamlit application
├── document_processor.py  # PDF processing and vector store creation
├── summarizer.py         # Document summarization
├── gap_analyzer.py       # Research gap identification
├── idea_generator.py     # Research idea generation
├── debate_simulator.py   # Academic debate simulation
├── citation_generator.py # Citation formatting
├── chat_handler.py       # Interactive Q&A
├── translator.py         # Multi-language translation
└── visualization.py      # Data extraction and visualization
```

### Technology Stack
- **Frontend**: Streamlit
- **LLM**: Groq API (Llama3-8b-8192)
- **Document Processing**: PyPDF2, pdfplumber
- **Vector Storage**: FAISS
- **Embeddings**: HuggingFace Sentence Transformers
- **Visualization**: Plotly, Matplotlib
- **Framework**: LangChain

## 🤝 Contributing

We welcome contributions! Please feel free to submit issues, feature requests, or pull requests.

### Development Setup
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

### Common Issues
- **API Key Error**: Ensure your Groq API key is correctly set in the `.env` file
- **PDF Processing Issues**: Some PDFs may have complex formatting; try with different files
- **Memory Issues**: Large PDFs may require more system memory

### Getting Help
- Check the [Issues](link-to-issues) page for common problems
- Create a new issue for bugs or feature requests
- Review the documentation for configuration options

## 🚀 Future Enhancements

- [ ] Support for more document formats (Word, PowerPoint)
- [ ] Batch processing capabilities
- [ ] Advanced visualization options
- [ ] Integration with reference managers
- [ ] Export to various formats (PDF, Word, LaTeX)
- [ ] Collaborative features
- [ ] Enhanced multilingual support

## 🏆 Acknowledgments

- Built with [Streamlit](https://streamlit.io/)
- Powered by [Groq](https://groq.com/) API
- Uses [LangChain](https://langchain.com/) framework
- Visualization by [Plotly](https://plotly.com/)

---

**Note**: This tool is designed to assist with research analysis and should not replace critical thinking and proper academic evaluation. Always verify AI-generated insights with original sources.
