#### **Project Title**
**AI-Powered Movie Recommendation Engine**

---

#### **Project Overview**
This project implements a collaborative filtering recommendation engine using the **MovieLens 100k Dataset**. The system predicts user preferences for movies and provides personalized recommendations. It leverages **Surprise** library's **SVD (Singular Value Decomposition)** algorithm to build and evaluate the model.

---

#### **Features**
- Fetches dataset directly using the Kaggle API.
- Preprocesses the dataset to extract user ratings and movie details.
- Builds a recommendation engine using SVD for collaborative filtering.
- Evaluates the model with RMSE (Root Mean Square Error).
- Provides personalized movie recommendations for any given user.

---

#### **Technologies Used**
- Python 3.8+
- Libraries:
  - `pandas`: Data manipulation and analysis.
  - `os`: File and directory operations.
  - `scikit-surprise`: Recommendation engine implementation.
  - `kaggle`: Dataset downloading.
- Dataset: **MovieLens 100k Dataset**

---

#### **Setup Instructions**
1. **Clone the Repository**
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. **Install Required Libraries**
   Install the dependencies using `pip`:
   ```bash
   pip install kaggle scikit-surprise pandas
   ```

3. **Configure Kaggle API**
   - Go to your Kaggle account settings and create an API token.
   - Save the downloaded `kaggle.json` file in `~/.kaggle/` (Linux/Mac) or `%USERPROFILE%\.kaggle` (Windows).
   - Ensure the file has appropriate permissions:
     ```bash
     chmod 600 ~/.kaggle/kaggle.json
     ```

4. **Run the Notebook**
   - Open the Jupyter notebook file `AI_powered_recommendation_engine.ipynb`.
   - Execute the cells step-by-step.

---

#### **Usage**
1. **Download the Dataset**
   - The Kaggle API fetches the **MovieLens 100k Dataset** and extracts it.

2. **Train the Recommendation Model**
   - The SVD model is trained on the user ratings data.

3. **Generate Recommendations**
   - Use the function `get_recommendations(user_id, model, movies, ratings, n)` to get the top **n** movie recommendations for a specific user.
   - Example:
     ```python
     recommendations = get_recommendations(user_id=1, model=model, movies=movies, ratings=ratings, n=10)
     print(recommendations)
     ```

---

#### **Project Structure**
```
AI_powered_recommendation_engine/
│
├── AI_powered_recommendation_engine.ipynb  # Main notebook
├── README.md                               # Documentation
└── data/                                   # Dataset directory (auto-downloaded)
```

---

#### **Sample Output**
**Recommendations for User 1**:
| Movie ID | Title                                |
|----------|--------------------------------------|
| 1        | Casablanca (1942)                   |
| 2        | One Flew Over the Cuckoo's Nest (1975) |
| 3        | Star Wars: Episode IV - A New Hope  |

---

#### **Future Enhancements**
- Add content-based filtering to complement collaborative filtering.
- Integrate a web interface for live recommendations.
- Explore more advanced algorithms like **Neural Collaborative Filtering (NCF)**.

---

#### **License**
This project is open-source and available under the MIT License.
