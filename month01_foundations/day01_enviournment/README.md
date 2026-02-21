# Day 01 — Python Environment & Reproducibility

## Objective
Set up isolated Python environment for AI development.

## Concepts Learned
- Virtual environments
- Dependency locking
- Reproducibility
- pip freeze

## Commands Used

```bash
python3 -m venv venv
source venv/bin/activate
pip install numpy pandas
pip freeze > requirements.txt
