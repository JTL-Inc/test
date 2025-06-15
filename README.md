🧪 Senior Fullstack Developer Take-Home Test


📘 Overview
Build a small event management system using a Node.js + Express + Knex backend and a Next.js frontend. The focus is on showcasing your architecture skills, code quality, and how you think through fullstack development challenges.

    ⚠️ You do not need to complete everything. Prioritize writing clear, well-structured, and intentional code.

📦 Requirements
🖥 Backend
✅ Tech Stack
Node.js with Express

Use Knex.js for database interactions


Use any relational DB (e.g. PostgreSQL, MySQL, SQLite)


📂 API Endpoints
Method	Route	Description
GET	/events	Paginated, searchable, sortable list of events
GET	/events/:id	Detailed view of a specific event
POST	/events	Create a new event
PUT	/events/:id	Edit an existing event


🧱 Architecture Guidelines
Follow a clean, scalable architecture, e.g.:

Controller → Service → Repository

Ports & Adapters (Hexagonal)

Organize your code so the database can be swapped (e.g., PostgreSQL to MySQL) with minimal code changes, ideally only at the repository layer.


🧪 Data Seeding
You must seed the database with 5,000 – 10,000 records


Use any data generation library (e.g., faker, @ngneat/falso, etc.)


Provide a seeding script or mechanism in your submission


❗ Do not include pre-generated data files. Instead, include code to generate and insert data dynamically.


🎨 Frontend
✅ Tech Stack
Next.js (App Router or Pages Router — your choice, explain why)

📋 Features
Display all events in a paginated table


Implement:

Search

Sort (by any column)

Filter (e.g., by organizer, venue, tags, date range)


Clicking an event opens a detailed view page


Create a dedicated page to add a new event


✅ Bonus: Add testing with any frontend testing tool (e.g., React Testing Library, Playwright, Cypress)

🧱 Sample Database Schema
Here’s a suggested relational schema:

events
Column	Type	Description
id	UUID / Int	Primary key
title	String	Event name
description	Text	Event details
date	DateTime	Date of event
venue_id	UUID / Int	FK → venues.id
organizer_id	UUID / Int	FK → organizers.id
created_at	Timestamp	Auto-generated timestamp

organizers
Column	Type	Description
id	UUID / Int	Primary key
name	String	Organizer name
contact	String	Email or phone

venues
Column	Type	Description
id	UUID / Int	Primary key
name	String	Venue name
location	String	City / address

event_tags (Many-to-many)
Column	Type	Description
event_id	UUID / Int	FK → events.id
tag	String	e.g., "Tech", "Music"


🧪 Optional Testing
Backend: Jest, Supertest, or your preferred framework

Frontend: React Testing Library, Cypress, Playwright, etc.


📄 What To Include in Your README
Please include a short write-up (README.md) with:

🧠 Design and architectural decisions

🔧 Setup instructions (both backend & frontend)

📊 Why you chose your stack/tools/patterns

🧪 (Optional) Your testing strategy

🚧 What you'd do next if given more time

🕐 Time Expectation
We care more about how you structure and write your code than about feature completeness.

Focus on:

Code clarity

Intentional architecture

Thoughtful abstraction

📬 Submission
Push your code to a public GitHub repo

Provide instructions for:

```bash
npm install && npm run dev
```

Include scripts or commands to:

Run migrations

Seed the database with dynamic dummy data.

Succes!