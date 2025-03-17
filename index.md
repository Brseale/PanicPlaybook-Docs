# PanicPlaybook

Panic Playbook is a Django-based web application that predicts setlists for future shows for the band Widespread Panic. 
It takes all available historical data on the band (from 1985 to present), and provides many different data visualizations.
It leverages this historical setlist data to train machine learning models that generate predictions for upcoming performances. 
The application uses PostgreSQL as its database, Gunicorn as the WSGI server, and Nginx as a reverse proxy with SSL provided by Let's Encrypt. 
It is designed to be deployed on DigitalOcean.

**Live Demo** [PanicPlaybook](https://www.panicplaybook.com)

### Index Page
![Homepage Screenshot](readme_images/PanicPlaybook_Index_Page.jpg)

## Table of Contents
- [Features](#features)
- [Tech Stack](#tech-stack)
- [How It Works](#how-it-works)
- [Screenshots](#screenshots)
- [License](#license)
- [Contact](#contact)

## Features
- **Machine Learning Setlist Prediction:**
    Uses a machine learning model built with scikit-learn to predict future setlists based on historical performance data. The model processes features such as historical trends, venue patterns, and past performances to generate accurate predictions.
- **AI Setlist Prediction:**
    Currently testing a new approach to setlist prediction using the Command-R LLM from Ollama. This method uses the same processing pipeline as the machine learning model, but uses the capabilities of Command-R to assess whether it can provide more accurate predictions.
- **Data Visualization:**
    Includes built-in data visualization tools to explore historical setlists and view prediction results, enabling users to better understand trends and patterns. Users can explore these charts and graphs on the Statistics page.
- **Playbook Picks:**
    Users can select five songs they think will be played at a show and compete for points. The points system is laid out on the Playbook Picks page. The users with the most points will be displayed on the leaderboard.
- **Setlists:**
    Users can view and filter setlists from the entire Postgres database. They can filter on venue, city, state, song, country, or a combination of filters.
- **Profile:**
    Users can view their profile to see the picks they made for a show. Users can also change their password and other information.
- **Merchandise:**
    Users can view and purchase available merchandise using this page. Payment processing is done through the Stripe API.
- **News:**
    Users can view current news about the band and upcoming shows.
- **About:**
    Users can view this page to see information about the website, its creator, future direction of the site, etc.
- **Data Management:**  
    Manage venues, songs, past and predicted setlists, future shows, PlaybookPicks, and subscribers through an intuitive Django admin interface.
- **Secure and Scalable:**  
    Utilizes PostgreSQL as the database, Gunicorn, and Nginx, with SSL managed by Certbot.
- **DigitalOcean Ready:**  
    Designed for easy deployment on DigitalOcean droplets.

## Tech Stack
### **Backend**
- Django 5.1.2 (Python 3.10.12)
- Django REST Framework
- PostgreSQL
- TensorFlow (ML model for predictions)

### **Frontend**
- HTML, CSS, JavaScript (Legacy)
- Next.js (Upcoming Upgrade)

### **Database & Deployment**
- PostgreSQL
- Gunicorn, Nginx, Certbot (SSL)
- Digital Ocean Droplets

### **Requirements**
For a full list of dependencies, see [`requirements.txt`](requirements.txt).

## How It Works
1. **Data Collection** - The app stores all available Widespread Panic setlist data from 1985 to present.
2. **Predicts Future Setlists** - Based on historical trends, venue patterns, and past performances:
    - **Machine Learning Setlist Prediction** - A **Random Forest Classifier** from scikit-learn analyzes patterns in the parameters above to generate setlist predictions.
    - **AI Setlist Prediction** - The **Command-R LLM** from Ollama analyzes patterns in the parameters above to generate setlist predictions. This is in the testing phase for now.
3. **Playbook Picks** - Users compete to predict songs and earn points.

## Screenshots
### Predictions Page
![Future Setlist Prediction Example](readme_images/PanicPlaybook_Future_Prediction.jpg)
![Past Setlist Prediction Example](readme_images/PanicPlaybook_Past_Prediction.jpg)

### Statistics Page
![Data Visualizations Example](readme_images/PanicPlaybook_stats_page.jpg)

### Playbook Picks Page
![Playbook Picks Page](readme_images/PanicPlaybook_Picks_Page.jpg)

### Setlist Page
![Setlist Page](readme_images/PanicPlaybook_Setlist_Page.jpg)

### Profile Page
![Profile Page](readme_images/PanicPlaybook_Profile_page.jpg)

### News Page
![News Page](readme_images/PanicPlaybook_News_Page.jpg)

### Merchandise Page
![Merchandise Page](readme_images/PanicPlaybook_Merch_Page.jpg)

### About Page
![About Page](readme_images/PanicPlaybook_About_Page.jpg)

## License
This project is licensed under the Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License - see the [LICENSE](LICENSE) file for details.

## Contact
If you have any questions or suggestions, feel free to reach out:

- **PanicPlaybook Email:** [panicplaybookad@gmail.com](mailto:panicplaybookad@gmail.com)
- **Personal Email:** [brooks.seale1@gmail.com](mailto:brooks.seale1@gmail.com)
- **LinkedIn:** https://www.linkedin.com/in/brooks-seale/
- **GitHub Issues:** [Submit an Issue](https://github.com/Brseale/WSP-WebApp/issues)
- **Website:** [PanicPlaybook](https://www.panicplaybook.com)