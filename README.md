
<div align="center">

  <h1>Silver Dragons Academy Web Platform</h1>

  <p><strong>React · TypeScript · Python · Django REST Framework</strong></p>

  <p>
    A full-stack website for Silver Dragons Academy, featuring a custom
    chatbot integration and a security-conscious REST API.
  </p>

  <p><em>Building Character. Developing Confidence. Preparing for Life.</em></p>

</div>

<hr>

<h2>Project Overview</h2>

<p>
  Silver Dragons Academy is a community-focused martial arts and education
  organization centered on character development, confidence, discipline,
  fitness, and practical life skills.
</p>

<p>
  This repository contains the Silver Dragons Academy website and its
  supporting backend API, including <strong>Silvia</strong>, a virtual
  assistant designed to answer questions about the academy.
</p>

<p>
  The platform combines a React-based frontend with a Python backend
  implemented using Django and Django REST Framework. It demonstrates
  practical full-stack development, REST API integration, chatbot development,
  software testing, and application security considerations.
</p>

<p>The current project focuses on:</p>

<ul>
  <li>Frontend development with React and TypeScript</li>
  <li>Website styling with Tailwind CSS</li>
  <li>Python backend development using Django</li>
  <li>REST API development with Django REST Framework</li>
  <li>Silvia chatbot integration</li>
  <li>Frontend-to-backend communication</li>
  <li>Input validation and error handling</li>
  <li>Application security and software testing</li>
</ul>

<h2>Architecture</h2>

<pre>
Silver Dragons Academy Web Platform
│
├── Frontend Website
│   ├── React
│   ├── TypeScript
│   ├── Vite
│   ├── Tailwind CSS
│   └── Silvia Chat Interface
│
└── Backend API
    ├── Python
    ├── Django
    ├── Django REST Framework
    └── Silvia Chat API
</pre>

<h3>Frontend</h3>

<p>
  The frontend provides the public-facing website and interactive chatbot
  interface.
</p>

<p><strong>Technologies:</strong></p>

<ul>
  <li>React</li>
  <li>TypeScript</li>
  <li>Vite</li>
  <li>Tailwind CSS</li>
</ul>

<p>The frontend is responsible for:</p>

<ul>
  <li>Displaying academy information and website content</li>
  <li>Providing navigation and program information</li>
  <li>Rendering the Silvia chatbot interface</li>
  <li>Sending chatbot messages to the backend API</li>
  <li>Displaying chatbot responses to visitors</li>
</ul>

<h3>Backend</h3>

<p>
  The backend uses Python, Django, and Django REST Framework to provide
  server-side API functionality.
</p>

<p>The backend is responsible for:</p>

<ul>
  <li>Exposing API endpoints</li>
  <li>Processing chatbot requests</li>
  <li>Returning JSON responses</li>
  <li>Supporting frontend-to-backend integration</li>
  <li>Providing a foundation for maintainable backend development</li>
</ul>

<h2>Silvia Chatbot</h2>

<p>
  <strong>Silvia</strong> is the virtual assistant for Silver Dragons Academy.
  It provides visitors with a conversational interface for asking questions
  about the academy, Taekwondo, training benefits, and other supported topics.
</p>

<p>
  Silvia is integrated into the website through a custom REST API built with
  Python, Django, and Django REST Framework.
</p>

<h3>Chatbot Features</h3>

<ul>
  <li>Interactive chatbot interface</li>
  <li>HTTP-based communication with the Django backend</li>
  <li>JSON request and response handling</li>
  <li>Academy-focused question answering</li>
  <li>Handling of unsupported questions</li>
  <li>Defined chatbot instructions and response boundaries</li>
</ul>

<h3>Chatbot Architecture</h3>

<pre>
Website Visitor
      │
      ▼
React Chat Interface
      │
      │ POST /api/chat
      ▼
Django REST Framework
      │
      ▼
Silvia Chat Processing
      │
      ▼
JSON Response
      │
      ▼
React Chat Interface
      │
      ▼
Visitor Receives Response
</pre>

<p>
  The frontend sends the visitor's message to the Django API. The backend
  processes the request and returns a response that the frontend displays
  in the conversation.
</p>

<h2>API Endpoints</h2>

<table>
  <thead>
    <tr>
      <th>Method</th>
      <th>Endpoint</th>
      <th>Purpose</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>GET</code></td>
      <td><code>/api/health</code></td>
      <td>Checks API health.</td>
    </tr>
    <tr>
      <td><code>POST</code></td>
      <td><code>/api/chat</code></td>
      <td>Processes chatbot messages.</td>
    </tr>
  </tbody>
</table>

<h3>Example Chat Request</h3>

<pre>
POST /api/chat
Content-Type: application/json

{
  "message": "What is Taekwondo?"
}
</pre>

<p>
  The API accepts a chatbot message and returns a response in JSON format.
  The exact response structure is determined by the current backend
  implementation.
</p>

<h3>Frontend API Configuration</h3>

<p>
  The frontend uses an environment variable to configure the chatbot API URL:
</p>

