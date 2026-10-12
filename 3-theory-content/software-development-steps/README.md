---
icon: book
cover: >-
  https://images.unsplash.com/photo-1512758017271-d7b84c2113f1?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwxfHxzb2Z0d2FyZSUyMGFnaWxlfGVufDB8fHx8MTczOTQ5MTY3NXww&ixlib=rb-4.0.3&q=85
coverY: 0
---

# Software Development Steps

{% hint style="info" %}
### **Learning Intention:**

* Explore fundamental software development steps used by programmers when designing software.
{% endhint %}

{% hint style="success" %}
### Success Criteria

* I can correctly order the software development steps.
* I can describe the purpose and key activities involved in each software development step, from requirements definition to maintenance.
* I can explain how each step (such as design, development, and testing) contributes to building functional and reliable software.
* I can identify the importance of each step and how they work together to ensure a successful software project.
{% endhint %}

### Fundamental Software Development Steps

When designing software, programmers will complete the following steps:

* requirements definition
* determining specifications
* design
* development
* integration
* testing and debugging
* installation
* maintenance



Software development is a structured process used by programmers to design, build, and maintain software systems. Following a clear development process ensures that software meets user needs, functions correctly, and can be maintained over time. While different development models exist, most software projects follow a set of fundamental steps.

These steps are: requirements definition, determining specifications, design, development, integration, testing and debugging, installation, and maintenance.

In modern software projects, online code collaboration tools also play an important role in supporting these stages.

### **Requirements Definition**

The **requirements definition** stage involves identifying and documenting what the software must do. This is achieved by consulting with stakeholders such as users, clients, and project managers. Functional requirements describe what the system should do (for example, tracking user data), while non-functional requirements outline constraints such as performance, security, usability, and reliability. Clearly defining requirements reduces ambiguity and helps ensure the final product meets user expectations. Poorly defined requirements can lead to scope creep, increased costs, and project failure.

<details>

<summary>Sample Requirements Definition</summary>

### Requirements Definition Document

**Project: School Study Planner App**

***

#### 1. Purpose of the System

The purpose of the Study Planner App is to help high school students organise homework, assessments, and study time in one place.\
The system aims to improve time management and reduce missed tasks.

***

#### 2. Target Users

• High school students (Years 7–12)\
• Teachers (view-only access in future versions)

***

#### 3. Functional Requirements

(What the system MUST do)

FR1 – The system must allow users to create an account and log in securely.

FR2 – The system must allow users to add subjects.

FR3 – The system must allow users to add homework and assessment tasks with due dates.

FR4 – The system must display tasks in a daily and weekly view.

FR5 – The system must allow users to mark tasks as complete.

FR6 – The system must send reminders before due dates.

***

#### 4. Non-Functional Requirements

(How the system should perform)

NFR1 – The system must load within 3 seconds.

NFR2 – The system must be easy to use for students with basic computer skills.

NFR3 – The system must keep user data secure and private.

NFR4 – The system should work on both computers and mobile devices.

***

#### 5. Constraints

• The system will be developed using Python and a simple web interface.\
• The project must be completed within 10 weeks.\
• Only free software tools will be used.

***

#### 6. Success Criteria

The system will be considered successful if:

• Users can add and manage tasks easily\
• No data is lost during normal use\
• Students report improved organisation

</details>

### **Determining Specifications**

Once requirements are established, programmers move to **determining specifications**, which translate user needs into precise technical descriptions.

Specifications describe

* inputs
* processes
* outputs
* data structures
* interfaces
* system constraints

This stage includes the creation of documentation such as **data dictionaries** and **system requirements specifications**. Clear specifications act as a reference point throughout development and ensure all team members have a shared understanding of how the system should function.

<details>

<summary>Sample Specifications Document</summary>

### Software Specifications Document

**Project: School Study Planner App**

Version: 1.0

***

#### 1. System Overview

The Study Planner App is a web-based application that allows students to create an account, enter subjects and tasks, view deadlines, mark work complete, and receive reminders.

***

#### 2. System Scope

**Included (Version 1.0)**

* User registration + login
* Subjects list
* Task creation and editing
* Weekly and daily task views
* Task completion tracking
* Reminder notifications (email or in-app)

**Not Included (Version 1.0)**

* Teacher accounts
* Sharing tasks with other users
* Automatic timetable import
* Push notifications to phones

