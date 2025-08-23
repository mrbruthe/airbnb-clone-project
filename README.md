# Airbnb Clone Project

## Overview
This project is a clone of Airbnb, designed to practice and showcase full-stack development skills.

## Goals
- Recreate core Airbnb features (listings, bookings, user authentication, payments, etc.)
- Learn and apply modern web development practices
- Build a scalable, maintainable codebase

## Tech Stack
- Frontend: React, Next.js, TailwindCSS
- Backend: Node.js, Express
- Database: PostgreSQL (with Prisma ORM)
- Authentication: NextAuth
- Deployment: Vercel / Render

## UI/UX Design Planning

### Design Goals
- Create an intuitive booking flow
- Maintain visual consistency across pages
- Ensure fast loading times
- Prioritize mobile responsiveness

### Key Features
- Property search and filtering
- Detailed property viewing
- Secure checkout process
- User authentication

### Primary Pages
| Page | Description |
|------|-------------|
| Property Listing View | Grid display of available properties with filters for price, location, and rating |
| Listing Detailed View | Complete property details with images, description, amenities, and booking form |
| Simple Checkout View | Streamlined payment process with booking confirmation |

### Importance of User-Friendly Design
A well-designed booking system reduces friction in the user journey, increases conversion rates, and improves customer satisfaction. Clear navigation, intuitive interfaces, and responsive design are critical for success.

### Design Properties from Figma

#### Color Styles
- Primary: #34967C
- Secondary: #222222
- Background: #FFFFFF
- Text: #161117
- Secondary Text: #F9F9F9

#### Typography
- Primary Font: Quicksand
  - Headings: Semibold (600), 22px
  - Body Text: Medium (500), 17px
  - Secondary Text: Medium (500), 12.16px

#### Importance of Identifying Design Properties
Identifying colors and typography from the mockup ensures the design is implemented consistently across all pages. It preserves visual identity, improves user experience, and helps developers replicate the intended look and feel accurately.

## Project Roles and Responsibilities.
| Role	| Responsibilities |
|-----|-----------------|
| Project Manager |	Oversees timeline, coordinates team, manages deliverables |
| Frontend Developers |	Implements UI components, ensures responsive design |
| Backend Developers |	Builds APIs, manages database, implements business logic |
| Designers |	Creates mockups, maintains design system, ensures UX quality |
| QA/Testers |	Writes test cases, performs testing, reports bugs |
| DevOps Engineers |	Manages deployment, CI/CD pipeline, server infrastructure |
| Product Owner |	Defines requirements, prioritizes features, represents stakeholders |
| Scrum Master |	Facilitates agile processes, removes blockers, organizes meetings |

## UI Component Patterns

### Planned Components

#### Navbar

- Logo
- Search bar
- User navigation
- Responsive menu

#### Property Card

- Property image
- Basic details (price, location, rating)
- Favorite button
- Responsive layout

#### Footer

- Site links
- Company information
- Social media links
- Copyright information

## Team Roles

| Role                   | Description                                                                                 |
|------------------------|---------------------------------------------------------------------------------------------|
| Backend Developer      | Designs and implements server-side logic, APIs, and ensures integration with the database.   |
| Database Administrator | Manages database schema, optimizes queries, and ensures data integrity and security.         |
| DevOps Engineer        | Sets up CI/CD pipelines, manages deployments, and maintains server infrastructure.           |
| QA/Testers             | Develops and executes test cases, ensures code quality, and reports bugs.                   |
| Product Owner          | Defines requirements, prioritizes features, and represents stakeholders.                    |
| Scrum Master           | Facilitates agile processes, removes blockers, and organizes team meetings.                 |

## Technology Stack

- **Django**: Web framework for building robust RESTful APIs and backend logic.
- **PostgreSQL**: Relational database system for storing structured data securely.
- **GraphQL**: API query language for flexible and efficient data retrieval.
- **Docker**: Containerization tool for consistent development and deployment environments.
- **GitHub Actions**: CI/CD automation for testing and deploying code changes.

## Database Design

**Entities and Key Fields:**
- **User**: id, name, email, password_hash, date_joined
- **Property**: id, owner_id (User), title, description, location, price_per_night
- **Booking**: id, user_id (User), property_id (Property), start_date, end_date, total_price
- **Review**: id, user_id (User), property_id (Property), rating, comment, created_at
- **Payment**: id, booking_id (Booking), amount, payment_method, status, timestamp

**Relationships:**
- A user can own multiple properties.
- A property can have multiple bookings and reviews.
- A booking is linked to one user and one property.
- A payment is associated with a booking.

## Feature Breakdown

- **User Management**: Handles user registration, authentication, and profile management to ensure secure access and personalized experiences.
- **Property Management**: Allows property owners to list, update, and manage their properties, including images and descriptions.
- **Booking System**: Enables users to book available properties, manage reservations, and view booking history.
- **Review System**: Lets users leave feedback on properties, helping maintain quality and trust within the platform.
- **Payment Processing**: Integrates secure payment gateways to handle transactions and booking confirmations.

## API Security

- **Authentication**: Ensures only registered users can access protected endpoints using secure login mechanisms (e.g., JWT, OAuth).
- **Authorization**: Restricts actions based on user roles (e.g., only property owners can edit their listings).
- **Rate Limiting**: Prevents abuse by limiting the number of requests per user/IP.
- **Input Validation**: Protects against injection attacks by validating and sanitizing user input.

Security is crucial to protect user data, prevent unauthorized access, and ensure safe payment processing.

## CI/CD Pipeline

CI/CD pipelines automate code testing, building, and deployment, ensuring rapid and reliable delivery of new features and bug fixes. Tools like **GitHub Actions** and **Docker** are used to automate testing, build container images, and deploy updates to production, reducing manual errors and speeding up development cycles.

## Monorepo Structure

- `frontend/` – All frontend code (React, Next.js, etc.)
- `backend/` – All backend code (Django, Node.js, etc.)


## Database Design

