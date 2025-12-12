# Project Folder Structure

This document outlines the complete folder structure for the Clinic Slot Booking System.

```
clinic-slot-booking-system/
│
├── backend/                          # Backend Node.js/TypeScript application
│   ├── src/
│   │   ├── config/                  # Configuration files
│   │   │   ├── database.ts          # Database connection configuration
│   │   │   ├── redis.ts             # Redis cache configuration
│   │   │   └── environment.ts       # Environment variable management
│   │   │
│   │   ├── controllers/             # Request handlers (route controllers)
│   │   │   ├── auth.controller.ts   # Authentication endpoints
│   │   │   ├── slot.controller.ts   # Slot management endpoints
│   │   │   ├── booking.controller.ts # Booking endpoints
│   │   │   └── clinic.controller.ts # Clinic endpoints
│   │   │
│   │   ├── services/                # Business logic layer
│   │   │   ├── auth.service.ts      # Authentication logic
│   │   │   ├── slot.service.ts      # Slot management logic
│   │   │   ├── booking.service.ts   # Booking logic
│   │   │   └── slot-lock.service.ts # Smart locking mechanism
│   │   │
│   │   ├── models/                  # Database models/schemas
│   │   │   ├── User.ts              # User model
│   │   │   ├── Clinic.ts            # Clinic model
│   │   │   ├── Slot.ts              # Slot model
│   │   │   └── Booking.ts           # Booking model
│   │   │
│   │   ├── middleware/              # Express middleware
│   │   │   ├── auth.middleware.ts   # JWT authentication
│   │   │   ├── validation.middleware.ts # Request validation
│   │   │   └── error.middleware.ts  # Error handling
│   │   │
│   │   ├── routes/                  # API route definitions
│   │   │   ├── auth.routes.ts       # Auth routes
│   │   │   ├── slot.routes.ts       # Slot routes
│   │   │   ├── booking.routes.ts   # Booking routes
│   │   │   └── clinic.routes.ts     # Clinic routes
│   │   │
│   │   ├── utils/                   # Utility functions
│   │   │   ├── logger.ts            # Logging utility
│   │   │   ├── errors.ts            # Custom error classes
│   │   │   └── validators.ts        # Validation helpers
│   │   │
│   │   ├── migrations/              # Database migrations
│   │   │   ├── 001_create_users.ts
│   │   │   ├── 002_create_clinics.ts
│   │   │   ├── 003_create_slots.ts
│   │   │   └── 004_create_bookings.ts
│   │   │
│   │   ├── app.ts                   # Express app configuration
│   │   └── server.ts                # Server entry point
│   │
│   ├── tests/                       # Test files
│   │   ├── unit/                    # Unit tests
│   │   │   ├── services/
│   │   │   └── utils/
│   │   ├── integration/             # Integration tests
│   │   │   └── api/
│   │   └── e2e/                     # End-to-end tests
│   │
│   ├── .env.example                 # Example environment variables
│   ├── .gitignore                   # Git ignore rules
│   ├── package.json                 # Dependencies and scripts
│   ├── tsconfig.json                # TypeScript configuration
│   ├── Dockerfile                   # Docker container definition
│   └── README.md                    # Backend documentation
│
├── frontend/                        # Frontend React/Vue application
│   ├── src/
│   │   ├── components/              # React/Vue components
│   │   │   ├── common/             # Reusable UI components
│   │   │   │   ├── Button.tsx
│   │   │   │   ├── Input.tsx
│   │   │   │   ├── Modal.tsx
│   │   │   │   ├── Card.tsx
│   │   │   │   └── LoadingSpinner.tsx
│   │   │   │
│   │   │   ├── auth/               # Authentication components
│   │   │   │   ├── LoginForm.tsx
│   │   │   │   └── RegisterForm.tsx
│   │   │   │
│   │   │   ├── booking/           # Booking-related components
│   │   │   │   ├── SlotCalendar.tsx
│   │   │   │   ├── BookingForm.tsx
│   │   │   │   ├── BookingCard.tsx
│   │   │   │   └── SlotSelector.tsx
│   │   │   │
│   │   │   └── admin/             # Admin components
│   │   │       ├── AdminDashboard.tsx
│   │   │       ├── SlotManagement.tsx
│   │   │       └── BookingList.tsx
│   │   │
│   │   ├── pages/                 # Page components (routes)
│   │   │   ├── Home.tsx           # Landing page
│   │   │   ├── Login.tsx          # Login page
│   │   │   ├── Register.tsx      # Registration page
│   │   │   ├── Clinics.tsx        # Clinic listing page
│   │   │   ├── BookSlot.tsx       # Booking page
│   │   │   ├── Dashboard.tsx      # User dashboard
│   │   │   └── AdminDashboard.tsx # Admin dashboard
│   │   │
│   │   ├── services/              # API service layer
│   │   │   ├── api.ts             # Axios/fetch configuration
│   │   │   ├── auth.service.ts    # Auth API calls
│   │   │   ├── slot.service.ts    # Slot API calls
│   │   │   └── booking.service.ts # Booking API calls
│   │   │
│   │   ├── hooks/                 # Custom React hooks
│   │   │   ├── useAuth.ts         # Authentication hook
│   │   │   ├── useSlots.ts        # Slot data hook
│   │   │   └── useBookings.ts     # Booking data hook
│   │   │
│   │   ├── context/               # React Context providers
│   │   │   └── AuthContext.tsx    # Authentication context
│   │   │
│   │   ├── utils/                 # Utility functions
│   │   │   ├── constants.ts       # App constants
│   │   │   ├── helpers.ts         # Helper functions
│   │   │   └── formatters.ts      # Data formatters
│   │   │
│   │   ├── types/                 # TypeScript type definitions
│   │   │   └── index.ts           # Shared types/interfaces
│   │   │
│   │   ├── styles/                # Global styles
│   │   │   └── globals.css        # Global CSS
│   │   │
│   │   ├── App.tsx                # Root component
│   │   └── main.tsx               # Application entry point
│   │
│   ├── public/                    # Static assets
│   │   ├── favicon.ico
│   │   ├── logo.svg
│   │   └── images/
│   │
│   ├── .env.example               # Example environment variables
│   ├── .gitignore                 # Git ignore rules
│   ├── package.json               # Dependencies and scripts
│   ├── tsconfig.json              # TypeScript configuration
│   ├── vite.config.ts             # Vite configuration (or next.config.js)
│   ├── Dockerfile                 # Docker container definition
│   └── README.md                  # Frontend documentation
│
├── docs/                           # Project documentation
│   ├── Project Plan.md            # This planning document
│   ├── coding-style.md            # Coding style guidelines
│   ├── API.md                     # API documentation
│   └── DEPLOYMENT.md              # Deployment guide
│
├── docker-compose.yml              # Docker Compose configuration
├── .editorconfig                   # Editor configuration
├── .gitignore                      # Root Git ignore rules
├── LICENSE                         # License file
└── README.md                       # Project README
```

## File Naming Conventions

- **Backend:** kebab-case for files (e.g., `auth.controller.ts`, `slot-lock.service.ts`)
- **Frontend:** PascalCase for components (e.g., `BookingForm.tsx`), camelCase for utilities (e.g., `helpers.ts`)
- **Config files:** lowercase with dots (e.g., `tsconfig.json`, `.env.example`)

## Directory Purposes

- **config/:** Environment-specific configurations
- **controllers/:** Handle HTTP requests and responses
- **services/:** Business logic and data processing
- **models/:** Database schema definitions
- **middleware/:** Request/response processing middleware
- **routes/:** API endpoint definitions
- **utils/:** Reusable helper functions
- **migrations/:** Database schema version control
- **components/:** Reusable UI components
- **pages/:** Full page components (routes)
- **services/:** API communication layer
- **hooks/:** Custom React hooks for state/logic
- **context/:** React Context providers
- **types/:** TypeScript type definitions











