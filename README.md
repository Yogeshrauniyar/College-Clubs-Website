# College Clubs Website

A full-stack web application for managing college clubs, events, and activities.

## 🌟 Key Features

### For Students
- Browse and join college clubs
- View upcoming events
- Track club activities
- Register for events

### For Admins
- Manage club listings
- Post and update events
- User management
- Content moderation

## 🛠️ Tech Stack

- **Frontend**: React + Vite
- **Backend**: Node.js, Express
- **Database**: MongoDB
- **Authentication**: JWT

## 📷 Screenshots
Initial Admin login 
![Screenshot 2024-11-02 045629](https://github.com/user-attachments/assets/a805dba4-b736-4475-9916-e641dee7e8f1)
Admin Dashboard: Manage CLubs, Manage Events, Add New Admin 
![Screenshot 2024-11-02 045724](https://github.com/user-attachments/assets/8b051580-d885-4b46-b624-704f6634d32a)
HomePage
![Screenshot 2024-11-02 045924](https://github.com/user-attachments/assets/1e04daa6-3217-4b2b-8051-69fcbdfdf26e)
![Screenshot 2024-11-02 050015](https://github.com/user-attachments/assets/ca581ea0-0e66-4cdc-9dcf-95081d95cd19)


## Prerequisites

Before you begin, ensure you have installed:
- [Node.js](https://nodejs.org/) (v14 or higher)
- [MongoDB](https://www.mongodb.com/try/download/community)
- [Git](https://git-scm.com/downloads)

## Installation

1. **Clone the repository**
```bash
git clone https://github.com/Kalpak26/fsd-mini-proj-main
cd fsd-mini-proj-main
```

2. **Set up the backend**
```bash
# Navigate to backend directory
cd backend

# Install dependencies
npm install

# Create .env file
cp .env.example .env
```

3. **Configure environment variables**
Edit the `.env` file in the backend directory:
```env
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
PORT=5000
```

4. **Set up the frontend**
```bash
# Navigate to frontend directory
cd ../vite-project

# Install dependencies
npm install vite@latest (React, Javascript)

# Create .env file
cp .env.example .env
```

**⚙️ Environment Variables**

  ### Backend (.env)
  MONGODB_URI=mongodb://localhost:27017/college-clubs
  JWT_SECRET=your_secret_key
  PORT=5000
  
  ### Frontend (.env)
  VITE_API_URL=http://localhost:5000/api


## Database Setup

1. Create a MongoDB Atlas account or use local MongoDB
2. Create a new cluster (if using Atlas)
3. Get your connection string
4. Add connection string to backend `.env` file

## Data Initialization

### Setting up Initial Data

1. **Prepare CSV Files**
Place your clubs.csv file in the `backend` directory: (a sample clubs.csv is already present)
```
backend/
├── clubs.csv
└── scripts/
    ├── import-clubs.js
    └── import-events.js
```

2. **Install Required Dependencies**
```bash
cd backend
npm install csv-parse
```

3. **Run Initialization Scripts**
```bash
# Make sure you're in the backend directory
cd backend

# Import clubs from CSV
node scripts/import-clubs.js

# Import sample events
node scripts/import-events.js
```

5. **Verify Data Import**
You can verify the data import using MongoDB Compass or the MongoDB Atlas web interface.


## Running the Application

1. **Start the backend server**
```bash
cd backend
npm start
```

2. **Start the frontend development server**
```bash
cd vite-project
npm run dev
```

3. Access the application:
- Frontend: http://localhost:5173
- Backend API: http://localhost:5000

## Project Structure

```
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
```

## Key Features & Usage

1. **Public Features**
   - View all clubs
   - Browse upcoming events
   - View club details
   - Register for events

2. **Admin Features**
   - Manage clubs (add, edit, delete)
   - Manage events
   - User management
   - Content moderation

## Admin Access

To access admin features:
1. Register a new account
2. Use the default admin credentials:
   - Email: admin@example.com
   - Password: admin123

## Common Issues & Solutions

1. **MongoDB Connection Error**
   - Check if MongoDB is running
   - Verify connection string in .env file
   - Ensure network connectivity

2. **Missing Assets**
   - Check if images are in correct directory
   - Verify file paths in components

3. **Authentication Issues**
   - Clear browser cache
   - Check token expiration
   - Verify credentials

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

---
Remember to replace placeholder values with your actual project information before publishing.
