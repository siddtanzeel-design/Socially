# Socially

A backend-focused social media application built with Python and FastAPI. Socially provides API endpoints for uploading posts, storing post information, and retrieving a chronological feed.

## Features

- **Post Uploads** — Accept image files and captions through a REST API.
- **Image Hosting** — Integrate ImageKit for image uploads and hosting.
- **Post Storage** — Store post metadata using an asynchronous database connection.
- **Feed API** — Retrieve posts ordered by creation date, newest first.
- **Automatic API Documentation** — Explore and test endpoints through FastAPI's interactive Swagger UI.

## Tech Stack

- **Language:** Python
- **Backend Framework:** FastAPI
- **Database:** SQLite with aiosqlite and SQLAlchemy's asynchronous ORM
- **Image Hosting:** ImageKit
- **Server:** Uvicorn
- **Dependency Management:** uv

## Getting Started

### Prerequisites

- Python 3.14 or a compatible version supported by the project
- [uv](https://docs.astral.sh/uv/)
- An ImageKit account for image hosting

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/YOUR-USERNAME/Socially.git
   cd Socially
   ```

2. Install the project dependencies:

   ```bash
   uv sync
   ```

3. Create a `.env` file in the project root and add the environment variables required by your application.

   ```env
   IMAGEKIT_PRIVATE_KEY=your_private_key
   IMAGEKIT_PUBLIC_KEY=your_public_key
   IMAGEKIT_URL_ENDPOINT=your_url_endpoint
   ```

   Adjust these variable names to match your application's configuration. Never commit your `.env` file or expose private credentials.

### Run the Server

```bash
uv run uvicorn app.app:app --reload
```

The development server will start at `http://127.0.0.1:8000`.

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/upload` | Submit an image and caption |
| `GET` | `/feed` | Retrieve posts in reverse chronological order |

### Interactive API Documentation

Once the server is running, visit:

- Swagger UI: http://127.0.0.1:8000/docs
- ReDoc: http://127.0.0.1:8000/redoc

You can test the available endpoints directly from your browser.

## Project Structure

```text
Socially/
├── app/
│   └── app.py
├── src/
│   └── socially/
├── .env
├── .gitignore
├── pyproject.toml
├── uv.lock
└── README.md
```

*The structure above reflects the current project layout; expand it as additional modules are added.*

## Future Improvements

- User authentication and authorization
- Likes and comments
- Pagination for the feed
- Post deletion and editing
- Input validation and improved error handling
- Automated tests

## License

No license has been specified yet. Add a license if you intend to permit others to use, modify, or distribute this project.
