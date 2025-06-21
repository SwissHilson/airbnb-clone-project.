# airbnb-clone-project.
A scalable booking platform simulating Airbnb's core features, built with Django (Python), MySQL, and modern DevOps practices.  

## 🛠️ Tech Stack  
- **Backend:** Django (Python)  
- **Database:** MySQL (with PostgreSQL-compatible design for scalability)  
- **API:** Django REST Framework (DRF) + GraphQL  
- **DevOps:** Docker, GitHub Actions (CI/CD)  
- **Security:** JWT, OAuth2, rate limiting  

## 🛠️ Tech Stack  
- **Backend:** Django (Python)  
- **Database:** MySQL (with PostgreSQL-compatible design for scalability)  
- **API:** Django REST Framework (DRF) + GraphQL  
- **DevOps:** Docker, GitHub Actions (CI/CD)  
- **Security:** JWT, OAuth2, rate limiting  

## 👥 Team Roles  
- **Backend Developer:** Builds APIs, integrates databases, implements security.  
- **Database Administrator:** Designs schemas, optimizes queries, ensures data integrity.  
- **DevOps Engineer:** Manages CI/CD, cloud deployment, and monitoring.  
- **QA Engineer:** Tests APIs, reviews security, validates edge cases.  

## 🗄️ Database Design  
### Key Entities:  
1. **Users**  
   - `id`, `email`, `password_hash`, `role` (host/guest)  
   - *Relationships*: One-to-many → `Properties`, `Bookings`.  

2. **Properties**  
   - `id`, `title`, `price`, `location`, `host_id` (FK to Users)  
   - *Relationships*: Many-to-many → `Bookings`.  

3. **Bookings**  
   - `id`, `guest_id` (FK to Users), `property_id` (FK to Properties), `check_in`, `check_out`  

## ✨ Feature Breakdown  
- **User Management**: Signup/login, role-based permissions (host/guest).  
- **Property Listings**: Hosts create/edit listings; guests search/filter.  
- **Booking System**: Date availability checks, payment integration.  
- **Reviews**: Guests leave ratings; hosts respond.  