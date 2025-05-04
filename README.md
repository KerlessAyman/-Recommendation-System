# -Recommendation-System
 
# News Recommendation System 📰

This project is a **Content-Based News Recommendation System** built using the [MIND dataset (small)](https://msnews.github.io/), which recommends news articles to users based on their explicitly preferred news.

## 📁 Project Structure

```
my_project/
├── 01_data_preprocessing.ipynb          # Load and clean the dataset; extract TF-IDF features
├── 02_user_profile_construction.ipynb   # Build user profile vector from preferred articles
├── 03_content_similarity.ipynb          # Compute similarities between user profile and all articles
├── 04_ranking_and_recommendation.ipynb  # Rank and display top-N recommendations
├── data/                                # Contains raw and processed data files
├── results/                             # Stores outputs like recommendations and logs
├── requirements.txt                     # Project dependencies
└── README.md                            # Project overview
```

## ⚙️ Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/news-recommender.git
   cd news-recommender
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Download and place the MINDsmall dataset into the `data/` folder. Required files:
   - `news.tsv`
   - `behaviors.tsv`

## 🚀 How to Run

1. Run `01_data_preprocessing.ipynb`  
   → Cleans the news data and builds the TF-IDF matrix.

2. Run `02_user_profile_construction.ipynb`  
   → Constructs a user profile vector from preferred article IDs.

3. Run `03_content_similarity.ipynb`  
   → Calculates cosine similarity between the user vector and all articles.

4. Run `04_ranking_and_recommendation.ipynb`  
   → Ranks articles and exports recommendations to `results/sample_recommendations.csv`.

## 📦 Output

- `sample_recommendations.csv`: Top-N personalized recommendations.
- `user_profile_vector.pkl`, `similarity_scores.pkl`: Intermediate serialized vectors.
- `user_feedback_notes.txt`: Placeholder for collecting manual user feedback (optional).

## ✨ Future Work

- Integrate collaborative filtering.
- Build an interactive UI.
- Collect real-time user feedback.
