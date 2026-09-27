# Silver Dragons Academy Web Platform

**Silver Dragons Academy** is a community-focused martial arts and education organization built around character development, confidence, discipline, fitness, and practical life skills.

> **Building Character. Developing Confidence. Preparing for Life.**

This repository contains the web platform for Silver Dragons Academy, including the public-facing website and backend services supporting the platform's AI assistant, **Silvia**.

---

## 📌 Project Overview

The Silver Dragons Academy web platform is being developed as a practical full-stack application while also serving as a learning and portfolio project focused on:

* Full-stack web development
* Python and Django backend development
* API development
* Software testing
* Application security
* AI application security
* Secure software design
* Cloud deployment
* Long-term application maintenance

The project is intentionally being developed incrementally, with security and testing considered throughout the development lifecycle rather than added only after the application is completed.

---

## 🏗️ Architecture

The current platform is divided into two primary components:

```text
Silver Dragons Academy Web Platform
│
├── Frontend
│   ├── React
│   ├── TypeScript
│   ├── Vite
│   └── Tailwind CSS
│
└── Backend
    ├── Python
    ├── Django
    └── REST-style API services
```

### Frontend

The frontend provides the public-facing Silver Dragons Academy website.

**Technologies:**

* React
* TypeScript
* Vite
* Tailwind CSS

The frontend is responsible for the user interface, navigation, academy information, program information, and communication with backend services.

### Backend

The backend is being developed using:

* **Python**
* **Django**

The Django backend provides the server-side application layer and API functionality used by the frontend and AI assistant.

Backend development is currently focused on creating a maintainable foundation that can later support additional application functionality.

---

## 🤖 Silvia AI Assistant

**Silvia** is the virtual assistant for Silver Dragons Academy.

Silvia is designed to answer questions about the academy using controlled application knowledge rather than unrestricted access to private systems.

Current areas of focus include:

* Academy information
* Taekwondo
* Training benefits
* General program information
* Appropriate user questions
* Safe handling of unknown questions

Silvia is also being used as a practical environment for studying **AI application security**.

### AI Security Considerations

The application is being designed to account for risks such as:

* Prompt injection
* Instruction disclosure
* Unauthorized access to internal information
* Fabrication of information
* Improper handling of unknown questions
* Attempts to access private application data
* Excessive or malformed requests

The goal is not simply to make an AI assistant that works, but to understand how an AI-enabled application can be tested and secured.

---

## 🔐 Application Security

Security is a major development consideration for this project.

The application is being developed with an application-security mindset that includes:

* Input validation
* Request validation
* API security
* Error handling
* Access control considerations
* Secure configuration
* CORS configuration
* Security headers
* Rate limiting
* Request-size limitations
* AI security testing
* Negative testing
* Automated security-oriented tests

The project is also being used to learn how vulnerabilities can be identified through testing and how defensive controls can be incorporated into the application.

---

## 🧪 Software Testing

Testing is an important part of the development process.

Rather than only testing whether expected requests work, the project also examines how the application behaves when it receives unexpected or malicious input.

Testing areas include:

* Valid requests
* Invalid requests
* Malformed input
* Unexpected request structures
* Unsupported HTTP methods
* Validation failures
* API error handling
* Security controls
* AI prompt-injection scenarios
* Unauthorized information requests
* Boundary conditions

The backend uses Python/Django testing tools as development progresses.

Typical Django development commands include:

```bash
python manage.py check
```

Run the development server:

```bash
python manage.py runserver
```

Run the test suite:

```bash
python manage.py test
```

---

## 📁 Project Structure

The repository is organized around the web frontend and Django backend.

A simplified structure is:

```text
SilverDragonsAcademyWeb/
│
├── frontend/
│   ├── src/
│   ├── public/
│   │   └── images/
│   │       └── virtual-assistant.jpg
│   ├── package.json
│   └── vite.config.*
│
├── silver-dragons-api-django/
│   ├── manage.py
│   ├── config/
│   │   ├── settings.py
│   │   ├── urls.py
│   │   ├── wsgi.py
│   │   └── ...
│   └── ...
│
└── README.md
```

> The exact directory structure may change as development continues.

---

## 🌐 Development Environment

### Frontend

The frontend development server currently runs on:

```text
http://localhost:5173
```

### Django Backend

The Django development server uses the standard Django development address:

```text
http://127.0.0.1:8000
```

The frontend communicates with the backend through API requests.

---

## 🔌 API

The Django backend provides the server-side API layer for the web platform.

The API architecture is being developed around endpoints for services such as:

```text
/api/health
/api/chat
```

The API layer is being designed with validation, controlled responses, and security testing in mind.

As development continues, additional endpoints may be added for future platform functionality.

---

## 🛡️ Security Development Philosophy

This project follows a simple principle:

> **Security should be part of the development process, not an afterthought.**

The application is being developed with the expectation that users may submit:

* Invalid data
* Unexpected input
* Malicious input
* Attempts to bypass application rules
* Attempts to manipulate the AI assistant
* Requests for information they should not receive

Testing these scenarios helps identify weaknesses before the application is deployed.

This project therefore serves as both a production-oriented application and a practical environment for learning application security.

---

## ☁️ Cloud Deployment

