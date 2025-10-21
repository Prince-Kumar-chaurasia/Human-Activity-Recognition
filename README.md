# Human-Activity-Recognition
This project analyzes smartphone sensor data from the UCI HAR Dataset to classify human activities like walking and sitting. It involves preprocessing the data and exploratory analysis to build a model for recognizing movement patterns.
Objective: The project's primary goal is to build a model that can automatically classify human physical activities using data from smartphone sensors.

Data Source: It utilizes the well-known UCI HAR Dataset, a benchmark dataset in the activity recognition field.

Sensor Data: The raw data is collected from the accelerometer and gyroscope of a smartphone, capturing movement and rotation signals.

Feature Engineering: The dataset provides 561 pre-engineered features derived from the raw sensor data, which include statistical measures like mean, standard deviation, and frequency domain components.

Data Loading: The code loads both the training and testing datasets from their respective text files into structured Pandas DataFrames for efficient manipulation.

Data Preprocessing: A key preprocessing step involves making all feature names unique to avoid conflicts during model training, as the original dataset contained duplicate feature names.

Data Integration: The subject identifiers (who performed the activity) and the activity labels (what activity was performed) are merged with the main feature data into a single, cohesive DataFrame for both training and test sets.

Activity Mapping: Numerical activity codes (1-6) are mapped to their descriptive string labels (e.g., WALKING, SITTING, LAYING) to make the data more interpretable.

Data Quality Checks: The project includes essential data cleaning steps, verifying that there are no duplicate rows and no missing (NaN) values in the dataset.

Exploratory Data Analysis (EDA): Initial analysis involves visualizing the distribution of activities across different subjects and the overall dataset to check for potential imbalances or biases.

Class Distribution: A count plot is used to visualize the number of data points for each activity, ensuring a balanced dataset for training a robust model.

Feature Name Cleaning: The code further processes the column names by removing parentheses and other characters to create cleaner, more programmer-friendly feature names.

Data Persistence: The processed and cleaned training and test DataFrames are saved as CSV files, making them readily available for the subsequent machine learning modeling phase.

Foundation for Modeling: All the steps above serve to create a clean, well-structured, and analyzed dataset, forming a solid foundation for training and evaluating various classification algorithms.

Real-world Application: The ultimate application is to recognize and classify human activities, which has uses in fitness tracking, healthcare monitoring, and smart environment systems.

