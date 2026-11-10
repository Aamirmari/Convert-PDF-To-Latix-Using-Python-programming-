Word → LaTeX/PDF Converter (Django Project)

1. Requirements
• Python 3.9+
• pip (Python package manager)
• Pandoc (for DOCX → LaTeX conversion)
• TeXLive (optional, required for PDF compilation)
• Django (installed via requirements.txt)
2. Install Dependencies
Windows:
1. Install Python from https://www.python.org/downloads/ and check 'Add to PATH'.
2. Install Pandoc from https://pandoc.org/installing.html (download Windows installer).
3. Install TeXLive (large, ~2GB) from https://www.tug.org/texlive/acquire-netinstall.html.
   Alternatively, install MikTeX from https://miktex.org/download for smaller size.
4. Verify installation:
•	   pandoc -v
•	   pdflatex -v
Linux (Ubuntu/Debian):
1. Update system:
•	   sudo apt update && sudo apt upgrade -y
2. Install Python, pip, Pandoc, TeXLive:
•	   sudo apt install -y python3 python3-pip pandoc texlive-latex-base
3. Verify installation:
•	   pandoc -v
•	   pdflatex -v
3. Setup Project
1. Extract the provided ZIP (word_to_latex_project.zip).
2. Open terminal/command prompt and navigate to the backend folder:
•	   cd word_to_latex_project/backend
3. (Optional) Create virtual environment:
•	   python -m venv venv
•	   On Windows: venv\Scripts\activate
•	   On Linux: source venv/bin/activate
4. Install dependencies:
•	   pip install -r requirements.txt
4. Run the Server
1. Run Django server:
•	   python manage.py runserver
2. Open browser and go to:
•	   http://127.0.0.1:8000/
5. Usage
1. Upload a DOCX file via the webpage.
2. The system will:
•	   • Convert DOCX → LaTeX (.tex) using Pandoc
•	   • Attempt PDF compilation using pdflatex (if TeXLive is installed)
•	   • Return a ZIP file containing output.tex and optionally output.pdf
6. Notes
• If PDF compilation fails, you will still get LaTeX (.tex) output.
• For large documents with equations, full TeXLive is recommended.
• Tested on Windows 10/11 and Ubuntu 22.04.
