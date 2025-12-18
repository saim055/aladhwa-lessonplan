# Al Adhwa Private School - AI Lesson Plan Generator

## 🎓 Overview
A comprehensive, AI-powered lesson plan generation system designed specifically for Al Adhwa Private School teachers. This web application automatically creates complete lesson plan packages including differentiated worksheets, rubrics, question banks, and PowerPoint presentations aligned with UAE/ADEK standards.

## ✨ Features

### Core Functionality
- **AI-Generated Content**: Higher Order Thinking (HOT) objectives and differentiated outcomes
- **DOK-Aligned Differentiation**: Tasks for all ability levels (DOK 1-4)
- **UAE/ADEK Integration**: My Identity, Moral Education, STEAM connections
- **Multiple Teaching Models**: 7E, 5E, I Do/We Do/You Do, Traditional
- **Digital Platform Integration**: PhET, Virtual Lab, Kahoot, and more
- **Gifted/Talented Support**: Optional advanced enrichment tasks

### Generated Package Contents
1. **Lesson Plan Document** (Word) - Fully filled with all columns
2. **Differentiated Worksheets** (DOK Levels 1-4)
3. **Assessment Rubrics** 
4. **Question Bank** (DOK-organized)
5. **PowerPoint Presentation** (Based on selected teaching model)
6. **Complete ZIP Package** (All files bundled)

## 🚀 Quick Start

### Prerequisites
- Python 3.9+
- pip package manager

### Installation

1. **Clone or download this repository**

2. **Install dependencies**:
```bash
cd aladhwa-lessonplan-generator
pip install -r requirements.txt
```

3. **Run the application**:
```bash
python app.py
```

4. **Access the application**:
Open your browser and navigate to: `http://localhost:5000`

## 🌐 Deployment

### Deploy to Render.com (Free)

1. **Create account** at [render.com](https://render.com)

2. **Create New Web Service**:
   - Connect your GitHub repository (or upload files)
   - Choose "Python" environment
   - Build Command: `pip install -r requirements.txt`
   - Start Command: `gunicorn app:app`

3. **Set Environment Variables** (if needed):
   - `PYTHON_VERSION`: `3.9.0`

4. **Deploy**: Your app will be live at `https://your-app-name.onrender.com`

### Deploy to Vercel (Free)

1. **Install Vercel CLI**:
```bash
npm install -g vercel
```

2. **Deploy**:
```bash
vercel
```

3. **Follow prompts** to complete deployment

## 📖 User Guide

### Input Fields

1. **Basic Information**:
   - **Date**: Select lesson date (auto-fills monthly Value)
   - **Semester**: Choose 1 or 2
   - **Grade**: Select grade 1-12
   - **Subject**: Choose from available subjects
   - **Topic**: Enter lesson topic
   - **Period**: Select lesson progression level (Introductory/Intermediate/Advanced)

2. **Standards & Digital Resources**:
   - **Standards**: Select applicable standards (Common Core, NGSS, AP)
   - **Digital Platform**: Optional platform integration

3. **Advanced Options**:
   - **Gifted/Talented**: Enable for advanced enrichment
   - **PPT Teaching Model**: Choose presentation structure

### Generation Process

1. Fill in all required fields (marked with *)
2. Click "Generate Lesson Plan Package"
3. Wait 1-2 minutes for AI generation
4. Download your complete package as ZIP
5. Extract and use Word documents and PowerPoint

## 🎨 Customization

### Modifying Month Values

Edit `app.py` to change the `MONTH_VALUES` dictionary:

```python
MONTH_VALUES = {
    9: "Your Custom Value",
    # ... add more
}
```

### Adding Subjects

Edit `templates/index.html` and add options to the subject dropdown:

```html
<option value="New Subject">New Subject</option>
```

### Changing Logo

Replace `static/images/school_logo.png` with your school logo (recommended: 512x512px PNG)

## 🔧 Technical Architecture

### Backend
- **Framework**: Flask (Python)
- **Document Generation**: python-docx, python-pptx
- **AI Integration**: Anthropic Claude API (optional)

### Frontend
- **HTML5/CSS3**: Modern, responsive design
- **JavaScript**: Vanilla JS for form handling
- **UI Framework**: Custom CSS with Poppins font

### File Structure
```
aladhwa-lessonplan-generator/
├── app.py                  # Main Flask application
├── lesson_generator.py     # Core generation logic
├── requirements.txt        # Python dependencies
├── templates/
│   └── index.html         # Main UI template
├── static/
│   ├── css/
│   │   └── style.css      # Stylesheet
│   ├── js/
│   │   └── app.js         # Frontend logic
│   └── images/
│       └── school_logo.png
├── documents/             # Template storage
└── output/               # Generated files
```

## 🔐 Security Notes

- No user data is stored permanently
- Generated files are temporary
- CORS enabled for API access
- File size limits enforced

## 📝 License

© 2024 Al Adhwa Private School. All rights reserved.

## 🤝 Support

For technical support or feature requests, contact your school IT department.

## 🎯 Roadmap

- [ ] Save lesson plan templates
- [ ] Teacher accounts and history
- [ ] Collaborative editing
- [ ] Mobile app version
- [ ] More digital platform integrations

---

**Made with ❤️ for Al Adhwa Private School Teachers**
