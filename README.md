# AI-Agent-OCRmyPDF

The script aims to convert physical or image-based documents into structured, searchable data. It uses open-source tools and Google's Gemini AI platform. The script's pipeline has three main phases: Preparation, Processing, and AI Interaction & Interface.

Document Intelligence Pipeline.

The entire process runs within a Kaggle Notebook.

Phase 1: Environment Preparation (Parts 1-4, 6-7)

This phase installs software, defines working directories, and authenticates with the AI service.

Step__Action__Tools/Tech

1. Set up Directories by os

2. Install System Dependencies by apt-get

3. Install Python Libraries by pip, ocrmypdf

4. Configure Authentication by GOOGLE_API_KEY
   
5. Import AI Libraries by Google ADK, google.genai

Phase 2: Document Processing & OCR (Part 5)

This phase transforms raw input files into machine-readable documents.

Step__Action__Tools/Tech

1. Scan Input Folder	by os.listdir

2. Iterate & OCR	by ocrmypdf

3. Create Searchable PDFs by Tesseract OCR

4. Save Outputs by /kaggle/working/

Outcome of Phase 2: The /kaggle/working/processed_files directory now contains PDFs with a searchable text layer. This is true regardless of the original input type.

Phase 3: AI Interaction & Data Extraction (Parts 8-14)

This phase uses the Google ADK (AI Device Kit) framework to run an AI agent and provide a user interface.

Step__Action__Tools/Tech

1. Define Helper Functions by Python async functions

2. Configure AI Agent by Gemini, google_search

3. Run Initial Test	by InMemoryRunner

4. Prepare Web UI Access by Kaggle Proxy Functions

5. Launch Web Interface by adk web CLI Command

Outcome of Phase 3: A web interface becomes available, allowing users to interact with the configured Gemini AI agent. The agent can analyze the processed documents and extract data through user prompts in the web UI.


Remarks:

-The difference in accuracy depends entirely on the type of PDF you are processing (image-based vs. digital text-based) and how you are interfacing with the AI.

In this specific scenario, combining ocrmypdf with AI will yield significantly higher accuracy for data extraction compared to using the AI alone.

Here is a breakdown of why:

1.	AI cannot directly read text from image-based PDFs.

If a PDF is a scanned image, AI models require multimodal computer vision capabilities to extract the text data. Otherwise, the AI will receive unintelligible input.

2.	The accuracy difference is substantial.

The combination of OCRmyPDF and AI creates an "Intelligent Document Processing" (IDP) pipeline.

-OCRmyPDF is only appliable to PDF, other than PDF such as .txt or docx file should be converted to PDF before using it.
