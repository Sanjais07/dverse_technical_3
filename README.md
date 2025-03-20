# Seven Hills Hospital AI Chatbot

## Overview
The **Seven Hills Hospital AI Chatbot** is a smart FAQ assistant that gives real-time answers to hospital-related questions. Developed with **Streamlit, Sentence-BERT, and Transformers**, the chatbot is able to fetch appropriate answers from a pre-defined knowledge base and improve its understanding over time based on user feedback.

## Features
- **Real-time FAQ Assistance**: Users can query, and the chatbot gives the most appropriate response.
- **Natural Language Processing (NLP)**: Utilizes **Sentence-BERT (SBERT)** for semantic search and **DistilBERT** for context-based question answering.
- **Interactive UI**: Built with **Streamlit**, offering a user-friendly experience.
- **Chat History**: Displays previous interactions in the sidebar.
- **Knowledge Base Expansion**: Users can provide feedback and add new question-answer pairs to improve the chatbot.
- **Custom Background and Branding**: Supports image-based branding with background images and hospital logos.

## Tech Stack
- **Python** (Core logic)
- **Streamlit** (UI framework)
- **Sentence-BERT (SBERT)** (Semantic similarity matching)
- **Hugging Face Transformers** (DistilBERT-based QA model)
- **Pandas & JSON** (Data storage and manipulation)
- **Torch (PyTorch)** (Model computation)

## Installation
### Prerequisites
Make sure you have Python 3.7+ installed and install the necessary dependencies.

```bash
pip install streamlit pandas torch transformers sentence-transformers
```

### Running the Application
1. Clone the repository or copy the project files.
2. Make sure the **Sevenhillshospital_faq.txt** file is available in the mentioned directory.
3. Run the following command to launch the chatbot:

```bash
streamlit run chatbot.py
```

## Project Structure
```
/SevenHillsChatbot
│── chatbot.py  # Main application file
│── Sevenhillshospital_faq.txt  # FAQ database in JSON format
│── background.jpg  # Background image for UI
│── seven-hills-logo.png  # Hospital logo for branding
└── README.md  # Project documentation
```

## How It Works
1. **FAQ Data Loading**: The chatbot reads questions and answers from `Sevenhillshospital_faq.txt`.
2. **Question Processing:**
- User input is preprocessed (lowercasing, punctuation stripping, whitespace normalization).
- SBERT processes the query and identifies the closest FAQ match.
3. **Response Generation**:
   - If a close match is discovered, the chatbot responds with the cached answer.
   - If no close match is discovered, DistilBERT is utilized to extract an answer from similar FAQs.
4. **User Feedback & Learning**:
- Users may introduce new questions and answers for enhancing the chatbot.
- Data is stored back in `Sevenhillshospital_faq.txt` for reuse.

## Customization
- **Change the UI**: Replace the **Streamlit** layout and branding images.
- **Expand the Knowledge Base**: Introduce new FAQs into `Sevenhillshospital_faq.txt`.
- **Enhance Model Performance**: Refine or swap the existing models.

## Future Improvements
- Incorporate **speech-to-text** for voice interactions.
- Add more hospital-specific questions to the dataset.
- Implement the chatbot as a **web application** or integrate it with a **hospital website**.

## License
This project is for research and educational purposes. Contact the owner of the project for commercial use.



