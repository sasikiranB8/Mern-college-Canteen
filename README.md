# 🍴 MERN College Canteen

A full-stack MERN application designed to **digitalize and streamline the college canteen experience**.  

This system provides:  
- 🎓 **Student App** – Browse menu & place orders  
- 🛠️ **Admin Dashboard** – Manage items, orders, and sales statistics  
- ⚡ **Backend API** – Node.js + Express with secure authentication & MongoDB  

---

## 📂 Project Structure  

```bash
Canteen/  
│── backend/                # Node.js + Express + MongoDB REST API  
│   ├── models/             # Mongoose schemas (User, Items, Orders, Cart)  
│   ├── routes/             # API routes (auth, items, cart, orders, sales)  
│   ├── controllers/        # Controller logic for CRUD operations  
│   ├── middlewares/        # Auth middleware, Multer, uploads, error handling  
│   ├── utils/              # bcrypt, JWT, Cloudinary helpers  
│   ├── connect.js          # MongoDB connection  
│   └── server.js           # Backend entrypoint  

│── admin/                  # React admin dashboard  
│   ├── src/  
│   │   ├── components/     # UI components (charts, tables, order cards)  
│   │   ├── pages/          # Pages (Orders, Analytics, Inventory, Users)  
│   │   ├── context/        # Context API for admin state  
│   │   └── utils/          # Debouncing, custom hooks  

│── client/                 # React student app  
│   ├── src/  
│   │   ├── components/     # Menu, Cart, Checkout  
│   │   ├── pages/          # Home, Orders, Profile  
│   │   ├── context/        # Cart & Auth context  
│   │   └── utils/          # Debouncing search, API helpers  

└── README.md               # Project Documentation  


🚀 Features
🔒 Authentication & Security

JWT Authentication for secure sessions

bcrypt password hashing

Role-based access (Student / Admin)

🍔 Menu & Ordering

Students can browse menu items by category

Add to cart, update quantity, remove items

Place orders with real-time order tracking (preparing → out for delivery → done)

🛠️ File Uploads

Multer for handling item image uploads

Cloudinary integration for secure storage & fast delivery

⚡ Frontend Enhancements

Debouncing for search inputs

Context API for global state management (Cart, Orders, Auth)

Green-themed modern UI with responsive design

📊 Admin Dashboard

View all orders (with live status updates)

Manage inventory (CRUD on items)

Track sales statistics & analytics:

Daily/Monthly revenue

Most popular items

Total completed orders

Pending vs Completed orders

📡 API Documentation
👤 Authentication
Method	Endpoint	Description
POST	/cred/signup	Register new user
POST	/cred/login	Login & get JWT token
🛒 Cart
Method	Endpoint	Description
POST	/user/cart/addcartitem/:userid	Add item to cart
PATCH	/user/cart/updatecartitem/:userid	Update item quantity
DELETE	/user/cart/deletecartitem/:userid	Delete item from cart
GET	/user/cart/getcartitems/:userid	Fetch user’s cart items
🍔 Items
Method	Endpoint	Description
POST	/admin/items/additem	Add new menu item (with image upload)
GET	/user/items/getitems/:category	Get items by category
DELETE	/admin/items/deleteitem/:itemid	Delete menu item
PATCH	/admin/items/update/:itemid	Update item quantity
PATCH	/admin/items/updateadmin/:itemid	Update item details
📦 Orders
Method	Endpoint	Description
POST	/user/orders/placeorder/:userid	Place an order
GET	/admin/orders/gettotalorders	Get all orders (Admin)
GET	/user/orders/getuserorders/:userid	Get user’s past orders
PATCH	/admin/orders/updateuserorder/:orderid	Update order status (Admin)
📊 Sales (Admin)
Method	Endpoint	Description
GET	/admin/sales	Get sales statistics & revenue reports
📊 Example Sales Statistics (Admin Dashboard)

Total Orders Today: 120

Total Revenue This Month: ₹45,000

Most Ordered Item: Veg Burger (320 orders)

Pending Orders: 12

Delivered Orders: 85%

🛠️ Tech Stack
Backend

Node.js + Express.js

MongoDB with Mongoose

JWT Authentication

bcrypt for password hashing

Multer + Cloudinary for image uploads

Frontend (Client + Admin)

React.js (hooks + functional components)

Context API for global state

Axios for API requests

React Router for routing

Debouncing for search optimization

⚙️ Setup Instructions
1️⃣ Clone Repository
git clone https://github.com/sasikiranB8/Mern-college-Canteen
cd Mern-college-Canteen

2️⃣ Backend Setup
cd backend
npm install


Create .env file:

MONGO_URI=your_mongodb_url
JWT_SECRET=your_secret
CLOUDINARY_CLOUD_NAME=xxxx
CLOUDINARY_API_KEY=xxxx
CLOUDINARY_API_SECRET=xxxx
PORT=5000


Start server:

npm start

3️⃣ Client Setup
cd ../client
npm install
npm start

4️⃣ Admin Setup
cd ../admin
npm install
npm start

📈 Future Improvements

Payment Gateway Integration (Stripe / Razorpay)

Push Notifications for order updates

AI-driven menu recommendations

Exportable sales reports (CSV/PDF)

Multi-admin access with role hierarchy

👨‍💻 Author

SasiKiran Simma
📌 MERN Developer | Problem Solver | Open Source Contributor
