# Bajaj Finserv Health | Java Assignment – Qualifier 1

## 🚀 Project Overview

This is a Spring Boot application built as part of the Bajaj Finserv Health Qualifier 1 (Java) assessment.

The application:

- Sends a POST request on startup to generate a **webhook** and receive a **JWT access token**.
- Based on the `regNo`, dynamically determines and solves a SQL query problem.
- Submits the SQL query to the webhook using the **JWT in the Authorization header**.

---

## 📌 Problem Statement

> **Task:** Automatically fetch a SQL problem based on the `regNo`, solve it, and post the final SQL query to a webhook.

**Workflow:**

1. Send a POST request to `generateWebhook/JAVA` with:
   ```json
   {
     "name": "John Doe",
     "regNo": "REG12347",
     "email": "john@example.com"
   }
Receive:

    webhook URL

    accessToken (JWT)

Based on the last two digits of regNo, determine:

    Odd → Question 1 → Question 1 PDF

    Even → Question 2 → Question 2 PDF

Submit the final SQL query to the webhook using:

    POST <webhook_url>

    Header: Authorization: Bearer <accessToken>

    Body:

{
  "finalQuery": "YOUR_SQL_QUERY_HERE"
}
