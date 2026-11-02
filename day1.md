 ### Course syllabus
Phase	Topics	What you'll understand
1	AI Fundamentals	What AI is and how it works
2	Types of AI	Narrow AI, General AI, Reactive AI
3	Machine Learning	How machines learn from data
4	ML Algorithms	Regression, classification, clustering
5	Mathematics for AI	Statistics, probability, linear algebra
6	Deep Learning	Neural networks and backpropagation
7	Generative AI	How AI generates new content
8	NLP	How machines understand human language
9	Transformers	Architecture behind modern LLMs
10	LLMs	GPT, tokens, embeddings, attention
11	Prompt Engineering	How to communicate effectively with AI
12	Vector Databases	Storing and searching semantic information
13	RAG	Connecting AI with external knowledge
14	AI Agents	AI systems that perform tasks
15	AI Development	Python, APIs, frameworks and deployment
16	Projects	Building practical AI applications

### (1) 1  What is Intelligence
Doing calculation, recognising things,language understanding, perception(understanding infromations from our surrounding),problem solving, taking decision and learning new things.

## What is Artificial Intelligence
It is branch of cse in which we focus on creating a machine that can perform tasks
that require normally human like intelligence.

## 2 How AI is different from traditional programming
Suppose we want to develop email spam detection system-

Approach A: Traditional programming
A developer writes explicit rules like - 
 if (email.contains("win money") ||
            email.contains("free prize") ||
            email.contains("claim now")) {
            return "Spam";
        }

Approach B: Artificial Intelligence using Machine Learning
Now imagine a different approach.
Instead of writing every rule manually, you provide thousands of examples of spam and legitimate emails and from that model learns and help to predict.

### 3 AI capabilities 
1. Learing
2. Reasoning
3. Perception
4. Natural Language Processing
5. Problem Solving

## 4 Branches Of AI
1. Machine Learning
2. Computer Vision  -- Understanding images and videos
3. Natural Language Processing
4. Expert System  -- Rule-based expert decisions
5. Robitics
6. Search & Planning -- Finding paths and solutions

## 5 AI system lifecycle
1. Data Collection --- Collect historical house information.
2. Data Preprocessing ---  Clean missing, incorrect, or inconsistent information.
3. Model Training ---  The algorithm learns relationships from the data.
4. Model Evaluation --- Check how accurately the model predicts house prices.
5. Model Deployment --- Make the trained model available through an application or API.
6. Prediction (Inference) --- Provide new house details and receive a predicted price.


####         ///////////////////////////////////////////

## (2) Types of Ai
#  i> Based on Capabilities(How intelligent or capable is the AI?):
1. ANI - Artificial Narrow Intelligence (Performs specific tasks) e.g google assistant, alexa, netflix;
2. AGI - Artificial General Intelligence (Performs a broad range of intellectual tasks at a human-comparable level)
3. ASI - Artificial Super Intelligence (Surpasses Human IQ and Abilities)

#  ii> Based on Functionality (How does the AI operate and use information?)
1. Reactive Ai - Good for simple classification and pattern recoginition e.g - IBM Deep Blue
     They observe the current situation and respond accordingly.
     They do not use stored past experiences to improve their decisions.
2. Limited Memory - It can handle complex classification and uses information from recent or historical observations to make decisions.
3. Theory of Mind - Able to understand human motives and reasoning and able to learn from 
few examples.
4. Self - Aware -> Human- level intelligence that can bypass human intelligence.


#####            //////////////////////////////////
### (3) Machine Learning
Machine Learining is a branch of Artificial Intelligence that enables computers to learn 
patterns from the data and make predictions and decisions without being explicitly programmed 
with every individual rule.
It is important concept in the entire ai field.

Q. "If we can already write programs using Java, Python, or JavaScript, why do we need Machine Learning?"
Traditional programming works very well when the rules are clear and predictable.

eg. of ml - spam detection, fraud detection, recommendation system, medical image analysis.

## Important Concepts of Machine Learning 
To understand how ML works internally, you need to understand six fundamental terms.

 1. Dataset - A dataset is the collection of informations that are used to train or evaluate a
 machine learning system.

 2. Features - Features are the input variables used by Machine Learning system to make predictions. e.g - marks, study hours, attendence.

 3. Labels - A label is the output or target value that a Machine Learning system is trained to predict.

 4. Algorithm - An algorithm is a mathematical procedure or method used to learn patterns from data.

 Different algorithms solve different types of problems.

Examples:
Algorithm               	Common purpose
Linear Regression   	Predict numerical values
Logistic Regression	    Classification
Decision Tree       	Classification and regression
Random Forest       	Classification and regression
K-Nearest Neighbors (KNN)    Classification and regression
K-Means                     	Clustering
Support Vector Machine (SVM)	Classification and regression

5. Model - A model is the result obtained after applying that learning procedure to training data.

For example:
- Algorithm: Linear Regression.
- Training data: Historical house prices.
- Trained model: A learned mathematical relationship between house area and price.
The trained model can then make predictions on new information.

6. Parameters ()- Parameters are the internal values learned by a model during training.

Consider this equation:
y = mx + c

Where:
- x = House area.
- y = Predicted house price.
- m = Slope.
- c = Intercept.
The model learns suitable values for m and c from the training data.

For our simplified example: y = 0.02x + 0

