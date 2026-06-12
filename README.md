**ScriptSense: Automated Multi-modal Document Intelligence & Text Extraction System
******ScriptSense is a robust, multi-modal automated document intelligence platform designed to decode unstructured visual entropy. It bridges the gap between physical ink, chaotic pixels, and actionable structured data.

**Project Overview:
**Script Sense addresses the industrial challenge of digitizing physical documents that contain unconstrained human handwriting, heavily degraded printed text, or complex invoice layouts. By employing a three-tier architectural model, it provides specialized processing for distinct document categories. 

**Key Features:
**
Detect and read Handwritten Text Recognition system(HTR): Uses a U-Net-based Fully Convolutional Network for spatial word detection and a Convolutional Recurrent Neural Network (CRNN) with CTC Word Beam Search decoding for accurate sequence transcription.  

Industrial PDF to text OCR: Leverages deterministic computer vision (OpenCV) for low-pass filtering, adaptive binarization, and morphological dilation to clean degraded documents before Tesseract processing. 

Image to text Extractor: Utilizes Generative AI (Google Gemini LLM) to bridge the gap between raw OCR strings and structured database schemas through zero-shot semantic extraction of key-value pairs.  

****System Architecture:
**
**ScriptSense utilizes a decentralized hub-and-spoke model:  

Central Web Hub: A unified frontend (HTML/CSS/JS) that routes user requests based on document type.  

Spoke 1 (HTR Pipeline): Gradio server (Port 7860) using ONNX Runtime for deep learning inference.  

Spoke 2 (PDF Pipeline): Streamlit server (Port 8501) for batch processing using OpenCV filters and Tesseract.  

Spoke 3 (Invoice API): Flask API (Port 5000) orchestrating Tesseract and Gemini LLM for semantic extraction.  

Technology Stack

Deep Learning: PyTorch (Research), ONNX Runtime (Production Edge Inference).  
Computer Vision: OpenCV, Pillow (PIL).  
OCR Engine: Tesseract-OCR (v5+).  
Web Frameworks: Flask, Streamlit, Gradio.  
Generative AI: Google Gemini API.  
Security: python-dotenv (environment isolation). 
