This Django-based API provides functionality for managing clients, projects, and user assignments.

## Setup

1. Clone the repository:
   ```
   git clone https://github.com/your-username/client-project-management.git
   cd client-project-management
   ```

2. Create a virtual environment and activate it:
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

4. Set up the MySQL database:
   - Install MySQL if you haven't already
   - Create a new MySQL database
   - Copy `.env.example` to `.env` and update the variables with your MySQL credentials

5. Run migrations:
   ```
   python manage.py makemigrations
   python manage.py migrate
   ```

6. Create a superuser:
   ```
   python manage.py createsuperuser
   ```

7. Run the development server:
   ```
   python manage.py runserver
   ```

## API Endpoints

- List all clients: GET /api/clients/
- Create a new client: POST /api/clients/
- Retrieve client info: GET /api/clients/:id/
- Update client info: PUT/PATCH /api/clients/:id/
- Delete client: DELETE /api/clients/:id/
- Create a new project for a client: POST /api/clients/:id/projects/
- List projects assigned to logged-in user: GET /api/projects/

## Authentication

This project uses Django's built-in authentication system. To access the API endpoints, you need to be logged in. You can use the Django admin interface to manage users and login.