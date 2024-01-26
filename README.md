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


## Deploying on GCP

1. Create a [GCP account](https://console.cloud.google.com/freetrial/signup/tos?_ga=2.25841725.1677013893.1627213171-706917375.1627193643&_gac=1.124122488.1627227734.Cj0KCQjwl_SHBhCQARIsAFIFRVVUZFV7wUg-DVxSlsnlIwSGWxib-owC-s9k6rjWVaF4y7kp1aUv5eQaAj2kEALw_wcB).
2. Create a [Project on GCP](https://cloud.google.com/appengine/docs/standard/nodejs/building-app/creating-project) (Keep note of the project id).
3. Create a [GCP bucket](https://console.cloud.google.com/storage/browser/).
4. Upload the potatoes.h5 model in the bucket in the path `models/potatos.h5`.
5. Install Google Cloud SDK ([Setup instructions](https://cloud.google.com/sdk/docs/quickstarts)).
6. Authenticate with Google Cloud SDK.

```bash
gcloud auth login
```

7. Run the deployment script.

```bash
cd gcp
gcloud functions deploy predict --runtime python38 --trigger-http --memory 1024 --docker-registry=artifact-registry --project eastern-cosmos-412414
```

8. Your model is now deployed.
9. Use Postman to test the GCF using the [Trigger URL](https://cloud.google.com/functions/docs/calling/http).

Inspiration: https://cloud.google.com/blog/products/ai-machine-learning/how-to-serve-deep-learning-models-using-tensorflow-2-0-with-cloud-functions snippet : https://github.com/codebasics/potato-disease-classification
