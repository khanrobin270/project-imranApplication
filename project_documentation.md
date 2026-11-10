# Project Documentation --- Free Full-Stack Application

## 1. Project Overview

**Project goal:** Rebuild the application shared through the user's
Gemini link as closely as possible, including its interface, features,
backend, database management, and complete source code.

**Budget goal:** Start with a **\$0 budget** by using free plans and
open-source tools wherever practical.

> **Reference required:** The exact Gemini app design and behavior have
> not yet been inspected. Before implementation, add screenshots, a
> screen recording, exported code, or a written feature list from the
> reference app. The final scope and database design must be based on
> that material---not assumptions.

## 2. Main Objectives

-   Reproduce the reference app's UI and user experience as closely as
    the supplied reference allows.
-   Implement working buttons, forms, navigation, and application
    workflows.
-   Build a backend and connect it to a managed database.
-   Include authentication and role-based access where required.
-   Provide an admin dashboard if the reference app requires one.
-   Deliver the complete source code, database schema, setup
    instructions, and deployment guide.
-   Keep the project deployable on free tiers initially.

## 3. Proposed Free-Tier Technology Stack

  -----------------------------------------------------------------------
  Layer                   Proposed technology     Purpose
  ----------------------- ----------------------- -----------------------
  Frontend                React + Vite            Application interface

  Styling                 Tailwind CSS            Responsive styling

  Backend / API           Supabase services;      Data access and
                          server functions if     server-side logic
                          needed                  

  Database                Supabase PostgreSQL     Persistent application
                                                  data

  Authentication          Supabase Auth           Sign-up, sign-in,
                                                  sessions

  Source control          Git + GitHub            Version history and
                                                  code hosting

  Hosting                 Vercel                  Frontend deployment

  Editor                  Visual Studio Code      Local development
  -----------------------------------------------------------------------

**Important:** Free-plan limits, features, and availability can change.
Check current provider limits before launch. A custom domain, higher
usage, extra storage, email delivery, or advanced server workloads may
incur costs.

## 4. Application Scope

The exact feature list will be confirmed after reviewing the Gemini
reference. The following are candidate capabilities, not confirmed
requirements.

### User-facing application

-   Responsive layout for desktop, tablet, and mobile
-   Navigation and page routing
-   Forms with validation and useful error messages
-   User account creation and sign-in, if required
-   Data views and search/filter tools, if required
-   Clear loading, empty, success, and failure states

### Admin area (if required by the reference)

-   Protected administrator sign-in
-   Dashboard overview
-   Create, view, edit, and delete relevant records
-   User and role management, if required
-   Search, filtering, and pagination where useful

### Backend and database

-   Database schema and relationships
-   Secure API/data access
-   Input validation
-   Role-based authorization
-   Database migrations or SQL setup scripts
-   Backup/export guidance appropriate to the chosen plan

## 5. Database Planning

The final schema depends on the actual features. Do not create
speculative tables before reviewing the reference.

For each required data entity, document:

-   Table name and purpose
-   Columns and data types
-   Primary key
-   Foreign-key relationships
-   Required and optional fields
-   Unique constraints and indexes
-   Row-level security (RLS) policies
-   Which user roles can read or modify records

All private keys and service-role secrets must remain on the server.
Never put privileged secrets in frontend code or commit `.env` files to
GitHub.

## 6. Suggested Project Structure

``` text
application/
├── public/
├── src/
│   ├── assets/
│   ├── components/
│   ├── layouts/
│   ├── pages/
│   ├── hooks/
│   ├── services/
│   ├── lib/
│   ├── styles/
│   ├── App.jsx
│   └── main.jsx
├── supabase/
│   ├── migrations/
│   └── seed.sql
├── .env.example
├── .gitignore
├── package.json
├── README.md
└── PROJECT.md
```

Adjust this structure to match the actual application and backend
approach.

## 7. Environment Configuration

Create a local `.env` file for development and configure the same
variables securely in the hosting provider.

Example only:

``` env
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

Only publish values intended for browser use. Keep database passwords,
service-role keys, API secrets, and other privileged credentials in
server-side environment variables. The `.env` file must be excluded from
version control.

## 8. Development Roadmap

### Phase 1 --- Reference review

1.  Open and inspect the Gemini reference.
2.  Collect screenshots of every important page and state.
3.  List all visible features and user workflows.
4.  Identify user roles and admin requirements.
5.  Confirm which actions must save or retrieve data.

**Deliverable:** Approved feature list and page map.

### Phase 2 --- UI implementation

1.  Set up React and Vite.
2.  Build the shared layout and reusable components.
3.  Implement each page from the reference.
4.  Add responsive behavior.
5.  Compare the result against the supplied reference.

**Deliverable:** Working frontend.

### Phase 3 --- Database and backend

1.  Create the Supabase project.
2.  Design and create the database schema.
3.  Configure authentication if needed.
4.  Configure Row Level Security policies.
5.  Connect frontend workflows to database operations.
6.  Add validation and error handling.

**Deliverable:** Functional data layer.

### Phase 4 --- Testing

-   Test all navigation and buttons.
-   Test forms and validation.
-   Test sign-up, sign-in, and permissions if applicable.
-   Test create, read, update, and delete operations.
-   Test mobile and desktop layouts.
-   Check that users cannot access data or admin actions they are not
    authorized to use.

**Deliverable:** Tested application and issue list.

### Phase 5 --- Deployment

1.  Push the source code to GitHub.
2.  Import the repository into Vercel.
3.  Add the required environment variables.
4.  Deploy and test the live application.
5.  Document how to update and maintain it.

**Deliverable:** Live deployment and setup guide.

## 9. Final Deliverables

-   Complete frontend source code
-   Backend/API code or configuration
-   Database schema and SQL migrations
-   Authentication and authorization setup, if required
-   Admin dashboard, if required
-   `.env.example` without real secrets
-   README with installation and run commands
-   Deployment instructions
-   Basic testing checklist

## 10. Free-Plan and Security Notes

-   Free hosting is suitable for learning, prototypes, and small
    projects, but it is not an unlimited production service.
-   Review current usage quotas, project pause rules, storage,
    bandwidth, and backup options.
-   Do not promise zero cost indefinitely; usage or business
    requirements may outgrow free plans.
-   Use Row Level Security and least-privilege access for database
    access.
-   Never share passwords, private API keys, database credentials, or
    service-role keys in chat or source control.
-   Use sample data during development; only import real user data when
    there is a clear need and appropriate permission.

## 11. Information Needed Before Exact Implementation

The following reference material is needed to reproduce the Gemini app
accurately:

-   Screenshots of all pages
-   A short screen recording showing key workflows, if possible
-   Any available source code or exported project files
-   A list of user roles (for example, user and admin)
-   Any special integrations or APIs the app uses

Once the reference is available, replace the candidate scope and generic
database notes in this document with the exact screens, features,
workflows, and schema.

------------------------------------------------------------------------

**Project status:** Planning\
**Budget target:** \$0 to start, subject to free-tier limits\
**Next action:** Provide the Gemini app screenshots or exported source
so the exact requirements can be documented.
