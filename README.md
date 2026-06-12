**ScriptSense: Automated Multi-modal Document Intelligence & Text Extraction System**
ScriptSense is a robust, multi-modal automated document intelligence platform designed to decode unstructured visual entropy. It bridges the gap between physical ink, chaotic pixels, and actionable structured data.

**Project Overview:**
Script Sense addresses the industrial challenge of digitizing physical documents that contain unconstrained human handwriting, heavily degraded printed text, or complex invoice layouts. By employing a three-tier architectural model, it provides specialized processing for distinct document categories. 

<img width="1731" height="742" alt="image" src="https://github.com/user-attachments/assets/78049842-d240-4c8c-866f-fb773c473f31" />
<img width="1717" height="746" alt="image" src="https://github.com/user-attachments/assets/743b69ea-ad67-4dc1-9534-82322d5a9ac3" />
<img width="1723" height="846" alt="image" src="https://github.com/user-attachments/assets/2f8af597-c251-4762-a18a-bc5d290e6f44" />
<img width="1425" height="840" alt="image" src="https://github.com/user-attachments/assets/4c37b855-c36b-4ddb-9f11-c1c79e27aa2a" />
<img width="1386" height="837" alt="image" src="https://github.com/user-attachments/assets/95fec7c2-0d54-415d-87f2-b53cc42d652e" />
<img width="1383" height="827" alt="image" src="https://github.com/user-attachments/assets/329072bb-cb76-4641-a0fc-3c2267001e8c" />
<img width="603" height="935" alt="image" src="https://github.com/user-attachments/assets/3f557c66-c3c3-4f32-8a0d-44a5126d8a47" />
<img width="602" height="823" alt="image" src="https://github.com/user-attachments/assets/d1e8e5fe-ded7-4fc8-9568-4c88993823d0" />
<img width="720" height="727" alt="image" src="https://github.com/user-attachments/assets/fb34b084-114b-4a10-b935-09c3358b6a44" />
<img width="890" height="505" alt="image" src="https://github.com/user-attachments/assets/07bb64a1-0bbb-4f10-916c-cebd2a3e5cf2" />
<img width="882" height="512" alt="image" src="https://github.com/user-attachments/assets/737f4963-436d-41f1-91d7-3f43dd9a0f0f" />
<img width="930" height="531" alt="image" src="https://github.com/user-attachments/assets/6fbc07e5-ee1e-4f4e-9ef2-5cbe3b54e225" />
<img width="1417" height="831" alt="image" src="https://github.com/user-attachments/assets/331f8617-91d2-4641-82ed-3f721d4dd9c8" />
<img width="1717" height="892" alt="image" src="https://github.com/user-attachments/assets/81cedda5-b50c-42aa-8422-e43069b81e14" />


**Key Features:**

**Detect and read Handwritten Text Recognition system(HTR):** Uses a U-Net-based Fully Convolutional Network for spatial word detection and a Convolutional Recurrent Neural Network (CRNN) with CTC Word Beam Search decoding for accurate sequence transcription.  

**Industrial PDF to text OCR:** Leverages deterministic computer vision (OpenCV) for low-pass filtering, adaptive binarization, and morphological dilation to clean degraded documents before Tesseract processing. 

**Image to text Extractor:** Utilizes Generative AI (Google Gemini LLM) to bridge the gap between raw OCR strings and structured database schemas through zero-shot semantic extraction of key-value pairs.  


**System Architecture:**

ScriptSense utilizes a decentralized hub-and-spoke model:  

**Central Web Hub:** A unified frontend (HTML/CSS/JS) that routes user requests based on document type.  
**ScriptSense Frontend web interface link:** [https://gauravsinghshekhawat1904.github.io/ScriptSense/]

**Model 1 (HTR Pipeline):** Gradio server (Port 7860) using ONNX Runtime for deep learning inference.  
**Model 1 Hugging Face Repo Link:** [https://huggingface.co/spaces/majshekhitbp1234/htr_model](https://huggingface.co/spaces/majshekhitbp1234/htr_model/tree/main)

**Model 2 (PDF Pipeline):** Streamlit server (Port 8501) for batch processing using OpenCV filters and Tesseract. 
**Model 2 GitHub Repo Link**: [https://github.com/gauravsinghshekhawat1904/PDF-To-Text-OCR-.]

**Model 3 (Image to text Extraction):** Flask API (Port 5000) orchestrating Tesseract and Gemini LLM for semantic extraction.  
**Model 3 GitHub Repo Link:** [https://github.com/gauravsinghshekhawat1904/Invoice-Info-Structured-Extraction-using-OCR-Gemini]

<img width="967" height="892" alt="image" src="https://github.com/user-attachments/assets/5f6f73e4-3e2a-4d09-afb8-e65a42d3d375" />


**Technology Stack:**

**Deep Learning:** PyTorch (Research), ONNX Runtime (Production Edge Inference).  
**Computer Vision:** OpenCV, Pillow (PIL).  
**OCR Engine:** Tesseract-OCR (v5+).  
**Web Frameworks** Flask, Streamlit, Gradio.  
**Generative AI:** Google Gemini API.  
**Security:** python-dotenv (environment isolation). 

<img width="1368" height="903" alt="image" src="https://github.com/user-attachments/assets/579c89f1-1789-420e-996a-f97a4c022815" />

