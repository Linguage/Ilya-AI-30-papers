# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is the "Ilya 30u30 Papers" collection - a curated set of 32 important research papers and documents in artificial intelligence and deep learning, reportedly recommended by Ilya Sutskever. The collection includes foundational papers that have shaped the development of modern AI, with a focus on neural networks, deep learning architectures, and theoretical foundations.

## Repository Structure

- **Root directory**: Contains the main summary document
- **original_documents/**: Contains all original PDF files and web archives (.mht)
- **processed_papers/**: Contains Markdown summaries and analyses of each paper
- **论文汇总文档.md**: Main index document with Chinese translations and links to all papers

## Key Commands

### Working with Papers
```bash
# View the main summary document
cat 论文汇总文档.md

# List all original documents
ls original_documents/

# List all processed papers
ls processed_papers/

# View a specific paper summary
cat processed_papers/[paper-name].md

# Find papers by topic (example)
grep -r "transformer" processed_papers/

# Count total papers
grep -c "论文汇总文档.md" 论文汇总文档.md
```

### Processing New Papers
```bash
# Extract text from PDF (requires pdftotext)
pdftotext "new-paper.pdf" -

# Process MHT web archives
# Use Python with html.unescape and regex to extract content
```

## Content Architecture

### Paper Categories
The collection is organized into several thematic areas:
- **Neural Network Architectures** (8 papers): Transformer, RNN, CNN, ResNet innovations
- **Optimization & Training** (5 papers): Parallel training, regularization, scaling laws
- **Theoretical Foundations** (6 papers): Complexity theory, MDL principle, information theory
- **Application Domains** (8 papers): Machine translation, speech recognition, image classification, quantum chemistry
- **Relational Reasoning** (2 papers): Relational reasoning and memory architectures
- **Educational Resources** (3 papers): Annotated implementations, blog posts, tutorials

### Document Processing Strategy
- **Large documents** (>100 pages): Extract table of contents, preface, and key chapters
- **Short papers** (<50 pages): Extract full abstract, introduction, and core content
- **Web archives**: Extract main content, structure with markdown, preserve context
- **Standard format**: All processed papers follow consistent markdown structure with metadata

### Summary Document Structure
Each processed paper includes:
- **Basic information**: Title, authors, institution, publication details
- **Abstract**: Core contribution and findings
- **Introduction**: Problem context and motivation
- **Technical content**: Key methods, architectures, and innovations
- **Results**: Main findings and performance metrics
- **Significance**: Impact on the field and historical context

## Development Workflow

### Adding New Papers
1. Place original file in `original_documents/` directory
2. Create processed summary in `processed_papers/` directory
3. Update main summary document with 5-column format:
   - English title
   - Chinese translation
   - Page count
   - MD document link
   - Original file link (pointing to `original_documents/`)

### Content Standards
- Maintain consistent markdown formatting across all summaries
- Include both English and Chinese titles for accessibility
- Preserve technical accuracy while making complex concepts understandable
- Focus on extracting the core contribution and significance of each work

### File Naming Conventions
- PDF files: Keep original academic naming (arxiv-style)
- MHT files: Descriptive names reflecting content
- Processed MD files: Match original filename with .md extension
- Summary document: Use Chinese title "论文汇总文档.md"

## Important Notes

- This collection represents a curated selection of historically significant papers
- The processed summaries are designed for educational and research purposes
- All original documents should be cited appropriately when used
- The collection spans from theoretical foundations to state-of-the-art architectures
- Chinese translations are provided to improve accessibility for Chinese readers

## Historical Context

This collection captures key developments in AI from:
- **Early theoretical work** (1990s-2000s): MDL principle, complexity theory
- **Deep learning revolution** (2010-2014): CNNs, RNNs, neural Turing machines
- **Modern architectures** (2015-2017): Attention mechanisms, transformers, residual networks
- **Scaling and systems** (2018+): Large-scale training, parallelization, efficiency

The collection provides a comprehensive view of the technical evolution that led to modern AI capabilities.