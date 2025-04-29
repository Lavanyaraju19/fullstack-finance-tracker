💰 Full-Stack Finance Tracker
A full-stack finance tracking application built with React (frontend) and Node.js (backend), using PostgreSQL as the database. It helps users manage their income, expenses, and savings with intuitive dashboards, charts, and CRUD operations. Dockerized and orchestrated with Docker Compose.

Building a Personal Finance Management App: Integrating REST API, Node.js, Express.js, TypeScript, PostgreSQL, and Docker
This is the code for the blogs

Building a Personal Finance Management App: Database Setup with PostgreSQL and Docker.

Building a Personal Finance Management App: Integrating REST API, Node.js, Express.js, TypeScript and Docker

🚀 Tech Stack

| Layer        | Tech Stack                      |
|--------------|---------------------------------|
| Frontend     | React.js, Bootstrap             |
| Backend      | Node.js, Express.js             |
| Database     | PostgreSQL                      |
| Auth         | JWT, bcrypt                     |
| Deployment   | Docker, Docker Compose          |
| DevOps       | GitHub Actions (CI/CD ready)    |

---

✨ Features

-  Authentication: Secure login & registration with JWT-based auth.
-  Role-Based Access: Admin and user privileges for transaction control.
-  Transaction Management: Add, view, edit, and delete income/expense logs.
-  Finance Dashboard: Visualize data with charts and real-time summaries.
-  Category Tracking: Monitor expenses by category (e.g., groceries, rent).
-  RESTful APIs: Modular routes and clean controller-based API logic.
-  Dockerized: Easily deployable with Docker & Docker Compose.

I chose to create a finance app because I was in search of a robust solution for documenting and managing my finances. 
The goal was to move away from the current approach of using multiple, extensive Excel spreadsheets, and instead, consolidate everything into a single, efficient platform.

App Structure

The application consists of the 3 components

- Backend: NodeJS, ExpressJS, Typescript
- Database: PostgreSQL, node-pg-migrate
- Frontend: ReactJS, Typescript

Backend and Frontend communicate via a basic `RestAPI`

All the components are containerized in `Docker` containers.

To run the project you first need to clone the repo
```
git clone {repo}
```

Then to start the containers you run

```
docker-compose up -d
```

you can also build your container by
````
docker-compose up --build
````

eventually you can access the frontend from

http://localhost/3001

if you want to shutdown the process then use
````
docker-compose down 
````
or
````
docker-compose down -v
````
to remove the data volumes

Change the port in docker-compose for `frontend` if `3001` is blocked for any reason.***

 Demo
Below is how the dashboard looks like with some demo data

Currency is hardcoded as danish crowns (DKK) in the frontend


 Backend/Database
Backend communicates with Frontend via a REST API and stores the data in PostgeSQL.

The Data model consists of 3 tables that contain all the relevant information for the dashboard.

Transactions: The day to day expenses and income

Expense Categories: The main expenses areas (eg. Personal running costs)

Expense Types: More detailed expenses that belong to one of the main categories (eg. Restaurants)

![](images/financeDM.png)


Frontend

The template, idea and resources for this dashboard were inspired by the following repo and corresponding youtube tutorial

Github: https://github.com/ed-roh/finance-app

Youtube: https://www.youtube.com/watch?v=uoJ0Tv-BFcQ

 Future Improvements
📱 Add mobile-friendly PWA support

🔍 Search & filter functionality

📤 Export transactions as PDF/CSV

📈 Weekly/monthly financial goals

🛡 Integrate unit & integration tests

 License
MIT License. 

🧑‍💻 Author
Lavanya J.
Bangalore, India
LinkedIn | GitHub


