Movie Recommender System 🎥🍿

A web application that provides personalized movie recommendations based on user selection. It also displays movie posters to enhance the user experience.


 Features

	•	Personalized Recommendations: Suggests movies based on the selected movie.
	•	Poster Display: Fetches and displays movie posters alongside recommendations.
	•	User-Friendly Interface: Built using Streamlit for a clean and interactive interface.


 Project Structure
 movie_recommender_system/
│
├── app.py                     # Main application file  
├── movie_dict.pkl             # Preprocessed movie dataset  
├── similarity.pkl             # Precomputed similarity matrix  
├── requirements.txt           # Python dependencies  
└── README.md                  # Documentation file  


Technologies and Libraries
Libraries Used:

	•	Streamlit: For building the web application interface.
	•	Pandas: For data manipulation and analysis.
	•	Requests: For API integration (fetching posters).
	•	Pickle: For loading preprocessed data and similarity matrices.




 How It Works

 	1.	Input Selection:
The user selects a movie from a dropdown list.
	2.	Recommendation System:
	•	The app computes the similarity of the selected movie with other movies using the cosine similarity technique.
	•	The top 5 similar movies are fetched based on the similarity scores.
	3.	Poster Retrieval:
	•	Movie IDs from the dataset are used to fetch posters via the TMDb API.
	•	The posters are displayed alongside the recommended movies.
	4.	Interactive Output:
	•	Recommendations and posters are displayed in a responsive grid layout.


  How to Set Up and Run

1. Clone the Repository
   git clone https://github.com/Krish95-bg/movie_recommender_system.git
cd movie_recommender_system

2.Create a Virtual Environment
  python3 -m venv env
source env/bin/activate  # For macOS/Linux
env\Scripts\activate     # For Windows

3. install Dependencies
   pip install -r requirements.txt

4.Add Your TMDb API Key
response = requests.get("https://api.themoviedb.org/3/movie/{}?api_key=YOUR_API_KEY".format(movie_id))

5. Run the Application
   streamlit run app.py

6. Explore the App

	•	Open the app in your browser (default: http://localhost:8501).
	•	Select a movie and view recommendations with posters.

