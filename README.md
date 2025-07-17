Here's a complete guide to run your QuizMakerApp on your local machine using XAMPP:

🖥️ STEP-BY-STEP TO RUN YOUR APP LOCALLY
✅ 1. Install XAMPP (if not already)
Download from https://www.apachefriends.org

Install it with default options

✅ 2. Start Apache & MySQL
Open XAMPP Control Panel

Click Start for both:

Apache ✅

MySQL ✅

They should turn green.

✅ 3. Setup Your Project Folder
Go to:


C:\xampp\htdocs\
Create a folder named:


QuizMakerApp
Copy all your files into this folder:


QuizMakerApp/
├── index.html
├── signup.html
├── login.html
├── admin.html
├── student-dashboard.html
├── take_quiz.html
├── styles.css
├── script.js
├── db.php
├── /api/
└── /python/
✅ 4. Set Up the Database
Go to:


http://localhost/phpmyadmin
Click New, create a DB called:


quizmaker
Click on quizmaker, then go to the Import tab.

Upload the file quizmaker_schema.sql (I gave earlier).

Click Go — the tables will be created.

✅ 5. Run the App
Open your browser and go to:

arduino

http://localhost/QuizMakerApp/
Examples:

Student Signup:


http://localhost/QuizMakerApp/signup.html
Admin Login:


http://localhost/QuizMakerApp/admin.html
🧪 TO RUN PYTHON MCQ GENERATOR (IF USED)
If you're calling a Python script from PHP:

🔧 1. Install Python + Dependencies
Open Terminal/Command Prompt:


pip install pymupdf
(Optional, for advanced NLP):


pip install spacy
python -m spacy download en_core_web_sm
🔧 2. Make sure python is in system PATH
🔧 3. Call from PHP (inside your API):

$output = shell_exec("python ../python/mcq_generator.py path_to_pdf");
✅ Summary of Commands
Step	Command
Start XAMPP Services	No command (Use GUI)
Access phpMyAdmin	http://localhost/phpmyadmin
Access App	http://localhost/QuizMakerApp/
Run Python	python mcq_generator.py somefile.pdf (for testing)
