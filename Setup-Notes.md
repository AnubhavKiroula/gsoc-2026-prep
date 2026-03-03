# 💻 Development Setup Notes

> **Purpose:** Document all setup steps for quick reproducibility
> **Last Updated:** [Today's Date]

---

## 🖥️ System Information

| Component | Details |
|-----------|---------|
| OS | Windows 11 |
| Shell | Command Prompt / PowerShell |
| Python Version | [Your Python Version] |
| Git Version | [Your Git Version] |
| IDE | VSCode |

---

## 📦 Common Tools Installation

### Required Tools
- [ ] Git
- [ ] Python (3.9+ recommended)
- [ ] Docker Desktop
- [ ] VSCode with Extensions

### VSCode Extensions
- [ ] Python
- [ ] Pylance
- [ ] Docker
- [ ] GitLens
- [ ] Markdown All in One
- [ ] Prettier

---

## 🐍 Apache Airflow Setup

### Prerequisites
```bash
# Install Docker Desktop
# Install WSL2 (for Windows)
```

### Clone Repository
```bash
git clone https://github.com/apache/airflow.git
cd airflow
```

### Using Breeze (Recommended)
```bash
# Install Breeze
pip install apache-airflow-breeze

# Start Breeze environment
breeze start-airflow

# Enter Breeze shell
breeze shell
```

### Local Development Setup
```bash
# Create virtual environment
python -m venv venv
venv\Scripts\activate

# Install dependencies
pip install -e ".[devel]"

# Set up database
airflow db init

# Create admin user
airflow users create -r Admin -u admin -e admin@airflow.com -f Admin -l User
```

### Running Tests
```bash
# Run specific test
python -m pytest tests/test_example.py -v

# Run with coverage
pytest --cov=airflow tests/
```

### Known Issues & Solutions
| Issue | Solution |
|-------|----------|
| | |

---

## 🦄 Django Setup

### Prerequisites
- Python 3.9+

### Clone Repository
```bash
git clone https://github.com/django/django.git
cd django
```

### Local Development Setup
```bash
# Create virtual environment
python -m venv venv
venv\Scripts\activate

# Install Django in editable mode
pip install -e .

# Run tests
python tests/runtests.py

# Start development server
python -m django runserver
```

### Running Tests
```bash
# Run all tests
python tests/runtests.py

# Run specific test
python tests/runtests.py auth_tests.test_views
```

### Known Issues & Solutions
| Issue | Solution |
|-------|----------|
| | |

---

## 🐘 PostgreSQL Setup

### Prerequisites
- C compiler (gcc/clang)
- Make

### Clone Repository
```bash
git clone https://github.com/postgres/postgres.git
cd postgres
```

### Building from Source
```bash
# Configure
./configure

# Build
make

# Install
make install

# Initialize database
initdb -D /path/to/data

# Start server
pg_ctl -D /path/to/data -l logfile start
```

### Setting up for Development
```bash
# Create regression test database
make installcheck
```

### Known Issues & Solutions
| Issue | Solution |
|-------|----------|
| | |

---

## 🔧 Environment Variables

### Airflow
```bash
AIRFLOW_HOME=~/airflow
AIRFLOW__CORE__EXECUTOR=LocalExecutor
```

### Django
```bash
DJANGO_SETTINGS_MODULE=tests.test_sqlite
```

### PostgreSQL
```bash
PATH=$PATH:/usr/local/pgsql/bin
```

---

## 📝 Quick Reference Commands

### Git
```bash
# Fork and clone
git clone https://github.com/YOUR_USERNAME/REPO.git
cd REPO
git remote add upstream https://github.com/ORIGINAL/REPO.git

# Create feature branch
git checkout -b feature/your-feature

# Keep fork updated
git fetch upstream
git merge upstream/main

# Commit changes
git add .
git commit -m "Description"
git push origin feature/your-feature
```

### Python Virtual Environments
```bash
# Create
python -m venv venv

# Activate (Windows)
venv\Scripts\activate

# Activate (Linux/Mac)
source venv/bin/activate

# Install package
pip install -e .
```

---

## → Next Technical Action

*[Set up the primary organization (Apache Airflow) development environment first]*

