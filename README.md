# Recipy
A flutter build Recipe-App
# Recipy - Recipe Management App

## Overview
Recipy is a Flutter-based mobile application that allows users to discover, save, and share recipes. The app provides a modern and intuitive interface for browsing recipes, managing favorites, and customizing user preferences.

## Features

### 1. Authentication
- Email and password-based authentication
- User registration and login
- Secure session management
- Profile customization with username
  

### 2. Recipe Management
- Browse recipes with detailed information
- Search functionality
- Category-based filtering
- Recipe details including:
  - Cooking time
  - Servings
  - Health score
  - Ingredients list
  - Step-by-step instructions
  - Cuisine types
  - Dietary information

### 3. Favorites
- Save favorite recipes
- Real-time synchronization with Firebase
- Swipe-to-delete functionality
- Pull-to-refresh for updates

### 4. Sharing
- Share recipes via social media or messaging apps
- Formatted recipe information including:
  - Title
  - Cooking time
  - Servings
  - Health score
  - Description
  - Cuisines

### 5. User Profile
- Username management
- Theme customization (Light/Dark/System)
- Account settings
- Help & Support section

## Technical Stack

### Frontend
- **Framework**: Flutter
- **Language**: Dart
- **UI Components**:
  - Material Design
  - Custom widgets
  - Responsive layouts
  - Theme support

### Backend
- **Authentication**: Firebase Auth
- **Database**: Firebase Firestore
- **API Integration**: Spoonacular Recipe API

### Dependencies
```yaml
dependencies:
  flutter:
    sdk: flutter
  firebase_core: ^latest
  firebase_auth: ^latest
  cloud_firestore: ^latest
  provider: ^latest
  http: ^latest
  google_fonts: ^latest
  share_plus: ^latest
```



```


## API Integration

### Spoonacular API
- Endpoint: `https://api.spoonacular.com/recipes/complexSearch`
- Parameters:
  - `apiKey`: Your API key
  - `number`: Number of recipes to return
  - `addRecipeInformation`: Include detailed recipe information
  - `instructionsRequired`: Include cooking instructions
  - `fillIngredients`: Include ingredient details
  - `imageType`: Specify image type

## Firebase Integration

### Authentication
- Email/password authentication
- User session management
- Secure data access

### Firestore Collections
1. **users**
   - Document ID: User UID
   - Fields:
     - username
     - email
     - createdAt
     - updatedAt

2. **favorites** (subcollection of users)
   - Document ID: Auto-generated
   - Fields:
     - recipe data
     - addedAt

## State Management

### Provider Pattern
- RecipeProvider: Manages recipe data and API calls
- ThemeProvider: Manages app theme
- UserProvider: Manages user data and authentication

## UI Components

### 1. Recipe Card
- Image display
- Title and description
- Cooking time
- Servings
- Health score
- Favorite button
- Share button

### 2. Recipe Detail Screen
- Full-size image
- Detailed information
- Ingredients list
- Step-by-step instructions
- Share functionality

### 3. Profile Screen
- User information
- Theme settings
- Account management
- Help & Support

## Error Handling

### 1. API Errors
- Network connectivity issues
- API rate limiting
- Invalid responses

### 2. Authentication Errors
- Invalid credentials
- Network issues
- Session expiration

### 3. Data Management Errors
- Failed updates
- Sync issues
- Invalid data

## Best Practices

### 1. Code Organization
- Separation of concerns
- Modular architecture
- Clean code principles

### 2. Performance
- Lazy loading
- Image optimization
- Efficient state management

### 3. Security
- Secure authentication
- Data validation
- Error handling

## Getting Started

1. **Prerequisites**
   - Flutter SDK
   - Firebase account
   - Spoonacular API key

2. **Setup**
   ```bash
   # Clone the repository
   git clone [repository-url]

   # Install dependencies
   flutter pub get

   # Run the app
   flutter run
   
3. **Configuration**
   - Add Firebase configuration
   - Set up Spoonacular API key
   - Configure theme settings

```

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Spoonacular API for recipe data
- Firebase for backend services
- Flutter team for the framework
