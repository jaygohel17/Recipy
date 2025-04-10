# Recipy
A flutter build Recipe-App
# Recipy - Recipe App

## Overview
Recipy is a Flutter-based mobile application that allows users to discover, save, and share recipes. The app provides a modern and intuitive interface for browsing recipes, managing favorites, and customizing user preferences.

## Features

### 1. Authentication
- Email and password-based authentication
- User registration and login
- Secure session management
- Profile customization with username

 ![Image](https://github.com/user-attachments/assets/8ddf7f1d-5c8c-4e2f-a513-7f34d019a861) 
 ![Image](https://github.com/user-attachments/assets/c0d38ab8-5125-4def-9bd5-c606b8bf7f0f)
 ![Image](https://github.com/user-attachments/assets/38e192b1-7d5d-46fc-bb7a-9f4181131b6e)

### 2. Recipe Management
- Browse recipes with detailed information
- Search functionality
- Category-based filtering
- Recipe details including:
  - Cooking time
  - Servings
  - Ingredients list
  - Step-by-step instructions
  - Cuisine types
  - Dietary information
 
    ![Image](https://github.com/user-attachments/assets/1e9de3b3-2018-4317-8635-f46509415c46)
    ![Image](https://github.com/user-attachments/assets/e4fab1e1-1378-48d7-a129-83d0f65fa73f)
    ![Image](https://github.com/user-attachments/assets/bc3a18f8-e465-4078-a07e-fd083cd5728e)
    
### 3. Favorites
- Save favorite recipes
- Real-time synchronization with Firebase
- Swipe-to-delete functionality
- Pull-to-refresh for updates

  ![Image](https://github.com/user-attachments/assets/97d2bd74-41a2-457e-8220-6c52a3c9b131)

### 4. Sharing
- Share recipes via social media or messaging apps
- Formatted recipe information including:
  - Title
  - Cooking time
  - Servings
  - Description

    ![Image](https://github.com/user-attachments/assets/2fb0e2a8-33df-4f31-aa44-db501795c26d)
    ![Image](https://github.com/user-attachments/assets/5e65cefc-6b95-415e-a522-3b0503b683ff)

### 5. User Profile
- Username management
- Theme customization (Light/Dark/System)
- Account settings
- Help & Support section
  
  ![Image](https://github.com/user-attachments/assets/20fb43c1-a2f6-4a82-8ff1-3b319896cb58)   ![Image](https://github.com/user-attachments/assets/f4520411-1971-431e-b9bc-ac24009e2c00)
 
  ![Image](https://github.com/user-attachments/assets/06f04401-009a-4df9-95ad-4f23a41f1a3d)   ![Image](https://github.com/user-attachments/assets/0b7e5dcf-e93d-474d-9c6b-b29743b107ac)

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