### Complete Machine Learning WorkFlow 
Machine Learning pipeline
1. Data Collection--  Collect information about students, attendance, study hours, and previous marks.
2. Data Preprocessing-- Remove duplicate records, handle missing values, correct errors, and prepare the data.
3. Feature Selection---  Select relevant inputs such as attendance, study hours, and previous marks.
4. Model Selection-- Choose an appropriate algorithm, such as Logistic Regression or a Decision Tree.
5. Model Training--- Give the algorithm training examples so it can learn patterns.
6. Model Evaluation--  Test how well the model predicts results on data it hasn't trained on.
7. Model Deployment--  Integrate the trained model into an application or API.
8. Prediction---  Give information about a new student and receive a predicted result.

### Training VS Testing 
Should you train the model using all 1,000 records and then test it using those same records?
Generally, no.

Why?
Because the model may simply memorize the training examples rather than learn patterns that work on new examples.

To evaluate whether it can generalize, we separate the dataset into two parts.

Training data: Used to teach the model.
Testing data: Used to evaluate the trained model on unseen examples.
 And Ratio is 80% and 20%.

 Suppose the model predicts:
- 190 correct results.
- 10 incorrect results.
Then:

Accuracy = correct prediction/total prediction *100;

### What is Valid Data
A separate subset of data used to evaluate a model's performance during development, specifically for tuning hyperparameters and preventing overfitting.

Example split:
- 70% training.
- 15% validation.
- 15% testing.

## Training vs Inference
Training is the process in which a learning algorithm uses data to learn the model's parameters.

Inference means using an already-trained model to generate predictions on new inputs.

## Overfitting and Underfitting
## Overfitting
Overfitting happens when a model learns the training data too closely, including noise and irrelevant details.
It performs very well on training data but poorly on new data.

Example:
A student memorizes the exact answers to previous examination papers but cannot solve new questions.

## Underfitting
Underfitting happens when a model is too simple or has not learned enough to capture important patterns.
It performs poorly on both training and testing data.

Example:
A student does not understand the fundamental concepts and cannot solve either familiar or unfamiliar questions.

## Good Fit
A good fit in machine learning is a balanced model state where the algorithm accurately captures the true underlying patterns in the training data without memorizing noise or random quirks

### Three major types of Machine Learning
1. Supervised Learning 
2. Unsupervised Learning
3. Reinforcement Learning

1. Supervised Learning 
Supervised Learning is a type of Machine Learning in which a model learns from labeled training data.

Two major types of Supervised Learning
A. Regression - Regression is used when we want to predict a continuous numerical value.

B. Classification - Classification is used when we want to predict a category or class.
eg- spam/Not spam, pass/fail


2. Unsupervised Learning
Unsupervised Learning is a type of Machine Learning in which an algorithm learns patterns or structures from unlabeled data.
Here, the data does not contain predefined correct answers.

Major types of Unsupervised Learning

A. Clustering
Groups similar data points together
The algorithm might discover:
- Group 1: Customers who frequently purchase expensive products.
- Group 2: Customers who purchase occasionally.
- Group 3: Customers who mostly purchase discounted products.

Examples:
- Customer segmentation.
- Grouping similar documents.
- Grouping news articles by topic.
Popular algorithm: K-Means.


B. Association
Discovers relationships between different items in a dataset.

Example:
A supermarket analyzes purchasing patterns and discovers:
Customers who purchase bread frequently also purchase butter
This is called Market Basket Analysis.
Popular algorithm: Apriori.

C. Dimensionality reduction 
Reduces the number of input variables while preserving important information.
Suppose you have a dataset with 100 features.
You want to represent the important information using fewer dimensions.
Popular algorithm: PCA (Principal Component Analysis).

3. Reinforcement Learning
 Reinforcement Learning is a type of Machine Learning in which an agent learns by interacting with an environment and receiving rewards or penalties for its actions.
 The cycle repeats as the agent interacts with its environment.

Real-world applications
- Game-playing AI.
- Robot navigation.
- Traffic signal optimization.
- Resource allocation.
- Certain autonomous control systems.

An important concept in Reinforcement Learning is the balance between:
- Exploration: Trying new actions to discover better strategies.
- Exploitation: Using actions already known to produce good rewards.
For example, a robot might already know a route that gives a reward of 5. It can either continue using that route or explore another route that might give a reward of 10.

This is called the exploration-exploitation trade-off.


Feature                 	Supervised	           Unsupervised	            Reinforcement
Training data           	Labeled	                Unlabeled	            Interaction experience
Correct answers provided?      	Yes                 	No                  	Rewards/penalties
Main objective	            Predict outputs     	Discover patterns       	Learn actions
Common task	                Classification	            Clustering	            Decision-making
Example	                    Spam detection	        Customer grouping	        Robot navigation
Algorithms	       Linear Regression, Decision Tree    	K-Means, PCA	        Q-Learning

### Summary of ML
These are the most important points to retain.
1. Machine Learning is a subset of Artificial Intelligence.
2. ML learns patterns from data.
3. Dataset is a collection of examples.
4. Features are input variables.
5. Labels are expected outputs in supervised learning.
6. An algorithm learns patterns.
7. A model is the result of training.
8. Parameters are values learned by the model.
9. Training means learning from data.
10. Inference means generating predictions using a trained model.
11. Training, validation and testing data have different purposes.
12. Overfitting means learning training data too closely.
13. Underfitting means failing to learn important patterns.
14. Supervised Learning uses labeled data.
15. Unsupervised Learning uses unlabeled data.
16. Reinforcement Learning uses rewards and penalties.


