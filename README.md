# Multi-Speaker AI Research Paper Summarizer

## 📌 Overview
This project extracts text from a research paper, summarizes it using an LLM (Llama model), generates an interactive dialogue between two scientists, and converts the dialogue into a multi-speaker audio conversation.

## 🚀 Features
- Extracts text from PDFs using a hybrid approach (PyPDF2 + OCR via PaddleOCR).
- Summarizes research papers using a Llama model.
- Generates structured dialogue between two AI scientists.
- Converts dialogue into realistic AI voice conversations with multiple speakers.
- Saves the conversation as an audio file (`dialogue.mp3`).

## 🛠️ Installation
### 1. Clone the Repository
```sh
git clone https://github.com/Ravij-p/ResearchPaperToPodcast.git
cd ResearchPaperToPodcast
```

### 2. Install Dependencies
```sh
pip install -r requirements.txt
```
Ensure that you have the following installed:
- `PyPDF2`
- `paddleocr`
- `edge-tts`
- `moviepy`
- `llama-cpp-python`
- `pdf2image`
- `Pillow`

### 3. Install Additional Requirements
#### Tesseract-OCR (if OCR is needed)
```sh
sudo apt install tesseract-ocr
```
#### Poppler (for pdf2image conversion)
```sh
sudo apt install poppler-utils
```

## 🔧 Usage
### 1. Set Up the Llama Model
Download a Llama model file and place it in an accessible directory. Update the model path in `research_paper_processor()`:
```python
llm = Llama(model_path="/path/to/llama-model.gguf", n_ctx=2048)
```

### 2. Run the Script
Specify a PDF file to process:
```python
pdf_path = "path/to/research_paper.pdf"
summary, dialogue = research_paper_processor(pdf_path)

print("Generated Summary:\n", summary)
print("\nGenerated Dialogue:\n", dialogue)
```

## 📂 Output Files
- `dialogue.mp3` - The final AI-generated dialogue in audio format.
- Extracted text and summary are printed to the console.

## 🎤 Demo Podcast
A sample AI-generated podcast is available as `dialogue.mp3`, based on an uploaded research paper.

## 📝 Example Dialogue Output
```
Scientist 1: Share your perspective on the key findings.
Scientist 2: Provide a counterargument or an alternative viewpoint.
Scientist 1: Discuss the methodology's strengths.
Scientist 2: Highlight any weaknesses.
...
```

## 🛠️ Troubleshooting
- **PyPDF2 not extracting enough text?** Try enabling OCR.
- **Missing dependencies?** Ensure all required packages are installed.
- **Audio issues?** Verify `edge-tts` is working and the required voices are installed.



https://github.com/user-attachments/assets/babf47fe-d7b5-4a10-802c-a881024780f0

