# PyGuide — Gamified Python Learning Platform

PyGuide is an interactive web application designed to make learning Python more engaging through **structured lessons, hands-on coding exercises, automatic grading, progress tracking, and gamification**.

The platform combines a guided Python curriculum with game-inspired features such as **points, levels, badges, avatars, and leaderboards**, encouraging learners to practice concepts and progress through increasingly advanced material.

## 🎯 Motivation

Many beginner programming platforms introduce concepts without giving learners enough opportunities to apply them. PyGuide was designed around a different approach: combine short, structured lessons with immediate practice, feedback, and visible progression.

The platform breaks Python learning into achievable milestones and rewards users as they advance through the curriculum.

## ✨ Features

- **Structured Python Curriculum** — Lessons progress from beginner to more advanced Python concepts.
- **Interactive Coding Exercises** — Users write Python directly within the application.
- **Automatic Grading** — Submitted solutions are evaluated automatically and users receive immediate feedback.
- **Progressive Lesson Unlocking** — New material becomes available as users complete prerequisite lessons.
- **Progress Tracking** — Completed lessons, scores, and recent activity are stored for each user.
- **Gamification System** — Users earn points, badges, titles, and unlockable avatars.
- **Leaderboard** — Users can compare their progress and scores with other learners.
- **User Profiles** — Profiles display progress, achievements, scores, titles, and selected avatars.
- **Account System** — User accounts and passwords are stored using bcrypt password hashing.

## 🏗️ System Architecture

PyGuide follows a three-layer architecture:

**Frontend**
- HTML/CSS templates
- Interactive lesson and question pages
- In-app Python code editor
- Gamified profile and progress interfaces

**Application Layer**
- Flask web server
- Authentication and session management
- Lesson progression logic
- Code execution and automatic grading
- Scoring, badges, titles, avatars, and leaderboard logic

**Database Layer**
- MySQL/MariaDB
- User accounts and authentication data
- Lesson metadata
- Scores and completed lessons
- User progression and avatar selections

## 🧠 How It Works

Users create an account and are placed into an appropriate starting level. Lessons introduce Python concepts through structured material followed by questions and coding exercises.

When a learner submits code, PyGuide evaluates the solution against predefined tests and provides immediate feedback. Successfully completing lessons updates the user's progress in the database, awards points, and unlocks additional content.

As users progress, they can earn new badges and titles, unlock avatars, and appear on the leaderboard.

## 🛠️ Tech Stack

`Python` `Flask` `SQLAlchemy` `MySQL` `MariaDB` `HTML` `CSS` `bcrypt`

## 📂 Project Structure

```text
PyGuide/
├── static/                 # CSS and avatar assets
├── templates/              # HTML templates and lesson pages
├── pyguide_backend.py      # Flask backend and application logic
├── questions_data.py       # Lesson questions and grading tests
├── pyguide.sql             # Database schema and demo data
├── requirements.txt        # Python dependencies
└── .gitignore
```

## 🚀 Running PyGuide Locally

### 1. Clone the repository

```bash
git clone <repository-url>
cd PyGuide-Python-Learning-Platform/PyGuide
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Set up the database

Install and start **MySQL/MariaDB**. XAMPP can also be used for a simple local MySQL and phpMyAdmin setup.

Create a database named:

```text
pyguide
```

Then import:

```text
pyguide.sql
```

The SQL file creates the required database structure and includes demo users at different stages of the curriculum for testing the application's progression and gamification features.

### 4. Run the application

```bash
python pyguide_backend.py
```

Then open:

```text
http://127.0.0.1:5000/
```

## 🔐 Security

PyGuide uses **bcrypt password hashing** and parameterized SQL queries for account and database operations.

The interactive code runner executes submitted Python in a restricted environment intended for **local educational use**. It is not designed as a production-grade sandbox for executing untrusted code on a public server.

## 🎮 Learning & Gamification

PyGuide uses progression and rewards to encourage continued learning. Users can earn:

- Points for completing lessons
- Achievement badges
- Score-based titles
- Unlockable avatars
- Positions on the leaderboard

Lesson progression is stored in the database so users can return to the application and continue where they left off.

## 🔮 Future Improvements

Future development could include:

- Additional Python levels and advanced topics
- More detailed autograder feedback
- AI-assisted learning and personalized hints
- Collaborative learning features
- Expanded testing and production deployment
- Stronger sandboxing for remote code execution


## 👥 Project Team

PyGuide was developed as a Senior Capstone project at **NYU Tandon School of Engineering** for **CS-UY 4523**.

**Team Members**
- Mariam Rukhaia
- Neel Dahake
- Oleg Vengrovych
- Elsa Mitchell
