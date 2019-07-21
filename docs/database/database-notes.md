# Database Design

## Admin
* Username (may be email)
* Email
* First, MI, Last Name
* Mobile phone number
* Dashboard
  * University ticket resolution
  * University access (add, remove, suspend, change role, send password reset link)
* Online help/support section available
  * Ticket status changes should be logged here

## University
* Remote access in addition to on campus
* Dashboard (adjustable by time period)
  * Students enrolled
  * Tutor session status (requests, scheduled, complete, incomplete, cancel)
    * Deep dive on each of these all the way down to a specific session
  * Submit ticket to `Admin` for resolution
  * Set student/tutor email reminder timeline (1 hr before - default, 24 hours before, etc...)

## Canvas / Blackboard / etc..
* Link from student page to tutor system

## Courses
* Textbook
* Curriculum link

## Faculty
* Username (may be email)
* Email
* First, MI, Last Name
* Mobile phone number (2FA)
* Ability to send student reminder of tutoring services available
  * Beginning of course
  * After grade drops below threshold
    * Ability to set grade threshold for reminder to students

## Tutor
* Username (may be email)
* Email 
* First, MI, Last Name
* Mobile phone number
* Qualified subjects / level (year?)
* Contact preference (email or text) can be set up for one or both (default to email)
* Chat capability
  * With student (?)
  * With Admin (help/troubleshooting)
* Calendar availability
  * Type of tutoring (Synchronous or Asynchronous)
  * Schedule up to (minimum notification time up to being on-call)
  * Allow recurring availability
* Dashboard
  * Profile
  * Number of sessions
  * Hours worke in a certain time period
  * Upcoming sessions (linked to calendar)

## Student
* Username (may be email)
* Email
* First, MI, Last Name
* Mobile phone number
* Contact preference (email or text) can be set up for one or both (default to email)
* Semester/Year/Date Enrolled at University
* Courses Enrolled in
* Tutor effectiveness - this will require more thought but should be a snapshot of where the student is when they request tutoring and where they are at the end of the semester/course
* Online help/support section available
* Ability to view past tutor session notes and video

## Tutor Session
* Student
* Requested at (timestamp on request)
* Type
* Time (Synchronous) -- via Calendar add on
* Materials (Asynchronous)
  * Questions from the student or the tutor
  * Answers to ^^^ questions
* Tutor
* Status (request, scheduled, active, complete, incomplete, cancel, rescheduled) -- Incomplete, rescheduled and cancel should have a why
  * Timestamp on all status changes with from status, to status, timestamp of change, initiator (student, tutor, admin, system)
  * System should allow a tutor to be automatically assigned to the tutor based on availability
* Student review (teacher rating and content feedback)
* Tutor review (student rating and content feedback)
* Faculty notes
* Admin notes
* Online help/support section available
* Synchronous sessions are automatically stored for (xx years)
* Way to apply for the program from a public facing website
* Last minute issue - 'Help Button' I'm not available, can someone fill in for me?
  * Automatically search, notify and received acknowledgement before reassigning tutor
  * Tutor session will have tutor details (reassigning tutor), but no notifications are necessary unless a tutor is not able to be procured by the time the tutor session should start. This status area should definitely be in the notification area.

## Calendar
* Tutor availability
* System down time restrictions
* Student request options
* Integrated with Google/Outlook/iCal
* Automatic reminders sent out to Student & Tutor (set by University)

### Process/Flow
* Student request tutor by subject/time (not specific tutor)
  * Tutors can be automatically assigned based on availability and ranking system (? FLG -- more thought here)
* Online help such as trouble ticket, chat, etc.. needs more work

### Stories Reviewed
- [X] [Student by Anthony](./stories/anthony-student.md)
- [X] [Admin by Dan](./stories/dan-admin.md)
- [X] [Student by Diana](./stories/diana-student.md)
- [X] [Tutor by Melissa](./stories/melissa-tutor.md)
- [X] [Student by Mikey](./stories/mikey-student.md)
- [X] [Tutor by Mikey](./stories/mikey-tutor.md)
- [X] [Student by Will](./stories/will-student.md)
- [X] [Tutor by Ben](./stories/ben-tutor.md)
