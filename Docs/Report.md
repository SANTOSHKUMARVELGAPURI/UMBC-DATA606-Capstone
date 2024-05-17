# Course Recommendation System for Coursera Users

  - Making progress continuously towards your goal.
  - Updating this document continuously along the way.
 
## 1. Title and Author

- **Project Title** : Course Recommendation System for Coursera Users
- Prepared for UMBC Data Science Master Degree Capstone by Dr Chaojie (Jay) Wang
- **Author**        : Santosh Kumar Velgapuri
- [Link to the author's GitHub profile](https://github.com/SANTOSHKUMARVELGAPURI)
- [Link to the author's LinkedIn profile](https://www.linkedin.com/in/velagapuri-santosh-rao-b6a77916b).
- [Link to your PowerPoint presentation file](https://www.canva.com/design/DAGDYbG5S64/-Z01TyOCdnajB3C3PJppvw/edit?utm_content=DAGDYbG5S64&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)
- Link to your YouTube video (TBA)
    
## 2. Background

**What is it about?**  
→ The project involves building a Course Recommendation System for Coursera users using machine learning models. The dataset contains information about various 
 courses available on the Coursera platform, including attributes such as (
- Course Title  
- Rating, Level  
- Duration  
- Schedule    
- Review  
- What you will learn  
- Skill gain
- Modules  
- Instructor  
- Offered By  
- Keyword  
- Course URL).  

→ The goal of the project is to analyze this dataset, perform exploratory data analysis (EDA), preprocess the data, and then build a machine learning model that 
 can recommend courses to users based on their preferences, historical interactions, and other relevant features. The recommendation system aims to improve user 
 experience by suggesting relevant and personalized courses that match their interests and learning goals.

**Why does it matter?**  
→ This project is important as it addresses the critical need for personalized learning experiences in online education platforms like Coursera.

→ By leveraging machine learning models to analyze user behavior and preferences, the recommendation system can efficiently sift through the vast array of 
 available courses to offer tailored suggestions, thereby saving users time and effort in finding relevant content.  
 
→ This not only enhances user satisfaction and engagement but also contributes to improved learning outcomes by matching learners with courses that align with 
 their interests, skill levels, and career aspirations. Additionally, the project's insights into algorithmic performance metrics and continuous improvement 
 strategies can inform the development of similar recommendation systems across diverse online learning platforms, ultimately advancing the accessibility and 
 effectiveness of online education worldwide.  

**What are your research questions?**  
→ How can user behavior and preferences on Coursera be effectively captured and utilized to generate personalized course recommendations?

→ Which machine learning algorithms and techniques are most suitable for building an accurate and efficient course recommendation system for Coursera users?   

→ What metrics should be used to evaluate the performance and effectiveness of the recommendation system considering the factors such as courses, rating, what will you learn?.  

## 3. Data

The dataset chosen for this recomendation system provides a comprehensive overview of factors potentially contributing to the best course for skill development of the users. It includes both categorical and numerical data, making it suitable for developing predicting and recomendation models.

- **Data sources:** [Coursera_Users_Dataset](https://www.kaggle.com/datasets/elvinrustam/coursera-dataset)
- **Data size:** 52.8 MB 
- **Data shape:** 8370 rows x 13 columns  
- **Data Description:**


  The dataset you've provided is for Coursera users & courses data and comprises 8370 entries across 13 columns of around 52.8 MB. Here's a breakdown of its structure, information and description of each column:

 
| Column Name     | Definition                                                | Data Type  |
|-----------------|-----------------------------------------------------------|------------|
| **Course**      |Title	Title of the course                                 | `object`   |
| **Rating**	    |Rating of the course (out of 5)	                          | `float64`  |
| **Level**	      |Difficulty level of the course	                            | `object`   |
| **Schedule**	  |Schedule of the course	                                    | `object`   |
| **What you will learn**|Description of what will be learned	                | `object`   |
| **Skill gain**	|Description of skills gained                               | `object`   |
| **Modules**	    |Modules included in the course	                            | `object`   |
| **Instructor**	|Instructor of the course	                                  | `object`   |
| **Offered By**  |Entity offering the course	                                | `object`   |
| **Keyword**     |Keywords associated with the course	                      | `object`   |
| **Course Url**	|URL of the course                                          | `object`   |
| **Duration to complete (Approx.)**|Approximate duration to complete the course | `float64`  |
| **Number of Review**|Number of reviews for the course	                       | `int64`    |

**Target/Label Variable:**  

The target variable is **"Number of Reviews."** The goal of the recommendation system is to predict or recommend courses that are likely to receive a high number of reviews, indicating popularity or perceived value.

**Features/Predictors:**

Level, What you will learn, Skill gain, Modules, Instructor, Keyword, Course Url, Number of Reviews.  

## 4. Exploratory Data Analysis (EDA)  
**1.Data Collection and Preparation:**  

_Data Collection:_ Gather the course dataset from Coursera and Kaggle, which includes course titles, rating, level and other relevant attributes mentioned above.
Data Pre-Processing: Clean the dataset by removing any irrelevant information, handling missing values, and ensuring data consistency along with performing few of the analysis on the data to understand the patterns. This step ensures that the data is ready for the next stages.

**2.Text Vectorization:**

_TF-IDF Vectorization:_ this function Converts the textual data (course descriptions and titles) into numerical vectors using TF-IDF (Term Frequency-Inverse Document Frequency). This process transforms text into a format that the machine learning model can process, emphasizing important terms while minimizing the impact of common, less informative words which is used to match the user input and his preferences of course search.  

**3.Stemming Technique:**

_Stemming Technique:_ This text preprocessing technique used in natural language processing (NLP) that involves reducing words to their base or root form. The goal is to simplify words by removing affixes (prefixes, suffixes) to ensure that different forms of a word are treated as the same term. This helps in reducing the complexity of text data and improving the performance of text-based algorithms.

**4.Similarity Computation:**

_Compute Cosine Similarity:_ This Function calculates the cosine similarity between the TF-IDF vectors of all courses. Cosine similarity measures the angle between two vectors, providing a similarity score that indicates how closely related two courses are based on their content with a score between 1 and -1. Where 1 indicates the vectors are identical. 0 indicates vectors are orthogonal (No match), -1 indicates that the vectors are diametrically opposite.

**5.Recommendation Algorithm:**

_Implement Recommendation Function_: Develops a function that accepts a course title as input, finds its corresponding vector, computes similarity scores with all other courses, and identifies the top N most similar courses. This function leverages the cosine similarity scores to rank courses based on their content similarity.

**6.Evaluation and Deployment:**

_Evaluate Recommendations:_ Tested the recommendation system to ensure it provides relevant and accurate course suggestions. Adjust parameters and improve the model as necessary based on user feedback and performance metrics, after successful evaluation the model is giving the recommended courses as per your experience level and along with the priority and sequence of skills ( Top 7 as a set and top 8 until the end of search sort).

_Deploy GUI:_ Create a user-friendly graphical interface using Tkinter that allows users to input a course title and receive personalized course recommendations. Deploy the final system for end-users to access and benefit. 

## 5. Summary.

