# Resume Analyzer

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![React](https://img.shields.io/badge/React-18.0+-61DAFB?logo=react&logoColor=white)](https://reactjs.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An intelligent career development platform that helps job seekers optimize their resumes, identify skill gaps, and improve their chances of landing their dream jobs using AI-powered analysis. The application provides actionable insights and recommendations to enhance your resume and career prospects.

## 🎯 Features

- **Smart Resume Parsing**: Extract and analyze information from PDF, DOCX, and TXT resumes with high accuracy
- **AI-Powered Role Classification**: Get instant role predictions based on your resume content
- **Comprehensive Skill Gap Analysis**: Identify missing skills for your target job roles with detailed insights
- **ATS Optimization**: Improve your resume's compatibility with Applicant Tracking Systems
- **Personalized Recommendations**: Get tailored course, certification, and project suggestions
- **Interactive Dashboard**: Modern, responsive UI built with React, TypeScript, and shadcn/ui
- **RESTful API**: Robust FastAPI backend with comprehensive documentation and type safety

## ✨ Features

- **Resume Parsing**: Extract and analyze information from PDF, DOCX, and TXT resumes
- **Role Classification**: AI-powered role prediction based on resume content
- **Skill Gap Analysis**: Identify missing skills for target job roles
- **ATS Optimization**: Get your resume past Applicant Tracking Systems
- **Interactive Dashboard**: Beautiful, responsive UI built with React and shadcn/ui
- **RESTful API**: FastAPI backend with comprehensive documentation

## 🚀 Quick Start

### Prerequisites

- Node.js 18+ and npm/yarn
- Python 3.8+
- Git
- CUDA-compatible GPU (recommended for better performance, but not required)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/vj-e/resume-analyzer.git
   cd resume-analyzer
   ```

2. **Set up the backend**
   ```bash
   # Navigate to backend directory
   cd backend
   
   # Create and activate virtual environment
   python -m venv venv
   source venv/bin/activate  # On Windows: .\venv\Scripts\activate
   
   # Install Python dependencies
   pip install --upgrade pip
   pip install -r requirements.txt
   
   # Download the sentence-transformers model (if not done automatically)
   python -c "from sentence_transformers import SentenceTransformer; SentenceTransformer('all-MiniLM-L6-v2')"
   ```

3. **Set up the frontend**
   ```bash
   # Navigate to frontend directory
   cd ../frontend
   
   # Install Node.js dependencies
   npm install
   ```

### Running the Application

1. **Start the backend server** (from the backend directory)
   ```bash
   # In the backend directory
   uvicorn main:app --reload --host 0.0.0.0 --port 8000
   ```
   The API will be available at `http://localhost:8000`
   - API documentation: `http://localhost:8000/docs`
   - Interactive docs: `http://localhost:8000/redoc`

2. **Start the frontend development server** (from the frontend directory)
   ```bash
   # In the frontend directory
   npm run dev
   ```
   The application will be available at `http://localhost:3000`

3. **Access the application**
   Open your browser to [http://localhost:3000](http://localhost:3000)

### Environment Variables

Create a `.env` file in the root directory with the following variables:

```env
# Frontend
VITE_API_URL=http://localhost:8000

# Backend
PYTHONUNBUFFERED=1
PYTHONPATH=.
```

## 🛠️ Tech Stack

- **Frontend**: 
  - React 18 with TypeScript
  - Vite for build tooling
  - shadcn/ui for beautiful, accessible components
  - React Query for data fetching
  - Tailwind CSS for styling

- **Backend**:
  - FastAPI
  - PyMuPDF for PDF processing
  - python-docx for DOCX processing
  - Sentence Transformers for NLP tasks
  - scikit-learn for similarity calculations

## 📂 Project Structure

```
resume-analyzer/
├── backend/               # FastAPI backend
│   ├── main.py           # Main application file
│   ├── requirements.txt  # Python dependencies
│   └── venv/             # Python virtual environment
├── frontend/             # React frontend
│   ├── src/              # Source code
│   ├── public/           # Static files
│   └── package.json      # Node.js dependencies
├── .env.example          # Example environment variables
├── .gitignore           # Git ignore file
└── README.md            # This file
```

## 🚀 Recent Improvements

- **Enhanced Skill Extraction**: Improved algorithm to accurately extract technology/skill names from recommendations
- **CUDA Support**: Added GPU acceleration for faster AI model inference
- **Error Handling**: Better error messages and recovery mechanisms
- **UI/UX Improvements**: More intuitive interface with better feedback

## 📚 API Documentation

Once the backend server is running, you can access the following API endpoints:

### Key Endpoints

- `POST /parse_resume`: Upload and parse a resume file (PDF/DOCX/TXT)
- `POST /classify_resume`: Get role predictions based on resume content
- `POST /skill_gap`: Analyze skill gaps for a target role
- `POST /ats_score`: Get ATS optimization suggestions

### Interactive Documentation

- **Swagger UI**: `http://localhost:8000/docs`
- **ReDoc**: `http://localhost:8000/redoc`

## 🧪 Testing

Run the test suite with:

```bash
# In the backend directory
pytest

# In the frontend directory
npm test
```

## 🤝 Contributing

We welcome contributions! Here's how you can help:

1. **Report Bugs**: Open an issue with detailed reproduction steps
2. **Suggest Features**: Share your ideas for new features
3. **Submit Pull Requests**: Follow these steps:
   - Fork the repository
   - Create a feature branch (`git checkout -b feature/AmazingFeature`)
   - Commit your changes (`git commit -m 'Add some AmazingFeature'`)
   - Push to the branch (`git push origin feature/AmazingFeature`)
   - Open a Pull Request

### Code Style

- **Frontend**: Follow [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript)
- **Backend**: Follow [PEP 8](https://www.python.org/dev/peps/pep-0008/)
- **Git**: Write clear, concise commit messages

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [FastAPI](https://fastapi.tiangolo.com/) for the awesome backend framework
- [React](https://reactjs.org/) for the frontend library
- [sentence-transformers](https://www.sbert.net/) for the NLP capabilities
- [shadcn/ui](https://ui.shadcn.com/) for the beautiful UI components

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [shadcn/ui](https://ui.shadcn.com/) for the beautiful component library
- [FastAPI](https://fastapi.tiangolo.com/) for the amazing backend framework
- [Hugging Face](https://huggingface.co/) for the transformer models
- All contributors and open-source maintainers who made this project possible

## What technologies are used for this project?

This project is built with:

- Vite
- TypeScript
- React
- shadcn-ui
- Tailwind CSS