<pre>
const API_URL =
  import.meta.env.VITE_SILVIA_API_URL ||
  "http://127.0.0.1:8000/api/chat";
</pre>

<p>
  For local development, the environment variable can be configured as follows:
</p>

<pre>
VITE_SILVIA_API_URL=http://127.0.0.1:8000/api/chat
</pre>

<p>
  The local URL is a development fallback. Environment-specific configuration
  allows the frontend endpoint to be changed without modifying the application
  source code.
</p>

<h2>Application Security</h2>

<p>
  Application security is an important consideration in the development of
  the website and chatbot. The project explores how web applications should
  handle untrusted input, communicate with backend services, and maintain
  appropriate information boundaries.
</p>

<h3>Security Considerations</h3>

<ul>
  <li><strong>Input validation:</strong> Handle missing, empty, malformed, or unexpected input.</li>
  <li><strong>API request handling:</strong> Process requests using appropriate HTTP methods and data formats.</li>
  <li><strong>Error handling:</strong> Avoid unnecessarily exposing internal implementation details.</li>
  <li><strong>CORS configuration:</strong> Configure permitted frontend origins for local development.</li>
  <li><strong>Request abuse prevention:</strong> Evaluate rate limiting and request-size restrictions.</li>
  <li><strong>Chatbot security:</strong> Evaluate attempts to override instructions or obtain internal information.</li>
  <li><strong>Information boundaries:</strong> Avoid exposing private information or inventing unsupported academy details.</li>
  <li><strong>Configuration security:</strong> Keep secrets and sensitive configuration out of source control.</li>
</ul>

<p>
  These items describe security considerations for the project. Individual
  controls should be verified against the current Django implementation
  before being described as implemented protections.
</p>

<h3>Chatbot Security Boundaries</h3>

<p>
  Silvia is designed to maintain defined behavioral boundaries when responding
  to user messages. Security testing can evaluate scenarios such as:
</p>

<ul>
  <li>Attempts to reveal internal chatbot instructions</li>
  <li>Prompt-injection attempts</li>
  <li>Requests for private or administrative information</li>
  <li>Requests for unsupported academy information</li>
  <li>Malformed or unexpected API requests</li>
  <li>Questions outside the chatbot's supported knowledge</li>
</ul>

<p>
  The objective is to evaluate the chatbot under normal and adversarial
  conditions and improve its reliability through testing.
</p>

<h2>Software Testing</h2>

<p>
  Testing helps verify expected application behavior and identify regressions
  as the website and backend evolve.
</p>

<p>Relevant testing areas include:</p>

<ul>
  <li>API endpoint behavior</li>
  <li>Valid and invalid chatbot requests</li>
  <li>Frontend-to-backend integration</li>
  <li>Request validation</li>
  <li>HTTP method handling</li>
  <li>Error responses</li>
  <li>Chatbot response behavior</li>
  <li>Security-related input scenarios</li>
</ul>

<h3>Django System Checks</h3>

<pre>
python manage.py check
</pre>

<h3>Start the Backend</h3>

<pre>
python manage.py runserver
</pre>

<h3>Run Django Tests</h3>

<pre>
python manage.py test
</pre>

<p>
  These commands support local development. Test coverage and passing results
  should reflect the tests that actually exist and run successfully in the
  current Django project.
</p>

<h2>Technology Stack</h2>

<h3>Frontend</h3>

<ul>
  <li>React</li>
  <li>TypeScript</li>
  <li>Vite</li>
  <li>Tailwind CSS</li>
</ul>

<h3>Backend</h3>

<ul>
  <li>Python</li>
  <li>Django</li>
  <li>Django REST Framework</li>
</ul>

<h3>Development Tools</h3>

<ul>
  <li>Git</li>
  <li>GitHub</li>
  <li>Node.js and npm</li>
  <li>Python and pip</li>
  <li>Django development and testing tools</li>
</ul>

<h2>Project Structure</h2>

<p>
  The following is an illustrative directory structure. Adjust directory
  names to match the actual repository.
</p>

<pre>
SilverDragonsAcademyWeb/
│
├── src/
│   ├── components/
│   ├── pages/
│   └── ...
│
├── public/
│   └── images/
│       └── virtual-assistant.jpg
│
├── package.json
├── vite.config.ts
│
├── silver-dragons-api-django/
│   ├── manage.py
│   ├── config/
│   ├── silvia/
│   └── requirements.txt
│
└── README.md
</pre>

<p>
  The frontend source directory and Django project directory should reflect
  the actual locations in your repository.
</p>

<h2>Getting Started</h2>

<h3>Prerequisites</h3>

<ul>
  <li>Python</li>
  <li>Node.js and npm</li>
  <li>Git</li>
</ul>

<h3>1. Start the Django Backend</h3>

<p>Open a terminal in the Django backend directory:</p>

<pre>
cd silver-dragons-api-django
</pre>

<p>Create a Python virtual environment:</p>

<pre>
python -m venv .venv
</pre>

<p>Activate the environment on Windows PowerShell:</p>

