# 🏆 Research Paper Parsing Competition

## Overview

This repository contains a Jupyter notebook for optimizing research paper parsing strategies. The goal is to extract structured content from academic research papers using one of three approaches.

## Setup

### Dependencies

```bash
pip3 install llama_parse pypdf together pydantic
```

### API Keys Required

- **LlamaParse API**: For Strategy 1 and 3
- **Together AI API**: For Strategy 2 and 3

## Available Strategies

### Strategy 1: Direct LlamaParse

- **Philosophy**: Use LlamaParse's built-in AI for direct PDF → structured content
- **Strengths**: High accuracy, handles complex layouts well
- **Optimization Areas**: System prompts, result types, post-processing

### Strategy 2: Raw PDF + AI Structuring

- **Philosophy**: Extract raw text with pypdf, then use AI to structure it
- **Strengths**: Full control over extraction and structuring
- **Optimization Areas**: Text extraction, AI prompts, chunking logic

### Strategy 3: Hybrid LlamaParse + AI

- **Philosophy**: Combine LlamaParse parsing with additional AI structuring
- **Strengths**: Best of both worlds - quality parsing + custom structuring
- **Optimization Areas**: Integration logic, dual-stage prompting, output merging

## Competition Rules

1. Choose ONE strategy to optimize
2. Process both available papers successfully:
   - `30YearsResearchGate.pdf`
   - `SchenkBekkerSchmitt2025PrecRes.pdf`
3. Document your optimizations and reasoning
4. Submit working code with performance improvements

## Evaluation Criteria

1. **Content Accuracy** (25%) - Text extraction quality
2. **Structure Preservation** (25%) - Academic section identification
3. **Figure/Table Detection** (20%) - Visual element handling
4. **Citation Handling** (15%) - Reference preservation
5. **Chunk Quality** (15%) - Logical segmentation

## File Structure

```
├── llamaparse_test.ipynb    # Main competition notebook
├── data/
│   ├── papers/             # Input PDF files
│   └── input_papers/       # Processed output files
└── README.md              # This file
```

## Getting Started

1. Open `llamaparse_test.ipynb`
2. Set up your API keys
3. Choose your strategy (1, 2, or 3)
4. Run the baseline implementation
5. Implement your optimizations
6. Test with both papers
7. Document your results

## Tips for Success

### Quick Wins (5-10 minutes):

- Adjust temperature for consistency/creativity
- Increase max_tokens for longer responses
- Add stop sequences to prevent repetition
- Filter too-short or too-long chunks

### Medium Effort (30-60 minutes):

- Custom prompt engineering for academic content
- Post-processing filters for content enhancement
- Section-specific handling (abstracts vs references)
- Quality validation and scoring

### High Impact (2-4 hours):

- Multi-stage processing pipelines
- Ensemble methods combining approaches
- Advanced PDF libraries (pdfplumber, PyMuPDF)
- Custom academic structure detection

## Common Optimization Areas

### LlamaParse Parameters:

```python
parser = LlamaParse(
    result_type="markdown",     # Try: "text", "markdown", "json"
    system_prompt=prompt,       # Academic-specific prompts
    language="en",             # Language settings
    verbose=True,              # Output control
    num_workers=4,             # Parallel processing
)
```

### AI Model Parameters:

```python
together.chat.completions.create(
    model="meta-llama/Llama-3.3-70B-Instruct-Turbo",
    temperature=0.1,           # 0.0-1.0 for creativity vs precision
    max_tokens=4000,           # Adjust based on paper length
    top_p=0.9,                # Response diversity
)
```

### Quality Assessment:

- Automatic section type counting
- Figure/table detection rates
- Citation preservation checking
- Content length distribution analysis

## Submission Requirements

1. **Optimized notebook** with clear documentation
2. **Output files** from processing both papers
3. **Performance comparison** with baseline
4. **Brief optimization report** explaining changes

## Support

For questions or issues:

- Check the notebook comments for optimization hints
- Review the baseline implementations first
- Test one strategy thoroughly before switching
- Document what works and what doesn't

Good luck! 🚀
