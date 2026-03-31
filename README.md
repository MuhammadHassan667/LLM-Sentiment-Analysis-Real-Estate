🤖 LLM Sentiment Analysis in Real Estate
BERT · RoBERTa · GPT-4 · Aspect-Based Sentiment Analysis

MSc Data Analytics Dissertation — Berlin School of Business & Innovation (BSBI), 2026


📌 Overview
This dissertation investigates how well large language models (LLMs) can understand and classify customer sentiment in the real estate sector. Using Aspect-Based Sentiment Analysis (ABSA), three models — BERT, RoBERTa, and GPT-4 — were evaluated on their ability to detect nuanced sentiment across specific aspects of the customer experience.
The study combined 785 real-world reviews from Trustpilot and Airbnb with primary survey data, providing both breadth (large-scale online reviews) and depth (structured survey responses) for a robust comparison.

🎯 Research Questions

How accurately can BERT, RoBERTa, and GPT-4 classify sentiment in real estate customer reviews?
Which model performs best across different sentiment aspects (price, location, agent behaviour)?
Do significant differences exist between model performance using statistical validation?


📊 Dataset
SourceTypeVolumeTrustpilotReal estate agency reviewsPublic reviewsAirbnbProperty rental feedbackPublic reviewsPrimary SurveyStructured questionnaire responsesOriginal data collectionTotalCombined corpus785 reviews
Aspect dimensions analysed:

💰 Price — sentiment around cost, value for money, fees
📍 Location — sentiment around area, accessibility, neighbourhood
🤝 Agent Behaviour — sentiment around responsiveness, professionalism, communication


🧠 Models Compared
ModelTypeArchitectureBERTBidirectional Encoderbert-base-uncasedRoBERTaRobustly Optimised BERTroberta-baseGPT-4Generative Pre-trained TransformerOpenAI GPT-4 API
All models were evaluated using the same labelled dataset to ensure fair comparison.

🔬 Methodology
Data Collection (Trustpilot + Airbnb + Survey)
        │
        ▼
Data Preprocessing & Cleaning
        │
        ▼
Aspect Extraction (Price · Location · Agent Behaviour)
        │
        ▼
Sentiment Classification per Aspect
   ┌────┴────┐─────────┐
  BERT   RoBERTa    GPT-4
        │
        ▼
Statistical Validation
  Chi-square Test · ANOVA
        │
        ▼
Results & Comparative Analysis

📈 Key Findings

RoBERTa achieved the highest overall accuracy in sentiment classification across all three aspect dimensions
GPT-4 demonstrated strongest performance on nuanced, context-dependent sentiment (agent behaviour)
BERT provided a solid baseline but was outperformed in fine-grained aspect classification
Price was the most negatively-discussed aspect across both Trustpilot and Airbnb reviews
Location was the most positively-discussed aspect overall
Agent Behaviour showed the most mixed and context-dependent sentiment — hardest for all models to classify consistently
Statistical validation via Chi-square and ANOVA confirmed significant differences between model performance


🛠️ Tech Stack
CategoryToolsLanguagePython 3.10+NLP ModelsBERT, RoBERTa (Hugging Face Transformers), GPT-4 (OpenAI API)LibrariesPandas, NumPy, Scikit-learn, Matplotlib, SeabornStatistical TestingSciPy (Chi-square, ANOVA)EnvironmentJupyter NotebookVersion ControlGit & GitHub

📁 Repository Structure
llm-sentiment-analysis-real-estate/
│
├── data/
│   ├── raw/                    # Raw review data (anonymised)
│   └── processed/              # Cleaned and labelled dataset
│
├── notebooks/
│   ├── 01_data_preprocessing.ipynb
│   ├── 02_bert_classification.ipynb
│   ├── 03_roberta_classification.ipynb
│   ├── 04_gpt4_classification.ipynb
│   └── 05_statistical_validation.ipynb
│
├── results/
│   ├── model_comparison.csv    # Accuracy scores per model per aspect
│   └── figures/                # Charts and visualisations
│
├── screenshots/
│   └── thumbnail.png
│
├── requirements.txt
└── README.md

🚀 How to Run
1. Clone the repository
bashgit clone https://github.com/MuhammadHassan667/llm-sentiment-analysis-real-estate.git
cd llm-sentiment-analysis-real-estate
2. Install dependencies
bashpip install -r requirements.txt
3. Run notebooks in order
Open Jupyter and run notebooks 01 through 05 in sequence.

Note: GPT-4 classification requires an OpenAI API key. Add it as an environment variable:
bashexport OPENAI_API_KEY=your_key_here


📦 Requirements
transformers>=4.30.0
torch>=2.0.0
openai>=1.0.0
pandas>=1.5.0
numpy>=1.24.0
scikit-learn>=1.2.0
matplotlib>=3.7.0
seaborn>=0.12.0
scipy>=1.10.0
jupyter>=1.0.0

🔮 Future Work

Extend the dataset beyond 785 reviews for higher statistical power
Fine-tune BERT and RoBERTa on domain-specific real estate corpora
Explore GPT-4 with structured prompting vs zero-shot classification
Apply the methodology to German-language real estate reviews (DACH market)


📄 Citation
If you use this work as reference:
Hassan, M. (2026). Comparative Analysis of LLMs for Aspect-Based Sentiment 
Analysis in Real Estate Customer Reviews. MSc Data Analytics Dissertation, 
Berlin School of Business & Innovation (BSBI).

👤 Author
Muhammad Hassan
MSc Data Analytics · Berlin School of Business & Innovation
🔗 LinkedIn
📧 Email
🐙 GitHub

📄 License
MIT License — feel free to use this as a reference for your own NLP research.
