Architectural Decision Record (ADR)

Title: Mobile App Architecture for a Retail Company

Status: Proposed

Context: We are building a mobile app for a retail company with several requirements, including offline support, push notifications, payment gateway integration, analytics, image storage and optimization, and internationalization.

Decision 1: Native, Web, or Hybrid App

Decision: Native App
Rationale: Native apps can more easily support offline functionality and tend to provide a smoother user experience with more seamless integration with device features like push notifications.
Decision 2: UI Framework

Decision: React Native
Rationale: React Native allows for development across multiple platforms (iOS and Android) using a single codebase. Additionally, it has a robust ecosystem and numerous libraries for various functionalities, including offline support and internationalization.
Decision 3: Backend Language

Decision: Node.js with Express.js framework
Rationale: Node.js is performant and works well for building scalable APIs. Express.js provides a minimal and flexible layer to build web applications, making it easier to integrate with various payment gateways and push notification services.
Decision 4: Permissions

Decision: Request essential permissions:
Internet Access (for syncing and fetching data)
Push Notifications (to notify users)
Storage (for offline support)
Rationale: Requesting only essential permissions ensures user trust and adherence to the principle of least privilege.
Decision 5: Data Storage

Decision: SQLite for local offline storage and PostgreSQL for server-side storage.
Rationale: SQLite is lightweight and suitable for local storage on mobile devices, ensuring offline capabilities. PostgreSQL is robust and scalable for server-side storage.
Decision 6: Push Notification Service

Decision: Firebase Cloud Messaging (FCM)
Rationale: FCM provides a reliable, efficient connection solution between the server and devices allowing for timely delivery of notifications.
Decision 7: Payment Gateways

Decision: Stripe and PayPal
Rationale: Both are globally recognized, secure, and offer wide compatibility. This dual approach caters to different customer preferences.
Decision 8: Analytics Tool

Decision: Google Analytics for Firebase
Rationale: Provides detailed insights into app usage and integrates well with React Native.
Decision 9: Image Storage and Optimization

Decision: Cloudinary for image storage, with implementation of lazy loading and compression techniques.
Rationale: Cloudinary automatically optimizes images for different devices and resolutions. Implementing lazy loading ensures faster page loads, while compression reduces data costs.
Decision 10: Localization

Decision: Use React Native's internationalization (i18n) libraries, and maintain multiple language packs as JSON files.
Rationale: This approach supports seamless addition of new languages in the future and caters to various cultural preferences.

Consequences:
Opting for React Native means developers skilled in both iOS and Android native development might not be fully utilized. However, the shared codebase will likely reduce development time and ensure consistency across platforms. 
Choosing SQLite and PostgreSQL mandates regular data syncing logic to ensure data consistency. Using Cloudinary incurs costs based on usage, but offers a hassle-free image management solution. 
The chosen analytics and push notification solutions might introduce additional costs, but are essential for the app's success and user engagement.

Link to Github https://github.com/Jlat21/ADR-Assignment/blob/main/index.md