<pre>
.\.venv\Scripts\Activate.ps1
</pre>

<p>Install the backend dependencies:</p>

<pre>
python -m pip install -r requirements.txt
</pre>

<p>Check the Django configuration:</p>

<pre>
python manage.py check
</pre>

<p>Start the development server:</p>

<pre>
python manage.py runserver
</pre>

<p>The backend should be available at:</p>

<pre>
http://127.0.0.1:8000/
</pre>

<h3>2. Configure the Frontend</h3>

<p>
  Create or update the frontend's local <code>.env</code> file:
</p>

<pre>
VITE_SILVIA_API_URL=http://127.0.0.1:8000/api/chat
</pre>

<p>
  Restart the Vite development server after changing environment variables.
  Do not commit local environment files containing sensitive configuration.
</p>

<h3>3. Start the Frontend</h3>

<p>From the frontend project directory, install dependencies:</p>

<pre>
npm install
</pre>

<p>Start the Vite development server:</p>

<pre>
npm run dev
</pre>

<p>The frontend should be available at:</p>

<pre>
http://localhost:5173
</pre>

<h3>4. Verify the Chatbot Integration</h3>

<ol>
  <li>Start both the Django and frontend development servers.</li>
  <li>Open the website in a browser.</li>
  <li>Navigate to the Silvia chatbot.</li>
  <li>Submit a question supported by the chatbot.</li>
  <li>Verify that the request reaches the Django API.</li>
  <li>Confirm that the response appears in the chat interface.</li>
</ol>

<h2>Development Philosophy</h2>

<p>
  The project follows an incremental software engineering approach:
</p>

<ol>
  <li>Implement website functionality.</li>
  <li>Develop and maintain the Django backend.</li>
  <li>Integrate frontend features with the REST API.</li>
  <li>Test normal and unexpected inputs.</li>
  <li>Evaluate security risks and relevant safeguards.</li>
  <li>Improve documentation and maintainability.</li>
</ol>

<p>
  Security and testing are considered throughout development rather than
  treated exclusively as final steps.
</p>

<h2>Current Project Scope</h2>

<table>
  <thead>
    <tr>
      <th>Component</th>
      <th>Scope</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>React website</td>
      <td>Included</td>
    </tr>
    <tr>
      <td>TypeScript frontend</td>
      <td>Included</td>
    </tr>
    <tr>
      <td>Tailwind CSS</td>
      <td>Included</td>
    </tr>
    <tr>
      <td>Python and Django backend</td>
      <td>Included</td>
    </tr>
    <tr>
      <td>Django REST API</td>
      <td>Included</td>
    </tr>
    <tr>
      <td>Silvia chatbot</td>
      <td>Included</td>
    </tr>
    <tr>
      <td>Frontend/API integration</td>
      <td>Included</td>
    </tr>
    <tr>
      <td>Local development</td>
      <td>Included</td>
    </tr>
   
  </tbody>
</table>

<p>
  The current project focuses on the website and its chatbot integration.
  It does not include plans for a mobile application, cloud deployment,
  or new database-backed functionality.
</p>

<h2>Silver Dragons Academy</h2>

<p>
  The website supports the mission of Silver Dragons Academy: helping students
  develop skills and habits that extend beyond martial arts training.
</p>

<p>The academy's Taekwondo program emphasizes:</p>

<ul>
  <li>Discipline</li>
  <li>Confidence</li>
  <li>Fitness</li>
  <li>Coordination</li>
  <li>Respect</li>
  <li>Perseverance</li>
  <li>Self-control</li>
  <li>Practical self-defense</li>
  <li>Character development</li>
</ul>

<h1>Screenshots of the Silver Dragons Academy Web App</h1>

<img width="1265" height="563" alt="Screenshot 2026-10-18 005719" src="https://github.com/user-attachments/assets/746d9aa7-b519-4fed-8e5f-a0690abcd576" />
<img width="1254" height="629" alt="Screenshot 2026-10-18 004951" src="https://github.com/user-attachments/assets/52e3e29f-d69b-4449-82e7-4906acc9999d" />
<img width="1257" height="700" alt="Screenshot 2026-10-18 005035" src="https://github.com/user-attachments/assets/26378a94-4a7e-4d26-9cb3-dfc6372a5ce5" />
<img width="1264" height="700" alt="Screenshot 2026-10-18 005128" src="https://github.com/user-attachments/assets/8759f44e-c5da-483b-a786-d7546c92b545" />
<img width="1262" height="702" alt="Screenshot 2026-10-18 005053" src="https://github.com/user-attachments/assets/9a03b4f6-7bf5-40e6-a596-082880f247f3" />
<img width="342" height="413" alt="Screenshot 2026-10-18 002457" src="https://github.com/user-attachments/assets/610be5aa-3471-4fe0-8705-949b63eb3ba5" />







<hr>

<div align="center">
  <p><strong>Maintained by Gary Collins</strong></p>
  <p>Silver Dragons Academy Web Platform</p>
  <p>Full-Stack Development · REST API Integration · Application Security</p>
</div>
