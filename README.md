# Frontend Academy - Project 3

## Overview

**Enable Good** is a complete web application that connects NGOs and companies for meaningful collaborations.
It was developed using **React**, **TypeScript**, and **Firebase Firestore**, designed to function like a real SaaS platform with both public and private user experiences.

Users can browse impact projects, register as NGOs, manage profiles, subscribe to plans, and even integrate with **Google Calendar** for real-time scheduling.

---

## Project Purpose

This project was created as part of Brainster’s Front-End Academy.
The goal was to simulate a real-world collaboration platform that demonstrates modern front-end development, strong UI/UX principles, and seamless integration between data, authentication, and third-party APIs.

It focuses on:

- Authentication and user management with Firebase
- Firestore data handling
- Google API integration
- Responsive and dynamic interface using React and SCSS Modules
- A clear separation between public and private experiences

---

## Main Features

### Public Layout

- Home, About, Explore, and Learning Hub pages
- Dynamic **Explore page** for filtering companies and projects
- Interactive video carousel and educational conten
- **Join** and **Login** pages with custom validation and Firebase integration
- Step-by-step registration including document upload, subscription, and simulated payment
- Access Restriction and 404 pages for invalid or unauthorized routes

### Private Layout

- Personal **Dashboard** with social-like posts, reactions
- **Statistics page** with interactive charts (ApexCharts)
- **Google Calendar** integration – authorize, view, and create events
- **Matchmaking** and **Saved Profiles** to connect NGOs with companies
- **Projects management** with document uploads, status tracking, and progress views
- **Account settings** for updating profile, password, and verification steps
- Fully responsive, designed for both desktop and mobile

---

## Technology Summary

### Core Frameworks

- React + TypeScript
- Firebase (Firestore, Auth, Storage)

### UI & Styling

- SCSS Modules
- Bootstrap
- Framer Motion for animations

### Integrations & Utilities

- Google OAuth + Calendar API
- ApexCharts for data visualization
- React Router for navigation
- React Dropzone for file uploads
- Moment.js for date handling

---

## Getting Started

To run the project locally:

1. Clone the repository:
   ```bash
   git clone https://git.brainster.co/Angel.Mladenoski-FE21/project003_angelmladenoski_fe21.git .
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start development server:
   ```bash
   npm run dev
   ```
   Then open your browser at http://localhost:5173

---

## How to Use

- Navigate freely through public pages (Home, Explore, Learning Hub).
- Register as an NGO to access the private dashboard.
- Upload your organization’s documents, select a subscription, and finalize registration.
- Use Google integration to sync your event calendar.
- Explore and connect with companies based on ESG/SDG goals and industries.
- Manage and track your organization’s projects, reports, and statistics.

---

## Development Approach

The project was built from the ground up with emphasis on scalability and maintainability.

**Key steps included:**

1. **UI/UX Analysis** – Translating Figma designs into reusable React components.
2. **Component Architecture** – Organized SCSS modules and layouts for clarity and reusability.
3. **Routing & State Management** – Protected routes with React Router and Context for global data.
4. **API Integration** – Firebase and Google APIs configured for authentication and calendar sync.
5. **Testing & Optimization** – Verified responsiveness, form validation, and data flows across pages.

---

## Data Structure

### Company

```ts
type CompanyType = {
  name: string;
  slug: string;
  shortDescription: string;
  logoUrl: string;
  esgGoals: string[];
  industry: string;
  sdgGoals: string[];
  type: string;
  projects: string[];
  whoAreWe: string;
  ourVision: string;
  ourHistory: string;
};
```

### Project

```ts
type ProjectType = {
  title: string;
  slug: string;
  description: string;
  startDate: string;
  endDate: string;
  logoUrl: string;
  longDesc: string;
};
```

### User (NGO)

```ts
type UserType = {
  causeArea: string;
  country: string;
  createdAt: string;
  email: string;
  id: string;
  image: string | null;
  industry: string;
  isVerified: boolean;
  organizationName: string;
  partnershipGoals: string[];
  partnershipPreferences?: {
    location?: string[];
    duration?: string[];
    partnerType?: string[];
    esgPillars?: string[];
  };
  password: string;
  confirmPassword: string;
  registeredCharityNumber: number;
  role: string;
  sdgs: string[];
  shortBio?: string;
  sizeOfOrganisation: number;
  subscriptionPlan: string;
  website?: string;
  documents: Array<{ type: string; file: File | null }>;
  savedProfiles: string[];
};
```

---

## Acknowledgments

- Built with guidance and design assets from **Brainster Front-End Academy**
- Special thanks to the mentors and instructors for continuous support
- Animations and icons adapted from the original Brainster Figma resources

## Author

Developed and written by **Angel Mladenoski**

📧 Email: [angel.mladenoski@gmail.com](mailto:angel.mladenoski@gmail.com)<br/>
💼 [LinkedIn](https://www.linkedin.com/in/angel-mladenoski-46a27330a) <br/>
🐙 [GitHub](https://github.com/angelmladenoski)
