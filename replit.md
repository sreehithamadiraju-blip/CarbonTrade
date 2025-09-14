# CarbonTrade Platform

## Overview

CarbonTrade is a web application that enables NGOs and individuals to track and trade tokenized carbon credits from blue carbon projects. The platform focuses on mangrove restoration, seagrass conservation, and other coastal ecosystem projects. Users can submit plantation projects for verification, earn C-BLUE tokens upon approval, and participate in carbon credit trading. The application includes comprehensive project management, educational resources about blue carbon ecosystems, and a trading marketplace for carbon credits.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

**Full-Stack Architecture**
The application follows a full-stack TypeScript architecture with a clear separation between client and server code. The client uses React with Vite for the frontend, while the server runs on Express.js with a custom storage layer. Shared schemas and types are maintained in a common directory to ensure type safety across the entire application.

**Frontend Framework**
Built with React 18 using Vite as the build tool and development server. The application uses wouter for client-side routing, providing a lightweight alternative to React Router. The UI leverages shadcn/ui components built on top of Radix UI primitives, ensuring accessible and consistent design patterns throughout the application.

**Styling and Design System**
Implements Tailwind CSS for utility-first styling with a custom design system configured for dark mode by default. The primary brand color is blue, reflecting the ocean-focused nature of blue carbon projects. CSS variables are used for theming, allowing for consistent color schemes and easy customization.

**State Management and Data Fetching**
Uses TanStack Query (React Query) for server state management, caching, and data synchronization. Form handling is managed through React Hook Form with Zod schema validation for type-safe form submissions. The application maintains client-side state for UI interactions while relying on the query layer for server data.

**Backend API Design**
Express.js server provides RESTful API endpoints with a modular route structure. The server includes middleware for request logging, error handling, and JSON parsing. A custom storage interface abstracts data operations, currently implemented as an in-memory store with mock data for prototyping.

**Database Schema and ORM**
Drizzle ORM is configured for PostgreSQL with a clear schema definition including users, projects, and transactions tables. The schema supports user authentication, project submission workflows, and carbon credit trading functionality. Database migrations are managed through Drizzle Kit.

**Authentication and User Management**
The application supports role-based access with individual and NGO/community user types. User profiles include wallet balances, carbon credit holdings, and project history. Mock authentication is implemented for development with predefined test users.

**Responsive Design Strategy**
Mobile-first responsive design with adaptive navigation patterns. Desktop users see a persistent sidebar navigation, while mobile users get a bottom navigation bar. The useIsMobile hook detects screen size and adjusts the UI accordingly.

**Chart and Data Visualization**
Recharts library provides interactive data visualizations including bar charts for regional carbon levels, trend analysis, and trading volume displays. Charts are responsive and themed to match the application's design system.

**File Upload and Media Handling**
Project submission includes file upload capabilities for photos and videos as evidence of plantation work. The UI provides clear guidelines for acceptable file formats and quality requirements.

## External Dependencies

**UI Component Library**
- Radix UI primitives for accessible component foundations
- shadcn/ui for pre-built component implementations
- Lucide React for consistent iconography
- class-variance-authority for component variant management

**Form and Validation**
- React Hook Form for performant form handling
- Zod for runtime type validation and schema definition
- @hookform/resolvers for Zod integration with React Hook Form

**Data Visualization**
- Recharts for interactive charts and graphs
- Date-fns for date manipulation and formatting

**Database and ORM**
- Drizzle ORM for type-safe database operations
- @neondatabase/serverless for PostgreSQL connectivity
- drizzle-zod for automatic Zod schema generation from database schemas

**Development and Build Tools**
- Vite for fast development and optimized builds
- TypeScript for type safety across the entire application
- Tailwind CSS for utility-first styling
- PostCSS and Autoprefixer for CSS processing

**AI Integration**
- @google/genai for Google's Generative AI capabilities (future features)

**Session Management**
- connect-pg-simple for PostgreSQL session storage
- Express session middleware for user session handling

**Mobile and Responsive Features**
- Custom hooks for mobile detection and responsive behavior
- Touch-friendly UI components optimized for mobile interaction