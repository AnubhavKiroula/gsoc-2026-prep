# 🔍 Django - Code Exploration Notes

> **Purpose:** Document understanding of Django codebase
> **Last Updated:** [Today's Date]

---

## 📁 Repository Structure

```
django/
├── django/                 # Main source code
│   ├── conf/              # Configuration
│   ├── contrib/           # Contrib modules (admin, auth, etc.)
│   ├── core/              # Core functionality
│   ├── db/                # Database and ORM
│   │   └── models/        # ORM models
│   ├── forms/             # Form handling
│   ├── http/              # HTTP handling
│   ├── middleware/        # Middleware
│   ├── template/          # Template engine
│   ├── urls/              # URL routing
│   ├── utils/             # Utilities
│   └── views/             # Views
├── tests/                  # Test suite
├── docs/                   # Documentation
└── scripts/                # Scripts
```

---

## 🎯 Key Files to Understand

### ORM Core

| Component | Key Files | Purpose |
|-----------|-----------|---------|
| **Models** | `django/db/models/base.py` | Base model class |
| **QuerySet** | `django/db/models/query.py` | Query building |
| **Migrations** | `django/db/migrations/` | Schema migrations |
| **SQL Compiler** | `django/db/models/sql/` | SQL generation |

### Forms & Validation

| Component | Key Files | Purpose |
|-----------|-----------|---------|
| **Form** | `django/forms/forms.py` | Form handling |
| **Fields** | `django/forms/fields.py` | Form fields |
| **Validators** | `django/core/validators.py` | Validation logic |

### Auth

| Component | Key Files | Purpose |
|-----------|-----------|---------|
| **User** | `django/contrib/auth/models.py` | User model |
| **Authentication** | `django/contrib/auth/` | Auth backends |

---

## 🔬 Exploration Notes

### Topic: [Topic Name]

#### Date: [Date]
**What I learned:**
*[Key understanding]*

**Code location:**
```python
# File: path/to/file.py
def example_function():
    pass
```

**Questions remaining:**
1. 

---

### Topic: [Topic Name]

#### Date: [Date]
**What I learned:**
*[Key understanding]*

**Code location:**
```python
# File: path/to/file.py
def example_function():
    pass
```

**Questions remaining:**
1. 

---

## 🧪 Testing Patterns

### Running Tests
```bash
# Run all tests
python tests/runtests.py

# Run specific app tests
python tests/runtests.py auth_tests

# Run with coverage
coverage run tests/runtests.py
```

### Test Patterns
```python
from django.test import TestCase

class MyTestCase(TestCase):
    def test_example(self):
        self.assertTrue(True)
```

---

## 🔧 Common Patterns

### Creating a Model
```python
from django.db import models

class MyModel(models.Model):
    name = models.CharField(max_length=100)
    created_at = models.DateTimeField(auto_now_add=True)
    
    class Meta:
        ordering = ['-created_at']
```

### Creating a Form
```python
from django import forms

class MyForm(forms.Form):
    name = forms.CharField(max_length=100)
    email = forms.EmailField()
```

---

## 📝 TODO: Explore These Areas

| Area | Priority | Status |
|------|----------|--------|
| ORM internals | High | ⬜ |
| QuerySet optimization | High | ⬜ |
| Migration system | High | ⬜ |
| Form validation | Medium | ⬜ |
| Authentication | Medium | ⬜ |

---

## → Next Technical Action

*[Focus on understanding Django ORM internals and query optimization]*

