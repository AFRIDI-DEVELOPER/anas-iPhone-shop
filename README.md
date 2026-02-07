# ANAS iPhone Shop

A professional, full-stack iPhone e-commerce application with OTP authentication, built with React and Node.js.

## 🚀 Features

- **Apple-Grade Design**: Premium UI with Inter/Poppins fonts and glassmorphism effects
- **OTP Authentication**: Secure phone-based login with 5-minute OTP expiry
- **Shopping Cart**: Full cart functionality with localStorage persistence
- **Product Filtering**: Search and filter by model, storage, and condition
- **Responsive Design**: Beautiful on all devices (mobile, tablet, desktop)
- **Protected Routes**: Cart requires authentication
- **Mock Data**: Ready-to-use product catalog with images

## 📁 Project Structure

```
ANAS IPHONE-SHOP/
├── iphone-store/          # React Frontend
│   ├── src/
│   │   ├── components/    # Reusable components
│   │   ├── pages/         # Page components
│   │   ├── context/       # React Context providers
│   │   ├── services/      # API services
│   │   ├── styles/        # Global styles
│   │   └── utils/         # Utility functions
│   └── package.json
│
└── server/                # Node.js Backend
    ├── controllers/       # API controllers
    ├── models/            # MongoDB models
    ├── routes/            # API routes
    ├── utils/             # Utility functions
    ├── index.js           # Server entry point
    └── package.json
```

## 🛠️ Technologies

### Frontend
- React 18
- React Router DOM
- Axios
- Vite
- CSS3 (Glassmorphism, Animations)

### Backend
- Node.js
- Express.js
- MongoDB (Mongoose)
- dotenv
- CORS

## 📦 Installation

### Prerequisites
- Node.js (v16 or higher)
- MongoDB (local or Atlas)
- npm or yarn

### 1. Clone & Install

```bash
# Install frontend dependencies
cd iphone-store
npm install

# Install backend dependencies
cd ../server
npm install
```

### 2. Configure MongoDB

**Option A: Local MongoDB**
```bash
# Make sure MongoDB is running
brew services start mongodb-community
```

**Option B: MongoDB Atlas (Cloud)**
1. Create a free cluster at [mongodb.com/cloud/atlas](https://www.mongodb.com/cloud/atlas)
2. Get your connection string
3. Update `server/.env`:
```env
MONGODB_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/anas-iphone-shop
```

### 3. Environment Variables

The `server/.env` file is already configured for local development:
```env
NODE_ENV=development
PORT=5000
MONGODB_URI=mongodb://localhost:27017/anas-iphone-shop
```

## 🚀 Running the Application

### Start Backend Server
```bash
cd server
npm run dev
```
Server runs on: `http://localhost:5000`

### Start Frontend
```bash
cd iphone-store
npm run dev
```
Frontend runs on: `http://localhost:5173`

## 🧪 Testing the App

### 1. **OTP Authentication Flow**
1. Go to `http://localhost:5173`
2. Click "Login" in the navbar
3. Enter a phone number (e.g., `9876543210`)
4. Click "Send OTP"
5. Check the **server console** for the OTP (it will be displayed like `OTP for +919876543210: 123456`)
6. Enter the OTP in the frontend
7. You're logged in! ✅

### 2. **Shopping Flow**
1. Browse products on Home page or Shop page
2. Use filters to narrow down products
3. Click "Add to Cart" on any product
4. Go to Cart (requires login)
5. Adjust quantities or remove items
6. See total price update automatically

### 3. **Features to Test**
- ✅ Navbar cart badge updates
- ✅ Protected cart route (redirects to login if not authenticated)
- ✅ Cart persists on page refresh (localStorage)
- ✅ Filters update products in real-time
- ✅ Responsive design on mobile/tablet
- ✅ Smooth animations and hover effects

## 📱 OTP Development Mode

Currently, OTP is logged to the server console for development. The OTP is also included in the API response during development:

```json
{
  "message": "OTP sent successfully",
  "devOTP": "123456"
}
```

**For Production**: Integrate with SMS services like:
- Twilio
- Firebase Authentication
- AWS SNS

## 🎨 Design Features

- **Fonts**: Inter (primary), Poppins (headings)
- **Color Scheme**: Dark mode with blue accents
- **Effects**: Glassmorphism, gradients, smooth animations
- **Icons**: Custom SVG icons
- **Images**: High-quality iPhone product images from Unsplash

## 🔐 Security Notes

- OTP expires after 5 minutes
- OTP is cleared from database after verification
- Protected routes require authentication
- CORS configured for frontend-backend communication

## 📝 API Endpoints

### Authentication
- `POST /api/auth/send-otp` - Send OTP to phone
- `POST /api/auth/verify-otp` - Verify OTP and login

### Health Check
- `GET /api/health` - Server status

## 🚧 Future Enhancements

- [ ] Add Twilio/Firebase SMS integration
- [ ] Implement JWT tokens for auth
- [ ] Add real product database
- [ ] Payment gateway integration
- [ ] Order management system
- [ ] Admin dashboard
- [ ] Product reviews and ratings
- [ ] Wishlist functionality

## 🤝 Contributing

This is a demonstration project. Feel free to fork and customize!

## 📄 License

MIT License - feel free to use this project for learning and development.

---

**Built with ❤️ using React & Node.js**

For questions or issues, check the console logs in both frontend and backend terminals.
# anas-iPhone-shop
# anas-iPhone-store
