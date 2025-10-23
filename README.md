# Academic Support System

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Django](https://img.shields.io/badge/Django-5.2+-green.svg)](https://www.djangoproject.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> An intelligent AI-powered academic support system that transforms learning materials into structured notes, mind maps, and practice questions. The Project is in progress. Feel free to follow [FutureMind@BJTU](https://github.com/Futuremind-BJTU).

## 🌟 Overview

Academic Support System is a comprehensive AI-driven learning assistant built with Django. It leverages advanced AI technologies to help students and educators efficiently process academic materials, generate structured notes, create interactive mind maps, and generate practice questions.

## ✨ Key Features

### 📚 **Intelligent Document Processing**
- **Multi-format Support**: Handles PDF, Word (DOCX), and PowerPoint (PPTX) files
- **Advanced Parsing**: Extracts text content and preserves document structure
- **Image Recognition**: Processes embedded images and diagrams

### 🤖 **AI-Powered Note Generation**
- **Structured Notes**: Automatically generates well-organized, hierarchical notes
- **Content Analysis**: AI analyzes document content to identify key concepts
- **Smart Summarization**: Creates concise summaries while maintaining academic rigor

### 🧠 **Interactive Mind Mapping**
- **Visual Learning**: Converts notes into interactive mind maps
- **Hierarchical Structure**: Organizes information in logical hierarchies
- **Export Options**: Supports multiple export formats

### 📝 **Intelligent Question Generation**
- **Multiple Question Types**: Generates various question formats
- **Difficulty Levels**: Adapts question complexity based on content
- **Customizable**: Allows users to specify preferences

### 💬 **Smart AI Assistant**
- **Context-Aware Responses**: AI understands document context
- **Chapter-Specific Q&A**: Use `@chapter_name` syntax for targeted questions
- **Content Modification**: Intelligent editing and enhancement

## 🚀 Quick Start

### **Prerequisites**
- Python 3.8 or higher
- pip package manager

### **Installation**

1. **Clone Repository**
   ```bash
   git clone https://github.com/yourusername/zhiwu-qiming-academic-system.git
   cd academic_support_system
   ```

2. **Create Virtual Environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure API Keys**
   ```bash
   cp academic_support_system/config_template.py academic_support_system/config.py
   # Edit config.py with your API keys
   ```

5. **Setup Database**
   ```bash
   python manage.py migrate
   ```

6. **Run Application**
   ```bash
   python manage.py runserver
   ```

7. **Access System**
   - Open browser: `http://localhost:8000`
   - Use guest mode or create account

## 📖 Usage Guide

### **Basic Workflow**

1. **Upload Documents**: Upload PDF, DOCX, or PPTX files (max 5MB)
2. **Generate Notes**: Type "生成笔记" to create AI-generated notes
3. **Create Mind Maps**: Click "思维导图" for visual representation
4. **Generate Questions**: Visit "出题" page for practice questions
5. **AI Q&A**: Use `@chapter_name` for targeted questions

### **Advanced Features**

#### **Chapter-Specific Interactions**
```
@Chapter_Name Your question here
Example: @Network_Basics What is TCP/IP protocol?
```

#### **Content Modification**
```
@Chapter_Name Modification request
Example: @Chapter_1 Please add more examples
```

## 🏗️ Architecture

### **Backend**
- **Django 5.2+**: Web framework with robust ORM
- **Django REST Framework**: API development
- **Channels**: WebSocket support

### **AI Integration**
- **OpenAI API**: GPT models for NLP
- **Custom Prompts**: Optimized for academic content
- **Streaming Responses**: Real-time generation

### **File Processing**
- **PyMuPDF**: PDF processing
- **python-docx**: Word documents
- **python-pptx**: PowerPoint files

## 🔧 Configuration

### **Environment Variables**
```bash
API_KEY=your_openai_api_key
BASE_URL=https://api.openai.com/v1
DEFAULT_MODEL=your-model
```

### **File Settings**
- **Formats**: PDF, DOCX, PPTX
- **Max Size**: 5MB
- **Storage**: `media/{user_id}/uploads/`

## 🧪 Testing

```bash
# Run all tests
python test/test_runner.py

# Specific modules
python test/test_api_client.py
python test/test_note_generation.py
```

## 📁 Project Structure

```
academic_support_system/
├── core/                    # Core functionality
├── notes/                   # Note generation
├── mindmap/                 # Mind map creation
├── questions/               # Question generation
├── users/                   # User management
├── templates/               # HTML templates
├── static/                  # Static files
├── media/                   # User content
├── test/                    # Test suite
├── api_client.py            # AI API client
├── config_template.py       # Configuration template
└── prompts.py               # AI prompts
```

## 🤝 Contributing

1. Fork the repository
2. Create feature branch: `git checkout -b feature/AmazingFeature`
3. Commit changes: `git commit -m 'Add AmazingFeature'`
4. Push to branch: `git push origin feature/AmazingFeature`
5. Open Pull Request

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details.

