Introduction :
    A movie recommendation system is a software tool designed to suggest movies to users based on their preferences
    interests, or past behavior. It leverages various algorithms and data to predict which movies a user might enjoy, helping them discover content that matches their tastes. These systems are commonly used by streaming platforms like Netflix, Hulu, and Amazon Prime.
    In our project we are going to use Content-based Filtering method: This method recommends movies based on the characteristics of the movies themselves, such as genre, director, actors, or keywords. It suggests movies that share similar attributes to those the user has already enjoyed.
Objectives :
    1. Personalized Recommendations: Provide tailored movie suggestions to users based on their preferences and past interactions.

    2. Utilization of Content Features: Analyze movie metadata (e.g., genres, actors, directors, plot, etc.) to match movies with user preferences.

    3. Improved User Engagement: Enhance user experience by offering relevant recommendations, encouraging more interaction with the platform.

    4. Cold Start Problem for Users: Address the cold start problem for new users by recommending movies based on their explicitly provided preferences or initial ratings.

    5. Transparency: Offer explainable recommendations by showing why a movie was recommended (e.g., similar genre, actor, or director).

    6. Independence from Popularity: Recommend niche or less-known movies that align with user preferences, not just popular ones.

    7. Scalability: Ensure the system can handle a growing number of users and movie data efficiently.

    8. Content Exploration: Help users discover new movies similar to their favorites that they might not have considered otherwise.

    9. Adaptability: Allow the system to adapt to a user’s changing preferences over time by considering recent feedback or interactions.

    10. Cross-Domain Recommendations: Enable connections between different domains, like recommending movies based on TV shows or books with similar themes.

Data : 
    In this project, we will use the "TMDB 10000 Movies Dataset.csv" and "10000_Movies_Data.csv" datasets, which are available on Kaggle. Here is the link to download the dataset: https://www.kaggle.com/datasets/muqarrishzaib/tmdb-10000-movies-dataset.
    The "TMDB 10000 Movies Dataset.csv" contains over 10,000 rows and four columns: (movie_id, title, cast, crew). The "10000_Movies_Data.csv" contains over 10,000 rows and five columns: (Unnamed: 0, movie_id, title, cast, crew).

Command to create environment -> "conda create --prefix ./env python==3.7 -y"
Command to activate environment -> conda activate "C:\Users\gites\OneDrive\Desktop\Movie Recomdation System\env"
To run the app.py run the following "command streamlit run app.py"