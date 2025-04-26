##  Project Overview  
This Ticket Booking Management System is a web application built with **Django** that allows users to browse available shows, book tickets, and view their booking history. It also features an admin panel for managing shows and users.

---

##  Features

###  User Features
-  **Authentication System**: Register, login, and logout  
-  **Show Browsing**: View list of available shows with details  
-  **Ticket Booking**: Select and book tickets for available shows  
-  **Booking History**: View all past bookings  

###  Admin Features
-**Show Management**: Add, edit, and delete shows  
-  **Booking Overview**: View all bookings  
-  **User Management**: Manage user accounts  

---

##  Tech Stack
- **Backend Framework**: Django (Python)  
- **Database**: MySQL  
- **Containerization & CI/CD**: Docker, Jenkins (configured)

---



---

##  Setup Instructions

###  Prerequisites
- Python 3.8+  
- MySQL  
- Git  

---

##  Manual Setup 

###  Clone the repository

```bash
git clone https://github.com/mrudulchaudhari/sl3tbms.git
cd sl3tbms
cd tbms
```
Create and activate a virtual environment
bash
Copy
Edit
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
 Install dependencies
bash
Copy
Edit
pip install -r requirements.txt
 Configure MySQL Database
Create a MySQL database named ticket_booking

Update config/settings.py with your database credentials:

python
Copy
Edit
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'ticket_booking',
        'USER': 'your_mysql_user',
        'PASSWORD': 'your_mysql_password',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
 Run migrations
bash
Copy
Edit
python manage.py makemigrations
python manage.py migrate
 Create a superuser
bash
Copy
Edit
python manage.py createsuperuser
Follow the prompts to create your admin user.

 Run the development server
bash
Copy
Edit
python manage.py runserver
 Access the application
Main App: http://localhost:8000

Admin Panel: http://localhost:8000/admin/dashboard/

 User Guide
For Regular Users
 Registration: Sign up with email and password

 Browse Shows: View available shows

 Show Details: Click to explore more

 Book Tickets: Select number of seats and confirm
View Bookings: Check your booking history

For Administrators
 Admin Access: Login via admin credentials

 Manage Shows: Add, edit, delete show details

 View All Bookings: Monitor system-wide ticket bookings

 User Management: Control user accounts

 Project Structure
bash
Copy
Edit
ticket_booking/
├── config/               # Django project settings
├── accounts/             # User authentication app
├── booking/              # Core booking functionality
├── admin_panel/          # Admin management interface
├── templates/            # HTML templates
├── Dockerfile            # Docker configuration (optional)
├── docker-compose.yml    # Docker Compose (optional)
├── Jenkinsfile           # Jenkins pipeline (optional)
└── requirements.txt      # Python dependencies
