**MOC**:: [[1. Python MOC]]
**Tags**:: #python #library
## Definition
FastAPI is a modern, fast (high-performance), web framework for building APIs with Python 3.7+ based on standard Python type hints.
## Components
- **[FastAPI](https://fastapi.tiangolo.com)**: API creation library
- **[Uvicorn](https://www.uvicorn.org)**: Asynchronous web server integrated to FastAPI.
- **[Pydantic](https://pydantic-docs.helpmanual.io)**: Static typing library (runtime typing), useful for request and response bodies.
- **[OpenAPI](https://www.openapis.org)**: Automatically generated documentation accessible from the URI "/docs".
## Code notes
### Hello World
```python
from fastapi import FastAPI


app = FastAPI()


@app.get("/")
async def root():
	return {"message": "Hello World"}


if __name__ == "__main__":
	uvicorn.run("fastapi_code:app")
```
