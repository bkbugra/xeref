# Xeref Project

Xeref is a modular AI platform integrating document crawling, embeddings, multi-agent orchestration, and a web UI. It leverages FastAPI, Supabase, OpenAI, and Docker for scalable deployment.

---

## Project Structure

```
.
├── backend/                 # Backend API and MCP server code
│   ├── app/                # FastAPI app
│   ├── xeref/              # Core backend modules
│   ├── Dockerfile
│   └── requirements.txt
├── frontend/               # Next.js frontend
│   ├── src/
│   ├── package.json
│   └── Dockerfile
├── streamlit_pages/        # Streamlit UI components
├── docker-compose.yml      # Multi-service orchestration
├── .env                    # Environment variables
├── README.md               # Project documentation
└── ...
```

---

## Components

- **Backend API:** FastAPI app exposing REST endpoints.
- **Xeref MCP Server:** Runs as a separate container (`xref-mcp`), provides Model Context Protocol services.
- **Frontend:** Next.js React app.
- **Streamlit UI:** Interactive dashboards and agent interfaces.
- **Database:** PostgreSQL via Docker.

---

## Installation

### Prerequisites

- Docker & Docker Compose
- Git

### Steps

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/xeref.git
cd xeref
```

2. **Configure environment variables**

Copy `.env.example` to `.env` and fill in your API keys and settings:

```bash
cp .env.example .env
```

3. **Build and start all services**

```bash
docker-compose up --build
```

This will start:

- Backend API on [http://localhost:8002](http://localhost:8002)
- MCP Server on [http://localhost:8003](http://localhost:8003)
- Streamlit UI on [http://localhost:8501](http://localhost:8501)

4. **Access the services**

- **Backend API:** `http://localhost:8002`
- **MCP Server:** `http://localhost:8003`
- **Streamlit UI:** `http://localhost:8501`

---

## Running the MCP Server

The MCP server runs in a separate container using the same backend image:

```bash
python mcp_server.py
```

It listens on port **8003** by default.

---

## License

MIT License

---

## Authors

- Your Name
- Contributors
