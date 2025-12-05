# Todo List API

A RESTful API for managing todo items built with FastAPI.

## Features

- Create, read, update, and delete todo items
- Filter todos by completion status
- Automatic OpenAPI documentation
- Data persistence with JSON file storage
- Comprehensive error handling

## Requirements

- Python 3.11+
- FastAPI
- Uvicorn

## Installation

1. Install dependencies:
```bash
pip install -r requirements.txt
```

Or using the project configuration:
```bash
pip install -e ".[test,dev]"
```

## Running the Application

Start the development server:
```bash
python -m todo_api.main
```

Or using uvicorn directly:
```bash
uvicorn todo_api.main:app --reload
```

The API will be available at `http://localhost:8000`

## API Documentation

Once the application is running, visit:
- Swagger UI: `http://localhost:8000/docs`
- ReDoc: `http://localhost:8000/redoc`
- OpenAPI JSON: `http://localhost:8000/openapi.json`

## Configuration

Configure the application using environment variables:

- `STORAGE_PATH`: Path to todos.json file (default: `./data/todos.json`)
- `CORS_ORIGINS`: Comma-separated list of allowed origins (default: `*`)
- `LOG_LEVEL`: Logging level (default: `INFO`)

## Testing

Run tests:
```bash
pytest
```

Run with coverage:
```bash
pytest --cov=todo_api
```

## Project Structure

```
todo_api/
├── api/           # API routes and endpoints
├── models/        # Pydantic data models
├── services/      # Business logic
├── repositories/  # Data access layer
├── config.py      # Configuration settings
└── main.py        # Application entry point

tests/
├── unit/          # Unit tests
├── property/      # Property-based tests
└── conftest.py    # Shared fixtures
```

## License

MIT
