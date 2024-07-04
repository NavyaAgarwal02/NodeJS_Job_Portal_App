# NodeJS Job Portal Application

The **Job Portal application** is a Node.js-based system developed using the Express.js framework, with MongoDB as the chosen database. This application manages information related to job postings and applicants. It exposes specific endpoints to handle CRUD (Create, Read, Update, Delete) operations for both job postings and applicant profiles, providing an efficient platform for job seekers and employers.

## Endpoints

### User
- **Update User:**
  - Endpoint: `PUT /api/v1/user/update-user`
  - Description: Update user's details on job portal.

### Job
- **Create Job:**
  - Endpoint: `POST /api/v1/job/create-job`
  - Description: Create jobs for job seekers (users).

- **Get Jobs:**
  - Endpoint: `GET /api/v1/job/get-job`
  - Description: Enables users to get jobs.

- **Update Jobs:**
  - Endpoint: `PATCH /api/v1/job/update-job/:id`
  - Description: Updates job profile section in app.

- **Delete Jobs:**
  - Endpoint: `DELETE /api/v1/job/delete-job/:id`
  - Description: Delete an existing job.

- **Jobs Stats Filter:**
  - Endpoint: `GET /api/v1/job/job-stats`
  - Description: Enables users to search jobs after application of filters.

### Auth
- **Register User:**
  - Endpoint: `POST /api/v1/auth/register`
  - Description: Register (sign up) new user on app.

- **Login User:**
  - Endpoint: `POST /api/v1/auth/login`
  - Description: Login already registered user.

### Test
- **Tests:**
  - Endpoint: `POST /api/v1/test/test-post`
  - Description: Enables us to test app based on various conditions.

## Data Models

### User
The `User` data model represents information about job seekers.

- **Fields:**
  - `name`: String (User's name)
  - `lastName`: String (User's last name)  
  - `email`: String (User's email address, unique)
  - `password`: String (User's password, must be greater than 6 characters)  
  - `location`: String (User's residance)

- **Example:**
  ```json
  {
    "name": "Harry",
    "lastName": "Khan",
    "email": "harry@gmail.com",
    "password": "123456",
    "location": "America"
  }

### Job
The `Job` data model represents information about jobs available in the company.

- **Fields:**
  - `company`: String (Company's name)
  - `position`: String (Job position)
  - `status`: String (Job status)
  - `workType`: String (Job work type)
  - `workLocation`: String (Company location)
  - `createdBy`: Unique ID to user

- **Example:**
  ```json
  {
   "company": "Google",
   "position": "Head",
   "status": "pending",
   "workType": "full-time",
   "workLocation": "london",
  }

## Usage

1. **Install Dependencies:**
   ```bash
   npm install
