# QueryParsing

1. This code is in compliance with a project given by ISRO to maintain an inventory management system using JAVA and MySQL.
2. Query optimization using AI/ML was an added feature for users to access the details of equipments using normakl human language.
3. This project demonstrates the use of BERT embeddings combined with an SVM (Support Vector Machine) model for intent recognition. The process involves preprocessing text data, generating embeddings using a pre-trained BERT model, and training an SVM model to classify the intent of a given query.
4. NumPy and Pandas: Used for data manipulation and handling.
5. scikit-learn's SVM (SVC): Used for training a Support Vector Machine model for intent classification.
6. Transformers Library: BERT tokenizer and model from Hugging Face's transformers library are used to generate embeddings.
7. PyTorch: Used to handle tensor operations required by the BERT model.
8. The code uses a pre-trained BERT model (bert-base-uncased) for generating embeddings of input queries.
9. AutoTokenizer and AutoModel classes are used to load the tokenizer and the BERT model.
10. The preprocess_query() function tokenizes the input text and generates the corresponding embeddings using the BERT model. The function returns the last hidden state of the model, which represents the contextual embeddings.
11. The training data is loaded from an Excel file (Intent_training_data.xlsx), containing columns for the input queries (Intent_Data) and their corresponding labels (Label).
12. The data is then converted into a Pandas DataFrame for easier manipulation.
13. The code generates embeddings for each training query using the BERT model. These embeddings are then averaged to create a single feature vector for each query.
14. The resulting embeddings are used as input features for training the SVM model.
15. An SVM model (SVC with probability=True) is trained using the generated embeddings and their corresponding labels. This model will later be used to predict the intent of new queries.
16. For debugging purposes, the code prints the number of embeddings generated and some example queries along with their labels. This section also includes example data for equipment IDs, equipment names, hardware locations, serial numbers, store reference numbers, and asset IDs, which could be used in further classification tasks.
