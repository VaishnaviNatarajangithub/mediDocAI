**MediDocAI**

MediDocAI is an interactive AI-driven platform for analyzing prescription images. Users can upload prescriptions in English and Tamil, extract key medical entities, generate concise summaries, and ask voice-based questions about the prescription. The project demonstrates the integration of OCR, multilingual NER, summarization, and voice-based question-answering in a single interface using Google Colab.

**Features**

Prescription Upload: Upload a single prescription image for processing.

Multilingual OCR: Extract text from images in English and Tamil.

Entity Extraction: Automatically extract patient, doctor, medicine, dosage, diagnosis, frequency, and duration.

Summary Generation: Generate structured English summaries from mixed-language prescriptions using mBART.

Voice-based Q/A: Ask questions using voice input; the AI responds based on prescription context.

Interactive Interface: Built using Gradio for a seamless demo experience.

**Project Structure**
mediDocAI/
│
├── data/                          # Folder to store uploaded prescription images
│   └── example_prescription.jpg   # Sample prescription image (optional)
│
├── models/                        # Pre-trained or downloaded models (optional)
│   ├── xlm-roberta-ner/           # NER model files
│   ├── mbart-summary/             # mBART summarization model
│   └── whisper/                   # Whisper model files
│
├── prescription_analysis.ipynb    # Main Colab notebook with full pipeline:
│                                   # - Upload image
│                                   # - OCR extraction
│                                   # - Entity extraction
│                                   # - Summary generation
│                                   # - Voice-based Q/A
│
├── requirements.txt               # Python dependencies for easy setup
├── README.md                      # Project documentation (this file)
└── LICENSE                        # License file (optional)

**Installation & Setup**

**Clone the repository:**

git clone https://github.com/VaishnaviNatarajangithub/mediDocAI.git
cd mediDocAI


**Install dependencies:**

!pip install -q gradio whisper transformers torch pytesseract sentencepiece


**Run the Colab notebook:**

Open prescription_analysis.ipynb in Google Colab.

Upload a prescription image.

Extract entities, generate summary, and ask voice-based questions interactively.

**Tech Stack**

Python – Core programming language.

Google Colab – Platform for running the project and showcasing interactive demos.

OCR: pytesseract for text extraction from images.

NER: transformers library with Davlan/xlm-roberta-base-ner-hrl model.

Summarization: mBART-50 multilingual translation model.

Voice-based QA: Whisper for speech-to-text, XLM-RoBERTa for question-answering.

Interface: Gradio for interactive UI within Colab.

Usage

Run the notebook in Colab.

Upload a prescription image.

View extracted entities.

Generate a concise English summary.

Ask questions using your microphone; the AI responds based on the prescription.

**Future Enhancements**

Support for more Indian languages in prescriptions.

Integration with a React.js frontend for standalone web deployment.

Add alerts section for dosage warnings or drug interactions.

Store historical prescriptions for patient-specific insights.

**License**

This project is for educational/demo purposes.
