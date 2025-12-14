# Sweet-Shop-Management

Indian Sweet Shop Management System – A full-stack web application with authentication, inventory control, and e-commerce capabilities.

## Project Overview

A TDD-driven full-stack Sweet Shop Management System, developed as part of a technical assessment.
This project demonstrates modern development practices, clean code principles, and AI-assisted collaboration.

## Features
### User Features

Secure Authentication: Register and login using JWT

Sweet Catalog: Browse sweets, search, and filter by name, category, or price

Purchase Functionality: Buy sweets with real-time inventory updates

Responsive Design: Works across mobile, tablet, and desktop

### Admin Features

Inventory Management: Add, edit, delete, and restock sweets

Dedicated Admin Panel: Full control over sweets and stock

## Tech Stack

### Backend:

Node.js + TypeScript

Express.js

PostgreSQL (raw SQL via pg)

JWT + bcrypt for authentication

Jest + Supertest for testing

express-validator for input validation

### Frontend:

React 18 + TypeScript

Vite

React Router v6

Tailwind CSS

Axios

## Prerequisites

Node.js 18+

PostgreSQL 14+

npm or yarn

## Backend Setup
```
cd backend
npm install
cp .env.example .env
# Edit .env with your database credentials
npm run migrate
npm run dev
```
## Frontend Setup
```
cd frontend
npm install
npm run dev
```
## Running Tests
```
#backend test
cd backend
npm test
npm run test:coverage
```

## Test Credentials:

### Admin

Email: admin@test.com

Password: admin123

Access: Full admin panel

### Regular User

Email: userone@test.com

Password: userone123

Access: Browse and purchase sweets

## API Endpoints

### Authentication

POST /api/auth/register - Register a new user

POST /api/auth/login - Login

### Sweets (Protected)

GET /api/sweets - Get all sweets

GET /api/sweets/search - Search sweets

POST /api/sweets - Create sweet (Admin)

PUT /api/sweets/:id - Update sweet (Admin)

DELETE /api/sweets/:id - Delete sweet (Admin)

### Inventory (Protected)

POST /api/sweets/:id/purchase - Purchase sweet

POST /api/sweets/:id/restock - Restock sweet (Admin)

## Testing Approach

Strict TDD Workflow: Followed Red-Green-Refactor pattern

Coverage: 54 unit & integration tests covering business logic, authentication, and inventory management

Test Metrics: Coverage above 70% across all metrics

## Design System

Theme: Inspired by traditional Indian sweet shops

Maroon #8B1538 & Gold #D4AF37 accents

Cream background #FFF5ED

Typography:

Headings: Playfair Display

Body: Inter

Aesthetic: Traditional charm meets modern UX

## AI Usage

### Tools Used

Claude Sonnet 4 – Architecture decisions and code generation

GPT-5 – Alternative approaches and debugging

### Backend (70% AI, 30% Me)

AI: Generated boilerplate for services and controllers, suggested PostgreSQL query patterns, test templates

Me: Designed database schema, implemented business logic, configured JWT & bcrypt, verified API endpoints

### Frontend (85% AI, 15% Me)

AI: Generated component structures, API client setup, Tailwind configuration, routing logic, form validation, state management

Me: Selected color scheme, refined UI/UX, tested responsiveness, optimized performance

Insight: AI speeds up repetitive tasks (~3–4x faster), but human oversight is essential for security, architecture, and business logic.

## Project Structure
```
meethi-dukaan/
├── backend/
│   ├── src/
│   │   ├── controllers/      # Request handlers
│   │   ├── services/         # Business logic
│   │   ├── middleware/       # Auth & validation
│   │   ├── routes/           # API routes
│   │   ├── database/         # DB connection & migrations
│   │   ├── types/            # TypeScript types
│   │   └── __tests__/        # Test suites
│   └── package.json
├── frontend/
│   ├── src/
│   │   ├── components/       # Reusable components
│   │   ├── pages/            # Route pages
│   │   ├── context/          # React Context
│   │   └── services/         # API client
│   └── package.json
└── README.md
```

## Security

Passwords hashed with bcrypt (10 rounds)

JWT-based authentication

Role-based access control for admin actions

Input validation & parameterized queries to prevent SQL injection

Protected routes for sensitive operations

## Test Results

Backend: 54 passing tests

Coverage: 70%+

## Deployment

The project is live and accessible:

Environment	Link	Description
Backend	Render
	API server handling authentication, inventory, and business logic
Frontend	Vercel
	Fully responsive React app for browsing and purchasing sweets

Use the test credentials above to explore admin and user features.
Note: Frontend communicates directly with the backend API, updating inventory in real-time
