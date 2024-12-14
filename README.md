# Course Management System

A Python-based Course Management System that offers functionalities like account creation, course recommendations, enrollment management, and user reviews. This project utilizes data structures such as graphs, hash tables, and queues to provide an efficient and interactive experience.

## Features
- **User Management**: Create accounts, log in, and track user activity.
- **Course Recommendations**: Personalized course suggestions based on subject and level.
- **Course Reviews**: Add, retrieve, and view course reviews.
- **Enrollment System**: Manage and start enrolled courses with a queue-based system.
- **Rating System**: Rate courses to provide feedback for other users.

## Technologies Used
- **Python**
- **Data Structures**: Graphs, Hash Tables, Queues

## Prerequisites
- Python 3.7 or higher installed on your system.
- Basic knowledge of running Python scripts.

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/Course-Management-System.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Course-Management-System
   ```
3. (Optional) Set up a virtual environment:
   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   ```
4. Install any dependencies (if required) listed in `requirements.txt`:
   ```bash
   pip install -r requirements.txt
   ```

## How to Run
1. Run the main Python script:
   ```bash
   python course_management_system.py
   ```
2. Follow the menu options displayed to interact with the system.

---

## Working of the Code

### **Core Functionalities**

#### 1. **User Management System**
- **Account Creation**: Users can create an account by providing a username and password.
- **Login**: Users log in using their credentials to access personalized features like course recommendations and enrollment.
- **Logged-in User Tracking**: Tracks the current logged-in user for operations like reviewing or enrolling in courses.

#### 2. **Course Recommendations**
- Recommendations are generated based on user-selected **subject** and **difficulty level**.
- The system uses a **Graph Data Structure** where courses are grouped by a key combining subject and level (e.g., `Mathematics_Beginner`).
- When a user inputs preferences, the system retrieves relevant courses and their instructors from the graph.

#### 3. **Rating System**
- Users can rate a course on a scale of their choice.
- Ratings are stored in a **Hash Table** (`ratings`), ensuring fast lookup and updates.

#### 4. **Course Reviews**
- Users can add and view course reviews.
- Reviews are stored in another **Hash Table** (`reviews`), allowing multiple reviews for each course.

#### 5. **Enrollment System**
- Courses selected by users are added to a queue, simulating a course "enrollment list."
- The queue ensures that courses are processed in the order of enrollment.
- When starting enrolled courses, they are dequeued and processed one by one.

#### 6. **Starting Courses**
- Enrolled courses can be started in sequence. The system simulates course duration using a `time.sleep()` delay.

---

### **Program Flow**
1. **Menu Options**:
   - The program starts by displaying a menu-driven interface with options for user actions, such as creating an account, logging in, viewing recommendations, and managing courses.
   - Users can select any option to proceed.

2. **Course Recommendation Workflow**:
   - User selects a **subject** (e.g., Mathematics, Science) and a **difficulty level** (e.g., Beginner, Intermediate).
   - Based on the selection, the system retrieves recommended courses from the graph and displays them.

3. **Rating and Review Workflow**:
   - User selects a course to rate or review.
   - Ratings and reviews are stored and can be retrieved later for any course.

4. **Enrollment Workflow**:
   - User selects a course to enroll in, which is added to the enrollment queue.
   - Courses are dequeued in order and "started" when the user opts to begin enrolled courses.

---

### **Example Usage**
#### Step 1: Log In or Create Account
- Create an account with a username and password.
- Log in using the credentials.

#### Step 2: Get Personalized Recommendations
- Select a subject and difficulty level to receive a list of recommended courses.

#### Step 3: Enroll in Courses
- Add one or more courses to your enrollment list.
- Display the enrollment list to confirm your selections.

#### Step 4: Start Enrolled Courses
- Begin your learning journey with courses processed in the order they were enrolled.

#### Step 5: Rate and Review Courses
- Rate the courses you completed and provide reviews for others to view.
