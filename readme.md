# AI-Powered Code Reviewer

An AI-powered web application that analyzes source code, identifies issues, and suggests improvements — acting like an automated senior code reviewer. Built with React on the frontend and Node.js/Express on the backend, powered by Google's Gemini AI.

## Features

- 🤖 AI-driven code analysis using Google Gemini
- ✍️ Live code editor with syntax highlighting
- 📄 Markdown-formatted review output for readability
- 🌐 Supports multiple programming languages
- ⚡ Fast, lightweight full-stack architecture

**AI**
- Google Gemini API (`gemini-2.5-flash`)

> Note: This project does not use a database. It is a stateless full-stack application — no user data or review history is persisted.

## How It Works

1. The user writes or pastes code into the React-based code editor.
2. On clicking **Review**, the frontend sends the code to the backend via an API request.
3. The backend forwards the code to the Google Gemini API with a system prompt instructing it to act as a senior code reviewer.
4. Gemini analyzes the code and returns structured feedback covering best practices, performance, security, and readability.
5. The response is rendered in the UI as formatted Markdown with syntax-highlighted code snippets.

## Project Structure

```
Ai-Powered-Code-Reviewer/
├── BackEnd/
│   ├── src/
│   │   ├── controllers/     # Request handlers
│   │   ├── routes/          # API route definitions
│   │   ├── services/        # Gemini AI integration logic
│   ├── server.js            # Express app entry point
│   ├── package.json
│   └── .env                 # Environment variables (not committed)
│
├── Frontend/
│   ├── src/
│   │   ├── components/      # React components
│   │   ├── App.jsx          # Main application UI
│   ├── package.json
│
└── README.md
```

## Environment Variables

| Variable            | Description                          |
|----------------------|--------------------------------------|
| `GOOGLE_GEMINI_KEY`  | Your Google Gemini API key (required) |

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a new branch: `git checkout -b feature-branch`
3. Commit your changes: `git commit -m "Add new feature"`
4. Push to the branch: `git push origin feature-branch`
5. Open a Pull Request