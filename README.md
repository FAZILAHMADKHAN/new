# Task Management App

This is a full-stack task management application built using Next.js for the frontend and Golang (Gin framework) for the backend. The backend also integrates with OpenAI API for additional functionality.

## Features
- Task creation, updating, and deletion
- Fetching tasks from the backend
- Next.js frontend for a seamless UI experience
- Golang backend with Gin framework
- CORS configured for frontend-backend communication
- OpenAI API integration

## Tech Stack
- **Frontend:** Next.js (React)
- **Backend:** Golang (Gin framework)
- **Database:** SQLite (or replace with your choice)
- **API Integration:** OpenAI API

## Getting Started

### Prerequisites
Ensure you have the following installed:
- [Node.js](https://nodejs.org/) and npm
- [Go](https://go.dev/) (latest version)

### Installation

#### 1. Clone the repository
```sh
git clone https://github.com/your-username/task-management-app.git
cd task-management-app
```

#### 2. Setup the backend
```sh
cd backend
# Install dependencies
go mod tidy
# Create a .env file and add your OpenAI API key
cp .env.example .env
# Run the backend
go run main.go
```

#### 3. Setup the frontend
```sh
cd frontend
# Install dependencies
npm install
# Run the frontend
npm run dev
```

### Environment Variables
Ensure you create a `.env` file in the backend with the following:
```
OPENAI_API_KEY=your-api-key
```

## API Endpoints

| Method | Endpoint | Description |
|--------|---------|-------------|
| GET    | `/api/tasks` | Fetch all tasks |
| POST   | `/api/tasks` | Create a new task |
| PUT    | `/api/tasks/:id` | Update a task |
| DELETE | `/api/tasks/:id` | Delete a task |

## Troubleshooting
- **CORS Issues?** Ensure the backend CORS settings allow `http://localhost:3000`
- **Server Not Responding?** Make sure the backend is running on port `3001`.
- **Port Conflict?** Change the port in `main.go` or use `lsof -i :3001` to check.

## Contributing
Feel free to fork this repository and submit pull requests.

## License
MIT License

