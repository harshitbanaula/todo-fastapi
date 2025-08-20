Got it! Here’s a **simple and clean version of your `README.md`** for your ToDo FastAPI project:

````markdown
# ToDo Application API

A simple **ToDo API** built with **Python**, **FastAPI**, **Pydantic**, and **Tortoise ORM**. Perform CRUD operations and test using **Insomnia**, **curl**, or Swagger UI.

---

## Features
- Add, view, update, and delete ToDo items  
- Data validation with **Pydantic**  
- Database integration with **Tortoise ORM**  
- Async support  
- Test endpoints via **Insomnia** or Swagger UI  

---

## Tech Stack
- Python 3.10+  
- FastAPI  
- Pydantic  
- Tortoise ORM  
- Uvicorn  
- Insomnia / curl / Swagger UI  

---

## Installation

```bash
git clone https://github.com/your-username/todo-fastapi.git
cd todo-fastapi
python -m venv myenv
# Activate virtual environment
# Windows
myenv\Scripts\activate
# Mac/Linux
source myenv/bin/activate
pip install fastapi "uvicorn[standard]" tortoise-orm
````

---

## Project Structure

```
todo-fastapi/
├─ main.py
├─ models.py
├─ routers/todo_router.py
├─ requirements.txt
└─ README.md
```

---

## API Endpoints

| Method | Endpoint    | Description    |
| ------ | ----------- | -------------- |
| GET    | `/api/`     | Get all todos  |
| POST   | `/api/`     | Add a new todo |
| PUT    | `/api/{id}` | Update a todo  |
| DELETE | `/api/{id}` | Delete a todo  |

**POST/PUT Body Example:**

```json
{
  "title": "Buy milk",
  "description": "Get from store"
}
```

---

## Testing API

### Swagger UI

uvicorn main:app --reload

Open: `http://127.0.0.1:8000/docs`

### Insomnia

* Create workspace `ToDo App` → add requests (GET, POST, PUT, DELETE) → send JSON body for POST/PUT → click Send

### curl Examples

curl http://127.0.0.1:8000/api/
curl -X POST http://127.0.0.1:8000/api/ -H "Content-Type: application/json" -d "{\"title\":\"Buy milk\",\"description\":\"Get from store\"}"
curl -X PUT http://127.0.0.1:8000/api/1 -H "Content-Type: application/json" -d "{\"title\":\"Buy bread\"}"
curl -X DELETE http://127.0.0.1:8000/api/1

---

## Run Project

uvicorn main:app --reload

* Server: `http://127.0.0.1:8000`
* Swagger UI: `http://127.0.0.1:8000/docs`

---


