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
- [Project Journal](link-to-your-github-project-journal)
- [Product & Sprint Backlog](link-to-your-google-sheet-or-project-board)

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
- Component Diagram: [See below or link to image]
- Deployment Diagram: [See below or link to image]

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
