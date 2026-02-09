# NextAuth Authentication

A full-featured authentication system built with Next.js 14 and NextAuth v5, featuring credentials-based login, OAuth providers, email verification, password reset, and two-factor authentication.

# Features

## Authentication Methods

- **Credentials Authentication** - Email and password-based login with bcrypt password hashing
- **OAuth Providers** - Sign in with GitHub and Google

## Security Features

- **Email Verification** - Verify user emails before allowing access
- **Two-Factor Authentication (2FA)** - Optional 2FA with email-based tokens
- **Password Reset** - Secure password reset flow with email tokens
- **Role-Based Access Control** - User and Admin roles for authorization

## Route Protection

- Middleware-based route protection
- Public, authentication, and protected routes configuration

# Tech Stack

- **Framework:** Next.js 14 (App Router)
- **Authentication:** NextAuth v5
- **Database:** MongoDB with Prisma ORM
- **UI:** Tailwind CSS, Radix UI components
- **Form Validation:** React Hook Form + Zod
- **Email Service:** Resend
- **Language:** TypeScript

# Key Features Implementation

## Database Schema

The application uses Prisma with MongoDB and includes models for:

- User authentication and profiles
- OAuth accounts
- Email verification tokens
- Password reset tokens
- Two-factor authentication tokens and confirmations

## Authentication Pages

- `/auth/login` - User login
- `/auth/register` - User registration
- `/auth/new-password` - Set new password
- `/auth/new-verification` - Email verification
- `/auth/reset` - Password reset request
- `/auth/error` - Authentication errors

### Protected Routes

Protected routes redirect unauthenticated users to the login page and authenticated users access the settings page by default.

### Email Configuration

The project uses Resend for sending emails:

- Email verification links
- Password reset links
- Two-factor authentication codes
  inks
- Password reset links
- Two-factor authentication codes
