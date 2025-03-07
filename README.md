# Senior Mobile Developer Hybrid Technology Challenge

Welcome to our Senior Mobile Developer Challenge, designed to assess your coding skills and problem-solving abilities in hybrid mobile development. This challenge encompasses both frontend and backend tasks, allowing you to demonstrate your proficiency in creating cross-platform mobile applications. Our aim is not only to evaluate your technical skills but also to see how you approach learning new tools and concepts.

## Frontend: React Native or React with Capacitor

### Introduction

This challenge involves creating a hybrid mobile application that leverages the Wikipedia Featured Content API. The goal is to develop a user-friendly mobile interface allowing users to explore featured content based on selected dates and languages. This project is an opportunity to demonstrate your skills in building interactive mobile applications with attention to code quality, UI/UX design, native device integration, and offline functionality.

### Objective

Build a hybrid mobile application using React Native or React with Capacitor that:

- Interacts with the [Wikipedia Featured Content API](https://api.wikimedia.org/wiki/Feed_API/Reference/Featured_content).
- Displays content based on user-selected dates and languages.
- Offers a card-based feed with proper mobile interaction patterns.
- Functions effectively on both iOS and Android platforms.

### Functional Requirements

#### Date and Language Selection

- Implement mobile-friendly UI elements for date and language selection.
- Fetch and display content based on these selections.
- Support platform-specific date/time pickers.

#### Mobile-Optimized Content Display

- Present the content in a scrollable card-based feed optimized for mobile devices.
- Implement pull-to-refresh functionality.
- **Bonus feature:** Enable users to bookmark favorite content.
- **Advance bonus feature:** Implement infinite scrolling, loading content for the next day as the user reaches the bottom.

#### Card Content

- Display the title, thumbnail image (if available), and a brief excerpt or description for each piece of content.
- Optimize image loading and caching for mobile networks.
- **Bonus feature:** Implement responsive layouts for different screen sizes and orientations.

#### Mobile-Specific Interactions

- Integrate native sharing capabilities to share content via messaging apps, social media, etc.
- Implement touch gestures (swipe to dismiss, long press for options).
- Mark viewed cards with a visual indicator.
- **Bonus feature:** Persist the 'viewed' status and bookmarks in local storage to maintain status across sessions.

#### Offline Capability

- Implement offline caching of previously viewed content.
- Show appropriate notifications when offline.
- **Bonus feature:** Allow users to save specific content for offline viewing.

### Technical Recommendations

- **Required:** Typescript, React Native or React with Capacitor (choose one).
- You may use any supporting libraries, ideally ones that can highlight your skills.

## Backend: Node.js API with NestJS

### Introduction

This challenge focuses on building a Node.js API using the NestJS framework. The API will act as a proxy to the Wikipedia Featured Content API. Additionally, it will incorporate translation features using the LibreTranslate API. This project tests your ability to create a scalable and maintainable backend service optimized for mobile application support, along with your skills in API development, data validation, and integration of external services.

### Objective

Develop a Node.js API using NestJS that:

- Proxies [Wikipedia Featured Content API](https://api.wikimedia.org/wiki/Feed_API/Reference/Featured_content).
- Offers translation for titles and extracts via the [LibreTranslate API](https://libretranslate.com/) (do not pay for the API, use self-hosted).
- Ensures robust validation and error handling.
- Optimizes response payloads for mobile consumption.

### Functional Requirements

#### Endpoints

- `/feed`  
  - Acts as a proxy to the Wikipedia Featured Content API.
  - Accepts only GET requests.
  - Supports all parameters of the Wikipedia API, validating them to ensure correct types and values.
  - Defines a standard error response format for validation failures and other errors.
  - Optimizes response size for mobile devices (e.g., image compression, payload minimization).
- `/feed/translate/#language`
  - Inherits all functionalities of the `/feed` endpoint.
  - Accepts a URL parameter specifying the target language for translation.
  - Validates the `#language` parameter to ensure it matches supported languages by the translation service.

#### Mobile-Specific API Features

- Implement versioning to support multiple app versions in the field.
- Add rate limiting to prevent API abuse.
- Include proper caching headers for mobile clients.
- **Bonus feature:** Implement a simple push notification system to alert users of new featured content.

#### Bonus Features

- Implement user authentication/authorization for personalized experiences.
- Persist request logs and user preferences using SQLite or another SQL server.
- Set up a local development and testing environment using Docker and docker-compose.

### Technical Recommendations

- **Required:** Typescript, NestJS, Node.js.
- You may use any supporting libraries, ideally ones that can highlight your skills.

### Advance Bonus Features

- **Push Notifications:** Implement a complete push notification system that works on both iOS and Android.
- **Offline Sync:** Create a robust data synchronization system for offline use.
- **Native Device Features:** Integrate device-specific features like camera, geolocation, or biometric authentication.
- **CI/CD Pipeline:** Set up a complete CI/CD pipeline for mobile app deployment.
- **App Store Package:** Prepare store-ready packages for both iOS and Android app stores.

## Evaluation Criteria

- **Code Quality:** Clarity, efficiency, and adherence to mobile development best practices.
- **UI/UX Design:** The application should be intuitive on mobile devices with proper touch interactions.
- **Cross-Platform Compatibility:** Must work effectively on both iOS and Android.
- **Mobile Performance:** Efficient battery usage, low memory footprint, and fast loading times.
- **Offline Capabilities:** Graceful handling of offline scenarios.
- **Unit Tests:** Coverage and effectiveness of unit tests for both frontend and backend.
- **Validation and Error Handling:** Properly handle and display errors in a mobile-friendly way.

## Scoring Mechanism

### Overview

The project will be scored over 300 total points, distributed across three main categories: Frontend (100 points), Backend (100 points), and Advanced Features (100 points). The average candidate is expected to score around 200 points, and we strongly encourage you to aim higher to demonstrate your exceptional skills.

### Breakdown

#### Frontend Mobile App (100 points)
- **Code Quality (20 points):** Code readability, efficiency, and structure.
- **UI/UX Design (15 points):** Mobile-specific design patterns, visual appeal, and user experience.
- **Functionality (20 points):** Fulfillment of the basic requirements.
- **Cross-Platform Compatibility (15 points):** Equal functionality on iOS and Android.
- **Performance & Offline Capabilities (10 points):** Battery efficiency, loading speed, offline behavior.
- **Unit Testing (10 points):** Coverage and effectiveness of tests.
- **Bonus Features (10 points total):** 
  - Bookmark favorite content (3 points)
  - Infinite scrolling (3 points)
  - Responsive layouts for different screen sizes (2 points)
  - Local storage persistence (2 points)

#### Backend API (100 points)
- **Code Quality (20 points):** Code readability, efficiency, and structure.
- **API Design (15 points):** RESTful principles, mobile-optimized endpoints.
- **Functionality (20 points):** Fulfillment of the basic requirements.
- **Security & Performance (15 points):** Rate limiting, proper authentication, response optimization.
- **Unit Testing (10 points):** Coverage and effectiveness of tests.
- **Documentation (10 points):** API documentation quality and completeness.
- **Bonus Features (10 points total):**
  - Push notification system (4 points)
  - User authentication/authorization (3 points)
  - Request logging and persistence (3 points)

#### Advanced Features (100 points)
- **Push Notifications System (25 points)**
- **Offline Sync Implementation (25 points)**
- **Native Device Features Integration (20 points)**
- **CI/CD Pipeline (15 points)**
- **App Store-Ready Packages (15 points)**

Projects achieving over 250 points will stand out from the average submission.

## Submission Instructions

- Upload the project to a public GitHub repository and share the URL by the due date specified in the email, please submit whatever you accomplished.
- Include a `README.md` with setup and running instructions, a project overview, and notes on libraries/frameworks used.
- Include screenshots or videos demonstrating the app running on both iOS and Android.
- Mention any assumptions or limitations in your implementation.
- Not submitting the project on time will immediately disqualify you as a candidate.
- Please do not introduce any commits after the submission time, these will not be taken into consideration.
- To avoid other candidates finding and using your work, **DO NOT: fork this repo, use this file content nor the name of the company in your readme.**

## Good Luck
