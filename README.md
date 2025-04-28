## 📡 **GitHub Actions CI/CD Pipeline for FastAPI**

This repository demonstrates the implementation of a **CI/CD pipeline** using **GitHub Actions** for a FastAPI application that performs basic mathematical operations (add, subtract, and multiply). 

✅ The pipeline runs API tests on each code push or pull request to ensure application reliability and prevent regressions.

---

## 🚀 **Project Overview**

### 🔹 **Key Features**
- FastAPI backend with endpoints:
  - `GET /add/{num1}/{num2}` – Add two numbers.
  - `GET /subtract/{num1}/{num2}` – Subtract two numbers.
  - `GET /multiply/{num1}/{num2}` – Multiply two numbers.
- Automated API testing using `pytest` and `requests`.
- GitHub Actions for CI/CD to automate the testing pipeline.
- Continuous Integration to ensure smooth development and avoid breaking changes.

---

## 📂 **Project Structure**
```
📦 GitHub-Actions-CI-CD-pipeline
├── 📂 .github
│   └── 📂 workflows
│       └── test.yml        # GitHub Actions workflow file
├── 📂 __pycache__
├── apiserver.py            # FastAPI application with endpoints
├── testAutomation.py       # Basic API tests using requests
├── testAutomationPytest.py # Enhanced API tests with pytest
└── README.md               # Project documentation
```

---

## 🛠️ **Setup and Installation**

### 1️⃣ **Clone the Repository**
```bash
git clone https://github.com/Rakshansharma30/GitHub-Actions-CI-CD-pipeline.git
cd GitHub-Actions-CI-CD-pipeline
```

### 2️⃣ **Create and Activate a Virtual Environment**
```bash
# Create virtual environment
python -m venv venv

# Activate the virtual environment
# Windows
venv\Scripts\activate
```

### 3️⃣ **Install Dependencies**
```bash
pip install -r requirements.txt
```

---

## 🚀 **Run the FastAPI Server**

### **Start the Server Locally**
```bash
python apiserver.py
```

### ✅ **API Endpoints:**
- `http://localhost:8000/add/2/2` → `{"result": 4}`
- `http://localhost:8000/subtract/5/3` → `{"result": 2}`
- `http://localhost:8000/multiply/2/3` → `{"result": 6}`

---

## 🧪 **Run Tests Locally**

### 1️⃣ **Basic Tests using Requests**
```bash
python testAutomation.py
```

### 2️⃣ **Enhanced Tests using Pytest**
```bash
pytest testAutomationPytest.py
```

---

## 🔄 **CI/CD Pipeline with GitHub Actions**

### 📄 **Workflow Configuration (`.github/workflows/test.yml`):**
- **Triggers:**
  - On every push to the `main` branch.
  - On pull requests to the `main` branch.

### 📝 **Pipeline Tasks:**
1. **Checkout Code:** Clones the repository.
2. **Set up Python Environment:** Installs Python and dependencies.
3. **Start FastAPI Server:** Starts the server using `nohup` to keep it running.
4. **Run Tests:** Executes `pytest` to validate API responses.

---

## 🎮 **Running the GitHub Actions Workflow**

### **Push Changes to GitHub**
```bash
git add .
git commit -m "Add API, tests, and GitHub Actions workflow"
git push origin main
```

### ✅ **View Workflow Results**
- Go to your repository → `Actions` tab.
- Select the latest workflow to view the test results and logs.

---

## 🛠️ **Enhancing the Project (Optional)**

### 🔹 **Add Database Support**
- Integrate PostgreSQL or MongoDB for persistence.
- Implement CRUD operations for more complex scenarios.

### 🔹 **Implement Authentication & Security**
- Use OAuth2 or JWT for securing API endpoints.
- Add tests to validate token-based authentication.

### 🔹 **Add Performance & Load Testing**
- Use `locust.io` or `pytest-benchmark` to simulate concurrent users.

---

## 📚 **Troubleshooting**

### ❗️ **Error: Port Already in Use**
If you encounter a `port 8000 already in use` error:
```bash
# Kill the process using the port
lsof -i :8000
kill -9 <PID>
```

---

## 🎯 **Future Enhancements**
- CI/CD pipeline for production deployment.
- Dockerize the application and use Kubernetes for container orchestration.

---

