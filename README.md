
# GearShift - AI-Powered Bicycle & Parts E-Commerce Platform

![GearShift Logo](https://via.placeholder.com/150x50/2E8B57/FFFFFF?text=GearShift) <!-- Replace with your actual logo path -->

## 🚀 Overview

GearShift is a modern, high-performance e-commerce platform dedicated exclusively to cycling enthusiasts and professionals. We don't just sell bicycles and components; we provide a data-driven, intelligent shopping experience. By leveraging cutting-edge Artificial Intelligence, GearShift offers personalized product recommendations, predictive maintenance insights, and a seamless user journey from discovery to purchase.

This repository contains the frontend and backend code for the GearShift web application.

## ✨ Features

### 🛒 Core E-Commerce
*   **Product Catalog:** Extensive, filterable catalog of bicycles (Road, Mountain, Hybrid, etc.) and spare parts (drivetrains, wheels, brakes, accessories).
*   **Advanced Search & Filtering:** Search by brand, component type, price range, rider level, and terrain.
*   **Secure User Accounts:** User registration, profile management, and order history.
*   **Shopping Cart & Wishlist:** Intuitive cart management and save-for-later functionality.
*   **Secure Checkout:** Integrated payment gateway supporting major credit cards and digital wallets.
*   **Order Management & Tracking:** Full order lifecycle management with real-time tracking integration.

### 🧠 AI-Powered Insights (Our Competitive Edge)
*   **Personalized Product Recommendations:** Our ML engine analyzes user browsing behavior, purchase history, and similar user profiles to suggest highly relevant bikes and parts.
*   **Predictive Maintenance Alerts:** Users can register their bike. Based on mileage, riding conditions, and component lifespan data, the system proactively suggests when to service or replace parts.
*   **"Build Your Dream Bike" Configurator:** An AI-assisted tool that helps users build a custom bicycle. The AI ensures component compatibility (e.g., frame/fork standards, derailleur capacity) and suggests optimal setups based on the rider's stated goals (e.g., "lightweight climbing," "durable trail bike").
*   **Intelligent Inventory Forecasting:** Our backend AI models predict demand for parts and complete bikes, helping to minimize stockouts and optimize warehouse logistics.
*   **Chatbot & Virtual Assistant:** An AI-powered assistant to answer product questions, provide basic technical support, and guide users through the purchase process.

## 🛠️ Technology Stack

GearShift is built on a modern, scalable, and decoupled architecture (JAMstack).

### Frontend
*   **Framework:** **[Next.js](https://nextjs.org/)** (React)
    *   **Why?** Enables server-side rendering (SSR) and static site generation (SSG) for blazing-fast page loads and superior SEO performance. Essential for an e-commerce site's discoverability.
*   **State Management:** **[Zustand](https://github.com/pmndrs/zustand)** / **[Redux Toolkit](https://redux-toolkit.js.org/)**
    *   **Why?** A lightweight yet powerful state management solution for managing complex application state like user sessions, shopping cart, and UI themes.
*   **Styling:** **[Tailwind CSS](https://tailwindcss.com/)**
    *   **Why?** A utility-first CSS framework that allows for rapid, consistent, and highly customizable UI development.
*   **Type Safety:** **[TypeScript](https://www.typescriptlang.org/)**
    *   **Why?** Catches errors at compile time, improves code quality and developer productivity, and provides excellent IDE support.

### Backend & API
*   **Runtime:** **[Node.js](https://nodejs.org/)**
*   **Framework:** **[NestJS](https://nestjs.com/)**
    *   **Why?** A progressive, TypeScript-first framework for building efficient and scalable server-side applications. Its modular architecture and dependency injection make the code highly maintainable.
*   **API Design:** **GraphQL** with **[Apollo Server](https://www.apollographql.com/docs/apollo-server/)**
    *   **Why?** Allows the frontend to request exactly the data it needs in a single query, reducing over-fetching and under-fetching, which is perfect for complex product pages.

### AI & Machine Learning
*   **Recommendation Engine:** **[Python](https://www.python.org/)** with **[scikit-learn](https://scikit-learn.org/)** / **[TensorFlow](https://www.tensorflow.org/)**
    *   **Implementation:** Collaborative filtering and content-based filtering models trained on user interaction data.
*   **NLP for Chatbot:** **[OpenAI API](https://openai.com/)** or **[Google Dialogflow](https://cloud.google.com/dialogflow)**
    *   **Implementation:** Powers the conversational interface for customer support and product discovery.
*   **ML Service Integration:** **RESTful APIs** built with **[FastAPI](https://fastapi.tiangolo.com/)** to serve ML models to the main backend.

### Database & Storage
*   **Primary Database:** **[PostgreSQL](https://www.postgresql.org/)**
    *   **Why?** A robust, open-source relational database perfect for handling complex product data, user information, and transactional orders with ACID compliance.
*   **Object Storage:** **[AWS S3](https://aws.amazon.com/s3/)** / **[Google Cloud Storage](https://cloud.google.com/storage)**
    *   **Why?** Scalable and secure storage for high-resolution product images, videos, and other static assets.
*   **Cache:** **[Redis](https://redis.io/)**
    *   **Why?** Used for session storage, caching frequent database queries (e.g., product listings), and managing rate limiting.

### DevOps & Infrastructure
*   **Deployment & Orchestration:** **[Docker](https://www.docker.com/)** & **[Kubernetes](https://kubernetes.io/)**
    *   **Why?** Containerization ensures consistency across environments, and Kubernetes provides auto-scaling, self-healing, and efficient management of microservices.
*   **Cloud Provider:** **[AWS](https://aws.amazon.com/)** / **[Google Cloud Platform (GCP)](https://cloud.google.com/)**
*   **CI/CD:** **[GitHub Actions](https://github.com/features/actions)** / **[GitLab CI](https://docs.gitlab.com/ee/ci/)**
*   **Monitoring:** **[Prometheus](https://prometheus.io/)** & **[Grafana](https://grafana.com/)**

### Third-Party Services
*   **Payments:** **[Stripe](https://stripe.com/)** (for its powerful API, security, and global reach)
*   **Search:** **[Algolia](https://www.algolia.com/)** (for its superior, typo-tolerant, and instant search capabilities)
*   **Email & Notifications:** **[SendGrid](https://sendgrid.com/)** / **[Resend](https://resend.com/)**
*   **Analytics:** **[Google Analytics 4](https://analytics.google.com/)** & **[Mixpanel](https://mixpanel.com/)**

## 🗂️ Project Structure

```
gearshift-app/
├── frontend/                 # Next.js application
│   ├── components/          # Reusable React components
│   ├── lib/                 # Configuration (Apollo, Stripe)
│   ├── pages/               # Application pages (App Router)
│   ├── styles/              # Global and module CSS
│   └── store/               # Zustand/Redux store
├── backend/                 # NestJS application
│   ├── src/
│   │   ├── modules/         # Feature-based modules (auth, products, orders)
│   │   ├── common/          # Guards, Interceptors, Pipes
│   │   └── main.ts
├── ml-services/             # Python AI/ML microservices
│   ├── recommendation-engine/
│   └── compatibility-checker/
├── infrastructure/          # Terraform/K8s configuration
└── README.md
```

## 🚦 Getting Started

### Prerequisites
*   Node.js (v18 or higher)
*   npm, yarn, or pnpm
*   Docker & Docker Compose

### Installation & Local Development

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-organization/gearshift-app.git
    cd gearshift-app
    ```

2.  **Backend Setup:**
    ```bash
    cd backend
    npm install
    cp .env.example .env
    # Update .env with your database and API keys
    docker-compose up -d  # Starts PostgreSQL and Redis
    npm run db:migrate
    npm run start:dev
    ```

3.  **Frontend Setup:**
    ```bash
    cd ../frontend
    npm install
    cp .env.local.example .env.local
    # Update .env.local with your GraphQL endpoint and Stripe key
    npm run dev
    ```
    The app will be running on `http://localhost:3000`.

## 🤝 Contributing

We love contributions! Please read our [Contributing Guide](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## 📞 Support & Contact

For support, email `support@gearshift.com` or join our community Slack channel.

---

**Built with passion for the cycling community.** 🚴‍♀️🚴‍♂️