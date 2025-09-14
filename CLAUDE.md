# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development Commands

### Virtual Environment Setup
```bash
# Activate virtual environment (macOS/Linux)
source venv/bin/activate

# Activate virtual environment (Windows)
venv\Scripts\activate
```

### Django Management Commands
```bash
# Start development server
python manage.py runserver

# Run database migrations
python manage.py migrate

# Create database migrations
python manage.py makemigrations

# Create superuser for admin access
python manage.py createsuperuser

# Collect static files
python manage.py collectstatic

# Run tests
python manage.py test

# Access Django shell
python manage.py shell
```

### Testing
```bash
# Run all tests
python manage.py test

# Run specific app tests
python manage.py test web_pic_grid
```

## Project Architecture

### Django Project Structure
- **web_pic_grid/**: Main Django project directory
  - `settings.py`: Django configuration with SQLite database, Brazilian Portuguese localization (pt-br), UTC-2 timezone
  - `urls.py`: Basic URL routing with admin interface only
  - `wsgi.py`: WSGI deployment configuration
  - `templates/`: Directory for HTML templates (currently empty)
- **manage.py**: Django management script
- **db.sqlite3**: SQLite database file
- **venv/**: Python virtual environment (excluded from version control)

### Configuration Details
- **Django Version**: 2.1.3
- **Database**: SQLite (db.sqlite3)
- **Language**: Brazilian Portuguese (pt-br)
- **Timezone**: UTC-2
- **Debug Mode**: Enabled for development
- **Secret Key**: Default Django key (needs to be changed for production)
- **Static Files**: Configured for `/static/` URL

### Current State
This is a basic Django project in experimental phase with:
- Basic Django project structure
- SQLite database configured
- Admin interface enabled
- Internationalization support for Brazilian Portuguese
- No custom Django apps or models
- No views or templates implemented
- No image grid functionality yet

### Development Focus
The project is intended to become an image grid/gallery application but currently only has the Django foundation set up. Next development steps should include:
- Creating Django models for image storage
- Implementing image upload functionality
- Designing responsive grid layout templates
- Adding image management views

### Security Notes
- Debug mode is enabled (development only)
- Default secret key needs to be changed for production
- ALLOWED_HOSTS is empty (needs configuration for production deployment)