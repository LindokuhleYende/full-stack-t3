# 📝 T3 Stack To-Do App

This is a simple **To-Do application** built using the **T3 Stack** (Next.js, tRPC, Prisma, and NextAuth).  
The app uses **email-based authentication**, **SQLite** for the database, and **Prisma Studio** for database viewing.

---

##  Features

- Email-based authentication using NextAuth
- Verification link printed to the server console
- Create and view to-do items
- SQLite database
- Prisma ORM with migrations
- Prisma Studio for database inspection

---

## 🧱 Tech Stack

- **Next.js**
- **tRPC**
- **Prisma**
- **NextAuth**
- **SQLite**

---

## 🔐 Authentication Flow

The app uses **email authentication** through NextAuth.

1. On the sign-in page, the user enters their email.
2. A verification link is generated.
3. Instead of sending an email, the verification link is printed to the **server console**.
4. The user opens the link from the console to complete login.
5. After authentication, the user can create

This behavior is configured in:
/src/server/auth.ts

The email provider is set up to log the verification link using `console.log()` instead of sending a real email.

---

## 📋 To-Do Functionality

Once logged in, users can:
- Create new to-do items
- View existing to-dos

This is a simple CRUD setup meant for learning and experimentation.
---

## 🧪 Running the App
npm run dev


Then open:

http://localhost:3000


Sign in with your email, copy the verification link from the terminal, and start adding to-dos.


---

## 🗄 Database Setup (Prisma + SQLite)

This project uses **SQLite** as the database and **Prisma** as the ORM.

## Generate Prisma Client
```bash
npx prisma generate

Create & Apply Migrations
npx prisma migrate dev --name init

This:

->Creates the database
->Applies the schema
->Generates a migration SQL file at:
    /prisma/migrations/**/migration.sql

##🔍 Viewing the Database
To open Prisma Studio:

>>npx prisma studio
You’ll see a message :Prisma Studio is up on http://localhost:5555

Open that link in your browser to:
1.View tables
2.Inspect users and to-dos
3.Edit records manually

