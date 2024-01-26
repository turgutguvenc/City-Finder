# City-Finder

### React App
Dependencies:
VS Code (you can use different one but this one is recommended)

Google Chrome (Web browser) to run applications.

Node.js we are not going to use it but some tools we are using running on Node.js Link= https://nodejs.org/en/download (use at least version : 18)

open your command prompt and go to folder whereever you want to create you project then run : $ npm create vite@latest

then give a project name 

then: disease
√ Select a framework: » React
√ Select a variant: » JavaScript
in your terminal:
  cd disease
  npm install
  npm run dev

Python packages:

numpy 1.24.3
OpenCV  4.9.0
tensorflow 2.13.0
pip install -U flask-cors
pip install flask
pip install opencv-python 


Deploying the TF Lite on GCP
Create a GCP account.
Create a Project on GCP (Keep note of the project id).
Create a GCP bucket.
Upload the potatoes.h5 model in the bucket in the path models/potatos.h5.
Install Google Cloud SDK (Setup instructions).
Authenticate with Google Cloud SDK.
gcloud auth login
Run the deployment script.
cd gcp
gcloud functions deploy predict_lite --runtime python38 --trigger-http --memory 512 --project project_id
Your model is now deployed.
Use Postman to test the GCF using the Trigger URL.
Inspiration: https://cloud.google.com/blog/products/ai-machine-learning/how-to-serve-deep-learning-models-using-tensorflow-2-0-with-cloud-functions
