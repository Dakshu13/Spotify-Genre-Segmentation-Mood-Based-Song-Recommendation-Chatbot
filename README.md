# 🎵 Spotify Genre Segmentation + Mood-Based Song Recommendation Chatbot

Spotify’s music recommendation system is known for its accuracy. It suggests songs based on listening history and clusters similar audio features to identify genres and moods.

In this project, we recreate a simplified version of that process using **KMeans clustering** and build a **simple AI chatbot** to suggest songs based on cluster (genre/mood).

### 📌 Project Workflow

1. **Load the Spotify Dataset**  
   Import the dataset containing audio features of various songs.

2. **Clean the Data**  
   Handle missing values and drop irrelevant columns.

3. **Visualize Audio Features**  
   Use scatter plots to compare audio characteristics like `danceability`, `energy`, `key`, etc., and find patterns.

4. **Apply KMeans Clustering**  
   Fit a KMeans model to group songs into 6 clusters representing moods/genres:
   - `pop`, `rap`, `rock`, `latin`, `r&b`, and `edm`.

5. **Visualize Clusters**  
   Plot the clusters using `hue="clustergroup"` in Seaborn to understand separation.

6. **(Optional)**:  
   Create bar graphs to show the number of songs in each cluster for visual clarity.

7. **Evaluate Clustering**
   Calculate the **Silhouette Score** to measure cluster quality.  
   *Score achieved:* **0.62**, indicating strong and well-separated clusters.

8. Build a Simple Chatbot 🤖  
   Create a rule-based chatbot using `if-else` conditions.  
   The chatbot:
   - Greets the user
   - Asks for a preferred music mood (mapped to cluster)
   - Recommends top 10 songs (by name) from the selected cluster
