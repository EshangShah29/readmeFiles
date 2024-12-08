## Django GFFA Project Setup

This document outlines the steps involved in setting up the Django GFFA project. It covers database migrations, superuser creation, and running the development server.

**Steps:**

1. **Project Creation:**

   - A new Django project named `gffa`  was created using:

     ```bash
     django-admin startproject gffa
     ```

   - This command generates the project structure, including essential files like `settings.py`, `urls.py`, and `wsgi.py`.

2. **Database Migrations:**

   - All pending migrations were applied to the PostgreSQL database using:

     ```bash
     python manage.py migrate
     ```

   - **Outcome:** 
      - The command executed successfully, applying migrations for various Django apps (account, auth, sessions, socialaccount).
      - Each migration was applied in sequence, ensuring table and field creation/modification as needed.
      - Logs displayed "OK" for each migration, confirming successful application.

3. **Superuser Creation:**

   - After applying migrations, a superuser was created for accessing the Django admin interface:

     ```bash
     winpty python manage.py createsuperuser
     ```

   - Prompts for username (e.g., gffa-superuser), email (e.g., eshang@umich.edu), and password were displayed.

   - **Error Handling:**
     - The password must meet security requirements (minimum length and complexity). 
     - A weak password triggers an error message, prompting correction.

4. **Running the Development Server:**

   - The development server was started locally to run the project using:

     ```bash
     python manage.py runserver
     ```

   - **Expected Outcome:**
     - The server starts running at http://127.0.0.1:8000.
     - "Watching for file changes with StatReloader" message indicates automatic server reload on code changes during development.
     - You can now access the project locally and navigate to the Django admin interface at http://127.0.0.1:8000/admin using the superuser credentials.

5. **Common Errors Handled:**

   - **Error:** DoesNotExist at /admin/login/
     - **Cause:** Missing `SITE_ID` setting or incorrect configuration of the `sites` framework (required by django-allauth) causes this login error.
     - **Solution:** Set `SITE_ID = 2` in `settings.py` and ensure proper configuration of the `sites` framework.

   - **Error:** PostgreSQL Connection Issues
     - **Cause:** Connection errors can occur due to issues connecting to the PostgreSQL database (e.g., incorrect credentials or non-running database).
     - **Solution:** Ensure the PostgreSQL server is running locally and the credentials (POSTGRES_USERNAME and POSTGRES_PASSWORD) in `secrets.py` are correct.
