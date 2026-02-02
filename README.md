# Global Open Investments

**Global Open Investments** is a high-load exchange platform (similar to Binance) designed for trading, storing, and managing digital and traditional assets such as cryptocurrencies, tokens, and stocks.

The platform is built using a **microservices architecture**, with **Java** and **Node.js** on the backend and **Next.js** on the frontend, focusing on scalability, fault tolerance, and security.

---

## 🚀 Key Features

- 📈 Spot trading (buy / sell)
- 💼 User wallet management
- 🔐 Authentication and authorization
- 💸 Deposits and withdrawals
- 📊 Real-time market data and order book
- 🧾 Trade and transaction history
- ⚙️ Admin panel
- 🔔 Event-driven notifications

---

## 🏗 Architecture

The project follows a **microservices architecture** with clear separation of responsibilities.



---

## 🧩 Backend (Microservices)

The backend consists of independent services communicating via REST / gRPC / message brokers.

### Core Services

| Service | Stack | Responsibility |
|------|------|----------------|
| API Gateway / BFF | Node.js (NestJS) | API aggregation, auth, rate limiting |
| Auth Service | Node.js | Users, JWT, OAuth, KYC |
| Trading Service | Java (Spring Boot) | Order book, trades, matching engine |
| Wallet Service | Java (Spring Boot) | Balances, deposits, withdrawals |
| Asset Service | Node.js | Assets, trading pairs, fees |
| Notification Service | Node.js | Email, WebSocket, events |
| Admin Service | Node.js | System management |

---

## 🔄 Service Communication

- **REST / gRPC** — synchronous communication  
- **Message Broker (Kafka / RabbitMQ)** — asynchronous events:
  - OrderCreated
  - TradeExecuted
  - BalanceUpdated
- **Redis** — caching and rate limiting

---

## 🗄 Data Storage

| Component | Purpose |
|--------|---------|
| PostgreSQL | Transactional data |
| MongoDB | Flexible data (logs, histories) |
| Redis | Cache, sessions, order data |
| S3-compatible storage | Documents and reports |

---

## 🎨 Frontend

### Tech Stack

- **Next.js**
- **React**
- **TypeScript**
- **Tailwind CSS / MUI**
- **WebSockets** (real-time updates)

### Main Modules

- Trading terminal
- Asset overview
- User wallet
- Transaction history
- Profile and security settings

---

## 🔐 Security

- JWT + Refresh Tokens
- RBAC (Role-Based Access Control)
- Rate limiting
- Idempotency keys
- Sensitive data encryption
- Audit logs

---

## ⚙️ DevOps & Infrastructure

- Docker / Docker Compose
- Kubernetes (optional)
- CI/CD (GitHub Actions / GitLab CI)
- Nginx / API Gateway
- Monitoring (Prometheus, Grafana)
- Centralized logging
