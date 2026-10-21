# Customizable Django Portfolio

A starter portfolio built with Django, HTML, CSS, and JavaScript. Design: dark futuristic base, Bento Grid cards, and subtle glassmorphism.

## 1. Requirements
- Python 3.10+
- pip

## 2. Setup

Open a terminal in this project folder and run:

### Windows
```powershell
py -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
py manage.py migrate
py manage.py runserver
```

### macOS / Linux
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

Open http://127.0.0.1:8000/

## 3. Customize your portfolio
Edit `portfolio_site/profile_data.py`:
- `PROFILE`: name, role, short intro, about text, email, location, GitHub, LinkedIn, profile image path.
- `SKILLS`: list of skill names.
- `PROJECTS`: project title, description, tags, GitHub URL, demo URL.

Put your profile photo inside `core/static/core/images/` and update `PROFILE["photo"]`, for example:
`core/images/profile.jpg`

If a project does not have a demo or GitHub URL yet, leave that value as an empty string.

## 4. Change the appearance
Edit `core/static/core/css/style.css`. The colors are defined at the top as CSS variables.

## 5. Change behavior
Edit `core/static/core/js/main.js`. The current JavaScript handles the mobile navigation and current year.

## 6. Contact form
The form validates and displays a success message locally. It does not send email yet. For production, configure Django email settings and add spam protection.

## 7. Before publishing
- Replace all sample profile details and project links.
- Do not publish secrets or private keys.
- Set `DEBUG = False`, configure `ALLOWED_HOSTS`, use environment variables for the secret key, and configure HTTPS before production deployment.
