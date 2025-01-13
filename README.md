# Login and Registration System

A practice project for building a **Login and Registration** page with added functionality to improve user experience and security.

---

## 📜 Features

### 1. **Registration System**
- Users can create an account with their email and password.
- If a user tries to register with an email that already has an account, they will be notified: 
  - _"This email is already registered. Please log in."_

### 2. **Login System**
- Users can log in with their email and password.
- Incorrect login attempts are limited to 5.
  - After 5 failed attempts, users are blocked temporarily:
    - _"Too many failed login attempts. Please try again after 30 minutes."_

### 3. **DDoS Prevention**
- Temporary lockout for repeated failed login attempts to protect against brute force attacks.
- Timeout period: **30 minutes**.

---

## 🛠️ Tech Stack

- **Frontend:** Next.js
- **Backend:** Node.js with Next.js API routes
- **Database:** MongoDB with Prisma ORM
- **Package Manager:** pnpm
- **Security:** Password hashing (e.g., bcrypt), Rate-limiting middleware

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
$ git clone https://github.com/qinisonhlakaniphoxulu/login.git
$ cd login
```

### 2. Install Dependencies
```bash
$ pnpm install
```

### 3. Set Up the Database
- Ensure MongoDB is running locally or use a cloud-based MongoDB instance.
- Configure the `.env` file with your database connection string (use `.env.template` as an example):
  ```env
  DATABASE_URL=mongodb+srv://username:password@cluster.mongodb.net/dbname?retryWrites=true&w=majority
  ```
- Run Prisma migrations to set up the schema:
```bash
$ pnpm prisma migrate dev
```

### 4. Start the Development Server
```bash
$ pnpm dev
```

### 5. Open the Application
Go to your browser and visit:
```
http://localhost:3000
```

---

## 📸 Screenshots

### Registration Page:
- **Inputs for email and password.**
- **Error message** when the user already has an account.

### Login Page:
- **Inputs for email and password.**
- **Error message** on incorrect login.
- **Lockout message** after 5 failed attempts.

---

## 📂 Folder Structure
```plaintext
login-registration-system/
├── prisma/
│   ├── schema.prisma
├── app/
│   ├── api
│   │   ├── auth/
│   │   │   ├── login.ts
│   │   │   ├── register.ts
│   │   ├── globals.css
|   |   ├── layout.tsx
|   |   ├── page.tsx
├── .env.template (.env.local / .env.development)
├── package.json
├── pnpm-lock.yaml
├── README.md
```

---

## 🌟 Future Improvements

- Add **password recovery** via email.
- Implement **multi-factor authentication** for enhanced security.
- Enhance **UI/UX** with additional Next.js components and animations.
- Add support for OAuth (e.g., Google, Facebook login).

---

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Fork the repository.
- Create a new branch for your feature/bugfix.
- Submit a pull request.

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 💡 Acknowledgments

- Inspired by common login systems and security best practices.
- Thanks to the open-source community for resources and tools.

---

### 🔗 Stay Connected

- **GitHub:** [qinisonhlakaniphoxulu](https://github.com/qinisonhlakaniphoxulu)
- **LinkedIn:** [Qiniso Xulu](https://linkedin.com/in/qinisoxulu)

