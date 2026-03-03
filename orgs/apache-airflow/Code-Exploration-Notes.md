# 🔍 Apache Airflow - Code Exploration Notes

> **Purpose:** Document understanding of Airflow codebase
> **Last Updated:** [Today's Date]

---

## 📁 Repository Structure

```
airflow/
├── airflow/                 # Main source code
│   ├── api/                # REST API
│   ├── cli/                # Command line interface
│   ├── config_templates/   # Configuration templates
│   ├── contrib/            # Contrib modules
│   ├── core/               # Core components (DAGs, operators)
│   ├── decorators/         # Python decorators
│   ├── executors/          # Executor implementations
│   ├── hooks/              # Hook implementations
│   ├── jobs/               # Background jobs (scheduler, etc.)
│   ├── models/             # Database models
│   ├── operators/          # Built-in operators
│   ├── providers/          # Provider packages
│   ├── secrets/            # Secrets backend
│   ├── sensors/            # Sensor operators
│   ├── serialization/     # DAG serialization
│   ├── ti_deps/            # Task instance dependencies
│   ├── utils/              # Utility functions
│   └── www/                # Web UI
├── breeze/                 # Breeze development environment
├── docs/                   # Documentation
├── tests/                  # Test files
└── scripts/                # Scripts and tools
```

---

## 🎯 Key Files to Understand

### Core Components

| Component | Key Files | Purpose |
|-----------|-----------|---------|
| **DAG Execution** | `airflow/models/dag.py` | DAG model and scheduling |
| **Task Instance** | `airflow/models/taskinstance.py` | Task execution state |
| **Scheduler** | `airflow/jobs/scheduler_job.py` | Task scheduling logic |
| **Executor** | `airflow/executors/base_executor.py` | Base executor interface |
| **Web Server** | `airflow/www/` | UI components |

### Database Models

| Model | File | Description |
|-------|------|-------------|
| DAG | `airflow/models/dag.py` | Workflow definition |
| TaskInstance | `airflow/models/taskinstance.py` | Task execution |
| DagRun | `airflow/models/dagrun.py` | DAG run instance |
| SerializedDAG | `airflow/models/serialized_dag.py` | Serialized DAG storage |

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

### Unit Tests
```python
# Example test pattern
import pytest

def test_example():
    assert True
```

### Integration Tests
```python
# Example integration test
def test_integration():
    pass
```

---

## 🔧 Common Patterns

### Creating an Operator
```python
from airflow.models.baseoperator import BaseOperator

class MyOperator(BaseOperator):
    def execute(self, context):
        # Operator logic
        pass
```

### Creating a Hook
```python
from airflow.hooks.base import BaseHook

class MyHook(BaseHook):
    def get_conn(self):
        # Connection logic
        pass
```

---

## 📝 TODO: Explore These Areas

| Area | Priority | Status |
|------|----------|--------|
| DAG serialization | High | ⬜ |
| Task execution flow | High | ⬜ |
| Scheduler internals | High | ⬜ |
| XCom mechanism | Medium | ⬜ |
| Provider mechanism | Medium | ⬜ |
| API endpoints | Medium | ⬜ |

---

## → Next Technical Action

*[Focus on understanding the scheduler and DAG execution flow]*

