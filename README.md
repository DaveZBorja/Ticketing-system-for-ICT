```markdown
# Ticketing System

This is a simple web-based Ticketing System built with Flask. It allows users to create, manage, and track tickets for various issues. The admin panel provides an overview of all tickets, their statuses, and the ability to update or delete them.

## Table of Contents
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [File Structure](#file-structure)
- [Contributing](#contributing)
- [License](#license)

## Features
- **User Ticket Creation**: Users can submit tickets with details such as title, description, name, and office.
- **Admin Panel**: Admins can view, update, and delete tickets.
- **Real-Time Updates**: New tickets are displayed at the top of the admin panel.
- **Export Functionality**: Admins can export tickets to CSV.
- **Status Management**: Admins can close tickets by updating their status.
- **Login/Logout Functionality**: Secure admin login and logout options.

## Prerequisites
- Python 3.7+
- Flask 2.0+
- SQLite3 (or any other database supported by Flask SQLAlchemy)
- HTML, CSS, and JavaScript

## Installation
1. **Clone the repository:**
   ```bash
   git clone https://github.com/DaveZBorja/Ticketing-system-for-ICT.git
   cd ticketing-system
   ```

2. **Create a virtual environment:**
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # On Windows use `venv\Scripts\activate`
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up the database:**
   ```bash
   flask db init
   flask db migrate -m "Initial migration."
   flask db upgrade
   ```

5. **Run the application:**
   ```bash
   flask run
   ```
   The application will start on `http://127.0.0.1:5000/`.

## Configuration
Create a `.env` file in the root directory with the following content:

```
FLASK_APP=app.py
FLASK_ENV=development
SECRET_KEY=your_secret_key
```
- Replace `your_secret_key` with a strong secret key of your choice.
- Adjust other environment variables as needed.

## Usage
- Navigate to `http://127.0.0.1:5000/` to access the ticket creation form.
- Admin panel is accessible at `http://127.0.0.1:5000/admin/login`.
- Use the admin credentials to log in and view the list of tickets.

### Admin Panel
- View a list of all tickets.
- Click "Close" to update a ticket's status.
- Click "Delete" to remove a ticket (this will only mark it as deleted in the database but retain its data).

## API Endpoints
| Endpoint                 | Method | Description                          |
|--------------------------|--------|--------------------------------------|
| `/api/tickets`           | POST   | Create a new ticket                  |
| `/api/tickets`           | GET    | Retrieve a list of all tickets       |
| `/api/tickets/<id>`      | PUT    | Update ticket status by ID           |
| `/api/tickets/<id>`      | DELETE | Delete a ticket (mark as deleted)    |
| `/admin/export`          | GET    | Export tickets to CSV                |
| `/admin/logout`          | POST   | Admin logout                         |

## File Structure
```
ticketing-system/
│
├── app.py                # Main Flask application
├── models.py             # Database models
├── routes.py             # API and view routes
├── templates/            # HTML templates
│   ├── index.html        # Ticket creation form
│   ├── admin_panel.html  # Admin panel page
├── static/
│   ├── styles.css        # CSS file for styling
│   ├── logo.png          # Logo image file
├── migrations/           # Database migrations
├── .env                  # Environment variables
├── requirements.txt      # Python dependencies
└── README.md             # Project documentation
```

## Contributing
1. Fork the repository.
2. Create a new branch for your feature or bug fix: `git checkout -b feature-name`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature-name`
5. Submit a pull request.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```

### Instructions:

- Replace `https://github.com/DaveZBorja/Ticketing-system-for-ICT.git` with your actual GitHub repository URL.
- Update any specific configurations or instructions if needed.
- Customize sections like **Contributing** and **License** as per your project requirements.

