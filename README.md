# Chloe Robinson
**Software Developer & Web Enthusiast**

![Profile Banner](PASTE_BANNER_IMAGE_URL_HERE)

## About Me
I'm a developer with a focus on full-stack web and desktop development, working with modern frameworks to build role-driven, real-world applications. My coding style includes tea, a hunched back and my cat trying to sit on my keyboard. When I'm not coding, I can be found reading a book, playing video games or riding my horse.

---

## Tech Stack

### Languages & Frameworks
- **JavaScript / TypeScript** (React, React Native, Node.js)
- **C# / ASP.NET Core** (.NET 10, Web API)
- **HTML5 & CSS3**
- **PostgreSQL, MySQL & MongoDB**
- **Entity Framework Core**
- **Express.js**
- **RESTful APIs**

### Tools & Technologies
- **Git & GitHub** (branching workflows, team collaboration)
- **Electron** (cross-platform desktop packaging)
- **Expo** (React Native, Expo Router)
- **Firebase** (Authentication, Cloud Firestore, security rules)
- **Vite**
- **Tailwind CSS & DaisyUI**
- **Framer Motion**
- **Swagger / Swashbuckle**
- **xUnit.net & Vitest** (automated testing)
- **AWS Cloud Services**
- **Figma** (UI/UX Design)
- **Docker**

---

## Flagship Project: Koru

![Koru](koru-banner.png)

**Full-Stack Learning Management System — 3rd Year Client Project**

Koru is a full-stack LMS built to centralise academic workflows — course management, scheduling, assessments, analytics and communication — into a single, cross-platform desktop application for Students, Teachers and Administrators. Built for a real client brief, it enforces compliance with South Africa's POPIA (Protection of Personal Information Act) by design.

