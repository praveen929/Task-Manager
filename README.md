# Task Manager Application

A full-stack task management application built with Next.js and Express.js.

## Project Structure

- `client/`: Next.js frontend application
- `backend/`: Express.js backend API

## Setup Instructions

### Backend Setup

1. Navigate to the backend directory:

   ```
   cd backend
   ```

2. Install dependencies:

   ```
   npm install
   ```

3. Create a `.env` file with the following variables:

   ```
   MONGO_URI=mongodb://localhost:27017/testing
   JWT_SECRET=your_secret_key
   CLIENT_URL=http://localhost:3000
   PORT=8000
   ```

4. Start the backend server:
   ```
   npm start
   ```

### Frontend Setup

1. Navigate to the client directory:

   ```
   cd client
   ```

2. Install dependencies:

   ```
   npm install
   ```

3. Create a `.env.local` file with the following variables:

   ```
   NEXT_PUBLIC_API_URL=http://localhost:8000
   ```

4. Start the frontend development server:
   ```
   npm run dev
   ```

## Running on Different Machines

When running the application on different machines, you need to:

1. Update the `NEXT_PUBLIC_API_URL` in the client's `.env.local` file to point to your backend server's address.
2. Update the `CLIENT_URL` in the backend's `.env` file to allow CORS from your client's address.

For example, if your backend is running on a machine with IP 192.168.1.100:

- In client's `.env.local`:

  ```
  NEXT_PUBLIC_API_URL=http://192.168.1.100:8000
  ```

- In backend's `.env`:
  ```
  CLIENT_URL=http://your-client-machine-address:3000
  ```

## Features

- User authentication (register, login, logout)
- Task management (create, read, update, delete)
- Task filtering by status (completed, pending, overdue)
- User profile management

## Technologies Used

- **Frontend**: Next.js, React, Tailwind CSS
- **Backend**: Express.js, MongoDB
- **Authentication**: JWT
