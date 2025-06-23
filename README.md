# Zap

Zap is a modern AI-powered workflow automation platform that helps you automate tasks and connect your favorite apps and services, streamlining your work and boosting productivity. Whether you're an individual or a team, Zap makes it easy to automate repetitive tasks, trigger actions across multiple tools, and build powerful bots—no coding required.

---

## 🚀 Key Features

- **Free Forever**: Enjoy core automation features at no cost, forever. Perfect for getting started and for simple workflows.
- **Extensive App Integrations**: Connect to more apps and services than most platforms, so you can automate across your tech stack.
- **Cutting Edge AI**: Leverage built-in AI to create smarter, more responsive automations and bots.
- **No-Code Setup**: User-friendly interface lets you build and manage workflows visually—no programming skills needed.
- **14-Day Premium Trial**: Access advanced features and premium integrations for 14 days, risk-free.
- **Fast Onboarding**: Get up and running in minutes with a modern, intuitive UI and clear guides.
- **Secure & Scalable**: Built with security best practices and scalable microservices architecture.
- **Webhooks & Custom Logic**: Trigger workflows via webhooks, and add custom logic for complex automations.
- **Composable Architecture**: Modular services for triggers, actions, and workflow processing.
- **Multi-Stage Automation**: Chain together multiple steps, conditions, and actions in a single workflow.
- **Open Source**: Transparent development enabling customization and community contributions.

---

## 🛠️ Tech Stack

**Frontend**
- [Next.js](https://nextjs.org/) (React-based framework)
- TypeScript for type safety
- Modern CSS (with support for custom fonts like Geist)
- Component-driven architecture

**Backend & Services**
- Node.js (TypeScript)
- Express.js for API and service logic
- Modular services: primary backend, hooks service, processor, and worker
- Prisma ORM for database access and migrations
- Webhooks handling for real-time triggers
- AI features and logic integration

**Database**
- Prisma ORM (compatible with PostgreSQL, MySQL, SQLite, and more)

**DevOps & Deployment**
- Docker: Each microservice and frontend has its own Dockerfile for isolated, reproducible deployments
- Cloud-ready: Optimized for deployment on platforms like Vercel, Render, or your own Kubernetes cluster

**Other Tools**
- ESLint for code quality
- Modern authentication (JWT-based)
- Environmental configuration for secrets and keys

---

## 📦 Repository Structure

```
zap/
├── frontend/         # Next.js frontend
├── primary-backend/  # Main backend service (API, auth, workflow logic)
├── hooks/            # Webhook handling service
├── processor/        # Workflow processor and job runner
├── worker/           # Worker for async/background tasks
├── shared/           # Shared code and types (if present)
└── README.md         # This file
```

---

## 🏁 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/krrakshit/zap.git
cd zap
```

### 2. Start the Frontend

```bash
cd frontend
npm install           # or yarn / pnpm / bun install
npm run dev           # or yarn dev / pnpm dev / bun dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### 3. Run Backend Services

Each backend microservice has its own directory and Dockerfile. You can run them locally with Node.js or Docker.

#### Example: Running the hooks service

```bash
cd hooks
npm install
npm run dev
```

Or with Docker:

```bash
docker build -t zap-hooks .
docker run -p 3002:3002 zap-hooks
```

> Repeat similar steps for `primary-backend`, `processor`, and `worker`.

### 4. Environment Variables

Each service may require environment variables such as database URLs, secret keys, etc. See the respective directory for a `.env.example` or instructions.

---

## 🧑‍💻 Example Usage

- **Create a Workflow**: Use the UI to visually define a trigger (e.g., "New email received") and actions (e.g., "Send a message to Slack").
- **Connect Apps**: Authorize and connect third-party apps to automate tasks across platforms.
- **AI-Powered Actions**: Use AI features to process, summarize, or transform data as part of your automations.
- **Advanced Users**: Set up custom webhooks to trigger workflows from any service that supports HTTP requests.

---

## 📚 Learn More

- [Next.js Documentation](https://nextjs.org/docs)
- [Prisma Docs](https://www.prisma.io/docs/)
- [Node.js Docs](https://nodejs.org/en/docs)
- [Docker Documentation](https://docs.docker.com/)

---

## 🛡️ Security

- Environment variables for all secrets
- JWT-based authentication
- Follows Node.js security best practices

---

## 🌎 Deployment

- **Frontend**: Deploy to [Vercel](https://vercel.com/) with one click, or use your own infrastructure.
- **Backend Services**: Deploy each service as a Docker container, or to popular cloud providers.
- **Database**: Compatible with managed databases (Supabase, Neon, AWS RDS, etc.)

---

## 🤝 Contributing

Contributions are welcome! Please open issues or pull requests for improvements, bug fixes, or new features.

---

## 📄 License

This project is open source. See [LICENSE](LICENSE) for details.

---

> For more details, see the source code or open an issue on [GitHub](https://github.com/krrakshit/zap).