**Technologies:** React 19, TypeScript, Vite, Electron, Tailwind CSS, DaisyUI, Framer Motion, Chart.js — ASP.NET Core (C#), Entity Framework Core, PostgreSQL, BCrypt, Swagger

**Highlights:**
- Delivered a native cross-platform desktop app (Windows & macOS) via Electron, wrapping a React + Vite frontend
- Designed and built a POPIA-compliant, normalised PostgreSQL schema with role-based access control across three distinct user types
- Shipped 15 REST API controllers covering the full academic pipeline (courses, assignments, submissions, grading, feedback, timetables)
- Wrote and maintained 216 automated tests (xUnit.net + FluentAssertions on the backend, Vitest + React Testing Library on the frontend), with 83% backend and ~80% frontend line coverage
- Took direct client and lecturer UX feedback and shipped concrete fixes: restructured dashboards into a clear visual hierarchy, decomposed a 3,500-line monolithic component into focused modules, and extended the data model to support per-course assignment due dates
- Collaborated as part of a team using Git branching, code review, and Discord/WhatsApp coordination to deliver a complete MVP within budget and a 12-week timeline

[View Repository](https://github.com/corbyn-jpg/learn-online)

---

## Envol

**Location-Based Birdwatching Race — Mobile App | DV300, Term 3, Open Window Institute**

Envol is a location-based mobile game where players travel to real-world "arenas," race to identify the bird species found there, and verify each sighting with a timestamped photograph. Built solo as a term project, it combines GPS-gated gameplay, live timing, and a Firestore backend secured almost entirely through server-side rules.

**Technologies:** React Native 0.81 (Expo SDK 54), TypeScript, Expo Router (file-based, typed routes), Firebase (Authentication & Cloud Firestore), react-native-maps, expo-location, expo-image-picker / expo-image-manipulator

**Highlights:**
- Built GPS-gated "arenas" using the haversine formula to unlock content only when a player is physically inside a location's radius
- Designed two race modes (open-ended Stopwatch Sprint and Countdown Challenge) sharing one race-clock architecture: a React Context deriving elapsed time from `Date.now()` rather than an interval, so timing survives navigation and stays accurate under throttling
- Implemented photo-based sighting verification using EXIF `DateTimeOriginal` checks to reject screenshots, downloads, and forwarded images — a deliberate free, offline trade-off over a costed-and-prototyped AI vision verification path (~R0.25/check, would have needed a serverless proxy to protect the API key)
- Modelled per-arena progress with mode-aware Firestore keys (`{arenaId}` for Sprint vs `{arenaId}_countdown_{limitSeconds}`) so both modes track independent completion without clobbering each other
- Derived 8 achievement medals from race history via predicate functions rather than stored flags, keeping medal logic to a single array entry per new medal
- Locked down every meaningful permission via Firestore security rules rather than client code: immutable race results scoped to their creator, a "first blood" arena field that can only be set once, and per-user document ownership
- Solved image storage on Firebase's free tier by cropping, compressing, and storing profile pictures as base64 data URIs (~15–25KB/user) instead of requiring paid Cloud Storage

[View Repository](https://github.com/corbyn-jpg/envol)

---

## Other Portfolio Projects

### Poseidon's Notebook
**Full-Stack Marine Species Logbook**
Technologies: React, Node.js, Express, MySQL, JWT Authentication
A deployed full-stack application for marine enthusiasts to log species sightings with secure authentication and CRUD operations. Features user registration, species database, and responsive mobile-friendly design.
[View Repository](https://github.com/corbyn-jpg/poseidons-notebook)

![Poseidon's Notebook](PASTE_POSEIDONS_NOTEBOOK_IMAGE_URL_HERE)

### Open Library Explorer
**API-Driven Data Visualization Platform**
Technologies: React, Chart.js, Axios, CSS Modules, Open Library API
Interactive data visualization dashboard that transforms Open Library API data into engaging charts and comparisons. Features trend analysis, author comparisons, and timeline exploration.
[View Repository](https://github.com/corbyn-jpg/formative-one-openlibrary)

![Open Library Explorer](PASTE_OPEN_LIBRARY_IMAGE_URL_HERE)

### Vinoir E-commerce
**Luxury Perfume E-commerce Platform**
Technologies: React, MongoDB, Express, Node.js, Material-UI
Collaborative MERN stack project featuring a luxury perfume marketplace with user authentication, product catalog, shopping cart, and responsive design.
[View Repository](https://github.com/corbyn-jpg/summative-vinoir)

![Vinoir E-commerce](PASTE_VINOIR_IMAGE_URL_HERE)

---

## GitHub Statistics
![Chloe's GitHub Stats](https://github-readme-stats.vercel.app/api?username=corbyn-jpg&show_icons=true&theme=radical&hide_title=true&count_private=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=corbyn-jpg&layout=compact&theme=radical&hide_title=true)

---

## Career Focus
**Full-Stack Development | Cross-Platform Applications | User Experience Design**

I'm passionate about shipping complete, real-world software — from client requirements and database design through to a polished, tested, deployable product. This year's focus has been on delivering a production-grade application end to end: architecting a compliant data model, building role-based systems for multiple user types, and packaging a web app as a native cross-platform desktop experience.

### Currently Learning
- **Advanced React Patterns** (Custom Hooks, Context API, Performance Optimization)
- **Backend Architecture** (Microservices, API Design, Database Optimization)
- **Cloud Deployment** (CI/CD Pipelines, Scalable Infrastructure)
- **Testing & QA at Scale** (branch coverage, integration testing, automated build checks)

![Learning Journey](PASTE_LEARNING_JOURNEY_GIF_URL_HERE)

---

## Skills & Competencies

**Technical Skills:** Full-Stack Development (React + ASP.NET Core), Mobile App Development (React Native / Expo), RESTful API Design, Relational, Document & NoSQL Database Design (PostgreSQL, MySQL, MongoDB, Firestore), Automated Testing (xUnit, Vitest), Cross-Platform Desktop Development (Electron), Location-Based & Real-Time App Features, Data Privacy & Compliance by Design (POPIA), Backend Security Rules & Access Control, Git Branching Workflows, Responsive UI Development

**Soft Skills:** Client Requirement Gathering, Team Collaboration & Delegation, Incorporating User & Stakeholder Feedback, Project Planning Under Budget/Timeline Constraints, Problem-Solving, Adaptability, Attention to Detail

---

## Contact Information
- **Email:** [corbyncrobinson@gmail.com](mailto:corbyncrobinson@gmail.com)
- **LinkedIn:** [www.linkedin.com/in/chloe-robinson-25b123351](https://www.linkedin.com/in/chloe-robinson-25b123351)
- **GitHub:** github.com/corbyn-jpg
- **Portfolio:** Coming Soon

---

## Personal Interests
- Equestrian Activities
- Fantasy and Sci-Fi Literature
- RPG and Indie Gaming
- Continuous Learning and Development

> "In the spirit of science, there really is no such thing as a 'failed experiment.' Any test that yields valid data is a valid test." — Adam Savage

---
*This profile showcases my journey as a developing full-stack engineer, highlighting my projects, skills, and passion for building meaningful, real-world software.*
