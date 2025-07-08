# SEPHYX - Cyberpunk Streetwear Platform

## Overview

SEPHYX is a cyberpunk-themed streetwear e-commerce platform built as a full-stack web application. The project combines a React frontend with a Node.js/Express backend, featuring a dark, glitchy aesthetic inspired by cyberpunk culture. The application includes user authentication, product management, shopping cart functionality, and an immersive gaming-like experience with user rankings and vault access.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: React hooks with localStorage for persistence
- **Styling**: Tailwind CSS with custom cyberpunk theme and CSS variables
- **UI Components**: Radix UI components with custom styling via shadcn/ui
- **Build Tool**: Vite for fast development and optimized builds

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Session Management**: Express sessions with PostgreSQL store
- **Development**: Hot reloading with Vite integration in development mode

### Key Design Decisions
- **Monorepo Structure**: Shared types and schemas between client and server
- **TypeScript First**: Complete type safety across the entire stack
- **localStorage Strategy**: Client-side persistence for user data, cart, and preferences
- **Component-Based UI**: Modular, reusable components with consistent theming

## Key Components

### Authentication System
- **Implementation**: Custom hook-based authentication with crypto API
- **Password Security**: SHA-256 hashing using Web Crypto API
- **Session Persistence**: localStorage-based session management
- **User Progression**: XP system with ranks (INITIATE to NEON_THIEF)

### Product Management
- **Categories**: Hoodies, masks, accessories, jackets, pants
- **Rarity System**: Common, rare, legendary, mythic tiers
- **Inventory**: Real-time stock tracking with localStorage persistence
- **Filtering**: Multi-dimensional filtering by category, rarity, and price

### Shopping Experience
- **Cart Management**: Persistent cart with quantity management
- **Checkout**: Instagram-based ordering system (copies order details to clipboard)
- **Real-time Updates**: Stock levels update immediately on purchase

### Gaming Elements
- **XP System**: Users gain experience through time spent and puzzle solving
- **Vault Access**: Special content unlocked through achievements
- **Konami Code**: Easter egg for instant vault unlock
- **Rank Progression**: Visual rank system with color coding

## Data Flow

### User Authentication Flow
1. User enters credentials in login modal
2. Password hashed using Web Crypto API
3. Credentials validated against localStorage user database
4. Session stored in localStorage for persistence
5. User state propagated through React context

### Shopping Cart Flow
1. User adds product to cart
2. Cart state updated in React hooks
3. Cart persisted to localStorage
4. Stock levels decremented
5. Real-time UI updates reflect changes

### Vault Access Flow
1. User gains XP through activities
2. Rank calculated based on XP thresholds
3. Vault access granted when conditions met
4. Special content and features unlocked

## External Dependencies

### UI Framework Dependencies
- **Radix UI**: Accessible, unstyled UI primitives
- **Tailwind CSS**: Utility-first CSS framework
- **Class Variance Authority**: Type-safe component variants
- **Lucide React**: Icon library

### Development Dependencies
- **Vite**: Build tool and development server
- **TypeScript**: Type safety and developer experience
- **ESBuild**: Fast JavaScript bundler for production

### Database Dependencies
- **Drizzle ORM**: Type-safe database queries
- **@neondatabase/serverless**: PostgreSQL adapter
- **connect-pg-simple**: PostgreSQL session store

## Deployment Strategy

### Build Process
- **Frontend**: Vite builds optimized React bundle to `dist/public`
- **Backend**: ESBuild bundles Node.js server to `dist/index.js`
- **Static Assets**: Frontend assets served by Express in production

### Environment Configuration
- **Development**: Hot reloading with Vite dev server
- **Production**: Express serves static files and API routes
- **Database**: PostgreSQL connection via environment variable

### Replit Integration
- **Development Banner**: Automatic Replit development banner injection
- **Cartographer**: Replit-specific development tools integration
- **Runtime Error Overlay**: Enhanced error reporting in development

## Changelog

```
Changelog:
- July 08, 2025. Initial setup
- July 08, 2025. Modernized UI with glass morphism effects, improved animations, contemporary styling, and better visual hierarchy
```

## Recent Changes

✓ Updated color palette with modern cyberpunk theme
✓ Implemented glass morphism design system throughout components
✓ Added smooth animations and transitions for better UX
✓ Modernized navbar with floating design and improved spacing
✓ Enhanced home page with larger typography and better visual hierarchy
✓ Updated shop page with modern card designs and filter styling
✓ Modernized login and cart modals with glass effects
✓ Added gradient text effects and modern button styles
✓ Improved product collection with higher quality images
✓ Enhanced overall visual consistency and contemporary appeal

## User Preferences

```
Preferred communication style: Simple, everyday language.
```