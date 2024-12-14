# **Evernote**
Welcome to the EverNote a service for managing notes efficiently. This app provides powerful features for creating, editing, organizing, and securing notes, using Django and Django REST Framework (DRF) for a robust and scalable architecture.

# **Features**
- **Create, Read, Update, Delete Notes**: Full CRUD functionality for managing notes.
- **User Authentication**: Secure user registration, login, and token-based authentication using SimpleJWT.
- **Search and Filter**: Easily search and filter notes by title or content.
- **Password Protection**: Each user's notes are securely stored and accessible only by the owner.
- **Sync Across Devices**: REST API for seamless integration with front-end apps for multi-device syncing.
- **Light/Dark Mode Support**: Back-end APIs to support theme toggling.
- **Media Handling**: API endpoints for importing and managing multimedia files in notes.

# Requirements
- Python: 3.8 or later
- Django: 4.2 or later
- Django REST Framework: 3.14 or later
- PostgreSQL (optional): For production-grade database support (default is SQLite for development).

# **Installation**
1. Clone the Repository
- git clone https://github.com/Phionanamugga/evernote-django.git
- cd evernote-django

2. **Create a Virtual Environment**
- python -m venv env
- source env/bin/activate  # On Windows, use .\env\Scripts\activate

3. **Install Dependencies**
- pip install -r requirements.txt

4. **Configure Environment Variables**
Create a .env file in the root directory and configure the following variables:
- SECRET_KEY=your-secret-key
- DEBUG=True
- ALLOWED_HOSTS=127.0.0.1, localhost
- DATABASE_URL=sqlite:///db.sqlite3

5. **Apply Migrations**
- python manage.py migrate

6. **Create a Superuser**
- python manage.py createsuperuser

7. **Run the Server**
- python manage.py runserver
- Visit the app at http://127.0.0.1:8000.

8. **API Endpoints**
Authentication:
- POST /api/token/: Obtain access and refresh tokens.
- POST /api/token/refresh/: Refresh access token.

**Notes**:
- GET /api/notes/: List all notes.
- POST /api/notes/: Create a new note.
- GET /api/notes/<id>/: Retrieve a specific note.
- PUT /api/notes/<id>/: Update a specific note.
- DELETE /api/notes/<id>/: Delete a specific note.

**Search**:
- GET /api/notes/?search=<query>: Search notes by content or title.
- Development
- Running Tests

9. **To run tests, use**:
- python manage.py test

10. **Code Formatting**
Use Black to maintain code consistency:
black .

11. **Deployment**
- Set DEBUG=False in .env.
- Configure a production database (e.g., PostgreSQL).
- Use gunicorn and a web server like Nginx for serving the application.

12. **Contributing**
Contributions are welcome! To contribute:

13. Fork the repository.
- Create a feature branch.
- Commit your changes.
- Submit a pull request.

14. **Roadmap**
We are continuously improving the EverNote Django App. Here’s what’s planned for future releases:
- **User Roles**: Add admin and standard user roles for better access management.
- **Collaborative Notes**: Allow multiple users to edit notes in real-time.
- **Tagging System**: Organize notes using tags and categories.
- **Export Notes**: Enable exporting notes to formats like PDF or Markdown.
- **Reminder Notifications**: Add reminders for specific notes.
- **Integration with Cloud Storage**: Support for Google Drive, Dropbox, and more.
- **Offline Mode**: Access notes without an internet connection.
- **Advanced Analytics**: Insights into note-taking habits.

15. **FAQ**
1. How can I reset my password?

Password reset functionality is included via API. Use the endpoint:
POST /api/password_reset/ with your email to receive reset instructions.

2. Which database is recommended for production?

We recommend PostgreSQL for its performance, scalability, and compatibility with Django.

3. How do I add support for multimedia (images/videos)?

Multimedia can be uploaded using the POST /api/notes/ endpoint with an upload field for files. Ensure the MEDIA_ROOT and MEDIA_URL settings are correctly configured.

4. Can I deploy this app on shared hosting?

Django apps typically require a WSGI server like Gunicorn or uWSGI, which is not always supported on shared hosting. Instead, consider using Heroku, AWS, or DigitalOcean for deployment.


16. **License**

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

MIT License

Copyright (c) [2024] [Evernote]

17. **Acknowledgments**
Inspired by Evernote and similar productivity tools.
Built with Django and Django REST Framework.
Special thanks to open-source contributors for libraries and tools used in this project.
Let me know if you'd like me to generate the requirements.txt file or provide additional sections!

**Email**: support@evernote.com
**GitHub Issues**: Report an Issue