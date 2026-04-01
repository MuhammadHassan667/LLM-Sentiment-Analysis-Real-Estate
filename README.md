🤖 LLM Sentiment Analysis in Real Estate
BERT · RoBERTa · GPT-4 · Aspect-Based Sentiment Analysis

MSc Data Analytics Dissertation — Berlin School of Business & Innovation (BSBI), 2026

📌 Overview
This dissertation investigates how well large language models (LLMs) can understand and classify customer sentiment in the real estate sector. Using Aspect-Based Sentiment Analysis (ABSA), three models — BERT, RoBERTa, and GPT-4 — were evaluated on their ability to detect nuanced sentiment across three specific aspects of the customer experience: price, location, and agent behaviour.
The study combined 785 real-world reviews from Trustpilot and Airbnb (secondary data) with a structured primary survey, providing both scale and depth for a robust cross-source comparison.

🎯 Research Questions

How accurately can BERT, RoBERTa, and GPT-4 classify sentiment in real estate customer reviews?
Which aspects (price, location, agent behaviour) drive the most positive and negative sentiment?
Do sentiment patterns differ between primary survey responses and secondary online reviews?
Are the differences between model performances statistically significant?


📊 Dataset
SourceTypeDescriptionTrustpilotSecondaryReal estate agency reviews — scraped public reviewsAirbnbSecondaryProperty rental customer feedbackPrimary SurveyPrimaryStructured questionnaire with open-text responsesTotalCombined785 reviews + survey responses
Survey questions analysed:

"What did you like most about your experience?"
"What could be improved?"
Overall experience rating, property description accuracy, agent communication, likelihood to recommend


🧠 Models Compared
ModelArchitectureApproachBERTbert-base-uncasedFine-tuned for sentiment classificationRoBERTaroberta-baseRobustly optimised BERT pre-trainingGPT-4OpenAI GPT-4Zero-shot and prompt-based classification

🔬 Methodology
Data Collection
├── Secondary: Trustpilot + Airbnb reviews
└── Primary: Structured survey (open-text + Likert scale)
        │
        ▼
Preprocessing & Cleaning
        │
        ▼
Aspect Extraction
├── Price
├── Location
└── Agent Behaviour
        │
        ▼
Sentiment Classification per Aspect
├── BERT
├── RoBERTa
└── GPT-4
        │
        ▼
Statistical Validation
├── Chi-square Test (distribution differences)
└── ANOVA (model performance comparison)
        │
        ▼
Cross-Source Comparison (Primary vs Secondary)

📈 Key Findings
Sentiment Distribution per Aspect
Stacked bar chart showing how positive, neutral, and negative sentiment is distributed across price, location, and agent behaviour aspects across the full dataset.
Show Image
Sentiment Comparison Across Datasets (Primary vs Secondary)
Grouped bar chart comparing how sentiment varies across aspects when broken down by data source — primary survey responses vs secondary online reviews.
Show Image
Primary Survey Sentiment — Likes vs Improvements
Side-by-side sentiment distribution for open-text survey responses: what respondents liked most vs what they felt could be improved.
Show Image
Survey Rating Results
Four-panel chart showing distribution of Likert-scale responses across: overall experience, property description accuracy, agent communication satisfaction, and likelihood to recommend.
Show Image
Key findings summary:

Price attracted the highest proportion of negative sentiment across both primary and secondary data
Location was the most consistently positively-discussed aspect
Agent Behaviour showed the most mixed and context-dependent sentiment — hardest for all models to classify consistently
Significant differences confirmed between model performance via Chi-square and ANOVA testing
Primary and secondary data sources showed notably different sentiment distributions for the agent behaviour aspect


🛠️ Tech Stack
CategoryToolsLanguagePython 3NLP ModelsBERT, RoBERTa (Hugging Face Transformers), GPT-4 (OpenAI API)Data AnalysisPandas, NumPyVisualisationMatplotlib, SeabornMLScikit-learnStatistical TestingSciPy (Chi-square, ANOVA)EnvironmentGoogle Colab / Jupyter NotebookVersion ControlGit & GitHub

📁 Repository Structure
LLM-Sentiment-Analysis-Real-Estate/
│
├── notebooks/
│   └── Cleaned_Chapter5_Notebook.ipynb   # Full analysis notebook
│
├── results/
│   └── figures/                          # All charts and visualisations
│       ├── chart_04.png                  # Sentiment distribution per aspect
│       ├── chart_13.png                  # Primary survey sentiment
│       ├── chart_14.png                  # Aspect sentiment across datasets
│       └── chart_19.png                  # Survey rating distributions
│
├── screenshots/
│   └── thumbnail.png                     # Project thumbnail
│
└── README.md

🚀 How to Run
Option 1 — Google Colab (recommended)

Open notebooks/Cleaned_Chapter5_Notebook.ipynb in Google Colab
Run all cells in order
Ensure your data files are uploaded to the Colab session

Option 2 — Local Jupyter
bashgit clone https://github.com/MuhammadHassan667/LLM-Sentiment-Analysis-Real-Estate.git
cd LLM-Sentiment-Analysis-Real-Estate
pip install -r requirements.txt
jupyter notebook notebooks/Cleaned_Chapter5_Notebook.ipynb

Note: GPT-4 classification requires an OpenAI API key:
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

Extend corpus beyond 785 reviews for higher statistical power
Fine-tune BERT and RoBERTa on domain-specific real estate corpora
Apply methodology to German-language reviews (DACH real estate market)
Explore structured prompting vs zero-shot for GPT-4 classification
Expand aspect dimensions beyond the three studied


📄 Citation
Hassan, M. (2026). Comparative Analysis of LLMs for Aspect-Based Sentiment
Analysis in Real Estate Customer Reviews. MSc Data Analytics Dissertation,
Berlin School of Business & Innovation (BSBI).

👤 Author
Muhammad Hassan
MSc Data Analytics · Berlin School of Business & Innovation (BSBI)
🔗 LinkedIn : www.linkedin.com/in/muhammad-hassan-saeed541
🐙 GitHub : 
