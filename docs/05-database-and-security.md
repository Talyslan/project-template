# 🗄️🔐 Database & Security

## Database Overview

The system uses a relational database to store structured data securely and efficiently.  
It is designed to support core features while allowing future expansion.

- Type: Relational (e.g., PostgreSQL, MySQL, SQLite)
- Accessed via ORM or query layer (e.g., Prisma, Sequelize, TypeORM)
- Ensures data integrity and consistency

## Tables & Models

### Example Tables

| Table Name  | Purpose                          |
|-------------|----------------------------------|
| users       | Stores user accounts and info    |
| tasks       | Stores tasks created by users    |
| projects    | Optional grouping of tasks       |
| activity_log| Tracks user actions for audit    |

Each table should include:

- Primary key
- Relevant foreign keys
- Timestamps (created_at, updated_at)

> Replace table names and fields based on your project needs.

## Relationships

- **One-to-Many:**  
  - `users → tasks` (one user can have many tasks)  
  - `projects → tasks` (one project can contain many tasks)

- **Many-to-Many:**  
  - Optional if adding shared tasks or teams  
  - Use a join table (e.g., `user_projects`)

> Define relationships clearly to maintain data integrity.

## Constraints

- Primary and foreign key constraints
- Unique fields where needed (e.g., email)
- NOT NULL where required
- Indexes for performance-critical queries

## Authentication

- Users must sign up / log in to access protected features
- Recommended methods:
  - JWT (JSON Web Tokens)
  - OAuth 2.0 (for social login)
- Passwords stored hashed with strong algorithms (e.g., bcrypt)

## Authorization

- Role-based access control (RBAC) or permission flags
- Protect routes / API endpoints based on user roles
- Ensure users cannot access or modify data they don’t own

## Data Protection

- Sensitive information encrypted at rest and in transit (HTTPS, TLS)
- Environment variables for secrets (API keys, database passwords)
- Backups and disaster recovery plan recommended
- Logging and monitoring for security incidents
