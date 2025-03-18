# 🚀 Mulligan Parking System - Distributed Systems Project

## 📌 Project Overview
The **Mulligan Parking System** is a distributed system designed for **efficient parking space management**. It enables customers to choose a parking zone, view available spaces, and select a slot dynamically. The system is built using **RabbitMQ** for messaging, **MongoDB** for data persistence, and follows best practices in **distributed computing**. The entire architecture is **clustered**, ensuring high availability and scalability.

## 👥 Contributors
| Name              | Role                          |
|---------------|-----------------------------|
| [**Matan Shabi**](https://github.com/Matan-Shabi)   | CI/CD & DevOps Lead, Database Architect, Documentation Engineer |
| [**Jamal Majadle**](https://github.com/JamalM02)   | UI Development, Server, RabbitMQ, Recommender System, Docker |
| [**Oran Alster**](https://github.com/Oran01)  | Server, Testing, Javadoc |

## 🔧 Key Technical Contributions

### 🏗️ CI/CD & Build System (Matan Shabi)
- **Gradle Configuration**: Designed a modular build system with cross-platform support
- **GitHub Actions Workflows**: Implemented automated testing with MongoDB and RabbitMQ clusters
- **Automated JavaDoc Generation**: Set up CI pipeline for continuous documentation generation

### 🗄️ Database Infrastructure (Matan Shabi)
- **MongoDB Cluster Configuration**: Designed and implemented a 3-node MongoDB replica set
- **Schema Design & Documentation**: Created comprehensive database schema design with mermaid diagrams
- **Data Access Layer**: Implemented robust database connectivity with transaction support

### 📑 Documentation & Automation (Matan Shabi)
- **Technical Documentation**: Created comprehensive markdown documentation for database, queue systems, and consensus protocol
- **Automation Scripts**: Developed robust setup and teardown scripts for development environment
- **Docker Compose Files**: Created containerization configurations for the entire distributed system

---

## 📜 Documentation

- [📑 Testing Plan](TestAcceptance.md)
- [🗄️ Database Design](Database_Design_Document.md) - *Matan Shabi*
- [📬 Queue Management](Queue_Design_Document.md) - *Matan Shabi*
- [📖 Consensus Protocol](Consensus_Protocol.md) - *Matan Shabi*

---

## 🏗️ System Architecture
### 🔹 **Key Components**

- **Frontend**: Web-based UI for selecting parking zones and spaces
- **Backend**: Handles requests, updates availability, and processes reservations
- **Database Cluster**: High-availability MongoDB 3-node replica set for storing parking data
- **Messaging Cluster**: Fault-tolerant RabbitMQ 3-node cluster for distributed task handling
- **Recommender Service**: AI-powered Recommender System with redundant copies

### 🔹 **Workflow**

1. Customers **log in** and select a **parking zone**.
2. System displays **available spaces** in the selected zone.
3. Customers **choose a parking space**, making it **unavailable for others**.
4. **Vehicle registration** field is enabled only after selecting a parking space.
5. Confirmation is sent, and the **booking is processed asynchronously**.

---

## ⚙️ Technologies Used
| **Category** | **Technology** |
|-------------|---------------|
| **Programming Languages** | Java, JavaScript |
| **Frameworks** | Spring Boot, Express.js |
| **Build System** | Gradle (multi-project) |
| **Database** | **Clustered MongoDB** |
| **Message Queue** | **Clustered RabbitMQ** |
| **CI/CD** | GitHub Actions |
| **Recommender System** | **Clustered AI-powered Recommender** |
| **Deployment & DevOps** | Docker, Docker Compose |
| **Testing** | JUnit, Mockito, TestFX |
| **Documentation** | JavaDoc, Markdown, Mermaid |

---

## 🛠️ Setup & Installation
### 1️⃣ **Clone the Repository**
```sh
git clone https://github.com/JamalM02/MulliganParkingSystem.git
cd MulliganParkingSystem
```

### 2️⃣ **Automated Setup (Using Scripts)**
For Linux/macOS:
```sh
chmod +x setup.sh
./setup.sh
```

For Windows:
```sh
setup.bat
```

### 3️⃣ **Manual Setup**
Create a `.env` file in the root directory:
```sh
MONGODB_URI=mongodb://cluster-url:27017/parking_system
RABBITMQ_USER=user
RABBITMQ_PASS=password
```

Start the infrastructure:
```sh
docker-compose -f docker-compose.mongo.yml up -d
docker-compose -f docker-compose.rabbitmq.yml up -d
docker-compose -f docker-compose.recommender.yml up -d
```

### 4️⃣ **Build and Run the Application**
```sh
./gradlew build
./gradlew :Server:run
```

---

## 📌 Usage Instructions

- Access the **web UI** at `http://localhost:3000`
- Select a **parking zone**
- Choose an **available parking space**
- Enter **vehicle details** (enabled after space selection)
- Confirm **reservation** and receive status updates

---

## 🧪 Testing

Run the automated test suite with:
```sh
./gradlew test
```

Generate test coverage reports:
```sh
./gradlew jacocoTestReport
```

---

## 📚 Documentation Generation

Generate JavaDoc for all modules:
```sh
./gradlew javadoc
```

Access documentation at:
- `build/docs/javadoc/index.html` - Main JavaDoc
- `Database_Design_Document.md` - Database schema and queries
- `Queue_Design_Document.md` - Message queuing architecture
- `Consensus_Protocol.md` - Recommender system consensus protocol

---

## 🔍 Future Improvements

- ✅ Enhance **real-time parking availability updates**
- ✅ Implement **automated notifications for users**
- ✅ Introduce **dynamic pricing based on demand**
- ✅ Add **payment gateway integration**
- ✅ Implement **mobile application versions**
