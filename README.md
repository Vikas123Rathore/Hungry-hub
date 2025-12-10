# Hungry-hub

A full-stack delivery management application with real-time features, built with Node.js, Express, and React.

## 📋 Project Overview

Hungry-hub is a comprehensive delivery platform that connects shops, customers, and delivery services. The application features real-time order tracking, user authentication, and a modern responsive interface.

## 🏗️ Project Structure

```
vingo/
├── backend/              # Node.js/Express server
│   ├── config/          # Database and configuration files
│   ├── controllers/     # Business logic controllers
│   ├── middlewares/     # Authentication and file upload middleware
│   ├── models/          # Database models (Mongoose schemas)
│   ├── routes/          # API route definitions
│   ├── utils/           # Utility functions
│   ├── public/          # Static files
│   ├── index.js         # Server entry point
│   └── socket.js        # WebSocket/Socket.io configuration
│
└── frontend/            # React/Vite application
    ├── src/             # React source code
    ├── public/          # Static assets
    ├── firebase.js      # Firebase configuration
    └── index.html       # Entry HTML file
```

## ✨ Features

- **User Authentication**: Secure login and registration system
- **Shop Management**: Create and manage shop profiles
- **Item Management**: Add, edit, and manage products/items
- **Order System**: Place and track orders in real-time
- **Delivery Assignment**: Assign and track delivery personnel
- **Real-time Updates**: WebSocket integration for live order status
- **File Upload**: Image upload support for shops and items
- **Firebase Integration**: Enhanced authentication and storage

## 🚀 Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- MongoDB database
- Firebase account (for additional features)

### Backend Setup

1. Navigate to the backend directory:
```bash
cd backend
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the backend directory with the following variables:
```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
NODE_ENV=development
```

4. Start the backend server:
```bash
npm start
```

The backend server will run on `http://localhost:5000` (or your specified PORT).

### Frontend Setup

1. Navigate to the frontend directory:
```bash
cd frontend
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the frontend directory with the following variables:
```env
VITE_API_URL=http://localhost:5000
VITE_FIREBASE_API_KEY=your_firebase_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_firebase_auth_domain
VITE_FIREBASE_PROJECT_ID=your_firebase_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_firebase_storage_bucket
VITE_FIREBASE_MESSAGING_SENDER_ID=your_messaging_sender_id
VITE_FIREBASE_APP_ID=your_firebase_app_id
```

4. Start the development server:
```bash
npm run dev
```

The frontend application will run on `http://localhost:5173` (default Vite port).

## 🛠️ Tech Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web application framework
- **MongoDB** - Database
- **Socket.io** - Real-time bidirectional communication
- **Multer** - File upload handling
- **JWT** - Authentication tokens

### Frontend
- **React** - UI library
- **Vite** - Build tool and development server
- **Firebase** - Authentication and storage services

## 📡 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login

### Users
- `GET /api/users` - Get all users
- `GET /api/users/:id` - Get user by ID
- `PUT /api/users/:id` - Update user
- `DELETE /api/users/:id` - Delete user

### Shops
- `GET /api/shops` - Get all shops
- `POST /api/shops` - Create new shop
- `GET /api/shops/:id` - Get shop by ID
- `PUT /api/shops/:id` - Update shop
- `DELETE /api/shops/:id` - Delete shop

### Items
- `GET /api/items` - Get all items
- `POST /api/items` - Create new item
- `GET /api/items/:id` - Get item by ID
- `PUT /api/items/:id` - Update item
- `DELETE /api/items/:id` - Delete item

### Orders
- `GET /api/orders` - Get all orders
- `POST /api/orders` - Create new order
- `GET /api/orders/:id` - Get order by ID
- `PUT /api/orders/:id` - Update order status
- `DELETE /api/orders/:id` - Cancel order

## 🔒 Security

- JWT-based authentication
- Password hashing
- Protected routes with middleware
- Environment variables for sensitive data
- CORS configuration

## 📝 Development

### Running in Development Mode

Backend:
```bash
cd backend
npm run dev
```

Frontend:
```bash
cd frontend
npm run dev
```

### Building for Production

Frontend:
```bash
cd frontend
npm run build
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License.

## 👥 Contact

For questions or support, please open an issue in the repository.

---

**Note**: Make sure to configure your `.env` files properly before running the application. Never commit `.env` files to version control.
```
