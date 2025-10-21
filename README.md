# Human-Activity-Recognition
Importing Libraries: The code begins by importing essential Python libraries: numpy for numerical operations and pandas for data manipulation and analysis, which are fundamental for handling the dataset.

Loading Feature Names: It reads the features.txt file, which contains the names of the 561 calculated features, and stores them in a list for use as column headers.

Handling Duplicate Features: A crucial data preparation step where it identifies and makes duplicate feature names unique by appending a numerical suffix (e.g., _1, _2) to avoid errors during model training.

Loading Training Data: The main training dataset (X_train.txt) is loaded into a Pandas DataFrame, using the cleaned feature names as column headers for structured data handling.

Adding Subject Information: A column for the subject ID (the person who performed the activity) is merged into the training DataFrame from the subject_train.txt file.

Loading and Mapping Activity Labels: The activity codes (y_train.txt) are loaded and then mapped from numbers (1-6) to descriptive string labels (e.g., 1 becomes 'WALKING') for better interpretability.

Creating a Consolidated Training Set: All the components—sensor features, subject ID, activity code, and activity name—are combined into a single, comprehensive training DataFrame called train.

Repeating the Process for Test Data: The exact same procedure for loading data, adding subjects, mapping activities, and creating a consolidated DataFrame is repeated for the test dataset (X_test.txt, subject_test.txt, y_test.txt), resulting in the test DataFrame.

Initial Data Quality Checks: The code performs basic data cleaning checks by printing the number of duplicate rows and the total number of missing (NaN) values in both the training and test sets.

Visualization Setup: It imports matplotlib.pyplot and seaborn for data visualization and sets a style (whitegrid) and font for the plots to ensure they are clear and aesthetically consistent.

Visualizing Data per Subject: A count plot is generated to show how many data samples each subject provided, broken down by the type of activity, helping to identify if data collection was balanced across participants.

Visualizing Overall Activity Distribution: Another count plot visualizes the total number of data points available for each activity type, which is vital for checking if the dataset is balanced across different activities.

Cleaning Column Names: To make the feature names more programmer-friendly and compatible with various machine learning libraries, it removes parentheses (), dashes -, and commas , from all column names in both DataFrames.

Saving Processed Datasets: Finally, the fully processed and cleaned training and test DataFrames are saved as new CSV files (train.csv and test.csv), creating a clean, ready-to-use dataset for the next stage: building and training the machine learning model.

