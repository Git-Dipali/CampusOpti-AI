# 🎓 CampusOpti AI
### Intelligent Campus Timetable & Resource Optimization System

---

## 💡 What is CampusOpti AI?

Imagine a college with multiple departments, hundreds of students, faculty members, classrooms and dozens of subjects.

Creating a timetable that satisfies everyone's requirements is a complex scheduling problem.

A faculty member cannot teach two classes simultaneously. A classroom cannot accommodate multiple batches at the same time. Student batches must attend their required lectures, and faculty workloads must remain within defined limits.

Managing all these constraints manually can be time-consuming and error-prone.

**CampusOpti AI is designed to solve this problem.**

It is an intelligent academic timetable and campus resource optimization system that automates lecture scheduling using three different optimization approaches:

- Greedy Algorithm
- Genetic Algorithm
- Google OR-Tools CP-SAT

The system generates optimized timetables, validates scheduling constraints, identifies unscheduled lectures and compares algorithm performance through an interactive web dashboard.

**The main goal is simple: Schedule more lectures, avoid conflicts and use campus resources efficiently.**

---

## 🚀 Why CampusOpti AI?

Traditional timetable preparation involves manually assigning lectures, faculty members, classrooms and time slots.

This creates several challenges:

| Traditional Challenges | CampusOpti AI Solution |
|---|---|
| Manual timetable preparation | Automated timetable generation |
| Faculty scheduling conflicts | Faculty clash validation |
| Classroom overlapping | Room allocation validation |
| Batch timetable conflicts | Batch-wise conflict checking |
| Complex workload management | Faculty workload constraints |
| Difficult performance comparison | Algorithm comparison dashboard |
| Hidden scheduling failures | Unscheduled lecture analysis |

---

## ✨ Key Features

### 1. Intelligent Timetable Generation

- Automatically schedules academic lectures.
- Assigns available time slots to lecture tasks.
- Supports multiple batches and faculty members.
- Allocates classrooms according to room compatibility.
- Generates structured timetable records.

### 2. Three Optimization Approaches

CampusOpti AI implements and compares three different approaches to timetable optimization.

**A. Greedy Algorithm**

A rule-based scheduling approach that assigns lectures to available slots based on scheduling priorities.

- Fast initial timetable generation.
- Checks available scheduling resources.
- Provides a baseline for comparison.

**B. Genetic Algorithm**

A population-based optimization technique inspired by natural evolution.

- Generates candidate timetable solutions.
- Uses selection, crossover and mutation.
- Evaluates timetable fitness.
- Validates scheduling constraints.

**C. Google OR-Tools CP-SAT**

A constraint programming optimization approach that models scheduling requirements mathematically.

- Represents lecture assignments as decision variables.
- Applies academic scheduling constraints.
- Maximizes the number of scheduled lectures.
- Identifies lectures that cannot be scheduled under current constraints.

### 3. Constraint Validation

The system checks important academic scheduling requirements:

- No batch scheduling clashes.
- No faculty scheduling clashes.
- No classroom scheduling clashes.
- Faculty availability restrictions.
- Classroom compatibility and capacity.
- Maximum daily faculty workload.
- Required weekly lectures for each subject.

### 4. Unscheduled Lecture Analysis

Instead of silently ignoring lectures that cannot be allocated, CampusOpti AI identifies unscheduled requirements and explains the reason.

For example, if a faculty member requires 18 lectures per week but can teach a maximum of 3 lectures per day over 5 working days, the weekly capacity is only 15 lectures.

The system identifies the remaining 3 lectures as unscheduled.

### 5. Interactive Web Dashboard

A web-based dashboard provides a centralized view of timetable optimization results.

| Dashboard Section | What It Shows |
|---|---|
| Performance Overview | Key scheduling statistics |
| Algorithm Performance | Algorithm comparison tables and charts |
| Optimised Timetable | Scheduled lectures, filters and CSV export |
| Unscheduled Lecture Analysis | Unscheduled lectures and explanations |
| Campus Resources | Faculty and classroom information |

---

## 📊 Project Results

CampusOpti AI was tested using an academic scheduling dataset containing 142 lecture requirements.

<details>
<summary><b>View Dataset Overview</b></summary>

| Parameter | Count |
|---|---:|
| Required Lectures | 142 |
| Available Weekly Time Slots | 30 |
| Faculty Members | 20 |
| Classrooms | 14 |
| Student Batches | 8 |

</details>

### Overall Optimization Results

<p align="center">
  <img src="https://img.shields.io/badge/Lectures_Scheduled-139-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Scheduling_Success-97.89%25-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Unscheduled-3-orange?style=for-the-badge" />
</p>

| Performance Metric | Result |
|---|---:|
| Total Required Lectures | 142 |
| Scheduled Lectures | 139 |
| Unscheduled Lectures | 3 |
| Scheduling Success | 97.89% |
| Room Utilisation | 33.1% |

### Algorithm Comparison

| Algorithm | Scheduled | Unscheduled |
|---|---:|---:|
| Greedy Algorithm | 139 | 3 |
| Genetic Algorithm | 139 | 3 |
| OR-Tools CP-SAT | 139 | 3 |

All three algorithms scheduled 139 out of 142 required lectures in the tested dataset.

The CP-SAT solver returned an **OPTIMAL** status for its configured model. This means the solver proved optimality for the objective and constraints supplied to it; it does not mean every required lecture was scheduled.

### An Example of Constraint-Based Analysis

The system identified the following unscheduled requirement:

| Parameter | Value |
|---|---|
| Batch | B004 |
| Subject | Operating Systems |
| Faculty | F008 |
| Required Weekly Lectures | 18 |
| Maximum Daily Workload | 3 |
| Working Days | 5 |
| Maximum Weekly Capacity | 15 |
| Unscheduled Lectures | 3 |

