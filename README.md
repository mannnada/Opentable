# Opentable
# BookTable Application

## Team Information
**Team Name**: Tech Tiro

**Team Members**:
- [Team Member 1 Name]
  - Areas of Contribution: Frontend UI/UX, Restaurant search functionality, Authentication system
- [Team Member 2 Name]
  - Areas of Contribution: Restaurant Manager Dashboard, Backend API implementation, Database design
- [Team Member 3 Name]
  - Areas of Contribution: Admin Dashboard, Deployment configuration, Testing and quality assurance

## Project Overview
BookTable is an end-to-end restaurant reservation application similar to OpenTable. The application allows customers to search for restaurants and make reservations, restaurant managers to manage their listings, and administrators to oversee the platform.

## Links
- [Project Journal](https://docs.google.com/document/d/1EjQj-mZ5t8NCFZjNkJTsHAGpv7AYtcZtDGQ5yq53YWc/edit?usp=sharing)
- [Product & Sprint Backlog](https://docs.google.com/spreadsheets/d/1iD2uDq-CfOlZMXjbR0RR1-VTIMA1FaoHdvj7BhhbBGs/edit?usp=sharing)

## Feature Set

### Customer Features
- Search for restaurants by Date, Time, Party Size, and location (City/State or Zip code)
- View available restaurants with details (Name, Cuisine type, Cost rating, Reviews/Ratings, Booking counts)
- Select available time slots to book tables
- View restaurant reviews
- View restaurant locations on Google Maps
- User registration and authentication
- Book tables with email/SMS confirmation
- Cancel bookings

### Restaurant Manager Features
- Add new restaurant listings
- Manage restaurant details (name, address, contact info, hours, available booking times, table sizes)
- Update descriptions and photos
- Secure authentication system

### Admin Features
- Remove restaurants from the platform
- Approve new restaurant listings
- Access analytics dashboard for reservation data

## Architecture & Design

## Project Structure

booktable-application/
├── public/                     # Static assets
│   └── table-icon.svg          # Application icon
├── src/                        # Source code
│   ├── components/             # Reusable UI components
│   │   ├── common/             # Shared components
│   │   │   ├── Button.tsx      # Button component
│   │   │   ├── Card.tsx        # Card component
│   │   │   ├── Input.tsx       # Input component
│   │   │   └── Modal.tsx       # Modal component
│   │   ├── layout/             # Layout components
│   │   │   ├── Header.tsx      # App header
│   │   │   ├── Footer.tsx      # App footer
│   │   │   └── Sidebar.tsx     # Navigation sidebar
│   │   ├── restaurant/         # Restaurant-specific components
│   │   │   ├── RestaurantCard.tsx     # Restaurant listing card
│   │   │   ├── ReservationForm.tsx    # Booking form
│   │   │   ├── ReviewsList.tsx        # Restaurant reviews
│   │   │   └── TimeSlotPicker.tsx     # Available time slots
│   │   ├── admin/              # Admin components
│   │   │   ├── RestaurantApproval.tsx # Restaurant approval
│   │   │   ├── AnalyticsDashboard.tsx # Analytics dashboard
│   │   │   └── UserManagement.tsx     # User management
│   │   └── manager/            # Restaurant manager components
│   │       ├── RestaurantForm.tsx     # Restaurant info form
│   │       ├── TableManagement.tsx    # Table management
│   │       └── BookingCalendar.tsx    # Booking overview
│   ├── pages/                  # Application pages
│   │   ├── Home.tsx            # Landing page
│   │   ├── SearchResults.tsx   # Restaurant search results
│   │   ├── RestaurantDetails.tsx # Individual restaurant page
│   │   ├── BookingConfirmation.tsx # Booking confirmation
│   │   ├── UserProfile.tsx     # User profile and bookings
│   │   ├── auth/               # Authentication pages
│   │   │   ├── Login.tsx       # Login page
│   │   │   └── Register.tsx    # Registration page
│   │   ├── manager/            # Restaurant manager pages
│   │   │   ├── Dashboard.tsx   # Manager dashboard
│   │   │   ├── EditRestaurant.tsx # Edit restaurant details
│   │   │   └── Reservations.tsx # View/manage reservations
│   │   └── admin/              # Admin pages
│   │       ├── Dashboard.tsx   # Admin dashboard
│   │       ├── Restaurants.tsx # Restaurant management
│   │       └── Analytics.tsx   # Detailed analytics
│   ├── hooks/                  # Custom React hooks
│   │   ├── useAuth.ts          # Authentication hook
│   │   ├── useRestaurants.ts   # Restaurant data hook
│   │   └── useReservations.ts  # Reservation management hook
│   ├── store/                  # Zustand state management
│   │   ├── authStore.ts        # Authentication state
│   │   ├── restaurantStore.ts  # Restaurant data state
│   │   └── reservationStore.ts # Reservation state
│   ├── services/               # API services
│   │   ├── api.ts              # Base API configuration
│   │   ├── authService.ts      # Authentication service
│   │   ├── restaurantService.ts # Restaurant data service
│   │   └── reservationService.ts # Reservation service
│   ├── utils/                  # Utility functions
│   │   ├── dateUtils.ts        # Date formatting utilities
│   │   ├── validation.ts       # Form validation helpers
│   │   └── formatters.ts       # Data formatting functions
│   ├── types/                  # TypeScript type definitions
│   │   ├── auth.types.ts       # Authentication types
│   │   ├── restaurant.types.ts # Restaurant data types
│   │   └── reservation.types.ts # Reservation types
│   ├── constants/              # Application constants
│   │   ├── routes.ts           # Route definitions
│   │   └── api.ts              # API endpoints
│   ├── assets/                 # Local assets (images, etc.)
│   ├── App.tsx                 # Main application component
│   ├── main.tsx                # Application entry point
│   └── supabase.ts             # Supabase client setup
├── .eslintrc.config.js         # ESLint configuration
├── index.html                  # HTML entry point
├── package.json                # Project dependencies
├── postcss.config.js           # PostCSS configuration
├── tailwind.config.js          # Tailwind CSS configuration
├── tsconfig.json               # TypeScript configuration
├── vite.config.ts              # Vite configuration
└── README.md                   # Project documentation

### Technology Stack
- **Frontend**: 
  - React 18.3.1 with TypeScript
  - React Router 6.30.0 for routing
  - Zustand 4.5.6 for state management
  - TailwindCSS 3.4.13 for styling
  - Lucide React for icons
  - Date-fns for date manipulation
- **Backend**: 
  - Supabase for authentication, database and storage
- **Database**: 
  - PostgreSQL (via Supabase)
- **Deployment**: 
  - AWS EC2 Auto-Scaled Cluster with Load Balancer

### Architecture Diagrams
- Component Diagram: # BookTable Component Architecture
This component diagram illustrates the architecture of our BookTable reservation application. The frontend leverages React 18 with TypeScript, Vite, and Tailwind CSS for the UI layer, with Zustand managing state and React Router handling navigation. The backend utilizes Supabase for authentication, database, and storage, while the deployment infrastructure runs on AWS with auto-scaling EC2 instances, S3 for static assets, and CloudFront CDN.
![image](https://github.com/user-attachments/assets/a4d066fe-8715-418f-a488-02d7de417112)

- Deployment Diagram: # Our BookTable application employs a robust AWS cloud infrastructure with Route 53 for DNS and CloudFront for content delivery, directing traffic to an Elastic Load Balancer that distributes requests across auto-scaling EC2 instances running our React frontend. Backend services are managed through Supabase Cloud, providing authentication, PostgreSQL database, file storage, and serverless edge functions. This architecture ensures high availability and performance through redundant systems, while CloudWatch monitoring provides real-time system health metrics. The separation of frontend and backend concerns allows independent scaling and maintenance, creating a resilient system that can handle varying loads from customers, restaurant managers, and administrators. 
![image](https://github.com/user-attachments/assets/6ba160ef-5058-4a5b-91a4-5f227eb8a262)


### UI Wireframes
[Link to wireframes folder or embedded images]

## XP Core Values
Our team embraced the following XP Core Values throughout the project:

### Communication
Throughout our project, our team maintained open communication channels via regular daily stand-ups and a dedicated Slack channel. We ensured everyone was informed about project status, blockers, and decisions. We used pair programming for complex features, which enhanced knowledge sharing and code quality. Our communication strategy was transparent, with team members feeling comfortable raising concerns and proposing solutions, fostering a collaborative environment where ideas flowed freely.

### Respect
Our team prioritized mutual respect by acknowledging each member's unique skills and perspectives. During code reviews, feedback was constructive and focused on improving the product rather than criticizing individuals. We respected each other's time by being punctual for meetings and adhering to agreed deadlines. When disagreements arose, we practiced active listening and ensured everyone had equal opportunity to express their views. This respect extended to respecting the codebase through adherence to clean code practices and established standards.

## Installation and Setup
```bash
# Clone the repository
git clone https://github.com/your-username/booktable-application.git

# Navigate to the project directory
cd booktable-application

# Install dependencies
npm install

# Start the development server
npm run dev

# Build for production
npm run build
```

## Environment Variables
Create a `.env` file in the root directory with the following variables:
```
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

## API Documentation
The application uses Supabase as the backend, with the following main API endpoints:

- Authentication
  - `/auth/signup` - Register a new user
  - `/auth/signin` - Sign in existing user
  - `/auth/signout` - Sign out user

- Restaurants
  - `/restaurants` - Get all restaurants
  - `/restaurants/:id` - Get restaurant by id
  - `/restaurants/search` - Search restaurants with filters
  - `/restaurants/:id/availability` - Get availability for a restaurant

- Reservations
  - `/reservations` - Create a new reservation
  - `/reservations/:id` - Get, update, or cancel a reservation
  - `/reservations/user/:userId` - Get all reservations for a user

- Admin
  - `/admin/restaurants/pending` - Get pending restaurant approvals
  - `/admin/restaurants/:id/approve` - Approve a restaurant
  - `/admin/analytics` - Get reservation analytics

## Demo
[Link to demo video if available]
