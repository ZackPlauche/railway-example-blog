# Simple Django Blog

A beautiful and modern blog built with Django, TailwindCSS, and Iconify Icons.

## Features

- Beautiful and responsive design with TailwindCSS
- Modern icons with Iconify
- Category-based organization
- Search functionality
- Like system for posts
- View counter
- Related posts
- Admin interface for content management
- Development and production settings
- Ready for Railway deployment

## Prerequisites

- Python 3.8 or higher
- pip (Python package manager)
- PostgreSQL (for production)

## Local Development Setup

1. Clone the repository:
```bash
git clone <repository-url>
cd simple-django-blog
```

2. Create and activate a virtual environment:
```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Create a `.env` file in the project root:
```bash
DJANGO_SECRET_KEY=your-secret-key-here
```

5. Run migrations:
```bash
python manage.py migrate
```

6. Create a superuser:
```bash
python manage.py createsuperuser
```

7. Run the development server:
```bash
python manage.py runserver
```

8. Visit http://localhost:8000 to see your blog.

## Production Deployment on Railway

1. Create a new project on Railway.

2. Add the following environment variables in Railway:
```
DJANGO_ENV=production
DJANGO_SECRET_KEY=your-secure-secret-key
ALLOWED_HOSTS=your-domain.railway.app
AWS_ACCESS_KEY_ID=your-aws-access-key
AWS_SECRET_ACCESS_KEY=your-aws-secret-key
AWS_STORAGE_BUCKET_NAME=your-bucket-name
AWS_S3_REGION_NAME=your-region
EMAIL_HOST=your-smtp-host
EMAIL_PORT=587
EMAIL_HOST_USER=your-email
EMAIL_HOST_PASSWORD=your-email-password
DEFAULT_FROM_EMAIL=your-email
```

3. Railway will automatically detect the Django project and set up the PostgreSQL database.

4. Deploy your application:
```bash
git push railway main
```

5. Run migrations on Railway:
```bash
railway run python manage.py migrate
```

6. Create a superuser on Railway:
```bash
railway run python manage.py createsuperuser
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
