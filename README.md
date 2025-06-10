# Videoflix - Movie & TV Series Catalog

A React Native application that provides an interactive catalog for discovering movies and TV series. This project is derived from the [Expo Template Suite Senior](https://github.com/narradorww/expo-template-suite-senior) and was created to study and implement the following technical challenge.

## 📋 Technical Challenge: Interactive Movie & TV Series Catalog (React Native Senior)

### Objective:
Develop a React Native application that allows users to search for movies and TV series, view details, manage a favorites list, and demonstrates best practices in development, architecture, and performance.

### Context:
Imagine you're developing a new feature for a streaming app: an interactive catalog where users can discover and save their favorite movies and TV series.

## 🎯 Functional Requirements

### 🔍 Search Screen (SearchScreen):
- Text input field for users to enter search terms (movie/series title)
- Real-time search with debounce to avoid excessive API calls
- Display results in a scrollable list (FlatList) showing:
  - Movie/series poster (image)
  - Title
  - Release year
- Loading indicator (ActivityIndicator) during search
- Friendly message for no results or API errors
- Clickable items to view details

### 📱 Details Screen (DetailsScreen):
- Navigation from search results to detailed view
- Display comprehensive information:
  - Featured poster
  - Title
  - Release year
  - Synopsis/Overview
  - Rating (0-10 scale)
- Favorite button (heart icon) to add/remove from favorites
- Visual state indication for favorited items

### ❤️ Favorites Screen (FavoritesScreen):
- Display all user-favorited movies and TV series
- Local persistence using AsyncStorage
- Clickable items leading to DetailsScreen
- Remove favorites functionality from both screens

### 🧭 Navigation:
- Tab Navigation between SearchScreen and FavoritesScreen
- Stack navigation to DetailsScreen from both tabs
- Implemented using react-navigation

## 🛠 Technical Requirements

### Core Technologies:
- **Language**: React Native with TypeScript
- **State Management**: Context API / Redux Toolkit 
- **Styling**: Styled Components
- **Navigation**: React Navigation

### Testing:
- Unit and component tests for main functionalities
- Jest and React Native Testing Library
- Test execution documentation

### Code Quality:
- Clean, organized, readable, and maintainable code
- SOLID principles where applicable
- Clear and reusable componentization

### Performance:
- Optimized long list rendering (FlatList with keyExtractor, memoization)
- Efficient API call management (avoid unnecessary calls, handle loading/error states)

### Documentation:
- Detailed setup and run instructions
- Architecture and library choice explanations
- Estimated development time
- Test execution guide
- Important development decisions

## 🌐 API Integration

**Primary API**: [The Movie Database (TMDB)](https://developer.themoviedb.org/docs/getting-started)
- Search endpoint: `https://api.themoviedb.org/3/search/multi`
- Movie details: `https://api.themoviedb.org/3/movie/{movie_id}`
- TV details: `https://api.themoviedb.org/3/tv/{tv_id}`

**Alternative**: Mock data with consistent structure in `mockData.json`

## 📊 Evaluation Criteria

- **Functionality**: Meets all functional requirements
- **Code Quality**: Clarity, organization, maintainability, TypeScript usage
- **Architecture**: Component design, project structure, state management
- **Testing**: Coverage, quality, and relevance of tests
- **Performance**: Efficient rendering, async handling, visual feedback
- **Documentation**: Clear and complete README
- **React Native Best Practices**: Proper use of components, hooks, ecosystem patterns
- **Attention to Detail**: Edge case handling, smooth UX

## 🚀 Quick Start

### Prerequisites
- Node.js (>= 16)
- npm or yarn
- Expo CLI
- Android Studio / Xcode for device testing

### Installation

```bash
# Clone the repository
git clone <repository-url>
cd videoflix

# Install dependencies
npm install

# Set up API key (create .env file)
echo "TMDB_API_KEY=your_api_key_here" > .env

# Start the development server
npm start
```

### Running the App

```bash
# Start Expo development server
npm start

# Run on Android
npm run android

# Run on iOS
npm run ios

# Run on web
npm run web
```

### Testing

```bash
# Run all tests
npm test

# Run tests in watch mode
npm run test:watch

# Generate coverage report
npm test -- --coverage
```

## 📁 Project Structure

```
src/
├── components/          # Reusable UI components
├── screens/            # Screen components (Search, Details, Favorites)
├── navigation/         # Navigation configuration
├── context/           # State management (Theme, App context)
├── services/          # API services and data management
├── hooks/             # Custom hooks
├── theme/             # Design system (colors, typography, spacing)
├── utils/             # Utilities and helpers
└── types/             # TypeScript type definitions
```

## 🎨 Design System

This project leverages a complete design system inherited from Expo Template Suite Senior:
- **Theme System** with light/dark mode support
- **Styled Components** with consistent styling
- **Typography Scale** for text hierarchy
- **Color Palette** with semantic tokens
- **Spacing System** for consistent layouts

## 🧪 Testing Strategy

- **Unit Tests**: Individual component and function testing
- **Integration Tests**: Screen flow and user interaction testing
- **Component Tests**: UI component behavior and styling
- **API Tests**: Service layer and data handling

## 📈 Performance Optimizations

- **FlatList Optimization**: Proper keyExtractor and item layout
- **Image Caching**: Efficient poster loading and caching
- **Search Debouncing**: Reduced API calls during typing
- **Memoization**: React.memo for expensive components
- **State Management**: Efficient data flow and updates

## 🔄 State Management Choice

[To be documented based on implementation choice]

## ⏱️ Development Time Estimation

[To be documented during development]

## 📝 Development Notes

[Key decisions and observations during development]

## 🌟 Bonus Features Considered

- Search result pagination
- API response caching strategies
- Accessibility implementation
- Architecture scalability for larger teams
- React Native New Architecture considerations (Fabric/TurboModules)

## 🤝 Contributing

This is a study project, but contributions and suggestions are welcome:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests for new features
5. Submit a pull request

## 📄 License

This project is licensed under the GPL-3.0-only License. See the [LICENSE](LICENSE) file for details.

---

**Note**: This project is based on [Expo Template Suite Senior](https://github.com/narradorww/expo-template-suite-senior) and serves as a practical implementation of advanced React Native development concepts and best practices.