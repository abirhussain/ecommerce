# E-commerce Application Architecture (Django + React + MySQL)

## Project Structure
```
ecommerce/
├── backend/                  # Django backend
│   ├── ecommerce_backend/    # Django project settings
│   ├── accounts/             # User authentication app
│   ├── products/             # Products management app
│   ├── cart/                 # Shopping cart app
│   ├── orders/               # Order processing app
│   └── requirements.txt      # Python dependencies
│
└── frontend/                 # React frontend
    ├── public/               # Static assets
    ├── src/
    │   ├── components/       # Reusable UI components
    │   ├── pages/            # Page components
    │   ├── services/         # API services
    │   ├── context/          # Context API (auth, cart)
    │   ├── utils/            # Helper functions
    │   └── App.js            # Main app component
    ├── package.json          # JavaScript dependencies
    └── README.md             # Frontend documentation
```

## Features Breakdown

### 1. Authentication System
- JWT Authentication with access & refresh tokens
- User registration and login
- Password reset functionality
- Token refresh mechanism
- Protected routes

### 2. Product Management
- Product listing with pagination
- Product search & filtering
- Product categories
- Product details page
- Product images

### 3. Shopping Cart
- Add/remove products
- Update quantities
- Cart persistence (local storage + database)
- Price calculations

### 4. User Experience
- Responsive design
- Loading states
- Error handling
- Toast notifications

### 5. Database Design (MySQL)
- Users table (using Django's built-in user model)
- Products table
- Categories table
- Cart items table
- Orders table
- Order items table

## API Endpoints

### Authentication
- `POST /api/auth/register/` - Register new user
- `POST /api/auth/login/` - Login user
- `POST /api/auth/refresh/` - Refresh JWT token
- `POST /api/auth/logout/` - Logout user

### Products
- `GET /api/products/` - List products (with filtering)
- `GET /api/products/<id>/` - Get single product
- `GET /api/products/categories/` - List categories

### Cart
- `GET /api/cart/` - Get user's cart
- `POST /api/cart/` - Add item to cart
- `PUT /api/cart/<id>/` - Update cart item
- `DELETE /api/cart/<id>/` - Remove item from cart

### Orders
- `POST /api/orders/` - Create order
- `GET /api/orders/` - List user's orders
- `GET /api/orders/<id>/` - Get order details