***

#### 3. Technical Specifications

**3.1 Platform**

* Web application accessible via modern browsers (Chrome, Edge, Safari)
* Responsive layout for desktop and mobile

**3.2 Technology (example stack)**

* Front-end: HTML, CSS, JavaScript
* Back-end: Python (Flask or FastAPI)
* Database: SQLite (local) or PostgreSQL (deployment)

***

#### 4. Data Specifications

**4.1 Data Entities**

**User**

* user\_id (integer, primary key)
* email (string, unique)
* password\_hash (string)
* created\_at (datetime)

**Subject**

* subject\_id (integer, primary key)
* user\_id (foreign key)
* subject\_name (string, max 30 chars)

**Task**

* task\_id (integer, primary key)
* user\_id (foreign key)
* subject\_id (foreign key)
* title (string, max 60 chars)
* description (string, max 300 chars, optional)
* due\_date (date)
* due\_time (time, optional)
* priority (enum: Low / Medium / High)
* status (enum: Not Started / In Progress / Complete)
* created\_at (datetime)

***

#### 5. Functional Specifications

(Features written in “system shall” form)

**FS1 — Registration**

* The system shall allow users to create an account using email + password.
* The system shall reject duplicate emails.
* The system shall require passwords to be at least 8 characters.

**FS2 — Login**

* The system shall authenticate users using stored password hashes.
* The system shall lock the account for 5 minutes after 5 failed attempts.

**FS3 — Subject Management**

* The system shall allow users to create, rename, and delete subjects.
* The system shall prevent duplicate subject names for the same user.

**FS4 — Task Management**

* The system shall allow users to add, edit, and delete tasks.
* The system shall require: title, subject, due date.
* The system shall allow optional: description, time, priority.

**FS5 — Task Views**

* The system shall provide a daily view showing tasks due on a selected date.
* The system shall provide a weekly view showing tasks due in the next 7 days.
* The system shall show overdue tasks at the top of each view.

**FS6 — Task Completion**

* The system shall allow a task to be marked “Complete.”
* Completed tasks shall display with a visual style difference (e.g., greyed out + strikethrough).

**FS7 — Reminders**

* The system shall generate reminders 24 hours and 1 hour before the due date/time.
* If due\_time is missing, the reminder shall default to 5:00 PM the day before.

***

#### 6. Non-Functional Specifications

**Performance**

* Page load time shall be ≤ 3 seconds on a typical school network connection.
* The system shall support 100 concurrent users without crashing.

**Usability**

* Users shall be able to create a task in ≤ 30 seconds (tested with new users).
* Text shall be readable on mobile screens without zooming.

**Security**

* Passwords shall never be stored in plain text.
* Sessions shall expire after 30 minutes of inactivity.
* The system shall prevent common injection attacks by using parameterised queries / ORM.

**Reliability**

* The system shall not lose tasks when refreshing the page.
* The system shall back up the database daily (if hosted).

***

#### 7. User Interface Specifications

**Screens (minimum)**

1. Login / Register screen
2. Dashboard (today’s tasks + overdue)
3. Subjects management screen
4. Add/Edit task form
5. Daily / Weekly views

**UI Rules**

* Buttons must have clear labels (e.g., “Add Task”, “Save”, “Cancel”)
* Forms must show error messages next to the field causing the error

***

#### 8. Testing Specifications

(How you prove it meets specs)

**Sample Test Cases**

**TC1**: Register with valid email + 8+ character password → account created\
**TC2**: Register with same email twice → second attempt rejected\
**TC3**: Add a task missing due date → error shown, task not saved\
**TC4**: Mark a task complete → status updates and persists after refresh\
**TC5**: Weekly view shows tasks due in next 7 days, overdue shown at top

</details>

### **Design**

The **design stage** focuses on planning how the software will be structured before coding begins. This includes designing algorithms, user interfaces, databases, and system architecture. Programmers commonly use design tools such as flowcharts, pseudocode, structure charts, and entity-relationship diagrams (ERDs). A well-designed system improves efficiency, reduces errors, and makes the software easier to maintain. Design decisions made at this stage strongly influence the performance and scalability of the final product.

