# Udatracker Starter Code

This directory contains the starter code for the Udatracker project. The initial structure of directories and files is described below.

```
.
├── backend
│   ├── __init__.py
│   ├── app.py
│   ├── in_memory_storage.py
│   ├── order_tracker.py
│   ├── requirements.txt
│   └── tests
│       ├── __init__.py
│       ├── test_api.py
│       └── test_order_tracker.py
├── frontend
│   ├── css
│   │   └── style.css
│   ├── index.html
│   └── js
│       └── script.js
├── pytest.ini
└── README.md
```

---

## Project Reflection

- I kept the business logic inside the `OrderTracker` class and used the Flask routes only to process requests, call the appropriate methods, and format JSON responses. This separation made the application easier to test and maintain.

- The test-first workflow helped identify problems early. For example, the tests revealed that invalid statuses and empty order IDs should be rejected before accessing the storage layer. This led to clearer validation and more predictable error handling.

- If I continued the project, I would replace the in-memory storage with persistent database storage. This would prevent orders from being lost when the application restarts. I would also add more API tests for invalid request data, duplicate order IDs, and missing JSON fields.
