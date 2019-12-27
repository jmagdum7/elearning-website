# elearning-website
This is an e-learning website prototype. This website was created as a final deliverable for our internship. Due to the sensitive nature of the data, actual code and datasets cannot be uploaded.
It consists of features such as Chatbot, Recommendation System, Search Engine, Profile and Course Management. 
The user is required to create a profile which consists of details such as interests, previous courses and educational information. Based on these details, courses are recommended to the user. 
The user can search for specific courses, check course details and can use the conversational chatbot interface to ask questions about the website.

Explanation:
1. The website was an integration of our 3 individual projects: Chatbot, Smart Search, Recommendation System.

A. Smart Search
1) A Search Engine that provided the features of Auto-Completion of Search queries, Fuzzy-String matching and filtering of results based on other user’s choices.
2) Search would enable learner to find a specific course among the entire list of courses based on Course Id, Course Title, Department, etc.
3) Returning results for search query is done based on Levenshtein Distance to calculate distances between sequences. This checks similarity between entered query and actual course title from the entire list.
4) The results are ranked and sorted based on the Clickstream Analysis to show courses with highest preference above other courses.
5) Smart Search ensures no null results are returned for any query. 
6) The engine is able to understand spelling errors and is able to approximate to most similar entries in the data.
7) Auto-Complete to suggest queries on typed individual characters is implemented to reduce learner effort to type out complicated course titles and to avoid spelling mistakes.

B. Recommendation System
1) A Recommendation System was to be developed that would recommend learners with courses based on their interests, overall profile, similarity to other courses, etc. 
2) Recommendation System would aggregate all attributes of a course such as Course Title, Course Description, Languages, Domains, etc.
3) Recommendation based on Related Courses and User Profile utilizes Scikit learn Feature extraction CountVectorizer to convert the data into a sparse matrix and then uses cosine similarity measure to find the next course most similar to the given course.
4) Recommendation based on Collaborative Filtering utilizes the surprise open source library to implement the SVD++ collaborative filtering algorithm which returns the courses you are most likely to take based on what you and people similar to you have rated.

C. Chatbot
1) This project involved the development of a Chatbot for customer service needs such as real-time querying and automated answering. 
2) Chatbot acts as atrained assistant that can provide learners with answers and guidance. 
3) There was a need for Live Natural Processing in the Chatbot.
4) A (8x8) neural network is trained based on the possible conversation users might have with chatbot such as questions based on course type and
course details.
5) Chatbot uses Lancaster Stemmer and Natural Language Toolkit(nltk), python libraries to perform NLP operation to better understand the context.
6) Tensorflow, tflearn are used for building the neural network.
