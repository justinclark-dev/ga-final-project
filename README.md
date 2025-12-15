# General Assembly - Final Project

## Job Application Tracker

Tech Stack:
**Frontend:** [https://github.com/justinclark-dev/job-tracker-ui](https://github.com/justinclark-dev/job-tracker-ui)<br>
**Backend:** [https://github.com/justinclark-dev/job-tracker-api](https://github.com/justinclark-dev/job-tracker-api)

### MVP
A job application tracker that I can use to apply for jobs and keep track of where I'm at in the application process for all jobs that I apply for. Core functionaility will be basic CRUD for adding job application detials 

#### Tech Stack:

Frontend: built with TypeScript/React (with React Routes)<br>
Backend: built with Java/Spring Boot (Python/Django as Backup)<br>
Database: PostgreSQL<br>

#### Core Features:
* Track job applications with details like company name, position, date applied, status (Bookmarked, Applied, Interviewing, Offer, Rejected)
* Add, edit, and delete job applications
*	View applications in a table/list format
* Filter and search functionality
*	User authentication with CSRF tokens so multiple users can track their own applications
*	Document uploads for different resume versions and cover letters
*	Interview schedule tracking for interview dates and times

#### Models:<br>
users 
* id
* username
* email
* password_hash

job_applications
* id
* user_id
* company_name
* position_title
* job_description
* status (bookmarked, applied, interviewing, offer, rejected)
* date_applied
* salary_range
* location
* notes

documents
* id
* job_application_id
* document_type (resume, coverletter)
* file_name
* file_path
* file_size
* uploaded

interviews
* id
* job_application_id
* interview_type (phone, video, onsite)
* scheduled_date
* duration
* notes
* reminder

follow-ups
* id
* job_application_id
* follow_up_type (application, interview, thnk_you, networking)
* method (phone, email, linkedin)
* contact_name
* contact_email
* subject_line
* message
* notes
* date_sent

### Level-ups (time permitting)
* JWT for securing stateless REST API
* API integration (or possibly web scraping) to import open jobs.
* Email reminders for follow-ups and upcoming interviews.
* AI integration for customizing Resumes and Cover Letters to specific job applications.
* Basic statistics dashboard (e.g., number of applications by status)

## Wordpress
A basic Portfolio Website