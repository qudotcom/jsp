# Job Shop Analytics 🏭

I built this tool to visualize and solve the **Job Shop Scheduling Problem (JSP)**. It helps you compare two different approaches side-by-side: an exact solver (Google OR-Tools) vs. a custom Genetic Algorithm.

It's great for seeing how "perfect" solutions differ from "fast" heuristic ones, especially on larger datasets.

## What it does

- **Dual Solving**: Runs a Constraint Programming model and a Genetic Algorithm at the same time.
- **Visuals**: Plots the production schedule on an interactive Gantt chart.
- **Benchmarks**: Comes with the classic FT06 instance and a generator for massive 20×20 problems.

## Quick Start

### Option 1: Run Locally

You'll need Python 3.10+.

**Install dependencies:**
```bash
pip install -r requirements.txt
```

**Run the app:**
```bash
python app.py
```

Open [http://127.0.0.1:5000](http://127.0.0.1:5000) in your browser.

### Option 2: Docker (Recommended)

If you want to deploy this (e.g., to Koyeb or Render), or just keep your machine clean:

**Build:**
```bash
docker build -t jsp-solver .
```

**Run:**
```bash
docker run -p 8000:8000 jsp-solver
```

Open [http://localhost:8000](http://localhost:8000).

## Tech Stack

- **Backend**: Flask & Google OR-Tools
- **Frontend**: Tailwind CSS & Plotly.js
- **Deployment**: Docker & Gunicorn

---

Enjoy breaking the scheduler! 🚀
