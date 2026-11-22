# AgriVibe

## Requirements

- Python 3.12 and [uv](https://docs.astral.sh/uv/)
- Docker with Compose v2
- OpenAI and Pinecone API keys
- Copernicus Data Space OAuth client credentials

## Run locally

```bash
cd fieldsat
uv sync
cp .env.example .env
uv run fieldsat --transport http --port 8001
```

```bash
cd backend
uv sync
cp .env.example .env
uv run fastapi dev
```

```bash
cd frontend
uv sync
cp .env.example .env
AGRIVIBE_BACKEND_MODE=lesson2 uv run python app.py
```

## Run with Docker Compose

```bash
cp .env.example .env
docker compose up -d --build
```

The app runs at http://localhost:7860.

## Tests

```bash
cd backend && uv run pytest
cd frontend && uv run pytest
cd fieldsat && uv run pytest
```
