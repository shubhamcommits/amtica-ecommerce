# 🛒 Amtica E-commerce

> A full-featured, web-based e-commerce platform for managing products, features, categories, and users with role-based administration

[![Node.js](https://img.shields.io/badge/Node.js-10.14.1-green.svg)](https://nodejs.org/)
[![Angular](https://img.shields.io/badge/Angular-6.0.8-red.svg)](https://angular.io/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-brightgreen.svg)](https://www.mongodb.com/atlas)
[![License](https://img.shields.io/badge/License-ISC-blue.svg)](LICENSE)

## 📋 Overview

Amtica E-commerce is a comprehensive e-commerce platform built using the **MEAN** stack (MongoDB, Express.js, Angular, Node.js). The application supports customizable product features, hierarchical category management, and advanced administration through a role-based user interface.

**🌐 Live Demo:** [amitca-ecommerce.herokuapp.com](https://amitca-ecommerce.herokuapp.com/)

## ✨ Features

### 🔐 Role-Based Access Control
- **Root Admin** - Full system control with advanced features
- **Seller** - Product and inventory management
- **Member** - Standard user access

### 📦 Product Management
- Create, update, and manage products
- Associate products with categories and subcategories
- Upload product images with Multer
- Define product specifications and details

### 🎛️ Custom Feature System
- **Single Choice** - Radio button style features
- **Multiple Choice** - Checkbox style features
- **Fill-in-the-Blank** - Text input features
- Define possible options/answers for each feature

### 📂 Category Organization
- Hierarchical category structure
- Unlimited subcategory nesting
- Easy product categorization
- Bulk category operations

### 👥 User Management
- Secure authentication with JWT
- Password hashing with bcrypt
- Profile pictures and contact information
- User roles and permissions

### 🎨 Modern UI/UX
- Responsive design with Bootstrap
- FontAwesome icons
- Dynamic reactive forms
- Mobile-friendly interface

## 🛠️ Tech Stack

### Backend

| Technology | Version | Purpose |
|------------|---------|---------|
| **Node.js** | 10.14.1 | Runtime environment |
| **Express.js** | 4.16.2 | Web framework |
| **MongoDB** | - | NoSQL database |
| **Mongoose** | 5.0.2 | MongoDB ODM |
| **JWT** | 8.1.1 | Authentication tokens |
| **bcrypt** | 3.0.2 | Password hashing |
| **Multer** | 1.4.1 | File upload handling |
| **Socket.io** | 2.1.1 | Real-time communication |
| **Morgan** | 1.9.0 | HTTP request logging |
| **CORS** | 2.8.4 | Cross-origin resource sharing |

### Frontend

| Technology | Purpose |
|------------|---------|
| **Angular 6** | Frontend framework |
| **TypeScript** | Programming language |
| **Bootstrap** | UI components |
| **FontAwesome** | Icon library |
| **RxJS** | Reactive programming |
| **SCSS** | Styling |
| **Karma** | Unit testing |
| **Protractor** | E2E testing |

## 📁 Project Structure

```
amtica-ecommerce/
├── 📂 public/                      # Angular frontend application
│   ├── 📂 dist/public/            # Production build output
│   ├── 📂 e2e/                    # End-to-end test specs
│   ├── 📂 src/                    # Angular source code
│   │   ├── 📂 app/               # Application components
│   │   │   ├── 📂 root-admin/   # Admin dashboard components
│   │   │   ├── 📂 products/     # Product management
│   │   │   ├── 📂 categories/   # Category management
│   │   │   └── 📂 shared/       # Shared components
│   │   ├── 📂 assets/            # Static assets
│   │   └── 📂 environments/      # Environment configs
│   ├── angular.json
│   ├── tsconfig.json
│   └── package.json
│
├── 📂 src/                         # Backend source code
│   ├── 📂 api/
│   │   ├── 📂 controllers/       # Route controllers
│   │   ├── 📂 models/            # Mongoose schemas
│   │   │   ├── categories.model.js
│   │   │   ├── product.model.js
│   │   │   └── user.model.js
│   │   ├── 📂 routes/            # API routes
│   │   │   ├── category.route.js
│   │   │   ├── product.route.js
│   │   │   └── user.route.js
│   │   └── app.js                 # Express configuration
│   ├── 📂 utils/                  # Utility functions
│   └── db.js                      # MongoDB connection
│
├── 📂 uploads/                     # Uploaded files storage
├── development.config.js           # Development config
├── nodemon.json                    # Nodemon config
├── package.json                    # Backend dependencies
└── server.js                       # Entry point
```

## 🚀 Getting Started

### Prerequisites

- **Node.js** >= 10.x
- **npm** >= 6.x
- **MongoDB** (local or cloud instance)
- **Angular CLI** v6.0.8

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/shubhamcommits/amtica-ecommerce.git
   cd amtica-ecommerce
   ```

2. **Install backend dependencies**
   ```bash
   npm install
   ```

3. **Install frontend dependencies**
   ```bash
   cd public
   npm install
   cd ..
   ```

4. **Configure environment**
   
   Update MongoDB connection in `src/db.js`:
   ```javascript
   const dbURL = 'mongodb://localhost:27017/amtica-ecommerce';
   // OR for MongoDB Atlas:
   const dbURL = 'mongodb+srv://<username>:<password>@cluster.mongodb.net/amtica';
   ```

### Running the Application

#### Development Mode

1. **Start the backend server**
   ```bash
   npm run dev
   ```
   Backend runs at `http://localhost:3000`

2. **Start the Angular dev server** (new terminal)
   ```bash
   cd public
   ng serve
   ```
   Frontend runs at `http://localhost:4200`

#### Production Mode

1. **Build the Angular app**
   ```bash
   cd public
   ng build --prod
   cd ..
   ```

2. **Start the server**
   ```bash
   npm start
   ```
   
   Access the app at `http://localhost:3000`

## 📡 API Endpoints

### Categories
| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/categories` | Get all categories |
| `GET` | `/api/categories/:id` | Get category by ID |
| `POST` | `/api/categories` | Create new category |
| `PUT` | `/api/categories/:id` | Update category |
| `DELETE` | `/api/categories/:id` | Delete category |

### Products
| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/products` | Get all products |
| `GET` | `/api/products/:id` | Get product by ID |
| `POST` | `/api/products` | Create new product |
| `PUT` | `/api/products/:id` | Update product |
| `DELETE` | `/api/products/:id` | Delete product |

### Users
| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/users` | Get all users |
| `GET` | `/api/users/:id` | Get user by ID |
| `POST` | `/api/users/register` | Register new user |
| `POST` | `/api/users/login` | User login |
| `PUT` | `/api/users/:id` | Update user |
| `DELETE` | `/api/users/:id` | Delete user |

## 🧪 Testing

### Backend Tests
```bash
npm test
```

### Frontend Unit Tests
```bash
cd public
ng test
```

### Frontend E2E Tests
```bash
cd public
ng e2e
```

## 🚢 Deployment

### Heroku Deployment

1. **Create Heroku app**
   ```bash
   heroku create amtica-ecommerce
   ```

2. **Set environment variables**
   ```bash
   heroku config:set NODE_ENV=production
   heroku config:set MONGODB_URI=<your-mongodb-uri>
   ```

3. **Deploy**
   ```bash
   git push heroku master
   ```

## 📊 Language Distribution

| Language | Percentage |
|----------|------------|
| TypeScript | 54.3% |
| HTML | 30.1% |
| JavaScript | 10.7% |
| SCSS | 4.9% |

## 🗃️ Data Models

### User Schema
```javascript
{
  fullName: String,
  email: String (unique),
  password: String (hashed),
  role: String (root/seller/member),
  profilePicture: String,
  contactInfo: Object,
  createdAt: Date,
  updatedAt: Date
}
```

### Product Schema
```javascript
{
  name: String,
  description: String,
  price: Number,
  category: ObjectId (ref: Category),
  features: Array,
  images: Array,
  seller: ObjectId (ref: User),
  createdAt: Date,
  updatedAt: Date
}
```

### Category Schema
```javascript
{
  name: String,
  description: String,
  parent: ObjectId (ref: Category),
  subcategories: Array,
  createdAt: Date,
  updatedAt: Date
}
```

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

## 📄 License

This project is licensed under the **ISC License**.

## 👤 Author

**Shubham Singh** - [@shubhamcommits](https://github.com/shubhamcommits)

---

<p align="center">
  Built with ❤️ for Amtica Ltd using the MEAN Stack
</p>

