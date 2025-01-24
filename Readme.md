# Country Capital Quiz App

A simple **Country Capital Quiz App** built with **Node.js**, **Express**, **PostgreSQL**, and **EJS**. The app fetches quiz data from a PostgreSQL database and allows users to test their knowledge of world capitals.

---

## 🚀 Features

- Randomly generates quiz questions using data stored in a PostgreSQL database.
- Tracks the user's total correct answers during the session.
- Displays a question, accepts user input, and evaluates answers.
- Renders dynamic web pages using **EJS** templating.

---

## 📋 Prerequisites

Before running the project, ensure the following tools are installed:

- [Node.js](https://nodejs.org/) (v14 or higher recommended)
- [PostgreSQL](https://www.postgresql.org/) (v12 or higher)
- A PostgreSQL database named `world` with a `capitals` table (see setup instructions below).

---

## 📂 Database Setup

1. **Create the Database**:
   - Open your PostgreSQL client and create a database named `world`:
     ```sql
     CREATE DATABASE world;
     ```

2. **Create the `capitals` Table**:
   - Use the following SQL to create the required table:
     ```sql
     CREATE TABLE capitals (
       id SERIAL PRIMARY KEY,
       country VARCHAR(100) NOT NULL,
       capital VARCHAR(100) NOT NULL
     );
     ```

3. **Insert Data**:
   - Add some sample data to the table:
     ```sql
     INSERT INTO capitals (country, capital) VALUES 
     ('France', 'Paris'),
     ('United Kingdom', 'London'),
     ('United States of America', 'Washington, D.C.'),
     ('Japan', 'Tokyo'),
     ('India', 'New Delhi');
     ```

---

## 🔧 Installation and Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/selenophile1805/CapitalGuessQuiz.git
   cd CapitalGuessQuiz-main
2. Install Dependencies
    npm install
3.Update database credentials in index.js:
    Locate the pg.Client setup:
    const db = new pg.Client({
    user: "your-username",
    host: "localhost",
    database: "world",
    password: "your-password",
    port: 5432,
    });

    Replace your-username and your-password with your PostgreSQL credentials.

## 🛠️ Running the Application
    
1. Start your PostgreSQL server.
2. Running the Application:
    node index.js
3. Open your browser and visit:
    http://localhost:3000
    

## 📄 Usage

1. A random country will be displayed when you visit the app.
2. Enter the capital of the displayed country and submit your answer.
3. The app will inform you whether your answer was correct and update the score.
4. A new question will appear after each submission.

## 🖼️ Screenshots

![alt text](<Screenshot 2025-01-24 at 10.55.08 AM.png>)

## 📄 File Structure

project-folder/
├── public/                 # Static assets (CSS, images, etc.)
├── views/
│   └── index.ejs           # Main HTML template
├── index.js                # Application entry point
├── package.json            # Project dependencies
└── README.md               # Project documentation

## 🛠️ Technologies Used:

1. Node.js: JavaScript runtime for server-side development.
2. Express.js: Framework for building web applications.
3. PostgreSQL: Relational database to store country-capital data.
4. EJS: Template engine for rendering dynamic web pages.
5. Body-Parser: Middleware for parsing incoming request bodies.


## ✨ Future Enhancements 

1. Add user authentication for personalized quiz sessions.
2. Include a leaderboard for displaying top scores.
3. Improve UI design with CSS frameworks like Bootstrap or Tailwind CSS.

## 👩‍💻 Author

- **Chetan Dongare**  
  [GitHub Profile](https://github.com/selenophile1805)  
  [LinkedIn Profile](https://www.linkedin.com/in/chetan-dongare-01854022b/)

Feel free to customize this file further based on your needs! Let me know if you'd like additional help. 😊





