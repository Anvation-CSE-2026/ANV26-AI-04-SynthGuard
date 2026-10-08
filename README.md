# 🛡️ SynthGuard

**Secure Synthetic Data Generation & Validation**

SynthGuard is an enterprise-grade web application designed to help organizations generate secure, privacy-compliant synthetic data. It allows users to upload datasets, generate synthetic counterparts, and run rigorous statistical tests for privacy, similarity, and machine learning utility.

## ✨ Features

* **📊 Data Profiling:** Automatically analyzes uploaded data for rows, columns, missing values, and duplicates. Supports CSV, XLSX, and JSON formats.


* **⚙️ Synthetic Generation:** Generates synthetic datasets with adjustable noise parameters to prevent exact data copying.


* **🔒 Privacy Validation:** Evaluates privacy risks by checking for exact duplicate rows between the original and synthetic datasets. Includes a "poison pill" attack test to check for data memorization.


* **🎯 Similarity Testing:** Compares the statistical distributions (mean and standard deviation) of the original and synthetic data to ensure the data shape is maintained.


* **📈 Utility Dashboard:** Evaluates the machine learning readiness of the synthetic data by comparing a `RandomForestClassifier` trained on synthetic data versus real data.


* **⬇️ Export Reports:** Download the generated synthetic data (CSV/Excel) and a comprehensive text-based validation report.



## 🛠️ Tech Stack

**Frontend:**

* **Framework:** React 18, Vite, TypeScript.


* **Styling:** Tailwind CSS & PostCSS.


* **Data Visualization:** Recharts.


* **Routing & HTTP:** React Router DOM, Axios.



**Backend & Data Science:**

* **API Framework:** FastAPI, Uvicorn, Pydantic.


* **Data Processing:** Pandas, NumPy.


* **Machine Learning & Stats:** Scikit-learn, SciPy.



## 🚀 Getting Started

### 1. Run the Backend (FastAPI)

The backend provides a high-performance REST API with CORS enabled for frontend communication.

```bash
# Navigate to the backend directory
cd backend

# Install Python dependencies
pip install -r requirements.txt

# Start the FastAPI server
uvicorn main:app --reload

```

### 2. Run the Frontend (React/Vite)

The frontend uses Vite for ultra-fast local development.

```bash
# Navigate to the frontend directory
cd frontend

# Install NPM dependencies
npm install

# Start the development server
npm run dev

```

### 3. (Optional) Run the Standalone Prototype

We also built a rapid-prototype version of the tool entirely in Streamlit.

```bash
pip install streamlit pandas numpy scikit-learn scipy openpyxl
python -m streamlit run app.py

```
