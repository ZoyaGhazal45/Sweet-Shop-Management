# Sweet-Shop-Management
Indian Sweet Shop Management System – A full-stack web application with authentication, inventory control, and e-commerce capabilities.
Project Overview
A TDD-driven full-stack Sweet Shop Management System, developed as part of a technical assessment. This project demonstrates modern development practices, clean code principles, and AI-assisted collaboration.

🚀 Features
User Features
Secure Authentication: Register and login using JWT.
Sweet Catalog: Browse sweets, search, and filter by name, category, or price.
Purchase Functionality: Buy sweets with real-time inventory updates.
Responsive Design: Works seamlessly across mobile, tablet, and desktop.

Admin Features
Inventory Management: Add, edit, delete, and restock sweets.
Dedicated Admin Panel: Full control over sweets and stock.

Tech Stack
Backend:
Node.js + TypeScript
Express.js
PostgreSQL (raw SQL via pg)
JWT + bcrypt for authentication
jest + supertest for testing
express-validator for input validation

Frontend:
React 18 + TypeScript
Vite
React Router v6
Tailwind CSS
Axios for API calls

Prerequisites
Node.js 18+
PostgreSQL 14+
npm or yarn

Backend Setup
cd backend
npm install
cp .env.example .env
# Edit .env with your database credentials
npm run migrate
npm run dev

Frontend Setup
cd frontend
npm install
npm run dev

Running Tests
Backend Tests
cd backend
npm test
npm run test:coverage


Test Credentials:

Admin:
Email: admin@test.com
Password: admin123
Access: Full admin panel

Regular User:
Email: userone@test.com
Password: userone123

Access: Browse and purchase sweets

API Endpoints

Authentication:
POST /api/auth/register - Register a new user
POST /api/auth/login - Login
Sweets (Protected):

GET /api/sweets - Get all sweets
GET /api/sweets/search - Search sweets
POST /api/sweets - Create sweet (Admin)
PUT /api/sweets/:id - Update sweet (Admin)

DELETE /api/sweets/:id - Delete sweet (Admin)
Inventory (Protected):
POST /api/sweets/:id/purchase - Purchase sweet
POST /api/sweets/:id/restock - Restock sweet (Admin)

Testing Approach
Strict TDD Workflow: Followed Red-Green-Refactor pattern.
Coverage: 54 unit and integration tests covering business logic, authentication, and inventory management.
Test Metrics: Coverage above 70% across all metrics.

Design System
Theme: Inspired by traditional Indian sweet shops
Maroon #8B1538 & Gold #D4AF37 accents
Cream background #FFF5ED

Typography:
Headings: Playfair Display
Body: Inter
Aesthetic: Traditional charm meets modern UX

AI Usage in the Project
Tools I Used
I leveraged three main AI tools during this project:
Claude Sonnet 4 – Assisted with architecture decisions and code generation.
GPT-5 – Provided alternative approaches and helped when I got stuck.

How AI Contributed vs What I Did
Backend (70% AI, 30% Me)
AI Contributions:
Generated boilerplate for services and controllers
Suggested PostgreSQL query patterns and TypeScript type definitions

Created test templates
My Contributions:
Designed the database schema
Implemented core business logic
Configured JWT and bcrypt for authentication
Verified and refined API endpoints
Frontend (85% AI, 15% Me)

AI Contributions:
Generated most component structures
Set up API client with Axios
Configured Tailwind CSS and routing logic
Provided form validation and state management patterns

My Contributions:
Chose color scheme and overall design direction
Refined UI/UX and tested responsiveness across devices
Optimized performance

How I Actually Used AI
Asked AI to generate basic structures, e.g., “create an auth service with login and register methods.”
Reviewed and understood the generated code before modifying it to fit project-specific requirements.
Used AI-generated test templates and adapted them to match the business logic.
ey Insight: AI significantly speeds up repetitive and boilerplate tasks, saving roughly 3–4x the time. However, human oversight is crucial for security, architecture, and business logic. Understanding AI-generated code is essential to effectively maintain and debug the system.

🗂 Project Structure
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

🔒 Security

Passwords: Hashed with bcrypt (10 rounds)
Authentication: JWT tokens
Authorization: Role-based access control for admin actions
Input Validation: Prevents SQL injection using parameterized queries and middleware
Protected Routes: All sensitive routes require authentication

✅ Test Results
Backend: 54 passing tests
Coverage: 70%+

Deployment
Backend: Deployed on Render Frontend: Deployed on Vercel