Cloud deployment is part of the project's long-term development plan.

The current infrastructure direction includes **Oracle Cloud Infrastructure (OCI)** for backend hosting and future application services.

Deployment considerations include:

* Secure environment configuration
* Secret management
* HTTPS
* Database security
* API security
* Logging
* Monitoring
* Application maintenance
* Secure deployment practices

Cloud infrastructure will be introduced incrementally as the application reaches appropriate development milestones.

---

## 🗄️ Database

Database functionality is planned as the platform expands.

Potential future functionality includes:

* User accounts
* Academy membership information
* Training records
* Communication features
* Application data
* AI-related application data

Database access will be designed around appropriate authentication, authorization, validation, and least-privilege principles.

---

## 📱 Future Development

The web platform is intended to provide a foundation for future Silver Dragons Academy applications.

Potential future functionality includes:

### Silver Dragons Online

A future mobile/online training platform could provide:

* Training videos
* Online learning
* Rank-test preparation
* Training resources
* Progress tracking
* Certificates
* Community features

### Mobile Application

A future mobile application may use:

* React Native
* TypeScript
* Django backend services
* Authentication
* Role-based access control
* Multi-factor authentication
* Secure API communication

The mobile platform will be developed after the core web platform and backend architecture have matured.

---

## 🥋 Silver Dragons Academy

The technology platform supports the broader mission of Silver Dragons Academy.

The academy's founding martial arts program is Taekwondo, with an emphasis on:

* Discipline
* Fitness
* Confidence
* Coordination
* Respect
* Perseverance
* Self-control
* Practical self-defense
* Character development

Future programs may expand the academy's martial arts and educational offerings.

---

## 🎯 Development Goals

The project is being developed with several long-term goals:

### 1. Build a Real Application

The platform is intended to become a functional technology platform for Silver Dragons Academy rather than simply a demonstration project.

### 2. Learn Secure Software Development

Security is incorporated into development, testing, architecture, and deployment decisions.

### 3. Develop Application Security Skills

The project provides a controlled environment for studying:

* Vulnerability prevention
* Security testing
* Secure API design
* AI security
* Authentication
* Authorization
* Cloud security
* Software maintenance

### 4. Practice Software Engineering

The project provides practical experience with:

* Version control
* Application architecture
* Backend development
* Frontend development
* API design
* Automated testing
* Debugging
* Documentation
* Deployment

---

## 🚧 Current Development Status

| Component                    | Status                |
| ---------------------------- | --------------------- |
| React frontend               | 🚧 Active development |
| TypeScript                   | 🚧 Active development |
| Tailwind CSS                 | 🚧 Active development |
| Django backend               | 🚧 Active development |
| Python API                   | 🚧 Active development |
| Silvia AI assistant          | 🚧 Active development |
| Application security testing | 🚧 Active development |
| AI security testing          | 🚧 Active development |
| Database                     | 📋 Planned/expanding  |
| Oracle Cloud deployment      | 📋 Planned            |
| Mobile application           | 🔮 Future             |

---

## 🧰 Technology Stack

### Frontend

* React
* TypeScript
* Vite
* Tailwind CSS

### Backend

* Python
* Django

### Development & Testing

* Git
* GitHub
* Python testing tools
* Django testing framework

### Cloud

* Oracle Cloud Infrastructure

### Security Focus

* Application Security
* API Security
* AI Security
* Secure Software Development
* Cloud Security
* Software Testing

---

## 🚀 Getting Started

### Frontend

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

The frontend should then be available at:

```text
http://localhost:5173
```

### Django Backend

Navigate to the Django backend:

```bash
cd silver-dragons-api-django
```

Create and activate a Python virtual environment:

### Windows

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

Install project dependencies:

```bash
pip install -r requirements.txt
```

Run Django's system checks:

```bash
python manage.py check
```

Start the development server:

```bash
python manage.py runserver
```

The backend should then be available at:

```text
http://127.0.0.1:8000
```

---

## 🧪 Running Tests

From the Django backend directory:

```bash
python manage.py test
```

Additional testing will be added as the application grows.

Security-oriented tests are intended to verify that the application behaves safely when presented with invalid, unexpected, or potentially malicious input.

---

## 🔒 Security Notice

This project is an actively developed application and should not be considered production-ready solely because individual security controls or tests have been implemented.

Security testing cannot guarantee that an application contains no vulnerabilities.

The project is continuously being evaluated and improved as new functionality is introduced.

---

## 📚 Learning Through Development

One of the primary purposes of this project is practical learning.

Instead of building isolated demonstration applications, the development process uses a real project to explore:

```text
Software Engineering
        ↓
Backend Development
        ↓
API Development
        ↓
Software Testing
        ↓
Application Security
        ↓
AI Security
        ↓
Cloud Security
        ↓
Secure Deployment
        ↓
Long-Term Maintenance
```

This approach allows new concepts to be studied and immediately applied to an evolving application.

---

## 📄 License

License information will be added as the project reaches its appropriate release stage.

---

## 👤 Maintainer

**Gary Collins**

Silver Dragons Academy

The project is independently developed as part of the ongoing development of Silver Dragons Academy and as a practical software engineering and application-security learning project.
