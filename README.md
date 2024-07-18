# YouTube Suggestion Engine
![Screenshot 2024-07-19 020152](https://github.com/user-attachments/assets/08f791e4-d9dd-402c-85b0-6da632efc35d)
Recommendations Using LDA (Latent Dirichlet Allocation): LDA is an unsupervised NLP model employed for uncovering topics within documents. This widely-used topic modeling technique functions similarly to clustering in numerical data, revealing hidden patterns in word collections. In this project, LDA is utilized to recommend videos based on their similarity to a given input video. The development process of this model includes:

Creating a New Dataframe: The original dataframe is refined by retaining only the 'title', 'channel_title', 'tags', and 'description' columns, removing duplicates. These columns are then combined into a single 'overview' column. The cleaned dataframe now features two columns: "title" (video name) and "overview" (comprehensive video information).

Text Preprocessing: The text data undergoes four preprocessing stages: (i) Removing non-English words, (ii) Eliminating stop words, (iii) Constructing bigrams, and (iv) Lemmatization.

Initializing the LDA Model: LDA operates under four key assumptions: (i) Documents are treated as bags of words, (ii) Stop words are considered non-informative, (iii) The number of topics (k) is predetermined, and (iv) All topic assignments are accurate except for the word in question. The LDA model is set up with k = 10 to generate the top 10 recommendations. LDA identifies and ranks the most common keywords across these ten topics.

Building the Recommender System: The recommender system functions based on probability scores. Given a test title, the model calculates its likelihood of belonging to one of the 10 topics. This is treated as a classification problem, and the top 10 highest-scoring videos are recommended to the user.
![Screenshot 2024-07-19 020237](https://github.com/user-attachments/assets/9e9e5e42-f064-4763-881e-e4320171a88a)
