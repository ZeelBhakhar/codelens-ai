# CodeLens AI

### AI-Powered Code Analysis and Repository Insights

🌐 **Live Demo:** [Try CodeLens AI](https://codelens-ai-mauve.vercel.app/)
💻 **Source Code:** [GitHub Repository](https://github.com/ZeelBhakhar/codelens-ai)

CodeLens AI is a web application designed to help developers analyze source code and GitHub repositories using AI. It provides a centralized workspace for code analysis, repository insights, architecture visualization, and analysis reports.

The project combines a modern Next.js interface with AI-powered analysis to make understanding and reviewing code more convenient.

## Overview

CodeLens AI provides a workspace where developers can analyze code, explore GitHub repositories, visualize software architecture, and access previous analysis results.

## Features

- **Dashboard** — A centralized workspace to access the application's main features and analysis activity.
- **GitHub Repository Analyzer** — Analyze a public GitHub repository using its URL.
- **Code Analyzer** — Submit source code for AI-powered analysis.
- **Architecture Visualization** — View architecture diagrams generated as part of the analysis workflow.
- **Analysis History** — Access saved analysis records stored in the browser's local storage.
- **Reports** — Access the application's report-related functionality and analysis results.
- **Interactive Code Editor** — Code editing experience powered by Monaco Editor.
- **AI Integration** — Uses Google's Gemini API for AI-powered analysis.
- **Modern User Interface** — A dark-themed interface with dedicated pages for the main tools.

## Tech Stack

| Technology | Purpose |
|---|---|
| Next.js | React framework and application routing |
| React | User interface development |
| TypeScript | Type-safe application development |
| Tailwind CSS | Styling and responsive UI |
| Google Gemini API | AI-powered code and repository analysis |
| Monaco Editor | Interactive code editor |
| Mermaid | Architecture diagram visualization |
| React Markdown | Rendering Markdown content |
| jsPDF | PDF generation functionality |
| Lucide React | Icons and interface elements |
| Vercel | Deployment and hosting |

## Application Pages

| Page | Description |
|---|---|
| Dashboard | Main workspace and navigation |
| GitHub Analyzer | Repository analysis using a GitHub URL |
| Code Analyzer | Analysis of submitted source code |
| Architecture | Architecture visualization |
| Analysis History | Previously saved analysis records |
| Reports | Report-related functionality |

## Getting Started

Follow these steps to run CodeLens AI locally.

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) — A version compatible with the project's Next.js dependencies
- npm — Included with Node.js
- [Git](https://git-scm.com/)
- A Google Gemini API key

### 1. Clone the Repository

```bash
git clone https://github.com/ZeelBhakhar/codelens-ai.git
```

### 2. Open the Project Directory

```bash
cd codelens-ai
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Configure Environment Variables

Create a `.env.local` file in the project root directory.

Add your Gemini API key using the exact environment variable name referenced by the application's API routes.

For example, if the source code uses `GEMINI_API_KEY`, configure it as follows:

```env
GEMINI_API_KEY=your_gemini_api_key_here
```

Replace the placeholder with your own API key. Do not commit `.env.local` or expose your API key in client-side code.

You can obtain a Gemini API key through [Google AI Studio](https://aistudio.google.com/).

**Important:** The environment variable name must match the one used in the project source code. The example above applies only if the code reads `GEMINI_API_KEY`.

### 5. Start the Development Server

```bash
npm run dev
```

Open the local URL shown in your terminal, usually:

```text
http://localhost:3000
```

## Environment Configuration for Deployment

CodeLens AI is deployed using Vercel.

To configure the Gemini API key for the deployed application:

1. Open the project in the [Vercel Dashboard](https://vercel.com/dashboard).
2. Navigate to **Settings → Environment Variables**.
3. Add the Gemini API key using the environment variable name expected by the application.
4. Select the appropriate deployment environments.
5. Redeploy the application so the updated variable is available to the deployment.

Never include API keys in your public repository, README, screenshots, or source control history.

## Project Structure

The application uses the Next.js App Router structure.

```text
codelens-ai/
├── app/
│   ├── api/
│   │   ├── analyze/
│   │   │   └── route.ts
│   │   ├── github/
│   │   │   └── route.ts
│   │   ├── ...
│   ├── ...
├── public/
├── package.json
├── package-lock.json
├── next.config.ts
├── tsconfig.json
└── README.md
```

*Note: The structure above is a high-level overview. The exact contents of `app/` may vary as the project evolves.*

## Available Scripts

Run these commands from the project directory:

| Command | Description |
|---|---|
| `npm run dev` | Starts the development server |
| `npm run build` | Builds the application for production |
| `npm run start` | Starts the production server, after a successful build |
| `npm run lint` | Runs the configured lint script, if available in the project |

The availability of individual scripts depends on the current `package.json`.

## Security Notes

- Keep Gemini API credentials private.
- Store secrets in environment variables rather than hardcoding them.
- Do not commit `.env.local` or other files containing secrets.
- Use server-side API routes for operations that require private API credentials.
- Review AI-generated analysis before relying on it for production code or security decisions.

## Limitations

- AI-generated analysis may be incomplete or inaccurate and should be reviewed by a developer.
- Analysis results depend on the submitted code, repository accessibility, API configuration, and the availability of the AI service.
- Repository analysis may be limited by GitHub access restrictions, repository size, or API rate limits.
- Analysis history stored in browser local storage is browser-specific and is not automatically synchronized across devices.

## Future Improvements

Potential areas for future development include:

- More detailed code quality and maintainability insights.
- Additional architecture visualization options.
- Enhanced report customization.
- Expanded analysis history management.
- Support for additional analysis workflows.

These are possible future enhancements and are not claims about currently implemented features.

## Author

**Zeel Bhakhar**

GitHub: [@ZeelBhakhar](https://github.com/ZeelBhakhar)

## Acknowledgements

- [Google Gemini](https://ai.google.dev/) for AI capabilities.
- [Next.js](https://nextjs.org/) for the application framework.
- [Vercel](https://vercel.com/) for deployment and hosting.
- The open-source community for the tools and libraries used in this project.
