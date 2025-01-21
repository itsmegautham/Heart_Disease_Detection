
# Heart Disease Detection Model  

## Project Overview  
This project is a **Heart Disease Detection Model** that predicts whether a person has heart disease based on various medical parameters. The model is built using a **Logistic Regression** algorithm and trained on a dataset containing features such as age, sex, cholesterol levels, and more.  

## Features  
The dataset includes the following features:  
- **age**: Age of the person  
- **sex**: Gender of the person (1 = male, 0 = female)  
- **cp**: Chest pain type  
- **trestbps**: Resting blood pressure (mm Hg)  
- **chol**: Serum cholesterol (mg/dl)  
- **fbs**: Fasting blood sugar (>120 mg/dl)  
- **restecg**: Resting electrocardiographic results  
- **thalach**: Maximum heart rate achieved  
- **exang**: Exercise-induced angina  
- **oldpeak**: ST depression induced by exercise relative to rest  
- **slope**: Slope of the peak exercise ST segment  
- **ca**: Number of major vessels colored by fluoroscopy  
- **thal**: Thalassemia status  
- **target**: 1 = presence of heart disease, 0 = absence of heart disease  

## Files in the Project  
- `heart_disease_model.pkl`: Serialized logistic regression model file for predictions.  
- `notebook.ipynb`: Jupyter Notebook containing the code, training process, and detailed comments for understanding the workflow.  
- `data.csv`: Dataset used to train and evaluate the model, including all features listed above.  

## Installation and Setup  
1. Clone the repository or download the project folder.  
2. Install the required dependencies by running:  
   ```bash  
   pip install -r requirements.txt  
   ```  
   *(Include `requirements.txt` in the project folder to list dependencies.)*  
3. Ensure you have Python 3.x and Jupyter Notebook installed in your environment.  

## Usage  
1. Open the Jupyter Notebook (`notebook.ipynb`) to view the code and experiment with the model.  
2. To use the model directly for predictions:  
   ```python  
   import pickle  
   import numpy as np  

   # Load the model  
   with open('heart_disease_model.pkl', 'rb') as file:  
       model = pickle.load(file)  

   # Example input data (replace with actual values)  
   sample_data = np.array([[57, 1, 2, 140, 241, 0, 1, 123, 1, 0.2, 1, 0, 2]])  

   # Predict  
   prediction = model.predict(sample_data)  
   print("Heart Disease Detected" if prediction[0] == 1 else "No Heart Disease Detected")  
   ```  

## Results and Performance  
- The model was trained using a logistic regression algorithm and evaluated for its performance.  
- Performance metrics, including accuracy, are discussed in the Jupyter Notebook.  

## Acknowledgements  
This project was inspired by datasets and resources available for healthcare predictions. Special thanks to the creators of the dataset and open-source tools.  

## Contact  
For any feedback, questions, or collaboration requests, feel free to reach out!  
