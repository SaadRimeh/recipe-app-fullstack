# 🍳 Recipe App - React Native

A modern, full-stack recipe application built with React Native (Expo) and Node.js, featuring user authentication, recipe search, favorites management, and a beautiful mobile-first interface.

## 📱 Features

### Core Functionality
- **Recipe Discovery**: Browse recipes by categories with beautiful cards and featured recipes
- **Advanced Search**: Search recipes by name or ingredients with debounced search
- **Favorites System**: Save and manage your favorite recipes with persistent storage
- **User Authentication**: Secure authentication using Clerk
- **Recipe Details**: View comprehensive recipe information including ingredients and instructions

### Technical Features
- **Cross-platform**: iOS, Android, and Web support
- **Real-time Updates**: Pull-to-refresh functionality
- **Responsive Design**: Optimized for various screen sizes
- **Offline Capable**: Cached data and graceful error handling
- **Modern UI/UX**: Smooth animations and intuitive navigation

## 🏗️ Architecture

### Frontend (Mobile App)
- **Framework**: React Native with Expo SDK 53
- **Navigation**: Expo Router with file-based routing
- **State Management**: React Hooks and Context
- **UI Components**: Custom components with consistent styling
- **Authentication**: Clerk for secure user management
- **API Integration**: TheMealDB for recipe data

### Backend (Node.js Server)
- **Runtime**: Node.js with Express.js
- **Database**: PostgreSQL with Drizzle ORM
- **Authentication**: Clerk integration
- **API**: RESTful endpoints for favorites management
- **Deployment**: Production-ready with environment configuration

## 🚀 Getting Started

### Prerequisites
- Node.js (v18 or higher)
- npm or yarn
- Expo CLI (`npm install -g @expo/cli`)
- iOS Simulator (for iOS development) or Android Studio (for Android development)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd react-native-recipe-app-yt
   ```

2. **Install backend dependencies**
   ```bash
   cd backend
   npm install
   ```

3. **Install mobile app dependencies**
   ```bash
   cd ../mobile
   npm install
   ```

4. **Environment Setup**

   Create `.env` files in both backend and mobile directories:

   **Backend (.env)**
   ```env
   DATABASE_URL=your_postgresql_connection_string
   NODE_ENV=development
   PORT=5001
   ```

   **Mobile (.env)**
   ```env
   EXPO_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
   ```

5. **Database Setup**
   ```bash
   cd backend
   npm run db:generate
   npm run db:migrate
   ```

### Running the Application

1. **Start the backend server**
   ```bash
   cd backend
   npm run dev
   ```

2. **Start the mobile app**
   ```bash
   cd mobile
   npm start
   ```

3. **Run on your preferred platform**
   - Press `i` for iOS Simulator
   - Press `a` for Android Emulator
   - Press `w` for Web browser

## 📁 Project Structure

```
react-native-recipe-app-yt/
├── backend/                 # Node.js backend server
│   ├── src/
│   │   ├── config/         # Configuration files
│   │   ├── db/            # Database schema and migrations
│   │   └── server.js      # Express server
│   ├── package.json
│   └── drizzle.config.js
├── mobile/                 # React Native mobile app
│   ├── app/               # Expo Router pages
│   │   ├── (auth)/        # Authentication screens
│   │   ├── (tabs)/        # Main app tabs
│   │   └── recipe/        # Recipe detail pages
│   ├── components/        # Reusable UI components
│   ├── services/          # API services
│   ├── constants/         # App constants
│   ├── hooks/            # Custom React hooks
│   ├── assets/           # Images, fonts, styles
│   └── package.json
└── README.md
```

## 🔧 Configuration

### API Configuration
Update the API URL in `mobile/constants/api.js` to match your backend server:
```javascript
export const API_URL = "http://your-ip-address:5001/api";
```

### Database Configuration
Configure your PostgreSQL database connection in `backend/src/config/db.js`.

## 📱 App Screenshots

The app includes several key screens:
- **Home**: Featured recipes and category browsing
- **Search**: Advanced recipe search functionality
- **Favorites**: User's saved recipes
- **Recipe Details**: Comprehensive recipe information
- **Authentication**: Sign in/sign up flows

## 🛠️ Technologies Used

### Frontend
- **React Native**: 0.79.3
- **Expo**: SDK 53
- **Expo Router**: File-based navigation
- **Clerk**: Authentication
- **React Navigation**: Navigation components
- **Expo Vector Icons**: Icon library

### Backend
- **Node.js**: Runtime environment
- **Express.js**: Web framework
- **Drizzle ORM**: Database ORM
- **PostgreSQL**: Database
- **CORS**: Cross-origin resource sharing

### External APIs
- **TheMealDB**: Recipe data source

## 🔌 API Endpoints

### Backend API
- `GET /api/health` - Health check
- `POST /api/favorites` - Add recipe to favorites
- `GET /api/favorites/:userId` - Get user's favorites
- `DELETE /api/favorites/:userId/:recipeId` - Remove recipe from favorites

### External API (TheMealDB)
- Recipe search by name
- Recipe lookup by ID
- Random recipe generation
- Category filtering
- Ingredient filtering

## 🎨 UI/UX Features

- **Modern Design**: Clean, intuitive interface
- **Smooth Animations**: Expo Reanimated for fluid transitions
- **Responsive Layout**: Adapts to different screen sizes
- **Loading States**: Comprehensive loading indicators
- **Error Handling**: Graceful error states and user feedback
- **Pull-to-Refresh**: Real-time data updates

## 🔒 Security

- **Authentication**: Secure user authentication with Clerk
- **Data Validation**: Input validation on both frontend and backend
- **Environment Variables**: Secure configuration management
- **CORS**: Proper cross-origin resource sharing configuration

## 🚀 Deployment

### Backend Deployment
1. Set up a PostgreSQL database
2. Configure environment variables
3. Deploy to your preferred hosting service (Heroku, Vercel, etc.)

### Mobile App Deployment
1. Build the app using Expo EAS Build
2. Submit to App Store and Google Play Store
3. Configure production environment variables

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request



## 🙏 Acknowledgments

- **TheMealDB**: For providing the recipe data API
- **Expo**: For the excellent React Native development platform
- **Clerk**: For secure authentication services
- **Drizzle**: For the modern database ORM

## 📞 Support

For support and questions:
- Create an issue in the repository
- Check the documentation
- Review the code comments for implementation details

---

**Built with ❤️ using React Native and Node.js** 