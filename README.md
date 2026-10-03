# SafeRide – Smart Bus Tracking & Student Safety Portal

SafeRide is a web-based student transportation management system designed to organize bus operations and support student safety. It provides a centralized platform for managing student details, buses, drivers, routes, trips, GPS records, boarding and alighting information, and transportation alerts.

## Project Overview

The project demonstrates how frontend technologies, backend APIs, and a relational database can work together to manage transportation-related information through a single web application.

## Features

- Student management
- Bus and vehicle management
- Driver information management
- Route management
- Trip management
- GPS and simulated location record handling
- Student boarding and alighting records
- Transportation alert management
- Web-based user interface
- Backend API endpoints
- MySQL database integration
- API testing using Postman

Note: Real-time GPS hardware integration, live map services, external notification delivery, and complete server-side authentication require additional implementation or verification.

## Technology Stack

| Component | Technology |
|---|---|
| Frontend | React.js, Vite, JavaScript, HTML, CSS |
| Backend | Node.js, Express.js |
| Database | MySQL |
| Database Connectivity | mysql2 |
| API Testing | Postman |
| Code Editor | Visual Studio Code |
| Version Control | Git and GitHub |

## System Architecture

The application follows a three-layer architecture:

1. Frontend: Provides the user interface and handles user interactions.
2. Backend: Processes API requests and application logic using Node.js and Express.js.
3. Database: Stores structured transportation information using MySQL.

The frontend communicates with the backend through HTTP API requests, while the backend interacts with the database to perform supported data operations.

## Project Structure

The exact folder structure may vary depending on the project version.

```text
SafeRide/
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── vite.config.js
├── backend/
│   ├── routes/
│   ├── controllers/
│   ├── db.js
│   ├── main.js
│   └── package.json
├── database/
│   └── schema.sql
└── README.md
```

Check the actual project folders and filenames before using this example structure.

## Prerequisites

Install the following software:

- [Node.js and npm](https://nodejs.org/)
- [MySQL](https://dev.mysql.com/downloads/)
- [Visual Studio Code](https://code.visualstudio.com/)
- [Postman](https://www.postman.com/downloads/)

## Installation and Setup

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd SafeRide
```

Replace `YOUR_GITHUB_REPOSITORY_URL` with your actual GitHub repository URL.

### 2. Set Up the Database

Start MySQL and create the database required by the project.

```sql
CREATE DATABASE saferide;
```

If a database schema or SQL setup file is included in the repository, execute it to create the required tables.

### 3. Configure the Backend

Navigate to the backend directory:

```bash
cd backend
npm install
```

Configure the database connection using the environment variable names expected by the backend source code.

Example configuration:

```env
PORT=5000
DB_HOST=localhost
DB_PORT=3306
DB_USER=your_mysql_username
DB_PASSWORD=your_mysql_password
DB_NAME=saferide
```

These variables are illustrative. Use the actual names expected by the project. Never commit real database passwords or other secrets to GitHub.

Start the backend using the script defined in `package.json`. For example:

```bash
npm start
```

Alternatively, if a development script is configured:

```bash
npm run dev
```

### 4. Configure the Frontend

Open a new terminal and navigate to the frontend directory:

```bash
cd frontend
npm install
npm run dev
```

Open the local URL displayed in the terminal, commonly `http://localhost:5173`.

### 5. Test the Backend

Use Postman to send requests to the API endpoints implemented by the backend.

Example health-check request, if supported:

```http
GET http://localhost:5000/health
```

Check the response status and returned data. Test the other available endpoints according to the backend implementation.

## Testing

The following testing methods can be used:

- Postman for backend API testing.
- Browser Developer Tools for frontend debugging and network inspection.
- MySQL queries for validating database records.
- Integration testing for verifying communication between the frontend, backend, and database.

A successful frontend display alone does not guarantee that data is being retrieved from the database. Verify API responses and database records when testing data-backed features.

## Current Limitations

- GPS tracking may rely on simulated location records.
- The current map interface uses a stylized visual rather than a confirmed live mapping service.
- External email, SMS, and push-notification delivery are not confirmed.
- Complete server-side authentication and role-based authorization require verification.
- Production hosting and deployment configuration depend on the deployment environment.

## Future Enhancements

- Real-time GPS tracking using physical GPS devices.
- Interactive maps and live route visualization.
- Estimated bus arrival times.
- Route deviation detection and alerts.
- Emergency SOS functionality.
- Automated email, SMS, and push notifications.
- Stronger authentication and role-based access control.
- Advanced reports and transportation analytics.
- Cloud deployment and performance monitoring.

## Security

- Store database credentials in environment variables.
- Do not upload `.env` files containing secrets.
- Restrict database access to authorized services.
- Validate user input and API requests.
- Use HTTPS when deploying the application publicly.

## Contributing

Contributions and suggestions are welcome. To contribute:

1. Fork the repository.
2. Create a feature branch.
3. Make and test your changes.
4. Submit a pull request describing your improvements.

## License

No license has been specified yet. Add a suitable open-source license if you intend to permit others to reuse, modify, or distribute this project.

## Author

Developed as an academic project focused on student transportation management and safety.

**Project Name:** SafeRide – Smart Bus Tracking & Student Safety Portal
