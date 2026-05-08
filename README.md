📋 Table of Contents

Overview
Features
Tech Stack
Project Structure
Getting Started
Author


🎯 Overview

UpTask is a project management web application that allows users to create projects, add tasks, assign statuses and track their progress through a clean dashboard. Built with a custom PHP MVC architecture without external frameworks, demonstrating strong fundamentals in server-side development, OOP and relational database design.

✨ Features

ModuleDescription🔐 AuthenticationUser registration, login and password recovery via email📁 ProjectsCreate, edit and delete projects with name and description✅ TasksAdd tasks to projects with custom names and status tracking🔄 Status managementMark tasks as pending, in progress or completed👤 User dashboardPersonalized view showing all owned projects📧 Email integrationAccount confirmation and password reset emails

🛠️ Tech Stack

LayerTechnologyBackendPHP 8 (custom MVC, no framework)FrontendHTML5, CSS3, JavaScript (ES6+), AJAXStylingSASS / SCSS compiled with GulpDatabaseMySQL (relational, normalized schema)RoutingCustom PHP RouterBuild ToolGulp 4

📁 Project Structure

UpTask/
├── classes/            # Base classes: Model, Router, Email
├── controllers/        # Controllers: ProjectController, TaskController, UserController
├── includes/           # Shared: header, footer, database config
├── models/             # Model classes with MySQL CRUD operations
├── public/             # Entry point (index.php) + compiled assets
│   └── build/          # Compiled CSS/JS
├── src/
│   └── scss/           # SASS source files
├── views/              # PHP HTML templates
│   ├── auth/           # Login, register, forgot-password views
│   ├── dashboard/      # Project list and detail views
│   └── tasks/          # Task management views
├── Router.php          # Main router
├── gulpfile.js         # Build tasks
└── package.json

🚀 Getting Started

Prerequisites

PHP 8.0+
MySQL 8+
Composer
Node.js + npm

Installation
bash# 1. Clone the repository
git clone https://github.com/LuisAOL2003/UpTask.git
cd UpTask

# 2. Install PHP dependencies
composer install

# 3. Install Node dependencies and compile SASS
npm install && npx gulp
Database Setup
sql-- Create the database
CREATE DATABASE uptask_db;

-- Import schema
-- mysql -u root -p uptask_db < database/uptask.sql
Configure Database
Edit the database config file in includes/:
phpdefine('DB_HOST', 'localhost');
define('DB_USER', 'root');
define('DB_PASS', '');
define('DB_NAME', 'uptask_db');
Run
Point your local server to the project root and visit:
http://uptask.test/ or http://localhost/UpTask/public

👤 Author
Luis Ojeda — Full Stack Developer

🌐 portafolio-luis-ojeda.vercel.app
💼 LinkedIn
🐙 GitHub @LuisAOL2003
