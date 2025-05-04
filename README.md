# GOLLA-SAIRAM-Deep-Learning-Based-Detection-of-Intracranial-Neoplasms

Brain Tumor Detection Project
Overview
This project, BrainTumor_Flask, aims to detect brain tumors from MRI images using a deep learning model built with TensorFlow and Keras. The dataset used is brain_tumor_dataset, which contains images labeled as yes (tumor present) and no (no tumor). The project includes a Jupyter notebook (EnhanceBrainTumor.ipynb) for model training and a Flask application for deployment.
Prerequisites
Before running the project, ensure you have the following installed:

Python 3.10.12
pip (Python package manager)
Virtualenv (for creating isolated Python environments)

Installation
Follow these steps to set up the project environment:

Clone the repository or extract the project files:If the project is in a repository, clone it. Otherwise, ensure you have extracted the project files (e.g., from archive.zip) into a directory, such as major-project.

Navigate to the project directory:Open a terminal and change to the project directory:
cd /path/to/major-project


Create a virtual environment:Create a virtual environment named venv:
python3 -m venv venv


Activate the virtual environment:

On macOS/Linux:source venv/bin/activate


On Windows:venv\Scripts\activate




Install dependencies:Install the required Python packages listed in requirements.txt:
pip install -r requirements.txt

If you encounter a pip version warning (e.g., "A new release of pip is available"), update pip:
pip install --upgrade pip



Dataset Preparation
The dataset is stored in the brain_tumor_dataset directory, with subfolders yes and no. The notebook extracts archive.zip into this structure. Ensure the following:

The archive.zip file is in the project directory.
Run the notebook cell that extracts the zip file:import zipfile
z = zipfile.ZipFile('archive.zip')
z.extractall()


Verify the extracted structure: archive/brain_tumor_dataset/{yes, no}.

Running the Project
Step 1: Train the Model

Open the Jupyter Notebook:Start Jupyter Notebook from the terminal (with the virtual environment activated):
jupyter notebook

This will open a browser window. Navigate to EnhanceBrainTumor.ipynb and open it.

Run the Notebook:

Execute the cells in sequence to install dependencies, preprocess the dataset, and train the model.
The notebook uses a VGG-like architecture (model_03) for brain tumor classification.
The training process saves the best model as model.h5.



Step 2: Run the Flask Application

Ensure the model is trained:Confirm that model.h5 exists in the project directory after training.

Run the Flask app:The project includes a Flask app (app.py) for deploying the model. Run the app with:
python app.py


This starts a local server (typically at http://127.0.0.1:5000).
Open a web browser and navigate to the URL to interact with the application.



Project Structure

archive.zip: Compressed dataset file.
brain_tumor_dataset/: Extracted dataset with yes and no subfolders.
EnhanceBrainTumor.ipynb: Jupyter Notebook for model training and evaluation.
app.py: Flask application for model deployment.
requirements.txt: List of Python dependencies.
model.h5: Trained model file (generated after training).
static/, templates/: Flask app assets (CSS, JS, HTML templates).

Additional Notes

Dependencies: The requirements.txt file includes libraries like seaborn, matplotlib, numpy, pandas, opencv-python (cv2), and tensorflow. Ensure they are installed correctly.
Environment: Always activate the virtual environment (venv) before running the notebook or Flask app.
Troubleshooting:
If the notebook fails to find the dataset, verify the path in the notebook matches your directory structure.
If the Flask app fails to load model.h5, ensure the model was saved during training.


Hardware: Training the model may require significant computational resources. If running locally is slow, consider using Google Colab (as noted in the notebook).

License
This project is for educational purposes. Ensure you have the right to use the dataset and libraries as per their respective licenses.
Contact
For issues or questions, please contact the project maintainer (update with your contact information if applicable).

