# StudyBud - A Random Chatroom Application

StudyBud is a simple Django-based web application that allows users to join random chatrooms, connect with peers, and chat in real time. The application uses **Django Channels** for WebSocket support, providing a modern chat experience.

## Features

- **Join Random Chatrooms**: Users can enter their name and choose or join a random chatroom.
- **Real-Time Communication**: Using Django Channels, users can send and receive messages in real time without refreshing the page.
- **No Registration Required**: Users can chat immediately without the need for creating an account.

## Technologies Used

- **Django**: Backend framework for web development.
- **Django Channels**: For handling real-time WebSocket connections.
- **Redis**: Channel layer backend for handling WebSocket communication.
- **HTML/CSS/JavaScript**: For frontend development and user interaction.
  
## Installation

### Prerequisites

Before running the app, ensure you have the following installed:

- Python 3.8 or above
- Django 5.x
- Redis (for the channel layer)

### Steps to Run the Project

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/studybud.git
   cd studybud
2. Create and activate a virtual environment:

python3 -m venv env
source env/bin/activate

3. Install the required dependencies:

pip install -r requirements.txt

4. Set up Redis:

Install Redis locally or use a cloud Redis service.
Ensure Redis is running on the default port (6379).

5. Apply migrations:

python3 manage.py migrate

6. Run the development server:

python3 manage.py runserver
Access the application: Open your browser and go to http://127.0.0.1:8000/.

## Features in Development

User Authentication: Future plans to allow users to sign in and keep track of their chat history.
Chat History: Storing messages in the database for persistent chat history.
User Profiles: Adding user profiles to personalize the chat experience.
Real-time Notifications: Push notifications to notify users about new messages or activity in the chatroom.

## Directory Structure

studybud/
├── chat/                   # Chat application
│   ├── migrations/         # Database migrations
│   ├── static/             # Static files (CSS, JS, Images)
│   ├── templates/          # HTML templates
│   ├── consumers.py        # WebSocket consumer for real-time chat
│   ├── routing.py          # WebSocket routing configuration
│   ├── views.py            # Views for the app
│   └── urls.py             # URL configuration for chat app
├── db.sqlite3              # SQLite database
├── manage.py               # Django's command-line tool for project management
├── requirements.txt        # Required dependencies for the project
└── studybud/               # Project settings
    ├── asgi.py             # ASGI configuration for Channels
    ├── settings.py         # Settings for the Django project
    ├── urls.py             # URL routing for the project
    └── wsgi.py             # WSGI configuration for deployment
    
## Contributing
Feel free to fork the project and submit pull requests. Any contributions, whether it’s bug fixes, new features, or improvements, are welcome.

Fork the repository.
Create a new branch (git checkout -b feature-branch).
Make your changes.
Commit your changes (git commit -am 'Add new feature').
Push to the branch (git push origin feature-branch).
Create a new Pull Request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements
Django: Web framework for building web applications.
Django Channels: Extends Django to handle asynchronous protocols like WebSockets.
Redis: Key-value database for managing WebSocket connections.
