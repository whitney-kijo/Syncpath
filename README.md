# Rongo University Postgraduate Project Tracker

A full-stack project tracking system for Rongo University postgraduate students, supervisors, and administrators, integrating AI-assisted correction workflows and milestone tracking.

---

## Team Members & Roles

| Name                 | Role                     | Responsibilities |
|----------------------|-------------------------|-----------------|
| Excels Kennedy       | Team Lead / Fullstack    | Oversees the project; coordinates team; writes database schema and migration files; resolves blockers; implements the student  state machine; final integration, testing, and QA |
| Japheth Some         | Backend Developer (Java) | Handles backend logic in Java; integrates APIs; supports database setup; builds business logic for modules B, D, and E |
| Jemimah Njee         | Frontend Developer       | Implements UI using HTML, CSS, JS; ensures responsiveness; connects frontend with backend; implements role-based routing and protected pages; builds dashboards for all 5 user roles |
| Whitney Macharia     | AI / DevOps Engineer     | Develops AI transcript-to-corrections ; handles AI prompts and parses API responses; implements all notification logic; manages GitHub branches, PRs, merges, and tags; leads deployment to hosting platform |

---

## Tech Stack

- **Frontend:** HTML, CSS, JavaScript  
- **Backend:** Java, Django (Python)  
- **Database:** MySQL (XAMPP / phpMyAdmin)  
- **Version Control:** Git & GitHub  

---

## Project Management (GitHub Issues)

All core features and tasks have been broken down into GitHub Issues, labelled, and assigned to team members for structured development and tracking.

### Current Issues

| Issue # | Title |
|--------|------|
| #1 | Repository scaffolding and CI/CD (Day 1) |
| #2 | Pipeline Tracker & Seminar Booking |
| #3 | Database Schema & Finance ERP Mock |
| #4 | AI Meeting Minutes & Correction Extractor |
| #5 | Digital Assessment Rubric |
| #6 | Multi-Level Approval Workflow |
| #7 | Document Submission |
| #8 | System Testing |

---

## Workflow

- Tasks are managed using GitHub Issues  
- Each issue is assigned to a team member  
- Progress is tracked using a project board:
  - Backlog  
  - In Progress  
  - Review  
  - Done  
- Pull Requests are used for code review before merging  

---

## Current Progress & Achievements

### Backend (Django)
- Set up models for:
  - `User`, `Student`, `PipelineStage`, `Milestone`, `StudentProgress`,  
    `Submission`, `Feedback`, `Correction`, `CorrectionItem`, `Notification`
- Implemented **student pipeline state machine** to track progress from Concept Note → Graduation.
- Built a **seed command (`seed_rongo_data`)** to populate users, students, milestones, submissions, feedback, corrections, and notifications.
- Integrated role-based access and protected views.

### Frontend / Dashboard
- Developed **student dashboard** showing:
  - Submissions and feedback
  - Milestones (done, active, pending)
  - Notifications (latest 5)
  - Progress tracker with dynamic pipeline steps
  - Pending tasks and tasks due this week
- Connected dashboard with backend via Django views and templates.

### AI Module
- Correction pipeline for parsing AI-generated corrections.
- Linking `Correction` and `CorrectionItem` with student submissions.
- Basic notifications triggered for corrections.

### Notifications System
- Created model and backend logic for sending notifications to users.
- Seeded initial notifications upon database setup.

---

## Database Seeding

To quickly populate the database, run:

```bash
python manage.py seed_rongo_data
