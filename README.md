# Chatgapt

An early chat API exercise using Python and FastAPI. The server stores users, contacts, and conversations in memory. `Client.py` is an unfinished command-line client.

## Run the server locally

Create and activate a Python virtual environment, then run from the repository root:

```bash
python -m pip install fastapi "uvicorn[standard]"
cd server
python -m uvicorn main:app --host 127.0.0.1 --port 8000
```

Open [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs) to inspect the routes.

| Method | Route | Purpose |
| --- | --- | --- |
| POST | `/register` | Create a user |
| POST | `/login` | Check credentials |
| GET | `/get` | Read a user's conversations |
| POST | `/send` | Send a message |
| POST | `/add` | Add a contact |
| POST | `/block` | Add a user to a block list |

## Status

This is a learning project. Accounts and messages disappear when the server restarts. Passwords are stored in plain text, and the routes do not provide complete authorization checks. Use sample data locally.

The client needs fixes to its startup input and several request paths and methods before it can be used end to end. Contact lookup and message handling also need validation for missing users.
