# Movie Recommendation System

This project implements a movie recommendation system using two different methods: **Collaborative Filtering** and **Content-Based Filtering**. The dataset used consists of three CSV files:

- **Movies.csv**
- **Ratings.csv**
- **Tags.csv**

The dataset contains information about approximately 9,700 movies across a variety of genres. The goal of this project is to build a recommendation system that can suggest movies to users based on their preferences, leveraging the power of machine learning techniques and data analysis.

### Dataset Overview

1. **Movies.csv**: Contains metadata about the movies, including titles, genres, and movie IDs.
2. **Ratings.csv**: Contains user ratings for movies, with user IDs, movie IDs, and ratings on a scale of 1-5.
3. **Tags.csv**: Includes user-generated tags for movies, allowing for additional information to enhance recommendations.

### Methods

#### 1. **Collaborative Filtering**
   Collaborative filtering uses user-item interactions to make recommendations. It identifies patterns in user behavior and suggests movies that similar users have liked. We use **Singular Value Decomposition (SVD)** for matrix factorization in this approach.

#### 2. **Content-Based Filtering**
   Content-based filtering makes recommendations based on the attributes of the items (movies). In this case, we use the **genres** of the movies to calculate similarity scores between movies and recommend those that are most similar to the user's preferences.

### Project Workflow

1. **Data Loading**: The CSV files are loaded into Pandas DataFrames for easy manipulation and analysis.
2. **Data Preprocessing**: The data is cleaned and prepared for both collaborative and content-based filtering.
3. **Model Building**:
   - Collaborative Filtering uses matrix factorization (e.g., SVD) to predict missing ratings.
   - Content-Based Filtering leverages **TF-IDF** vectorization to calculate cosine similarity between movies based on their genres.
4. **Recommendation Generation**: The system suggests top N movies based on user preferences or movie similarity.

### Requirements

- Python 3.x
- Pandas
- NumPy
- Scikit-learn
- Surprise (for Collaborative Filtering)
- Matplotlib (optional for visualizations)

### Installation

To install the necessary dependencies, you can create a virtual environment and use the following command to install the required packages:

```bash
pip install -r requirements.txt
```

### Usage

To run the recommendation system, execute the following command:

```bash
python recommendation_system.py
```

This will run the collaborative filtering and content-based filtering models, and output a list of recommended movies.

### Future Improvements

- Implement **Hybrid Recommendation Systems** by combining both Collaborative and Content-Based Filtering methods.
- Use advanced techniques such as **Deep Learning** for more accurate predictions.
- Include additional features, such as movie descriptions or user demographics, to further enhance recommendations.

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

This version of the README provides a professional, clear, and concise description of your project, and it explains the context, methods, and usage in a structured format.
