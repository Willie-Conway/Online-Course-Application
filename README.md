
# Add a New Assessment Feature to an Online Course Application 🎓

![Online Course Application](https://github.com/Willie-Conway/Online-Course-Application/blob/8ce1a99e2e35bbd0142377b30788b9dfccbaf5be/Screenshots/Online%20Courses%20App.gif)

## Overview 🌟

In this project, we implement an assessment feature to an **Online Course Application**. The feature allows learners to take an exam, submit their answers, and get results based on their performance. This process includes creating models, handling form submissions, displaying dynamic content in templates, and providing feedback to the learner.

## Tasks Completed ✅

### 1. **Build New Models** 🛠️
We created the following models:
- **Course**: Represents the course details.
- **Enrollment**: Links a learner to a specific course.
- **Question**: Represents a question in the exam.
- **Choice**: Represents possible answers for each question.
- **Submission**: Stores learner responses and links to an enrollment.

These models allow for the creation of relationships between courses, students, questions, and answers.

### 2. **Register Model Changes** 📋
After creating models, we registered them in Django's **admin panel** for easy management. This allows us to add courses, questions, and choices directly via the admin interface.

### 3. **Update the Course Detail Template** 🖥️
We updated the `course_details_bootstrap.html` template to display:
- The exam questions for the course.
- The choices for each question in a user-friendly, Bootstrap-styled interface.
- An option to start the exam when the user is authenticated.

### 4. **Test Data** 🧪
We added sample test data including:
- **Instructor** (admin user).
- **Course**: "Learning Django", with lessons and course content.
- **Test Questions** with correct and incorrect choices.

### 5. **Submission Evaluation** 📈
We implemented the **submit** view that:
- Captures answers submitted by the learner.
- Creates a new **Submission** record.
- Compares answers with the correct choices and calculates the score.
- Redirects the user to the **exam result page**.

### 6. **Complete the Exam Result Template** 🏆
We created the `exam_result_bootstrap.html` template to display:
- The learner’s **total score**.
- Whether the learner **passed** or **failed** the exam.
- Feedback on each question showing:
  - Correct answers.
  - Incorrect answers with an option to retake the exam.

This was all styled using **Bootstrap** to create a responsive, user-friendly interface.

## Technologies Used ⚙️

- **Django**: Backend framework for creating models, handling forms, and rendering templates.
- **Bootstrap**: Frontend framework for styling the templates.
- **Python**: Programming language for implementing the business logic and views.
- **HTML/CSS**: For structuring and styling the course exam interface.

## How to Run the Project Locally 🚀

1. **Clone the repository**:

   ```bash
   git clone <repo-url>
   cd <repo-directory>
   ```

2. **Install dependencies**:

   Ensure you have `virtualenv` installed and create a virtual environment.

   ```bash
   python -m venv venv
   source venv/bin/activate  # For MacOS/Linux
   venv\Scripts\activate     # For Windows
   pip install -r requirements.txt
   ```

3. **Run migrations** to set up the database:

   ```bash
   python manage.py migrate
   ```

4. **Create a superuser** to access the Django admin panel:

   ```bash
   python manage.py createsuperuser
   ```

5. **Run the development server**:

   ```bash
   python manage.py runserver
   ```

6. **Access the application** by visiting `http://127.0.0.1:8000` in your browser.

7. **Login to the Django Admin panel** to manage data (courses, questions, etc.) by navigating to `http://127.0.0.1:8000/admin/`.

## How the Exam Process Works 📝

1. **Learner Enrollment**: Users can enroll in courses by signing up and selecting courses.
2. **Exam Start**: Once enrolled, they can start the exam by clicking the "Start Exam" button.
3. **Answer Submission**: Learners choose their answers from a list of multiple-choice questions, and then submit their answers.
4. **Exam Results**: After submission, learners are redirected to a results page showing their score, whether they passed or failed, and feedback on their answers.

## Key Features ⭐

- **Multiple Choice Questions**: Each question can have multiple correct choices, and the user selects the answers they think are correct.
- **Dynamic Exam Interface**: The exam interface is updated dynamically based on the questions and choices for each course.
- **Results Feedback**: Learners receive detailed feedback on their answers, including which choices were correct or incorrect, and their overall score.
- **Admin Panel**: Instructors and admins can manage courses, questions, and choices through the Django admin panel.

## Screenshot Examples 📸

### 1. **Course Details Page**
![Course Details](https://github.com/Willie-Conway/my-course-repo/blob/dae527f430247697b2b6137fa198c5c1c79d8a96/Screenshots/Lesson%20Page.png)

### 2. **Exam Results - Pass** 🎉
![Exam Results - Pass](https://github.com/Willie-Conway/my-course-repo/blob/dae527f430247697b2b6137fa198c5c1c79d8a96/Screenshots/Answers.png)

### 3. **Exam Results - Fail** 😞
![Exam Results - Fail](https://github.com/Willie-Conway/my-course-repo/blob/dae527f430247697b2b6137fa198c5c1c79d8a96/Screenshots/Incorrect%20Answers.png)

## Authors ✍️
- **Willie Conway**
- **Yan Luo**
- **Muhammad Yahya**

## Acknowledgements 🤝

This project is part of the **IBM Developer Skills Network**. All rights reserved by **IBM Corporation**.

---
```
Feel free to contribute or ask any questions regarding the project! 😊
```
**ER Diagram**
![Onlinecourse ER Diagram](https://github.com/ibm-developer-skills-network/final-cloud-app-with-database/blob/master/static/media/course_images/onlinecourse_app_er.png)
