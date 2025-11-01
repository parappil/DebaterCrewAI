# CrewAI Engineering Team

Welcome to the CrewAI Engineering Team project! This is a comprehensive AI-powered software development platform that uses multiple specialized agents to generate complete applications based on user requirements. The system includes a modern React GUI for easy interaction and project management.

## Features

- **Multi-Agent Architecture**: 5 specialized AI agents work together:
  - **Architect**: Designs system architecture and technical specifications
  - **Developer**: Implements application code following best practices
  - **QA Engineer**: Creates comprehensive test plans and test cases
  - **Tester**: Executes tests and validates functionality
  - **Code Validator**: Performs code reviews and ensures quality standards

- **React GUI**: Modern, intuitive web interface for:
  - Inputting project requirements
  - Real-time monitoring of agent interactions
  - Viewing progress and results
  - Downloading generated projects
  - Pushing projects directly to GitHub

- **Project Generation**: Creates complete, runnable applications with:
  - Source code
  - Configuration files
  - Documentation
  - Test suites

- **GitHub Integration**: Direct push to GitHub repositories with customizable settings

## Installation

### Prerequisites
- Python >=3.10 <3.14
- Node.js >=16.0.0
- Git

### Backend Setup

1. Install UV for dependency management:
```bash
pip install uv
```

2. Install Python dependencies:
```bash
uv sync
```

3. Set up environment variables in `.env`:
```bash
GOOGLE_API_KEY=your_google_api_key_here
OPENAI_API_KEY=your_openai_api_key_here
```

### Frontend Setup

1. Install Node.js dependencies:
```bash
cd frontend
npm install
```

2. Build the React application:
```bash
npm run build
```

## Running the Application

### Development Mode

1. Start the backend server:
```bash
uv run start_server
```

2. In another terminal, start the frontend development server:
```bash
cd frontend
npm start
```

The application will be available at `http://localhost:3000` with the backend API at `http://localhost:8000`.

### Production Mode

1. Build the frontend:
```bash
cd frontend
npm run build
```

2. Start the combined server:
```bash
uv run start_server
```

The application will be available at `http://localhost:8000`.

## Usage

1. **Enter Requirements**: Describe your application requirements in the text area
2. **Generate Project**: Click "Generate Project" to start the engineering team
3. **Monitor Progress**: Watch real-time agent interactions and progress updates
4. **Download Project**: Download the complete generated project as a ZIP file
5. **Push to GitHub**: Optionally push the project to a new GitHub repository

## Project Structure

```
crewai-engineering-team/
├── src/
│   └── engineering_team/
│       ├── __init__.py
│       ├── api.py              # FastAPI backend server
│       ├── crew.py             # CrewAI engineering team definition
│       ├── main.py             # CLI interface
│       └── config/
│           ├── agents.yaml     # Agent configurations
│           └── tasks.yaml      # Task definitions
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── App.js
│   │   ├── index.js
│   │   └── components/
│   │       ├── AgentInteractions.js
│   │       ├── ProjectDownloader.js
│   │       └── GitHubPusher.js
│   └── package.json
├── output/                    # Generated projects directory
├── pyproject.toml
├── README.md
└── .env
```

## Configuration

### Agents Configuration
Modify `src/engineering_team/config/agents.yaml` to customize agent behaviors, models, and roles.

### Tasks Configuration
Modify `src/engineering_team/config/tasks.yaml` to adjust the engineering workflow and task definitions.

### Environment Variables
- `GOOGLE_API_KEY`: Your Google AI API key for Gemini models (required)
- `OPENAI_API_KEY`: Your OpenAI API key (required - CrewAI needs this for internal functionality even when using Gemini)
- `OLLAMA_BASE_URL`: Base URL for Ollama (if using local models)
- `GITHUB_TOKEN`: GitHub token for automatic repository creation (optional)

## CLI Commands

- `uv run engineering_team`: Run the engineering team directly
- `uv run start_server`: Start the web server
- `uv run train`: Train the crew
- `uv run test`: Test the crew

## API Endpoints

- `GET /`: Serve the React application
- `POST /api/generate`: Start project generation
- `GET /api/progress`: Get real-time progress updates
- `GET /api/download/{project_id}`: Download generated project
- `POST /api/github/push`: Push project to GitHub

## Support

For support, questions, or feedback:
- Visit the [crewAI documentation](https://docs.crewai.com)
- Check out the [crewAI GitHub repository](https://github.com/joaomdmoura/crewai)
- Join our [Discord community](https://discord.com/invite/X4JWnZnxPb)

## License

This project is built on crewAI. Please refer to crewAI's licensing terms.

Let's build amazing applications together with the power of AI-driven software engineering!
# CrewAIEngeeringTeamVer2