* **Top-Down Design Approach -** an approach to program design that starts with the general concept and repeatedly breaks it down into its component parts. Top down allows you to see the big picture immediately and discover the details as you go. It can be useful if you are starting your software from scratch as you may not know any of the specific details.
  * **Advantage -** Breaking problems into parts help us to identify what needs to be done and each step of refinement, new parts will become less complex and therefore easier to solve.
  * **Disadvantage -** You may not see any 'show stoppers' until well into the effort, as you may not hit snags in the first components you work on.
* **Bottom-Up Design Approach -** an approach which starts with the component parts and repeatedly combines them to achieve the general concept.
  * **Advantage** - Create robust, reusable low-level utilities then decide how they will be put together to create high-level construct.
  * **Disadvantage -** The complete program does not exist without the addition of the last module such that testing of system-level functions is not possible during development.



<figure><img src="https://3561174481-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FrghhiYQesvwDpbd2pl4R%2Fuploads%2FdpGlzyDkLT1kkRnYYB8p%2FChatGPT%20Image%20Jan%2030%2C%202026%2C%2002_10_28%20PM.png?alt=media&#x26;token=7d256ad3-d554-4d2a-9afd-68d719e2aebe" alt=""><figcaption></figcaption></figure>

### **Development**

The **development stage** is where the software is actually written using a programming language. Programmers convert design documents into executable code, often working in modules to simplify the process. Modern development frequently uses **version control systems** to manage changes and prevent conflicts. Writing clean, **well-commented code** improves readability and allows other developers to understand and modify the software in the future. **Errors** introduced at this stage are expected and addressed later through **testing and debugging.**

### **Integration**

**Integration** involves combining individual program modules into a complete system. Since software is often developed by multiple programmers or in separate components, integration ensures these parts work together correctly. Integration can be done incrementally, allowing issues between modules to be identified early. This stage is critical in large systems where incompatible modules can cause system failures if not addressed promptly.

### **Testing and Debugging**

**Testing and debugging** are essential to ensuring software reliability and correctness. Testing involves checking the software against its specifications to identify errors, while debugging is the process of locating and fixing those errors. Common testing methods include unit testing, integration testing, system testing, and user acceptance testing (UAT). Regular testing improves software quality, reduces security vulnerabilities, and ensures the software behaves as intended under different conditions.

### **Installation**

The **installation stage** involves deploying the software so it can be used by end users. This may include installing the program on user devices, configuring servers, and setting up databases. **Documentation and user training are often provided** at this stage to help users understand how to operate the system. A smooth installation process improves **user satisfaction and reduces the need for early technical support.**

### **Maintenance**

Once software is installed, it enters the **maintenance stage**, which often represents the longest phase of the software lifecycle. Maintenance includes fixing bugs, improving performance, updating features, and adapting the software to changes in hardware, operating systems, or user requirements. Preventive maintenance aims to reduce future issues, while adaptive and corrective maintenance respond to changes and errors. Effective maintenance ensures the software remains useful and relevant over time.

## Online Code Collaboration Tools

Online code collaboration tools are widely used in modern software development to support teamwork, version control, and project management. These tools are especially prevalent in large projects and distributed development teams. **A popular tool is GitHub.**

#### **Prevalence and Use**

Tools such as **GitHub**, **GitLab**, and **Bitbucket** are commonly used to store and manage source code using version control systems like Git. They allow multiple developers to work on the same project simultaneously without overwriting each other’s work. Features such as branching and merging enable experimentation while preserving stable versions of the software.

Collaboration tools also support **issue tracking**, **pull requests**, and **code reviews**, which improve code quality and accountability. Cloud-based platforms make it easier for teams to collaborate remotely, an increasingly common practice in the software industry.

#### **Key Features of collaboration tools**

The use of online collaboration tools **increases efficiency, reduces errors, and improves communication between developers.** They provide a clear history of changes, making it easier to identify when bugs were introduced and who made specific changes. However, they require reliable internet access and a basic understanding of version control concepts, which can be challenging for beginners.

Overall, online code collaboration tools are now an essential part of professional software development, supporting almost every stage of the development process from design to maintenance.

***

**HSC Queston: Describe the software development lifecycle**

> _The software development process provides a <mark style="background-color:blue;">**systematic**</mark>\*\* \*\***approach to creating reliable and effective software.** Each stage, from requirements definition through to maintenance, plays a critical role in ensuring software quality. In modern development environments, online code collaboration tools further enhance productivity and teamwork. Together, these processes and tools enable programmers to develop software that meets user needs and adapts to change over time._
