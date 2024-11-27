# EdTech Platform Q&A 🌱

The **EdTech Platform Q&A** system is a streamlined question-and-answer solution designed for the e-learning company [Codebasics](https://codebasics.io). Leveraging the power of **Google PaLM**, **LangChain**, and advanced text embedding technologies, this system provides instant answers to learners' questions, reducing the workload of human support staff. 

Learners can interact with a user-friendly web interface built using **Streamlit**, asking questions about courses, bootcamps, and more, and receiving accurate responses directly from a preloaded FAQ knowledge base.

---

## ✨ Project Highlights

- **Real FAQ Data**: Utilizes an actual CSV file of FAQs currently in use by Codebasics.
- **Streamlit-Based Interface**: Provides an intuitive UI for learners to interact with the system.
- **Efficiency Boost**: Automates the Q&A process to alleviate the workload of support staff.
- **Seamless Workflow**: Allows quick creation of a knowledge base and real-time question answering.

---

## 🚀 Features

- **Knowledge Base Creation**:
  - Automatically builds a searchable knowledge base from an FAQ CSV file.
  - Uses FAISS for efficient vector database management.
- **AI-Powered Q&A**:
  - Employs Google PaLM for natural language processing.
  - Retrieves answers from the knowledge base with high accuracy using LangChain.
- **Sample Questions**:
  - Supports queries like:
    - *Do you provide internships?*
    - *Can I use Power BI on a Mac?*
    - *Should I learn Power BI or Tableau?*
- **Error Handling**:
  - If an answer is not found in the context, the system transparently responds with *"I don't know."*

---

## 🛠️ Technology Stack

- **Framework**: [Streamlit](https://streamlit.io/) for the web application.
- **LLM**: [Google PaLM](https://makersuite.google.com/) for language understanding and question answering.
- **Text Embeddings**: 
  - [HuggingFace Instructor Embeddings](https://huggingface.co/) for creating high-quality document embeddings.
- **Vector Database**: [FAISS](https://faiss.ai/) for efficient storage and retrieval.
- **Environment Management**: [python-dotenv](https://github.com/theskumar/python-dotenv) for secure handling of API keys.
- **LangChain**: Orchestrates the interaction between LLM, embeddings, and retrieval components.

---

## 📋 Prerequisites

1. **Python Version**: Python 3.7 or higher.
2. **API Key**: A valid Google PaLM API key from [MakerSuite](https://makersuite.google.com/).
3. **Required Libraries**: Install dependencies listed in the `requirements.txt` file.

---

## 📦 Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Swayamjexe/Q-A-CSV-Bot.git
   ```
2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
3. **Set Up API Key**:
   - Create a `.env` file in the project directory:
     ```bash
     touch .env
     ```
   - Add your Google PaLM API key:
     ```
     GOOGLE_API_KEY="your_api_key_here"
     ```

---

## 🖥️ Usage

1. **Run the Application**:
   ```bash
   streamlit run main.py
   ```
2. **Using the App**:
   - Click **Create Knowledge Base** to generate the FAQ database (this may take a moment).
   - After creation, a directory named `faiss_index` will be generated in the project folder.
   - Ask questions in the provided input field and receive instant answers!

---

## 🛠️ Project Structure

```plaintext
📁 3_project_codebasics_q_and_a/
├── main.py                   # Streamlit application
├── langchain_helper.py       # LangChain utilities for embeddings and retrieval
├── codebasics_faqs.csv       # FAQ dataset used for knowledge base creation
├── requirements.txt          # Required Python packages
├── .env.example              # Example of environment configuration
├── faiss_index/              # Vector database storage (created after knowledge base generation)
└── README.md                 # Project documentation
```

---

## 🧠 Sample Questions

Here are some sample questions you can ask the system:
- *Do you provide internships or offer EMI payments?*
- *Do you have a JavaScript course?*
- *Should I learn Power BI or Tableau?*
- *Can I use Power BI on a Mac?*
- *How do I enable Power Pivot?*

---

## 🌱 Learning Outcomes

Through this project, you will gain hands-on experience with:
- **LangChain and Google PaLM**: Implementing a Q&A system using advanced language models.
- **Text Embeddings**: Creating embeddings with HuggingFace Instructor.
- **FAISS**: Building and querying a vector database.
- **Streamlit**: Developing interactive web applications.

---

## 🌟 Future Enhancements

- Enable multiple file formats for knowledge base creation (PDFs, JSON, etc.).
- Add multi-language support for broader accessibility.
- Integrate user feedback to refine answers and improve the model over time.

---
