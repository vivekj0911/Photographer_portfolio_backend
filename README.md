# 🖥️ V-Digitals – Photographer Portfolio (Backend)

This is the **backend API** for *V-Digitals*, a modern photographer portfolio website.  
It is built with **Node.js + Express** and uses **MongoDB** for database storage.  
The backend handles:
- Media upload & management (images/videos)
- Admin authentication
- Feedback submission & approval
- API endpoints for the frontend

Live API: [https://v-digitals-backend.onrender.com](https://v-digitals-backend.onrender.com)

---

## 🚀 Tech Stack
- **Node.js**
- **Express.js**
- **MongoDB + Mongoose**
- **Multer** – File uploads
- **CORS** – Cross-origin support
- **JWT** – Admin authentication
- **dotenv** – Environment variable management

---

## 📂 Folder Structure
```
Directory structure:
└── vivekj0911-photographer_portfolio_backend/
    ├── generateHash.js
    ├── package.json
    ├── sample.env
    ├── server.js
    ├── Config/
    │   └── cloudinary.js
    ├── controllers/
    │   ├── authController.js
    │   ├── feedbackController.js
    │   └── mediaController.js
    ├── middleware/
    │   └── auth.js
    ├── models/
    │   ├── Feedback.js
    │   └── Media.js
    └── routes/
        ├── authRoutes.js
        ├── feedbackRoutes.js
        └── mediaRoutes.js

```

---

## ⚙️ Installation & Setup
```bash
# 1️⃣ Clone the repository
git clone https://github.com/vivekj0911/Photographer_portfolio_backend.git

# 2️⃣ Navigate into the project folder
cd backend

# 3️⃣ Install dependencies
npm install

# 4️⃣ Run the server
npm run dev
```

---

## 🔑 Environment Variables
Create a `.env` file in the root with:

```env
PORT=5000
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_secret_key
ADMIN_USERNAME=your_admin_username
ADMIN_PASSWORD_HASH=hashed_password_from_bcrypt
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```

> ⚠️ Do **NOT** commit `.env` files to GitHub (add it to `.gitignore`).

---

## 📡 API Endpoints

### Auth Routes
- **POST** `/api/auth/login` → Admin login (returns JWT)

### Media Routes
- **POST** `/api/media/upload` → Upload image/video (Admin only)
- **GET** `/api/media/:category` → Get media by category
- **DELETE** `/api/media/:id` → Delete media (Admin only)

### Feedback Routes
- **POST** `/api/feedback` → Submit feedback (public)
- **GET** `/api/feedback` → Get approved feedback (public)
- **PATCH** `/api/feedback/:id/approve` → Approve feedback (Admin only)

---

## 📌 Features
- Secure **JWT-based authentication** for admin
- File uploads using **Multer**
- Organized **media categories** (baby shoot, maternity shoot, weddings, etc.)
- Feedback approval workflow
- CORS configuration for frontend integration
- Optimized API responses for fast gallery loading

---

## 🌐 Deployment
The backend is deployed on **Render**.  
To deploy your own:
```bash
# Install Render CLI (optional for local deploys)
npm install -g render-cli

# Or deploy from GitHub using Render dashboard
```

---

## 🔗 Frontend Repository
Frontend code is available here:  
[https://github.com/vivekj0911/V_Studios_Portfolio_Web](https://github.com/vivekj0911/V_Studios_Portfolio_Web)

---

## 📜 License
This project is licensed under the **MIT License** – you’re free to use, modify, and distribute with attribution.

---

## ✨ Author
Developed by **Vivek Janbandhu**  
📷 Photographer: **Vidhi Digitals**
