# Portfolio Website

## Overview

This is a modern, full-stack portfolio website for Kiran Paul K, an AI Engineer and Software Developer. The application showcases professional experience, skills, projects, and provides a contact form for potential opportunities. Built with React frontend and Express backend, featuring a clean Nike-inspired design with smooth animations.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript and Vite as the build tool
- **Routing**: Wouter for lightweight client-side routing
- **Styling**: Tailwind CSS with custom Nike-inspired design system
- **UI Components**: shadcn/ui component library built on Radix UI primitives
- **State Management**: TanStack Query for server state management
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Framework**: Express.js with TypeScript
- **API Design**: RESTful API with a simple contact form endpoint
- **Request Logging**: Custom middleware for API request/response logging
- **Error Handling**: Centralized error handling with proper HTTP status codes
- **Validation**: Zod schemas for input validation

### Development Setup
- **Hot Reloading**: Vite dev server with HMR for frontend development
- **Build Process**: Vite for frontend bundling, esbuild for backend compilation
- **TypeScript**: Strict type checking across the entire application
- **Path Aliases**: Configured for clean imports (@/, @shared/, @assets/)

## Key Components

### Frontend Components
- **Responsive Layout**: Mobile-first design with smooth scroll navigation
- **Hero Section**: Professional introduction with call-to-action buttons
- **About Section**: Education background and achievements
- **Skills Section**: Programming languages with animated progress bars
- **Projects Section**: Featured AI/ML projects with visual cards
- **Experience Section**: Professional work history with company logos
- **Awards Section**: Recognition and achievements grid
- **Contact Section**: Interactive form with toast notifications

### Backend Components
- **Contact API**: POST endpoint for form submissions with validation
- **Static File Serving**: Serves built React application in production
- **Development Middleware**: Vite integration for hot reloading
- **Storage Interface**: Abstracted storage layer (currently in-memory)

### UI/UX Features
- **Animation**: Intersection Observer for scroll-triggered animations
- **Toast Notifications**: User feedback for form submissions
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Accessibility**: Proper ARIA labels and keyboard navigation support

## Data Flow

### Client-Side Flow
1. User navigates through single-page application
2. Smooth scroll navigation between sections
3. Contact form submission triggers API call
4. Toast notifications provide user feedback
5. Skill bars animate on scroll using Intersection Observer

### Server-Side Flow
1. Express server handles static file serving
2. API routes process contact form submissions
3. Request logging middleware tracks API usage
4. Validation middleware ensures data integrity
5. Error handling provides appropriate HTTP responses

## External Dependencies

### Core Dependencies
- **React Ecosystem**: React, React DOM, React Hook Form
- **UI Framework**: Radix UI primitives, shadcn/ui components
- **Styling**: Tailwind CSS, class-variance-authority for component variants
- **Data Fetching**: TanStack Query for server state management
- **Validation**: Zod for schema validation
- **Icons**: Lucide React for consistent iconography
- **Date Handling**: date-fns for date utilities

### Development Dependencies
- **Build Tools**: Vite, esbuild, TypeScript
- **Backend**: Express, tsx for TypeScript execution
- **Database Setup**: Drizzle ORM with PostgreSQL dialect (configured but not actively used)
- **Session Management**: connect-pg-simple for PostgreSQL sessions

### Database Configuration
- **ORM**: Drizzle ORM configured for PostgreSQL
- **Schema**: Basic user schema defined but not currently utilized
- **Migration**: Drizzle Kit for database migrations
- **Connection**: Neon Database serverless driver configured

## Deployment Strategy

### Build Process
1. **Frontend**: Vite builds React application to `dist/public`
2. **Backend**: esbuild compiles TypeScript server to `dist/index.js`
3. **Static Assets**: Frontend assets served by Express in production
4. **Environment Variables**: Database URL and other config via environment

### Production Setup
- **Server**: Single Express server serves both API and static files
- **Process Management**: Node.js with proper error handling
- **Asset Serving**: Express static middleware for built frontend
- **API Endpoints**: RESTful API under `/api` prefix

### Development Workflow
- **Hot Reloading**: Vite dev server with React Fast Refresh
- **TypeScript**: Real-time type checking and compilation
- **API Development**: tsx for running TypeScript server files
- **Database**: Drizzle push command for schema synchronization

### Scaling Considerations
- **Database**: PostgreSQL configured for production scaling
- **Session Storage**: PostgreSQL session store for horizontal scaling
- **Static Assets**: Can be moved to CDN for better performance
- **API Rate Limiting**: Not currently implemented but easily addable