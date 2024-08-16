# Jump Database

## Overview
The Jump Database is a PostgreSQL database designed to support the URL shortening service (ju.mp). It stores user information, shortened URLs, and analytics data related to the usage of the service. This README provides instructions for setting up and managing the database.

## Database Schema
The database schema includes the following key tables:

- **Users**: Stores user account information.
  - `id`: Primary key, unique identifier for each user.
  - `username`: Unique username for the user.
  - `password_hash`: Hashed password for user authentication.
  - `created_at`: Timestamp of when the user account was created.

- **URLs**: Stores the original and shortened URLs.
  - `id`: Primary key, unique identifier for each URL entry.
  - `user_id`: Foreign key referencing the user who created the URL.
  - `original_url`: The long URL that is being shortened.
  - `shortened_url`: The generated short URL.
  - `click_count`: Number of times the shortened URL has been accessed.
  - `created_at`: Timestamp of when the URL was created.

## Getting Started

### Prerequisites
- Ensure you have PostgreSQL installed on your machine.
- Have access to a terminal or command prompt.

### Setup Instructions

1. **Create the Database**:
   Open your terminal and run the following command to create a new database:
   ```bash
   createdb jump_db
   ```

2. **Run Migrations**:
   If you are using a migration tool (like Knex.js or Sequelize), run the migration command to set up the database schema:
   ```bash
   npm run migrate
   ```

3. **Seed the Database** (Optional):
   If you have seed data to populate the database, run the seed command:
   ```bash
   npm run seed
   ```

4. **Configure Environment Variables**:
   Ensure that your environment variables are set up correctly to connect to the PostgreSQL database. You may need to create a `.env` file in the root of your project with the following variables:
   ```plaintext
   DATABASE_URL=postgres://username:password@localhost:5432/jump_db
   ```

## Development
To contribute to the database setup or management, please follow these guidelines:

- Ensure that any changes to the database schema are documented.
- Write migration scripts for any schema changes.
- Test database interactions thoroughly to ensure data integrity.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- Thanks to the PostgreSQL community for their support and documentation.
- Inspired by various database management practices in web applications.