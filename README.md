# EduTech
## Student Management Software /LMS


## ***Things to take note of***

- Business model and Business Logic.
- Area of specialization.
- objectives and what Impact are we going to create or what problems are we gonna solve with the application.
- Our target audience.

## Business Model

### Base Model/Entity

- Id
- CreatedAt
- UpdatedAt
- IsDeleted

### Schools

- School name
- Address
- School Type
- Subscription
- IsSuspended
- IsDeactivated

### School Type

- Creche
- Primary School
- Secondary School
- Tertiary Institution.

### Subscription

- Payment Method (Credit Card, Debit card, cryptocurrency)
- Amount paid per month/year
- subscriptionId
- schoolId
- subscriptionDate
- expirationDate
- isActive

### Payment Method

- Credit Card
- Debit Card
- Cryptocurrency

### Transactions

- TransactionId
- schoolId
- UserId(optional)
- madeBy
- amount
- paymentFor

### 1. Users

- Students
  - UserId
  - First name
  - Middle Name
  - Last name
  - BirthDate
  - Gender
  - ParentId
  - ClassId
  - ResultId
  - Bio
  - Email Address
  - Password
  - Phone Number(Optional)
  - Street Name
  - House number
  - City
- Admin
  - UserId
  - Full name
  - Username
  - Password
  - Address
  - Bio
  - Role

- Teachers
  - Full Name
  - Email Address
  - Phone number
  - Address
  - Courses taught by the teacher (Many to Many with subjects).

- Subjects/Courses
  - Id
  - Subject
  - TeacherId
  - SchoolType
  - forWhichGradeOfStudent

- Results
  - Id
  - Grade
  - Remarks
  - Subjects
  - Students that submitted their assessments.
    - Their names
    - Grades
      - StudentId <-> Student Information
      - Grade: *Teachers can see all students scores, but parents can only see their children's reports, same is applicable to students, they can only see their own reports*. We can Introduce a feature for student to request to view another students report by submitting a view ones request from the student.

- Classes
  - Id
  - ClassName
  - RoomNumber
  - TeacherId <-> Teacher Information

- Parents / Guardians
  - UserId
  - Child's full name
  - Contact details
  - Students they are related to.

### Messages

Messages will be sent between users, teachers and parents. They can also be sent from the system about important announcements or notifications.

- GroupId (Optional)
- SenderUserId
- RecipientUserId
- MessageText
  
### 2. Exams

- Students
- Teachers
- Administrators
- Marking system (marks, grades)

### 3. Results

- Student
- Parents/Guardians
- Exam
- Subjects

## User Roles

- Student
- Teacher
- Staff
- Admin
- Super Admin

## Business Logics
 <!-- will come to this later. 
 Here I just need to elaborate about the flow of the application and everything we need to implement with the business model drafted at the top. -->

## Area of Specialization

We are going to focus mainly on this two: Creche/Primary School students and Secondary school students but we might also provide such features for university students as well.

The app will be focused on providing an easy way for students to access their results from exams in a structured manner.

### Our Objectives

- To automate the process involved in managing students.
- Provide a system to track the performance of each students.
- A platform to help both the teachers and the students  communicate effectively about their studies.
- Facilitate easy access to results for all stakeholders.
- Promote academic integrity by providing tools that can assist in detecting plagiarism and cheating attempts.

**Impact:**

- Increase efficiency by reducing manual workload.
- Improve communication between teachers and students.
- Enhance transparency and accountability.
- Promote academic success through effective learning strategies.

### Features

### *Users & Authentication*

1. Registration / Login Page

- Allow users to register or login with valid credentials.
- Display user profiles upon successful authentication.
    
### *Students*

2 .Dashboard

- Showcase student's profile information.
- List subjects enrolled.
 View marks obtained in each subject.
- Access study materials provided by teachers.
   
### *Parents/Guardians*

1. Communication Channel 

   - Send messages to classmates, teachers, or parents.
   - Receive notifications from teachers regarding updates on your child’s progress.
   
2. Marksheet Generation
   - Generate marksheets at regular intervals (e.g., end of term).
   - Make available for download.
   
3. Attendance Tracker
   - Track attendance regularly.
   - Generate attendance reports for parents.

4. Class Management
   - Manage classes and assignments.
   - Add/remove students from a class.
   - Upload study materials for students.
   - Assign tasks/quizzes to individual or multiple students.
   - Provide feedback on submissions.
   
5. Student Progress Reporting

   - Monitor overall academic performance.
   - Keep track of academic progress over time.
   - Get comprehensive reports on a student’s performance over time.

### *Teachers*

6. Courses & Subjects
   - Create new courses and add/remove subjects within them.
   - Set up assessment criteria for each subject.
   - Distribute study materials to all students in the course.
   - Record grades given out for each assessment criterion.
   - Provide feedback on assignments submitted by students.

### *Optional*

7. Classroom Tools
   - Use collaborative tools like Chat room/Group Chat for discussions during lessons.
   - Share resources such as articles, videos, or documents relevant to the topic being taught.

## Our Target Audience

Our target audience is primarily parents and schools that want their children/students to learn independently but also have access to educational materials with guides from teachers and parents.

We are on a mission to providing  an easy-to-use platform that is accessible  to both teachers and students. We aim to create a platform to automate the processes involved in setting, marking and calculating students performance manually.

We want to make learning very easy and a day-to-day activities to students. With this software, we are trying to kill two bird with one stone, because in this our present generation technology tend to provide both good and bad effect on our children. Children and youths use all this modern devices to browse daily, scrolling and navigating from one social media to the other, downloading both relevant and irrelevant contents instead of using the time to read and do their assessments.

Our software will not only help both parents and teachers pave a way for their child's education but also provide an easy platform where they can now spend time with that same device without giving them access to other softwares that will distract them or channel their energy in the wrong direction.
