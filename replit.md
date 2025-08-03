# Overview

This is a full-stack AI chat application that allows users to interact with Google's Gemini AI model for both text conversations and image generation. The application features a Discord-inspired UI design with a chat interface that supports real-time messaging and AI-powered responses. Users can send text messages to receive AI responses or request image generation through natural language prompts.

The application is built as a modern web app with a React frontend and Express.js backend, utilizing TypeScript throughout for type safety. It includes a comprehensive UI component library based on shadcn/ui and supports both text-based conversations and AI image generation capabilities.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React 18 with TypeScript and Vite as the build tool
- **UI Components**: shadcn/ui component library with Radix UI primitives
- **Styling**: Tailwind CSS with custom Discord-inspired theme colors and CSS variables
- **State Management**: TanStack Query (React Query) for server state management
- **Routing**: Wouter for lightweight client-side routing
- **Form Handling**: React Hook Form with Zod validation integration

## Backend Architecture
- **Framework**: Express.js with TypeScript running on Node.js
- **API Design**: RESTful API with structured endpoints for conversations and messages
- **Request Handling**: JSON middleware for parsing requests and custom logging middleware
- **Error Handling**: Centralized error handling with proper HTTP status codes
- **Development Setup**: Hot reloading with tsx and custom Vite integration for development

## Data Storage Solutions
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Schema Management**: Drizzle Kit for migrations and schema management
- **Development Storage**: In-memory storage implementation for development/testing
- **Connection**: Neon Database serverless PostgreSQL for production
- **Session Management**: PostgreSQL-based session storage with connect-pg-simple

## Authentication and Authorization
- **Session-based**: Traditional session-based authentication (infrastructure present)
- **User Management**: User creation and retrieval with username/password system
- **Storage**: Session data stored in PostgreSQL with automatic cleanup

## External Dependencies

### AI Services
- **Google Gemini AI**: Primary AI service for text generation using @google/genai
- **Text Model**: gemini-2.5-flash for conversational responses
- **Image Model**: gemini-2.0-flash-preview-image-generation for image creation
- **API Integration**: Environment variable-based API key configuration

### Database Services
- **Neon Database**: Serverless PostgreSQL hosting
- **Connection**: @neondatabase/serverless for optimized serverless connections
- **ORM**: Drizzle ORM with PostgreSQL dialect for type-safe database operations

### UI and Styling
- **Component Library**: Comprehensive set of Radix UI components for accessibility
- **Icons**: Lucide React for consistent iconography
- **Styling**: Tailwind CSS with PostCSS for processing
- **Theming**: CSS custom properties for light/dark mode support

### Development Tools
- **Replit Integration**: Custom Vite plugins for Replit environment
- **Build Tools**: ESBuild for server bundling and Vite for client bundling
- **Type Checking**: TypeScript with strict configuration
- **Hot Reloading**: Custom Vite middleware integration for development