# React Native MVVM Todo & Photo App

A React Native mobile application built with **MVVM architecture**, **IDesign methodology**, and **SOLID principles** that provides offline-first functionality for managing personal information, todo items, and photo collections.

## 🚀 Features

- **Dashboard Navigation** - Central hub with color-coded tiles showing completion status
- **Personal Information Form** - User profile management with reusable validation framework
- **Todo Management** - Full CRUD operations with offline storage and status tracking
- **Photo Gallery** - Camera integration with local photo storage and gallery display
- **Offline-First** - All operations work without internet connectivity using TypeORM + SQLite
- **Status Tracking** - Real-time dashboard updates based on page completion status

## 🏗️ Architecture

### MVVM + IDesign + SOLID
- **MVVM Pattern**: Clear separation of Models, Views, and ViewModels
- **IDesign Methodology**: Services, Data Access, Infrastructure, Presentation, and Contracts layers
- **SOLID Principles**: Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion
- **Design Patterns**: Repository, Command, Strategy, Observer, Factory, Adapter, Decorator

### Tech Stack
- **React Native** 0.80.1+ with TypeScript
- **TypeORM** with SQLite for offline data persistence
- **React Navigation** 6+ for routing
- **Jest** + React Native Testing Library for testing
- **Dependency Injection** for service management

## 📱 App Structure

```
src/
├── models/          # TypeORM entities and data contracts
├── views/           # React Native screens (Presentation Layer)
├── viewmodels/      # Business logic and orchestration (Services Layer)
├── repositories/    # Data access abstraction (Data Access Layer)
├── services/        # Business services and external integrations
├── infrastructure/  # Cross-cutting concerns (logging, validation, etc.)
├── contracts/       # Interface definitions and data contracts
└── utils/           # Shared utilities and helpers
```

## 🛠️ Getting Started

### Prerequisites
- Node.js >= 18
- React Native development environment
- iOS Simulator (for iOS) or Android Emulator (for Android)

### Installation

```bash
# Install dependencies
npm install

# iOS (requires macOS)
cd ios && pod install && cd ..
npm run ios

# Android
npm run android

# Start Metro bundler
npm start
```

## 🧪 Testing

### Run All Tests
```bash
npm test
```

### Run Tests with Coverage
```bash
npm run test:coverage
```

### Run Specific Test Files
```bash
npm test -- --testPathPattern=UserInfo
```

### Testing Strategy
- **Unit Tests**: Individual components, services, and utilities
- **Integration Tests**: Service interactions and data flow
- **E2E Tests**: Complete user workflows
- **Dependency Injection**: All tests use mocked services for isolation

## 🏛️ Development Methodology

### IDesign Layers
1. **Services Layer**: Business logic with clear contracts
2. **Data Access Layer**: Repository pattern with abstraction
3. **Infrastructure Layer**: Cross-cutting concerns
4. **Presentation Layer**: UI components with minimal logic
5. **Contracts Layer**: Interface definitions

### SOLID Principles
- **SRP**: Each class has one responsibility
- **OCP**: Open for extension, closed for modification
- **LSP**: Derived classes can substitute base classes
- **ISP**: Clients depend only on interfaces they use
- **DIP**: High-level modules don't depend on low-level modules

### Key Design Patterns
- **Repository Pattern**: Data access abstraction
- **Command Pattern**: Operations and queue management
- **Strategy Pattern**: Validation and business rules
- **Observer Pattern**: State management
- **Factory Pattern**: Object creation
- **Adapter Pattern**: External integrations

## 📊 Data Models

```typescript
// Core entities with TypeORM
interface UserInfo { /* Personal information */ }
interface Todo { /* Todo items with priority and status */ }
interface Photo { /* Photo metadata and storage */ }
interface PageStatus { /* Dashboard completion tracking */ }
```

## 🔄 Development Workflow

1. **Foundation** (Phase 1): IDesign setup, SOLID principles, DI container
2. **Personal Info** (Phase 2): Form validation, status tracking
3. **Todo Management** (Phase 3): CRUD operations, business rules
4. **Photo Gallery** (Phase 4): Camera integration, file management
5. **Optimization** (Phase 5): Performance, error handling
6. **API Prep** (Phase 6): Future synchronization capabilities

## 🚧 Future Enhancements

- Web API integration for data synchronization
- Cloud photo storage
- Advanced filtering and search
- Push notifications
- Multi-user support

## 📝 Contributing

1. Follow SOLID principles and IDesign methodology
2. Write comprehensive tests for all new features
3. Use dependency injection for service management
4. Maintain clear separation of concerns
5. Document interfaces and contracts

## 📄 License

This project is private and proprietary.
