# 🏫 SVECW College Chatbot 🤖

**Your Intelligent Guide to Shri Vishnu Engineering College for Women**  
*A Streamlit-powered chatbot delivering accurate college information through AI-powered semantic search*

## 📑 Table of Contents
- [🌟 Overview](#-overview)
- [🚀 Features](#-features)
- [🛠️ Tech Stack](#️-tech-stack)
- [⚙️ Installation](#️-installation)
- [💡 Usage](#-usage)
- [🎨 Customization](#-customization)
- [🤝 Contributing](#-contributing)
- [📜 License](#-license)
- [📞 Contact](#-contact)

## 🌟 Overview
The **SVCEW College Chatbot** is an intelligent Q&A system designed to provide instant, accurate information about Shri Vishnu Engineering College for Women. Leveraging Google's Gemini AI and FAISS semantic search, it understands natural language queries about:
- Admission procedures 🎓
- Academic programs 📚
- Campus facilities 🏛️
- Student life 🎉
- Administrative processes 📋

Built with Streamlit, it features a vintage-styled interface that combines college branding with modern AI capabilities.

## 🚀 Features
- **🎯 Context-Aware Responses**: Gemini-1.5-Flash model delivers human-like answers
- **🔍 Semantic Search**: FAISS index + Sentence-BERT for question understanding
- **🎨 College-Themed UI**: Custom CSS with official colors and styling
- **📈 Dynamic Knowledge Base**: Easy CSV data updates without code changes
- **🛡️ Error Resilience**: Graceful failure handling and user feedback
- **📱 Mobile-Ready**: Responsive design for all devices

## 🛠️ Tech Stack
| Component | Technology | Purpose |
|-----------|------------|---------|
| Frontend | `Streamlit` | Interactive web interface |
| AI Model | `Google Gemini-1.5-Flash` | Response generation |
| NLP | `sentence-transformers` | Question embedding |
| Search | `FAISS` | Semantic similarity matching |
| Data | `Pandas` | CSV processing |
| Backend | `Python 3.10` | Core logic |

## ⚙️ Installation
1. **Clone Repository**
   ```bash
   git clone https://github.com/yourusername/svcew-chatbot.git
   cd svcew-chatbot

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt

3. **Setting Up the Gemini API Key**
   - Before running the application, configure the Gemini API key in your `app.py` file:
   ```python
   # In app.py:
   import google.generativeai as genai
   genai.configure(api_key="your_actual_gemini_api_key")

4. **Prepare the Data**
    - Place your college Q&A CSV file in the following location:
    - data/yourcollege_details.csv

   **✅ CSV Format**
   - The CSV file should have the following columns:
   - `Question` – The question text
   - `Answer` – The corresponding answer
     
    **Example:**
     | Question                          | Answer                          |
     |----------------------------------|---------------------------------|
     | What is the college address?     | SVECW, Bhimavaram, Andhra Pradesh |
     | Who is the principal of SVECW?   | Dr. XYZ                         |

     Make sure the file is saved as `svcew_details.csv` inside the `data` directory.

5. **Run Chatbot**
   ```bash
   streamlit run app.py

## 💡 Usage

Access the chatbot at [http://localhost:8501](http://localhost:8501)

Ask questions like:

- "What's the eligibility for CSE program?"
- "How do I apply for hostel accommodation?"
- "List extracurricular activities available"

The chatbot handles follow-up questions and context switching.

## 🎨 Customization

1. **✏️ Modify Data**
   - Update `svcew_details.csv` with new Q&A pairs to reflect the latest information.

2. **🎨 Change Styling**
   /* Modify custom CSS in app.py */
   ```css
   .college-font {
   font-family: 'Your Custom Font';
   color: #your-brand-color;
   }


3. **🧠 Adjust AI Parameters**
   - To fine-tune the chatbot's response behavior, modify the parameters inside the `generate_response()` function
   in `app.py`:
   
   ```python
   # Modify in generate_response():
   response = gemini.generate_content(
   prompt,
   generation_config=genai.types.GenerationConfig(
   temperature=0.7,
        top_p=0.95
   )
   )

## 🤝 Contributing

We welcome contributions! To get started:

1. **Fork** the repository
   
2. **Create your feature branch**  
   ```bash
   git checkout -b feature/amazing-feature

3. **Commit your changes**  
   ```bash
   git commit -m 'Add amazing feature'

4. **Push to the branch**  
   ```bash
   git push origin feature/amazing-feature

5. **Open a Pull Request** on GitHub

## 📜 License

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This project is distributed under the **MIT License**.  
For more details, please refer to the [LICENSE](LICENSE) file.

## 📞 Contact

**Project Maintainer**  
[Dutta Krishna Madhumita]  
📧 [krishnamadhumitadutta@gmail.com](mailto:krishnamadhumitadutta@gmail.com)  








