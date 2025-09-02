# 📚 BookNook

> Social Platform for Readers built with React and Node.js

BookNook is a full-stack web application that provides users with a comprehensive digital bookstore experience. Users can browse books, manage their reading progress, maintain wishlists, and discover new authors in an intuitive, responsive interface.

## ✨ Features

### 📖 Core Functionality
- **Book Browsing**: Browse books with multiple sorting options (Popular, Latest, Top Rated)
- **User Authentication**: Secure Firebase-based authentication system
- **Personal Library**: Track reading progress and manage personal book collections
- **Wishlist Management**: Add/remove books from personal wishlist
- **Book Discovery**: Explore recommended authors and trending books
- **Book Details**: Comprehensive book information including ratings, descriptions, and metadata
- **Add Books**: Users can contribute by adding new books to the platform

### 🎨 User Experience
- **Responsive Design**: Modern UI built with Tailwind CSS
- **Dark/Light Mode**: Toggle between day and night themes
- **Sidebar Navigation**: Collapsible sidebar for easy navigation
- **Progress Tracking**: Visual progress bars for ongoing reads
- **Rating System**: Community-driven book ratings and reviews
- **Search & Filter**: Multiple ways to discover content

## 🛠️ Tech Stack

### Frontend
- **React 18.3.1** - Modern React with hooks
- **React Router DOM** - Client-side routing
- **Redux** - State management
- **Tailwind CSS 4.0.3** - Utility-first CSS framework
- **SweetAlert2** - Beautiful alert dialogs
- **Vite** - Fast build tool and development server

### Backend
- **Node.js** - Runtime environment
- **Express.js 4.21.2** - Web application framework
- **Firebase Admin SDK** - Database and authentication
- **Firebase Firestore** - NoSQL document database
- **Multer** - File upload handling
- **CORS** - Cross-origin resource sharing

### Database Collections
- **Users** - User profiles and preferences
- **Resources** - Book metadata and content
- **Feedback** - User reviews and ratings
- **Admin** - Administrative data

## 📁 Project Structure

```
bookNook/
├── Backend/
│   ├── controllers/          # Request handlers
│   │   ├── authController.js
│   │   ├── userController.js
│   │   ├── resourceController.js
│   │   └── feedbackController.js
│   ├── models/              # Data models and Firebase operations
│   │   ├── authModel.js
│   │   ├── userModel.js
│   │   ├── resourceModel.js
│   │   └── feedbackModel.js
│   ├── routes/              # API route definitions
│   │   ├── authRouter.js
│   │   ├── userRouter.js
│   │   ├── resourceRouter.js
│   │   └── feedbackRouter.js
│   ├── firebaseAdminConfig.js # Firebase configuration
│   ├── server.js            # Express server setup
│   └── package.json
├── frontend/
│   ├── src/
│   │   ├── components/      # Reusable UI components
│   │   │   ├── Navbar.jsx
│   │   │   ├── Sidebar.jsx
│   │   │   ├── BookList.jsx
│   │   │   ├── BookItem.jsx
│   │   │   └── AddBook.jsx
│   │   ├── pages/           # Main application pages
│   │   │   ├── homePage.jsx
│   │   │   ├── LoginPage.jsx
│   │   │   ├── SignupPage.jsx
│   │   │   ├── BookPage.jsx
│   │   │   ├── Addbook.jsx
│   │   │   └── ProfilePage.jsx
│   │   ├── redux/           # State management
│   │   ├── middleware/      # Authentication middleware
│   │   ├── assets/          # Static assets
│   │   └── App.jsx          # Main application component
│   ├── firebaseConfig.js    # Firebase client configuration
│   ├── vite.config.js
│   └── package.json
└── README.md
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v16 or higher)
- npm or yarn
- Firebase project with Firestore enabled
- Firebase service account credentials

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/07Sarthak/bookNook.git
   cd bookNook
   ```

2. **Backend Setup**
   ```bash
   cd Backend
   npm install
   ```

3. **Frontend Setup**
   ```bash
   cd ../frontend
   npm install
   ```

4. **Firebase Configuration**
   - Create a Firebase project at [Firebase Console](https://console.firebase.google.com/)
   - Enable Firestore Database
   - Generate service account credentials
   - Add `credentials.json` to the `Backend/` directory
   - Update `frontend/firebaseConfig.js` with your Firebase config

5. **Environment Variables**
   ```bash
   # Create .env file in frontend directory
   cd frontend
   touch .env
   ```

### Running the Application

1. **Start Backend Server**
   ```bash
   cd Backend
   npm start
   # or for development
   npm run dev
   ```
   Server will run on `http://localhost:4000`

2. **Start Frontend Development Server**
   ```bash
   cd frontend
   npm run dev
   ```
   Application will be available at `http://localhost:5173`

## 📚 API Endpoints

### Authentication
- `POST /auth/signup` - User registration
- `POST /auth/login` - User login with Firebase ID token

### Users
- `GET /users/get/:id` - Get user profile
- `PUT /users/update/:id` - Update user profile

### Resources (Books)
- `GET /resources/all` - Get all books
- `GET /resources/get/:id` - Get book by ID
- `POST /resources/add` - Add new book
- `PUT /resources/update/:id` - Update book information
- `PUT /resources/updateRating` - Update book rating
- `DELETE /resources/delete/:id` - Delete book

### Feedback
- `POST /feedback/add` - Add book review/feedback
- `GET /feedback/get/:bookId` - Get reviews for a book

## 🔧 Key Features Implementation

### Authentication Flow
- Firebase Authentication integration
- JWT token-based session management
- Protected routes with middleware validation
- Automatic redirection for unauthenticated users

### Book Management
- CRUD operations for book resources
- File upload support for PDFs and cover images
- Dynamic rating system with user aggregation
- Progress tracking for individual users

### User Experience
- Responsive grid layouts for book display
- Pagination for large datasets
- Real-time wishlist updates
- Visual progress indicators
- Theme switching capabilities

## 🔐 Security Features

- Firebase Admin SDK for secure backend operations
- Token verification middleware
- CORS configuration for cross-origin requests
- Input validation and sanitization
- Secure file upload handling

## 🎯 Future Enhancements

Based on the current codebase, potential improvements include:

- Search functionality implementation
- Advanced filtering and sorting options
- Social features (friend connections, shared reading lists)
- Book recommendation engine
- Mobile application development
- Payment integration for premium features
- Advanced analytics and reporting

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the ISC License.

## 👨‍💻 Author

**KunalNath04** - [GitHub Profile](https://github.com/KunalNath04)

## 🙏 Acknowledgments

- Firebase for authentication and database services
- React community for excellent documentation
- Tailwind CSS for the utility-first approach
- All contributors who help improve this project

---

**Note**: This project is currently in active development. Some features mentioned in the TODO.txt file are still being implemented.
