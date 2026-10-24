# gpec: Dubai to the Stars

A small Flask web app for booking fictional space trips, with a dashboard that lists your bookings.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=flat-square&logo=css&logoColor=white)

## Features

- **Trip booking:** three destinations with prices: International Space Station ($500,000), Lunar Hotel ($1,000,000) and Mars Colony ($2,000,000)
- **Packages:** Economy, Luxury and VIP seat classes. The list updates in the browser to show only the classes each destination offers
- **Validation:** the server checks the destination, the seat class and the departure date, which must be in the future
- **Booking details:** each booking gets a random 4-digit ID, a countdown in days, a suggested accommodation and a travel tip for the chosen destination and class
- **Dashboard:** lists your bookings and shows each travel tip in a pop-up

## How it works

Destinations, accommodations and travel tips are hard-coded in `app.py`, and there is no database. Bookings live in the Flask session cookie. The secret key is generated each time the app starts, so bookings are lost when the server restarts.

## Tech Stack

Python, Flask 2.3.2, Jinja2 templates, HTML/CSS with the Orbitron font from Google Fonts, and vanilla JavaScript.

## Getting Started

```bash
git clone https://github.com/4waiz/gpec.git
cd gpec
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
python app.py
```

Open <http://localhost:5000>. Set the `PORT` environment variable to use a different port. The `Procfile` (`web: python app.py`) runs the same command on Procfile-based hosts such as Heroku.

## Project Structure

```
gpec/
├── app.py              # routes, destination data and booking logic
├── requirements.txt    # Flask==2.3.2
├── Procfile            # web: python app.py
├── static/styles.css   # space theme
└── templates/
    ├── index.html      # booking form
    └── dashboard.html  # bookings list and travel-tip pop-up
```

---

Built by [Awaiz Ahmed](https://github.com/4waiz)
