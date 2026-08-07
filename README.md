# FullStackLab

A full-stack e-commerce practice project: Node.js + Express backend, MySQL database,
and a Bootstrap 5 frontend with user authentication and a product catalog.

Built as a hands-on exercise to practice the MVC + Repository architecture across
the whole stack: views, controllers, services, repositories, and relational storage.

## Tech Stack

- **Backend**: Node.js, Express 4
- **Database**: MySQL (mysql2)
- **Frontend**: Bootstrap 5, vanilla JavaScript (ES modules)
- **Architecture**: MVC + Repository (Controller → Service → Repository)

## Features

- **User registration** with client-side validation:
  - Full name, email, phone, and document number validation
  - Password strength indicator and policy (8+ chars, uppercase, number, special char)
  - Duplicate detection for document number and username
- **Login** with user verification against the database
- **Product catalog** page rendered with Bootstrap cards
- Responsive Bootstrap 5 UI

## Project Structure

```
src/
├── controllers/      # Request handlers (login, register, catalog)
├── services/         # Business logic (validation, duplicate checks)
├── repositories/     # Data access layer (MySQL queries)
├── routes/           # Express route definitions
├── views/            # HTML pages (login, register, catalog)
└── public/           # Static assets (CSS, JS, images)
```

## Prerequisites

- Node.js 18+
- MySQL (local server, e.g. XAMPP/WAMP)
- npm

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/stefieston/FullStackLab.git
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up the database:
   - Run `ecommerce.sql` in your MySQL server to create the `ecommerce` database
     and the `users` table (includes a default `admin` user).

4. Configure the DB connection in `src/repositories/userRepository.js`
   (host, user, password, database).

5. Start the server:
   ```bash
   npm start
   ```

6. Open `http://localhost:3000` in your browser.

## Roadmap

- [ ] Hash passwords (e.g. bcrypt) instead of storing them in plain text
- [ ] Add sessions or JWT-based authentication
- [ ] Serve the catalog dynamically from the database
- [ ] Move DB credentials to environment variables
- [ ] Add tests

## Contributing

Fork the repository and submit a pull request. Keep the existing code style
and follow the MVC + Repository structure.

## License

ISC
