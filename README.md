
# CodeConclave v2.0

> **Run While you sleep.**

CodeConclave is an AI-native development environment designed to multiply engineering output. It combines a full cloud terminal, intelligent refactoring agents, and a global edge network into a single, cohesive workspace. 

We built this because switching between your IDE, terminal, and AI tools breaks flow. CodeConclave brings them all together—your code never leaves your private VPC, but your capacity to ship scales infinitely.

---

### ⚡ Core Capabilities

- **Cloud Terminal**: A fully persistent bash environment. Install packages, run servers, and deploy instantly without configuring local environments.
- **AI Co-Pilot**: Context-aware code generation that understands your entire file structure, not just the open file.
- **Jupyter Integration**: Native support for `.ipynb` notebooks for data science workflows alongside your web application code.
- **Global Edge**: Low-latency workspace streaming from the nearest edge node.

### 🛠️ Architecture

Built with a modern stack designed for performance and security:
- **Frontend**: React + Vite for sub-millisecond interaction.
- **Editor**: Custom implementation of Monaco Editor (VS Code core).
- **Styling**: Styled-components for themeable, component-scoped CSS.
- **Backend**: Node.js microservices handling auth, file systems, and LLM orchestration.
- **Infrastructure**: Dockerized containers orchestrated for isolation and security.

### 🚀 Running Locally

#### Prerequisites
- **Node.js** v16 or higher
- **npm** (comes with Node.js)

#### Steps

1. **Fork and clone the repository**
   ```bash
   git clone https://github.com/<your-username>/CodeConclave.git
   cd CodeConclave
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment setup**
   Copy `.env.example` to `.env` and fill in the required values:
   ```bash
   cp .env.example .env
   ```
   At minimum you will need:
   - `VITE_API_URL` — backend API base URL
   - `JWT_SECRET` — secret for signing JWT tokens
   - `MONGODB_URI` — MongoDB connection string

4. **Start the development server**
   ```bash
   npm run dev
   ```
   The app will be available at `http://localhost:5173`.

#### Available Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start development server with hot reload |
| `npm run build` | Build for production |
| `npm run preview` | Preview the production build locally |
| `npm test` | Run unit tests with Vitest |
| `npm run lint` | Run ESLint |

> **Before pushing**: always run `npm run build` to verify the build succeeds.

---

### 🔒 Security Code

Your code integrity is paramount.
- **Zero-Knowledge**: We don't train on your private repos.
- **VPC Isolation**: Each workspace runs in an isolated container.

---

### Contributing

We are open-source at heart. If you want to improve the terminal emulation or add new AI agents:
1. Fork the repo.
2. Create a feature branch (`git checkout -b feature/amazing-agent`).
3. Commit your changes.
4. Open a generic Pull Request.

### License

MIT © 2024 CodeConclave. Created by Mohak.
