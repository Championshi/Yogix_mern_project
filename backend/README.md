# yogamaster-server

 # 🧘 Yoga Master - Backend (Node.js + Express + MongoDB)

This is the backend for the Yoga Master MERN stack application. It manages users, classes, instructors, cart operations, payments (Stripe), and admin-level controls using MongoDB as the primary database.

---

## 📦 Technologies Used

- **Node.js**
- **Express.js**
- **MongoDB (with Mongoose + MongoClient)**
- **JWT (jsonwebtoken)**
- **Stripe for payments**
- **dotenv for environment configuration**
- **CORS for cross-origin handling**
- **Cookie-parser & Body-parser**

---

## 🚀 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/yoga-master-backend.git
cd yoga-master-backend
. Install Dependencies
bash
Copy
Edit
npm install
3. Create a .env File
Make a .env file in the root directory and add the following:

env
Copy
Edit
DB_PASSWORD=your_mongodb_password
ACCESS_SECRET=your_jwt_secret
STRIPE_API_KEY=your_stripe_secret_key
Make sure your MongoDB URI is structured like this: mongodb+srv://jins:${process.env.DB_PASSWORD}@cluster0.6mg1vml.mongodb.net/mern-yogamaster

🧪 Start the Server
bash
Copy
Edit
npm run start
It will start your server on the default port (e.g. localhost:5000 if set).

🛠️ API Endpoints
🔐 Authentication
POST /api/set-token — Set JWT token on login

👤 User Management
POST /new-user — Register a new user

GET /getallusers — Fetch all users

GET /user/id/:id — Fetch user by ID

GET /user/:email — (Protected) Fetch user by email

DELETE /user/:id — Delete user by ID

DELETE /delete-user/:id — (Admin only) Delete user

PUT /update-user/:id — (Admin only) Update user profile

🧑‍🏫 Instructor Routes
GET /instructors — Get all instructors

📚 Class Management
POST /new-class — (Instructor only) Create a new class

PUT /update-class/:id — (Instructor only) Update a class

PUT /change-class/:id — (Instructor only) Request changes for approval

PUT /change-status/:id — (Admin only) Approve/Reject a class

GET /getallclasses — Get all approved classes

GET /classes-manage — Get all classes (admin view)

GET /classes/:email — (Instructor only) Get all classes by email

GET /pendingclasses/:email — Get all pending classes

GET /approvedclass/:email — Get all approved classes

GET /classes/id/:id — Get single class details

🛒 Cart Operations
POST /add-to-cart — (Protected) Add item to cart

GET /cart/:email — (Protected) Get items in cart

More payment, enrolled, and application-related endpoints are likely present after this block.

🔐 Middleware
verifyJWT — Verifies if a valid JWT token is present

verifyAdmin — Checks if user role is admin

verifyInstructor — Checks if user is instructor or admin

🧾 Payments Integration
Integrated with Stripe API

Add your STRIPE_API_KEY in .env for live or test mode.

🧠 MongoDB Collections
users

classes

cart

enrolled

payments

applied

📌 Author
Developed by Abhinav
Drop a ⭐ if you like it!



