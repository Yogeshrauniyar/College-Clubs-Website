College Clubs Website
A full-stack web application for managing college clubs, events, and activities.

🌟 Key Features
For Students
Browse and join college clubs
View upcoming events
Track club activities
Register for events
For Admins
Manage club listings
Post and update events
User management
Content moderation
🛠️ Tech Stack
Frontend: React + Vite
Backend: Node.js, Express
Database: MongoDB
Authentication: JWT
📷 Screenshots
Initial Admin login Screenshot 2024-11-02 045629 Admin Dashboard: Manage CLubs, Manage Events, Add New Admin Screenshot 2024-11-02 045724 HomePage Screenshot 2024-11-02 045924 Screenshot 2024-11-02 050015

Prerequisites
Before you begin, ensure you have installed:

Node.js (v14 or higher)
MongoDB
Git
Installation
Clone the repository
git clone https://github.com/Kalpak26/fsd-mini-proj-main
cd fsd-mini-proj-main
Set up the backend
# Navigate to backend directory
cd backend

# Install dependencies
npm install

# Create .env file
cp .env.example .env
Configure environment variables Edit the .env file in the backend directory:
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
PORT=5000
Set up the frontend
# Navigate to frontend directory
cd ../vite-project

# Install dependencies
npm install vite@latest (React, Javascript)

# Create .env file
cp .env.example .env
⚙️ Environment Variables

Backend (.env)
MONGODB_URI=mongodb://localhost:27017/college-clubs JWT_SECRET=your_secret_key PORT=5000

Frontend (.env)
VITE_API_URL=http://localhost:5000/api

Database Setup
Create a MongoDB Atlas account or use local MongoDB
Create a new cluster (if using Atlas)
Get your connection string
Add connection string to backend .env file
Data Initialization
Setting up Initial Data
Prepare CSV Files Place your clubs.csv file in the backend directory: (a sample clubs.csv is already present)
backend/
├── clubs.csv
└── scripts/
    ├── import-clubs.js
    └── import-events.js
Install Required Dependencies
cd backend
npm install csv-parse
Run Initialization Scripts
# Make sure you're in the backend directory
cd backend

# Import clubs from CSV
node scripts/import-clubs.js

# Import sample events
node scripts/import-events.js
Verify Data Import You can verify the data import using MongoDB Compass or the MongoDB Atlas web interface.
Running the Application
Start the backend server
cd backend
npm start
Start the frontend development server
cd vite-project
npm run dev
Access the application:
Frontend: http://localhost:5173
Backend API: http://localhost:5000
Project Structure
college-clubs-website/
├── backend/
│   ├── models/         # Database models
│   ├── routes/         # API routes
│   ├── middleware/     # Custom middleware
│   └── server.js       # Main server file
│
└── vite-project/
    ├── src/
    │   ├── components/ # React components
    │   ├── pages/      # Page components
    │   ├── assets/     # Static assets
    │   └── styles/     # CSS files
    └── index.html
Key Features & Usage
Public Features

View all clubs
Browse upcoming events
View club details
Register for events
Admin Features

Manage clubs (add, edit, delete)
Manage events
User management
Content moderation
Admin Access
To access admin features:

Register a new account
Use the default admin credentials:
Email: admin@example.com
Password: admin123
Common Issues & Solutions
MongoDB Connection Error

Check if MongoDB is running
Verify connection string in .env file
Ensure network connectivity
Missing Assets

Check if images are in correct directory
Verify file paths in components
Authentication Issues

Clear browser cache
Check token expiration
Verify credentials
Contributing
Fork the repository
Create your feature branch
Commit your changes
Push to the branch
Create a Pull Request
