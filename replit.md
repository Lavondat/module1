# UzNavi - Uzbekistan Travel Companion

## Overview

UzNavi is a comprehensive travel companion application designed specifically for tourists and travelers visiting Uzbekistan. The application features voice-controlled AI assistance, rotating global landmark backgrounds, multi-language support (Uzbek, English, Russian), and an integrated payment system supporting both local Uzbek payment methods (UzCard, Payme, Click) and international cards (MasterCard, Visa).

**Key Features Implemented:**
- **48-hour Free Trial**: All users get 48 hours of free access after registration
- **Voice-Only AI Assistant**: Speech recognition and voice responses for hands-free interaction
- **Flexible Pricing**: 72h/$2.99, 168h/$5.99, 720h/$24.99 subscription plans
- **Local Payment Support**: UzCard, Payme, Click integration alongside international cards
- **Dynamic Backgrounds**: Rotating carousel of global landmarks and historical sites
- **Responsive Design**: Fully responsive with dark/light theme support

The application targets tourists, business travelers, and adventure seekers who need reliable navigation and local recommendations while exploring Uzbekistan's historic Silk Road cities and cultural heritage sites.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
The client-side is built using **React 18** with **TypeScript** for type safety and better developer experience. The application uses **Vite** as the build tool and development server, providing fast hot module replacement and optimized production builds.

**UI Framework**: Implements **shadcn/ui** component library built on top of **Radix UI primitives** and **Tailwind CSS** for consistent, accessible, and customizable user interface components. The design system supports both light and dark themes with CSS custom properties.

**State Management**: Utilizes **TanStack Query (React Query)** for server state management, providing efficient data fetching, caching, and synchronization between client and server.

**Routing**: Uses **Wouter** as a lightweight client-side routing solution for navigation between different application views.

**Animation**: Integrates **Framer Motion** for smooth animations and transitions, particularly for the image carousel and interactive elements.

### Backend Architecture
The server-side is built with **Express.js** running on **Node.js** with TypeScript support. The application follows a modular architecture with clear separation of concerns.

**API Design**: RESTful API structure with all endpoints prefixed under `/api` for clear separation from static file serving.

**Development Setup**: Uses **tsx** for TypeScript execution in development and **esbuild** for production bundling, ensuring fast build times and optimal performance.

**Static File Serving**: Configured to serve the built React application from the Express server, making it a single deployable unit.

### Data Storage Solutions
**Database**: Configured to use **PostgreSQL** as the primary database with **Neon Database** as the serverless PostgreSQL provider for cloud deployment.

**ORM**: Implements **Drizzle ORM** for type-safe database operations with automatic TypeScript schema generation. The ORM configuration supports migrations and schema validation.

**In-Memory Storage**: Includes a fallback in-memory storage implementation for development and testing scenarios.

### Authentication and Authorization
The application includes a basic user management system with username/password authentication. The schema supports user registration and login functionality, though the full authentication flow implementation is prepared for future development.

### External Dependencies
**UI Components**: Extensive use of Radix UI primitives for accessible, unstyled UI components that are then styled with Tailwind CSS.

**Database Connection**: Integration with Neon Database for serverless PostgreSQL hosting with connection pooling and automatic scaling.

**Maps and Location Services**: Prepared architecture for offline map functionality, though specific mapping providers are not yet integrated.

**Session Management**: Includes `connect-pg-simple` for PostgreSQL-based session storage, enabling persistent user sessions.

### Development and Build Tools
**Type Safety**: Comprehensive TypeScript configuration covering client, server, and shared code with strict type checking enabled.

**CSS Framework**: Tailwind CSS with custom design tokens and CSS variables for theming support.

**Development Experience**: Hot reloading, error overlay, and development-specific tooling for improved developer productivity.

**Build Process**: Separate build processes for client (Vite) and server (esbuild) with optimized production outputs.

## External Dependencies

### Core Framework Dependencies
- **React 18** with TypeScript support for the frontend application
- **Express.js** for the backend API server
- **Node.js** runtime environment

### Database and ORM
- **PostgreSQL** as the primary database system
- **Neon Database** (@neondatabase/serverless) for serverless PostgreSQL hosting
- **Drizzle ORM** for type-safe database operations and migrations
- **connect-pg-simple** for PostgreSQL-based session storage

### UI and Styling
- **Tailwind CSS** for utility-first CSS framework
- **shadcn/ui** component library configuration
- **Radix UI** primitives for accessible, unstyled components
- **Framer Motion** for animations and transitions
- **Lucide React** for consistent iconography

### Development Tools
- **Vite** for fast development server and optimized builds
- **tsx** for TypeScript execution in development
- **esbuild** for fast production builds
- **PostCSS** with Autoprefixer for CSS processing

### Data Fetching and State Management
- **TanStack Query (React Query)** for server state management
- **Wouter** for lightweight client-side routing

### Form Handling and Validation
- **React Hook Form** with resolver support
- **Zod** for schema validation
- **drizzle-zod** for database schema validation

### Utility Libraries
- **class-variance-authority** for component variant management
- **clsx** and **tailwind-merge** for conditional CSS classes
- **date-fns** for date manipulation and formatting
- **cmdk** for command palette functionality