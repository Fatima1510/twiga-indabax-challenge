# 🚀 Twiga AI Challenge: Document Processing & RAG System

## 🎯 Overview

This repository contains two interconnected challenges for building a complete document processing and RAG (Retrieval-Augmented Generation) system for academic research papers.

## 📝 What You'll Build

This project is split into two main challenges:

- **Document Parsing**: Convert academic PDFs into clean, structured markdown, preserving academic sections, citations, and logical hierarchy. This prepares your data for downstream AI tasks.
- **RAG System**: Build a Retrieval-Augmented Generation (RAG) pipeline that uses your parsed documents to answer academic questions with accurate, cited responses.

## 📁 Project Structure

```
twiga-challenge-1/
├── README.md                    # This file - Main overview
├── parsing-challenge/           # Challenge 1: Document Parsing
│   ├── README.md                # Parsing challenge documentation
│   └── strategy1_llamaparse_direct.ipynb
├── rag-challenge/               # Challenge 2: RAG Implementation
│   ├── README.md                # RAG challenge documentation
│   └── strategy1_chromadb_basic.ipynb     RAG
├── data/
│   ├── papers/                  # Original PDF files
│   ├── input_papers/            # Parsed markdown files
│   └── vector_store/            # Vector database storage
└── LICENSE
```

## 🏆 Challenge Progression

### Phase 1: Document Parsing

- **Notebook**: `parsing-challenge/strategy1_llamaparse_direct.ipynb`
- **Goal**: Parse academic PDFs into structured markdown for RAG.

### Phase 2: RAG System

- **Notebook**: `rag-challenge/strategy1_chromadb_basic.ipynb`
- **Goal**: Build a RAG pipeline for question answering over your parsed documents.

## 🛠️ Setup & Installation

### Prerequisites

```bash
# Core dependencies
pip3 install llama_parse pypdf together pydantic

# RAG dependencies
pip3 install chromadb sentence-transformers langchain openai
pip3 install faiss-cpu numpy pandas matplotlib
```

### API Keys Required

Create a `.env` file in the project root based on `.env.example`:

## 🎮 Getting Started

### Phase 1: Document Parsing (Required First)

1. Navigate to `parsing-challenge/`
2. Open `strategy1_llamaparse_direct.ipynb`
3. Set up API keys and dependencies
4. Parse your research paper(s)
5. Validate output quality

### Phase 2: RAG System (After Phase 1)

1. Navigate to `rag-challenge/`
2. Open `strategy1_chromadb_basic.ipynb`
3. Set up API keys and dependencies
4. Use parsed markdown from Phase 1
5. Test with academic questions

## 📊 Available Research Papers

- **Mobile-Based_Deep_Learning_Models_for_Banana_Disease.pdf** - Deep learning for banana disease detection
- **Examining_the_Awareness_of_Mobile_Money_Users_on_S.pdf** - Mobile money user awareness study
- **Practical Machine Learning_25_05_04_14_32_34.pdf** - Practical machine learning applications

Both papers contain rich academic content including:

- Complex figures and tables
- Mathematical equations
- Extensive citations and references
- Multi-level section hierarchies

## 🏅 Evaluation Criteria

### Parsing Challenge (Phase 1)

- **Content Accuracy** (25%) - Text extraction quality
- **Structure Preservation** (25%) - Academic section identification
- **Figure/Table Detection** (20%) - Visual element handling
- **Citation Handling** (15%) - Reference preservation
- **Chunk Quality** (15%) - Logical segmentation

### RAG Challenge (Phase 2)

- **Retrieval Accuracy** (30%) - Relevant chunk identification
- **Answer Quality** (25%) - Generated response accuracy
- **Context Preservation** (20%) - Academic context maintenance
- **System Performance** (15%) - Query response time
- **User Experience** (10%) - Interface and usability

## 🚦 Success Metrics

### Phase 1 Completion Criteria:

✅ Successfully parse all research papers  
✅ Generate clean, structured markdown output  
✅ Preserve academic formatting and citations  
✅ Create logical, RAG-ready text chunks

### Phase 2 Completion Criteria:

✅ Build functional vector database from parsed content  
✅ Implement semantic search capabilities  
✅ Generate accurate, contextual answers  
✅ Handle complex academic queries effectively

## 💡 Tips for Success

### For Parsing Challenge:

- Focus on academic structure preservation
- Test different prompt engineering approaches
- Validate output against source PDFs
- Optimize for downstream RAG usage

### For RAG Challenge:

- Experiment with chunk size and overlap
- Try different embedding models
- Implement query expansion techniques
- Focus on citation preservation in responses

## 🎯 Next Steps

1. **Start with Phase 1**: Open the parsing notebook and process your PDFs
2. **Move to Phase 2**: Open the RAG notebook and build your Q&A system
3. **Test end-to-end** with academic questions

## 📞 Support

- Check individual challenge READMEs for detailed instructions
- Review baseline implementations before optimizing
- Test incrementally and document your findings
- Focus on one challenge at a time for best results

Ready to build the future of academic document processing? Let's go! 🚀
