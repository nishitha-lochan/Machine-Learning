Movie Recommendation System using K-Nearest Neighbors (User-Based)

Project Overview:

This project is a User-Based Movie Recommendation System built using the K-Nearest Neighbors (KNN) algorithm.
The system recommends movies to a target user based on the preferences of similar users.

Instead of predicting ratings directly, it finds users with similar movie-watching behavior and suggests movies that those similar users liked but the target user hasn’t watched yet.

How the Recommendation Works (Concept):

->Each user is represented as a vector of movie ratings

->Users with similar rating patterns are considered neighbors

->KNN finds the K most similar users

->Movies liked by these users but not watched by the target user are recommended

->Similarity between users is calculated using Cosine Similarity.

Dataset Used:

->MovieLens 100K Dataset

Required files:

->u.data → User–Movie ratings

->u.item → Movie details (movie_id, title)

Other files in the dataset are not required for this project.

Libraries Used:

->pandas – data manipulation

->numpy – numerical operations

->scikit-learn – KNN model (NearestNeighbors)

⚙️ Step-by-Step Workflow
1️⃣ Load the Dataset:

Read ratings and movie details into pandas DataFrames

2️⃣ Create User–Movie Matrix:

Rows → users

Columns → movies

Values → ratings

Missing ratings filled with 0 (means not watched)

3️⃣ Train KNN Model:

->Use NearestNeighbors

->Metric: cosine

->Fit the model on the user–movie matrix

4️⃣ Find Similar Users:

->Select a target user

->Use KNN to find nearest neighbors

->Retrieve similar users’ rating vectors

5️⃣ Generate Recommendations

->Compute mean ratings from similar users

->Remove movies already watched by the target user

->Recommend top movies with highest mean ratings

📊 Example Output
Recommended Movies:
1. Toy Story
2. Star Wars
3. Fargo
4. Jurassic Park

Why KNN for Recommendation?

->Simple and intuitive

->No training phase (lazy learning)

->Works well for collaborative filtering

->Easy to explain in interviews

Future Improvements

Item-based collaborative filtering

Weighted ratings based on similarity

Hybrid recommendation system

Evaluation using precision / recall