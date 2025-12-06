# API Documentation

## 1. Authentication Module (AuthController)

Handles login, 2FA, and password recovery.

| Method | Endpoint | Description | Access |
|------|---------|------------|--------|
| POST | /api/auth/login | Login with username/password. Returns JWT for Staff; prompts 2FA for Admin. | Public |
| POST | /api/auth/2fa/send | Send 2FA OTP to Admin (Email/Phone). | Admin (Partial Auth) |
| POST | /api/auth/2fa/verify | Verify Admin OTP and return final JWT. | Admin (Partial Auth) |
| POST | /api/auth/forgot-password/initiate | Send OTP to reset forgotten credentials. | Public |
| POST | /api/auth/forgot-password/verify | Verify OTP and get a temporary reset token. | Public |
| POST | /api/auth/forgot-password/reset | Use reset token to change username/password. | Public |
| POST | /api/auth/staff/reset/initiate | Send OTP for logged-in Staff to change their own info. | Staff |
| POST | /api/auth/staff/reset/verify | Verify OTP and update Staff credentials. | Staff |

---

## 2. User Management Module (UserController)

Handles managing employees (Staff) and Admins.

| Method | Endpoint | Description | Access |
|------|---------|------------|--------|
| GET | /api/users | Get a list of all users (Staff & Admins). | Admin |
| GET | /api/users/{id} | Get details of a specific user. | Admin |
| POST | /api/users | Register a new user (Staff/Admin). | Admin |
| PUT | /api/users/{id} | Update user details (Email, Phone, Role). | Admin |
| DELETE | /api/users/{id} | Remove a user from the system. | Admin |