This demonstrates how CampusOpti AI can identify scheduling limitations and provide understandable explanations.

---

## 🖥️ Dashboard Preview

The CampusOpti AI dashboard provides an interactive interface for viewing scheduling results and campus resources.

**Recommended screenshots to add:**

1. Performance Overview
2. Algorithm Performance
3. Optimised Timetable
4. Unscheduled Lecture Analysis
5. Campus Resources

To display your screenshots here, create a folder named `screenshots` in the repository and upload your dashboard images.

Then add:

```markdown
![CampusOpti AI Dashboard](screenshots/dashboard.png)
```

---

## 🏗️ How Does It Work?

The system follows a structured optimization workflow.

```text
             INPUT DATA
                 |
                 v
       DATA PREPROCESSING
                 |
                 v
        LECTURE TASK CREATION
                 |
                 v
       OPTIMIZATION ENGINE
                 |
       +---------+---------+
       |         |         |
       v         v         v
     Greedy   Genetic   OR-Tools
   Algorithm  Algorithm  CP-SAT
       |         |         |
       +---------+---------+
                 |
                 v
       CONSTRAINT VALIDATION
                 |
                 v
        OPTIMIZED TIMETABLE
                 |
          +------+------+
          |             |
          v             v
     Scheduled      Unscheduled
      Lectures        Analysis
          |             |
          +------+------+
                 |
                 v
          FASTAPI BACKEND
                 |
                 v
       INTERACTIVE DASHBOARD
```

### System Architecture

**Frontend:** Displays timetable data, statistics, filters, charts and resource information.

**Backend:** FastAPI provides APIs to retrieve optimization results and dashboard data.

**Optimization Engine:** Greedy, Genetic Algorithm and OR-Tools CP-SAT generate and evaluate timetable solutions.

**Dataset and Reports:** CSV files store academic input data, generated schedules and algorithm comparison results.

---

## 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Backend | FastAPI |
| Optimization Solver | Google OR-Tools CP-SAT |
| Algorithms | Greedy, Genetic Algorithm |
| Data Processing | Pandas, NumPy |
| Frontend | HTML, CSS, JavaScript |
| Data Visualization | Plotly.js |
| Data Storage | CSV |
| API Documentation | Swagger UI |
| Development Tools | Anaconda, Jupyter Notebook, VS Code |
| Version Control | Git, GitHub |

---

## 📂 Project Structure

```text
CampusOpti-AI/
│
├── backend/
│   └── main.py
│
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── dataset/
│   ├── faculty.csv
│   ├── classrooms.csv
│   └── student_batches.csv
│
├── reports/
│   ├── cp_sat_timetable.csv
│   ├── algorithm_comparison.csv
│   ├── greedy_timetable_revised.csv
│   └── genetic_algorithm_timetable.csv
│
├── notebooks/
│   └── Optimization experiments
│
├── requirements.txt
├── .gitignore
└── README.md
```

*The structure above illustrates the main project components. File and folder names should match the actual repository.*

---

## ⚙️ Installation and Setup

Follow these instructions to run CampusOpti AI locally.

### Prerequisites

- Python 3.10 or later
- Anaconda or Python environment
- Git
- pip

### 1. Clone the Repository

```bash
git clone https://github.com/Mangesh-7683/CampusOpti-AI.git
```

### 2. Navigate to the Project

```bash
cd CampusOpti-AI
```

### 3. Create and Activate the Environment

```bash
conda create -n campusopti python=3.11
conda activate campusopti
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Start the Backend

If the project contains `backend/main.py`:

```bash
uvicorn backend.main:app --reload
```

If `main.py` is directly in the repository root:

```bash
uvicorn main:app --reload
```

### 6. Open the Dashboard

Open your browser and visit:

**Dashboard:** `http://127.0.0.1:8000/app/`

**API Documentation:** `http://127.0.0.1:8000/docs`

Keep the backend server running while using the dashboard.

---

## 🧪 Testing and Validation

The project includes validation checks for:

- Batch clashes.
- Faculty clashes.
- Classroom clashes.
- Faculty availability violations.
- Invalid room assignments.
- Faculty daily workload violations.
- Unscheduled lecture requirements.

The Genetic Algorithm validation reported zero violations across the tested constraints.

The CP-SAT model returned an OPTIMAL solver status for the configured optimization problem.

---

## 🔮 Future Scope

CampusOpti AI can be extended with:

- Multi-department and multi-semester scheduling.
- Real-time database integration.
- Administrator and faculty login.
- Manual timetable editing.
- Dynamic faculty availability updates.
- Automated timetable notifications.
- Advanced room utilization analytics.
- Cloud deployment and public dashboard access.

---

## 🌍 Real-World Applications

The concepts used in CampusOpti AI can be applied to:

- Engineering colleges and universities.
- Schools and academic institutions.
- Faculty workload management.
- Classroom and laboratory allocation.
- Examination scheduling.
- Resource-constrained academic planning.

---

## 👩‍💻 Developer

**DIPALO PATIL**

Third-Year B.Tech – Artificial Intelligence & Data Science

Dr. D. Y. Patil College of Engineering, Akurdi, Pune

Interested in Artificial Intelligence, Machine Learning, Optimization Algorithms and Full-Stack Development.

---

## ⭐ Support the Project

If you find CampusOpti AI interesting or useful:

- Give this repository a ⭐ Star.
- Explore the optimization algorithms.
- Share feedback and suggestions.
- Contribute ideas for future improvements.

<p align="center">
  <b>CampusOpti AI — Making Academic Scheduling Smarter, Faster and More Efficient.</b>
  <br/>
  Built with Python, Optimization Algorithms and Innovation.
</p>
