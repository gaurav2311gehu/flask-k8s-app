\# Flask Kubernetes App



A simple Flask application deployed using Kubernetes.



\## 🧱 Stack



\- Python Flask

\- Docker

\- Kubernetes

\- NodePort Service



\## 📁 Project Structure



flask-k8s-app/

├── app.py # Flask application code

├── Dockerfile # Dockerfile to build the image

├── requirements.txt # Python dependencies

└── k8s/

├── deployment.yaml # Kubernetes Deployment manifest

└── service.yaml # Kubernetes Service manifest





\## 🐳 Docker Instructions



\### 🔨 Build the Docker image



Push to Docker Hub

docker build -t your-dockerhub-username/flask-k8s-app .

docker push your-dockerhub-username/flask-k8s-app

Deploy to Kubernetes
kubectl apply -f k8s/



Check the pods and services:

kubectl get pods

kubectl get svc



&nbsp;Access the App (Minikube)
minikube service flask-service





