# Film Junky Union - Sentiment Analysis Project

- [Film Junky Union - Sentiment Analysis Project](#film-junky-union---sentiment-analysis-project)
  - [Project Objective](#project-objective)
  - [Project Structure and Steps](#project-structure-and-steps)
  - [Tools and Techniques Utilized](#tools-and-techniques-utilized)
  - [Specific Results and Outcomes](#specific-results-and-outcomes)
  - [What I Have Learned From This Project (Skills and Competences)](#what-i-have-learned-from-this-project-skills-and-competences)

## Project Objective
The objective of this project was to build a model for Film Junky Union, a community of classic film enthusiasts, to automatically detect negative movie reviews. Using a labeled IMDB dataset, the aim was to train a machine learning model capable of classifying reviews as positive or negative, with a target F1 score of at least **0.85**.

[back to top](#film-junky-union---sentiment-analysis-project)

## Project Structure and Steps
1. **Data Loading and Exploration**  
   - The dataset containing labeled movie reviews was loaded from a `.tsv` file.  
   - An initial analysis was conducted to understand the distribution of positive and negative reviews, as well as to identify any imbalances or anomalies in the data.
   
2. **Data Preprocessing**  
   - The review texts were tokenized and cleaned by removing stop words, punctuation, and performing stemming.
   - The text data was then converted into numerical format, making it suitable for input into machine learning models.
   - Exploratory Data Analysis (EDA) was performed to visualize the class distribution and assess potential challenges in classification.

3. **Model Training and Validation**  
   - Multiple machine learning models were trained and evaluated:
     - **Logistic Regression**: Provided a strong baseline and was effective for text classification.
     - **Gradient Boosting Models**: Explored to capture complex relationships within the data.
   - Models were trained on a subset of the dataset (`train`), and then validated using the remaining `test` set.

4. **Custom Review Classification**  
   - After training, custom movie reviews were written and classified using the trained models.
   - The results were used to test the model’s performance beyond the provided dataset, allowing for a practical evaluation of real-world applicability.

5. **Model Comparison and Optimization**  
   - The models were compared based on F1 scores, and hyperparameters such as `learning_rate` and `max_depth` were fine-tuned to enhance performance.
   - The models were evaluated based on both training speed and prediction accuracy.

[back to top](#film-junky-union---sentiment-analysis-project)

## Tools and Techniques Utilized
- **Python Libraries**: 
  - `pandas` for data manipulation.
  - `scikit-learn` for model training, hyperparameter tuning, and performance evaluation.
- **Text Processing and Embedding**:
  - Tokenization, stemming, and stop-word removal for data preprocessing.
  - Optional exploration of BERT for advanced text embedding, though computational constraints limited its use.
- **Modeling Techniques**:
  - Logistic Regression for baseline classification.
  - Gradient Boosting algorithms to improve prediction accuracy and capture non-linear patterns.
- **Evaluation Metrics**:
  - **F1 Score** as the primary metric for model evaluation, ensuring a balance between precision and recall.
  - Comparison of model performance on both training data and unseen test data to avoid overfitting.

[back to top](#film-junky-union---sentiment-analysis-project)

## Specific Results and Outcomes
**1. Exploratory Data Analysis:**
- The dataset was analyzed for trends, patterns, and anomalies in the movie review text.
- A clear class imbalance was identified, with either positive or negative reviews being overrepresented.

**2. Data Preprocessing and Tokenization:**
- Reviews were preprocessed by tokenizing the text and converting it into vectors suitable for model input.
- Techniques like stop-word removal and stemming were employed to standardize the input text.

**3. Model Training and Performance:**
- Logistic Regression Model: Achieved an F1 score of **0.88** on the test data.
- Gradient Boosting Model: The F1 score was around **0.87**, slightly lower than logistic regression, but it captured more complex patterns in the data.
- Comparative Analysis: Logistic regression performed the best in terms of both accuracy and F1 score on the test set.

**4. Classifying Custom Reviews:**
- New movie reviews were manually written and classified using the trained models.
- The results were compared, demonstrating that the models performed consistently across both training data and new, unseen examples.

**5. Hyperparameter Tuning and Model Selection:**
- Various hyperparameters like `learning_rate` and `max_depth` were optimized using grid search and cross-validation.
- The final selection of models was based on achieving an F1 score of at least **0.85**, which was met by both logistic regression and gradient boosting models.

**6. Key Insights:**
- The imbalance in class distribution was effectively managed to prevent model bias toward the majority class.
- Simple models like logistic regression were found to perform robustly compared to more complex models like gradient boosting for this text classification problem.

[back to top](#film-junky-union---sentiment-analysis-project)

## What I Have Learned From This Project (Skills and Competences)
- **Text Preprocessing and Feature Engineering**:
  - Techniques such as tokenization, stemming, and stop-word removal are crucial for converting raw text into a usable format for model training.
- **Model Training and Performance Evaluation**:
  - Gained experience in training multiple models and optimizing their hyperparameters.
  - Developed a deeper understanding of F1 score as a balanced metric for model performance, especially in cases of class imbalance.
- **BERT for Embeddings**:
  - Applied **BERT** (Bidirectional Encoder Representations from Transformers) to transform text data into embeddings. This provided a robust approach to handle context and semantics in text, enhancing model performance for more accurate sentiment detection.
- **Comparing Models and Techniques**:
  - Understood the trade-offs between simpler models like logistic regression and more complex boosting models in terms of accuracy and computational requirements.
- **Hyperparameter Tuning and Model Optimization**:
  - Improved skills in optimizing model performance through grid search and cross-validation, effectively balancing model accuracy and computational efficiency.

- **Managing Imbalanced Datasets**:
  - Gained insights into handling imbalanced classes, ensuring that the models do not develop biases towards the majority class and achieve reliable results across both positive and negative reviews.

- **Real-World Model Application and Testing**:
  - Practically tested model robustness by classifying custom-written reviews and ensuring that the trained models generalize well to unseen data, thereby validating the model’s performance beyond the original dataset.

[back to top](#film-junky-union---sentiment-analysis-project)