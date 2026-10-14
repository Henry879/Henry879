# 👋 Hi, I'm Henry Carreño!

### 🎯 Software Engineer | Backend & Python Developer
📍 Colombia | 🌐 Spanish (Native), English (B2)  
💼 **Focus:** Building scalable backend systems, RESTful APIs, and process automation tools.  
🚀 **Tech Stack:** Python, FastAPI, Java, Spring Boot, PostgreSQL, SQL, Git.

---

### 🧰 Technical Stack

* **Languages:** Python, Java, SQL, JavaScript, HTML/CSS
* **Backend & Frameworks:** FastAPI, Spring Boot, REST APIs, Microservices Architecture
* **Databases & Modeling:** PostgreSQL, MySQL, Relational Database Modeling
* **Tools & Practices:** Git, GitHub (Git Flow, Feature Branching, Code Reviews), Docker, Postman, Swagger UI / OpenAPI, Agile/Scrum
* **Engineering Focus:** API Design & Validation, State Machine Design, Asynchronous Workflows, Performance Optimization, Clean Code

---

### 💻 Featured Engineering Projects

#### 🛒 [DomiLocal — Food Delivery REST API](https://github.com/DomiLocal/Domilocal)
**Collaborative Project | Python · FastAPI · PostgreSQL · Git Flow · Test Automation · Scrum**
* **Client Domain Ownership:** Architected and engineered the end-to-end backend business logic for the Client module across 5 core User Stories (user registration, catalog browsing, order creation, real-time status tracking, and order cancellation).
* **State Machine & Business Logic:** Designed RESTful state controls prohibiting order cancellation during transit (`in_transit`), filtering out-of-stock items (`stock=0`), and restricting multi-vendor cart creation with explicit `400 Bad Request` responses.
* **HTTP Exception Mapping & Testing:** Standardized API contracts with strict HTTP status code mapping (`200`, `201`, `400`, `404`, `409`, `503`) and consistent JSON schemas (`success`, `message`, `data`). Validated edge cases and error contracts using FastAPI's interactive Swagger UI.
* **Collaborative Git Flow:** Coordinated feature development using structured Git Flow practices—managing isolated feature branches per user story, resolving merge conflicts, and conducting PR code reviews prior to merging into testing and development branches.

#### 🤖 [HALLEY COL — CRM & Automated Integration Engine](https://github.com/Henry879/HalleyCol)
**Full-Stack Project | Python · Backend Logic · API Integration · PostgreSQL · Process Automation**
* **Automated Integration Engine:** Engineered a full-stack system integrating an automated WhatsApp conversational agent with an operational CRM web dashboard to handle 24/7 client operations.
* **Backend Workflows & State Management:** Implemented real-time backend logic to manage order processing, payment status transitions, and synchronized customer history logs between external messaging APIs and the core CRM panel.
* **Data Consistency:** Structured persistent backend workflows ensuring data integrity across automated client interactions and administrative interfaces.

---

### 🛠️ Client Module Specification Example (DomiLocal)

To demonstrate contract-first API design and strict validation practices, here is a summary of the endpoints built for the **Client Domain**:

| Method | Endpoint | Description | Business Rules & HTTP Status |
| :--- | :--- | :--- | :--- |
| `POST` | `/api/v1/clients/register` | Client Onboarding | Password strength validation (min 8 chars + number), email format checking, duplicate email prevention (`409 Conflict`). |
| `GET` | `/api/v1/merchants/{id}/products` | Catalog Browsing | Excludes out-of-stock items (`stock=0`), supports category filtering (`?category=`), returns `404 Not Found` for invalid merchants. |
| `POST` | `/api/v1/orders` | Order Placement | Blocks empty carts, prevents multi-vendor orders, requires delivery address validation (`400 Bad Request`). |
| `GET` | `/api/v1/orders/{id}/status` | Status Tracking | Tracks state transitions (`received` -> `in_preparation` -> `in_transit` -> `delivered`), includes assigned driver details and historical timestamps. |
| `PATCH` | `/api/v1/orders/{id}/cancel` | Order Cancellation | Restricted cancellation: permitted ONLY in `received` or `in_preparation` states. Returns `400 Bad Request` if `in_transit`. |

---

### 🎓 Education & Certifications
* **Information Systems Development Technology** — UTS (In Progress)
* **B2 Intermediate English** — Smart Language Academy (2026)
* **Basic Cybersecurity (15 Hours)** — MinTIC / Talento Tech (2025)

---

### 📫 Connect with Me
* **LinkedIn:** [Henry Carreño](https://www.linkedin.com/in/henry-felipe-3176a8363/)
* **Email:** henryfelipe709@gmail.com
