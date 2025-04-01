# intelliB
## Backend API

This is a simple backend API built using Node.js, Express, TypeScript, and Prisma ORM. It provides basic authentication functionality with user registration and login features.

### Project Structure
```
backend/
├── node_modules/
├── prisma/
│   ├── migrations/
│   ├── schema.prisma
├── src/
│   ├── controllers/
│   │   ├── userController.ts
│   ├── routes/
│   │   ├── userRoutes.ts
│   ├── utils/
│   ├── index.ts
├── .env
├── .gitignore
├── package-lock.json
├── package.json
├── tsconfig.json
```

### Technologies Used
- Node.js
- Express.js
- TypeScript
- Prisma ORM
- PostgreSQL (or any Prisma-supported database)
- bcrypt.js (for password hashing)
- JSON Web Tokens (JWT) for authentication
- dotenv for environment variable management

### Installation

1. Clone the repository:
   ```sh
   git clone <repo_url>
   cd backend
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Set up environment variables:
   Create a `.env` file in the root directory and add:
   ```env
   DATABASE_URL="your_database_url"
   JWT_SECRET="your_secret_key"
   ```
4. Run Prisma migrations:
   ```sh
   npx prisma migrate dev --name init
   ```
5. Start the development server:
   ```sh
   npm run dev
   ```

### API Endpoints
#### User Authentication
##### Register a new user
- **Endpoint:** `POST /register`
- **Body:**
  ```json
  {
    "email": "user@example.com",
    "password": "password123"
  }
  ```
- **Response:**
  ```json
  {
    "id": 1,
    "email": "user@example.com"
  }
  ```

##### Login user
- **Endpoint:** `POST /login`
- **Body:**
  ```json
  {
    "email": "user@example.com",
    "password": "password123"
  }
  ```
- **Response:**
  ```json
  {
    "token": "jwt_token_here"
  }
  ```

### License
This project is licensed under the ISC License.

