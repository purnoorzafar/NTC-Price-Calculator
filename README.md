# NTC-Price-Calculator

# NTC Data Center Price Calculator

## 1. Project Introduction

The **NTC Data Center Price Calculator** is a responsive web application developed to provide an easy-to-use interface for estimating service costs based on the tariff information configured in the application.

The application allows a user to select a service, enter the required configuration, review the calculated estimate, and export the estimate for printing or saving as a PDF.

The interface is designed with a clean responsive layout, Light/Dark mode support, NTC branding, and a print-friendly estimate view.

> **Data note:** The application contains tariff information provided for the project. Detailed tariff values, source documents, internal references, and calculation tables are intentionally **not reproduced in this README**. They should be handled according to the applicable authorization and sharing requirements.

---

## 2. Main Features

* Responsive NTC-branded web interface
* Light and Dark mode
* Service-category based price calculation
* Interactive configuration inputs
* Automatic cost estimation
* One-time and recurring cost presentation where applicable
* Estimate export / print functionality
* Print-friendly estimate page
* Browser-tab NTC favicon
* NTC logo and contact section
* Client-side application with no database requirement
* Docker support for consistent deployment
* GitHub-ready project structure

---

## 3. Service Categories

The calculator interface is organized into the following service areas:

1. Virtual Dedicated Servers (VDS)
2. Bandwidth
3. Co-location
4. Email Services
5. Miscellaneous Items / Services
6. Shared Web Hosting Services

The application source contains the configured tariff data required by the calculator. The README deliberately does not publish individual rates or tariff tables.

---

## 4. Technologies and Tools

### Frontend

* **React** — user interface
* **Vite** — development server and build tool
* **JavaScript / JSX** — application logic
* **CSS** — responsive styling and theme system
* **HTML5** — document structure

### Development

* **Visual Studio Code** — development environment
* **Node.js / npm** — dependency management and local development
* **Git / GitHub** — version control and project sharing

### Deployment

* **Docker** — containerized application environment
* **Docker Compose** — simplified container startup
* **Nginx** — production web server inside the container

---

## 5. Project Structure

```text
ntc-price-calculator/
│
├── public/
│   └── ntc-logo.png
│
├── src/
│   ├── assets/
│   │   └── ntc-logo-transparent.png
│   │
│   ├── data/
│   │   └── tariffs.js
│   │
│   ├── main.jsx
│   └── styles.css
│
├── docs/
│   └── project reference material
│
├── index.html
├── package.json
├── vite.config.js
├── Dockerfile
├── docker-compose.yml
├── nginx.conf
├── .dockerignore
├── .gitignore
└── README.md
```

The `src/data/tariffs.js` file contains the application data used by the calculator. The source reference material in `docs/` is kept separate from the application code.

---

## 6. Running the Project Locally

### Requirements

Install the following before running the project locally:

* Node.js
* npm
* Visual Studio Code (recommended)

### Step 1 — Open the project

Extract the project ZIP and open the project folder in Visual Studio Code.

### Step 2 — Install dependencies

Open the VS Code terminal and run:

```bash
npm install
```

### Step 3 — Start the development server

```bash
npm run dev
```

Vite will display the local address in the terminal. Open that address in a browser.

---

## 7. Using the Calculator

1. Open the application in a browser.
2. Select the required service category.
3. Enter or select the required service configuration.
4. Review the calculated estimate.
5. Check the selected configuration and totals.
6. Use **Export Estimate** when a printable estimate is required.
7. From the browser print dialog, the estimate can be printed or saved as PDF.

The export view is designed so that the normal website interface is not included in the printed estimate.

---

## 8. Running with Docker

Docker is included so that the project can be run in a consistent environment on another computer.

From the project root directory, run:

```bash
docker compose up --build
```

After the container starts, open:

```text
http://localhost:8080
```

To stop the application:

```bash
docker compose down
```

### Docker CLI alternative

```bash
docker build -t ntc-price-calculator .
docker run --rm -p 8080:80 ntc-price-calculator
```

The Docker image builds the frontend and serves the production files through Nginx.

---

## 9. GitHub Procedure

After the project has been tested and approved, create a Git repository and push the project:

```bash
git init
git add .
git commit -m "Initial project version"
git branch -M main
git remote add origin YOUR_REPOSITORY_URL
git push -u origin main
```

For later updates:

```bash
git add .
git commit -m "Update project"
git push
```

### Sharing with another developer

A team member can clone the repository and run the project locally or through Docker, depending on the required workflow.

For Docker testing:

```bash
git clone YOUR_REPOSITORY_URL
cd ntc-price-calculator
docker compose up --build
```

---

## 10. Data and Repository Handling

This repository is intended to contain the application source code and deployment configuration required for the project.

Detailed tariff documents, internal reference material, and other source material should **not be published publicly unless the project owner/authorized organization permits that sharing**.

Before creating a public GitHub repository, review the repository contents and confirm that any reference documents or sensitive material that should remain private are excluded.

The calculator's configured data should also be treated according to the project's authorization and sharing requirements.

---

## 11. Application Contact Section

The application includes the contact information required for the project's user interface. The README intentionally does not reproduce the detailed contact/reference material here.

---

## 12. Disclaimer

This application is an estimation interface. Final charges, applicable taxes, availability, contractual conditions, tariff revisions, and other commercial matters should be confirmed through the appropriate official channel before any commercial commitment.

---

## 13. Project Status

**Status:** Final development version — pending project/supervisor approval before public repository publication.




