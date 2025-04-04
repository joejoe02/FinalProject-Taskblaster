# Task Blaster

This is my final project for the Web APIs course. The assignment was to implement a full-stack task management platform inspired by systems like Trello and JIRA. The project combines several core concepts including API development, authentication, background processing, and notifications.

## Technologies used

- ASP.NET Core (.NET 8)
- Entity Framework Core
- PostgreSQL
- Next.js
- Auth0 (regular and M2M authentication)
- Hangfire (for background jobs)
- Mailjet (for sending email notifications)
- Docker and Docker Compose

## Features

- REST API for managing tasks, users, tags, comments, priorities, and statuses
- Token-based authentication using Auth0
- Automatic creation of users on login
- Background job setup using Hangfire to send task reminders
- Email notifications using Mailjet
- Support for protected internal API calls via M2M Auth0
- Docker support for all services
- CI/CD pipeline setup (Azure DevOps)


## Setup

1. Fill in the required Auth0 credentials in `.env.local` for the frontend.
2. Configure `appsettings.json` files with connection strings and secrets for the API and notification services.
3. Use `docker-compose up --build` to start all services.

## Notes

- Hangfire jobs run every 30 minutes to send due date and follow-up reminders via email.
- New users are added to the database automatically the first time they log in.
- Sensitive values like Auth0 keys and Mailjet API keys are not included in the repository and should be provided locally.

