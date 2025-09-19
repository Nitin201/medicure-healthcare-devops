# Medicure Healthcare DevOps Project

## 📌 Project Overview
Medicure is a healthcare microservice application designed for managing doctor records.  
The project demonstrates **end-to-end DevOps automation** including build, test, deployment, and monitoring.

### Features:
- Spring Boot microservice with Maven
- In-memory H2 database
- REST APIs for CRUD operations on doctors
- JUnit & TestNG test cases with HTML reports
- CI/CD pipeline with Jenkins
- Containerization with Docker
- Infrastructure automation with Terraform & Ansible
- Deployment on Kubernetes clusters
- Automated UI testing with Selenium
- Monitoring with Prometheus & Grafana

---

## 🚀 Tech Stack
- **Backend:** Java, Spring Boot, Maven
- **Database:** H2 (in-memory)
- **CI/CD:** Git, Jenkins, Docker
- **Automation & Infra:** Ansible, Terraform
- **Orchestration:** Kubernetes
- **Testing:** JUnit, TestNG, Selenium
- **Monitoring:** Prometheus, Grafana

---

## 📂 Project Structure
medicure-healthcare-devops/
│── src/ # Spring Boot microservice code
│── pom.xml # Maven build file
│── Dockerfile # Docker image build file
│── Jenkinsfile # CI/CD pipeline
│── ansible/ # Ansible playbooks
│── terraform/ # Terraform infrastructure scripts
│── k8s/ # Kubernetes manifests
│── tests/ # JUnit, TestNG, Selenium tests
│── README.md # Documentation


---

## ⚡ REST API Endpoints

| Endpoint                          | Method  | Description                     |
|-----------------------------------|---------|---------------------------------|
| `/registerDoctor`                 | POST    | Register a new doctor           |
| `/updateDoctor/{doctorRegNo}`     | PUT     | Update doctor details           |
| `/searchDoctor/{doctorName}`      | GET     | Search doctor by name           |
| `/deleteDoctor/{doctorRegNo}`     | DELETE  | Delete doctor by registration # |

📌 Preloaded data is available in the H2 database.  
H2 Console can be accessed at: `http://localhost:8080/h2-console`  

---

## 🔧 Local Setup Instructions

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/<your-username>/medicure-healthcare-devops.git
cd medicure-healthcare-devops
2️⃣ Build the Application
bash
Copy code
mvn clean install
3️⃣ Run the Application
bash
Copy code
mvn spring-boot:run
4️⃣ Access the Application
API Base URL: http://localhost:8080

H2 Console: http://localhost:8080/h2-console

🐳 Docker Setup
Build Docker Image
bash
Copy code
docker build -t medicure-healthcare .
Run Container
bash
Copy code
docker run -p 8080:8080 medicure-healthcare
⚙️ CI/CD Pipeline (Jenkins)
Jenkins pipeline triggers on git push to main branch.

Stages include:

Checkout → Build (Maven) → Test (JUnit/TestNG) → Package (JAR) → Dockerize

Deploy to Kubernetes test cluster → Run Selenium Tests

On success → Deploy to Production Kubernetes cluster

☸️ Kubernetes Deployment
bash
Copy code
kubectl apply -f k8s/
📊 Monitoring Setup
Prometheus: Collects metrics

Grafana: Visualizes dashboards

✅ Testing
Run Unit Tests:

bash
Copy code
mvn test
Generate HTML Reports (TestNG):

bash
Copy code
mvn surefire-report:report
Selenium tests will run automatically in CI/CD pipeline.

👨‍💻 Contributors
Nitin Dodamani (DevOps Engineer)

