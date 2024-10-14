Project Overview
This project designs a MongoDB database for a hypothetical Zen Class Program, managing various aspects such as students, tasks, attendance, company drives, and mentors. The goal is to efficiently store and query data for insights, such as user performance, placement statistics, and program engagement.

Database Collections and Structure
Users
Stores information about students enrolled in the program.
Fields: _id, name, email, mentor_id

Codekata
Tracks the number of coding problems solved by each user.
Fields: _id, user_id, problems_solved

Attendance
Logs student attendance for each session.
Fields: _id, user_id, status (present/absent), date

Tasks
Records tasks assigned to students for each topic and tracks submission status.
Fields: _id, topic_id, user_id, name, submitted (true/false), date

Topics
Stores topics covered during the program, along with the date they were taught.
Fields: _id, name, date

Company Drives
Tracks placement drives organized for students and logs participants.
Fields: _id, company_name, date, students_appeared

Mentors
Stores mentor information and their mentee count.
Fields: _id, name, mentee_count

Queries Implemented
Find all topics and tasks taught in October
Query the topics and tasks collections for records where the date falls within October.

Find all company drives between 15-Oct-2020 and 31-Oct-2020
Retrieves company drives held in the specified date range.

Find all company drives and students who appeared for placement
Joins the company_drives and users collections to list students who attended each placement drive.

Find the number of problems solved by each user in Codekata
Aggregates the codekata collection to summarize the problems solved per user.

Find all mentors with mentees count greater than 15
Searches the mentors collection for mentors with more than 15 mentees.

Find the number of users who were absent and did not submit tasks between 15-Oct-2020 and 31-Oct-2020
Uses attendance and tasks collections with a lookup and match to find students who were absent and did not submit tasks within the given date range.

