# SocialEcho
Table of Contents
Project Overview
Features
Technologies
Schema Diagram
Getting Started
Usage
License
Project Overview
The project is a social networking platform built using the MERN (MongoDB, Express.js, React.js, Node.js) stack. It incorporates two major features: an automated content moderation system and context-based authentication. These features are accompanied by common functionalities found in social media applications, such as profile creation, post creation and sharing, liking and commenting on posts, and following/unfollowing users.

Automated Content Moderation
The platform's automated content moderation system utilizes various NLP (Natural Language Processing) APIs. These APIs include:

Perspective API: Used for filtering spam, profanity, toxicity, harassment etc.
TextRazor API: Integrated for content categorization.
Hugging Face Interface API: Utilized with BART Large MNLI for content categorization.
A Flask application has been developed to provide similar functionality as the Hugging Face Interface API's classifier. The Flask app utilizes the BART Large MNLI model. It operates as a zero-shot classification pipeline with a PyTorch framework.

The system allows flexibility in choosing different services for API usage or disabling them without affecting overall functionality by using a common interface for interacting with the APIs.

When a user posts content, it undergoes a thorough filtering process to ensure compliance with the community guidelines. Additionally, users have the ability to report posts that they find inappropriate, which triggers a manual review process.

Context-Based Authentication
The platform implements context-based authentication to enhance user account security. It takes into consideration user location, IP address, and device information for authentication purposes. Users can conveniently manage their devices directly from the platform. To ensure data privacy, this information is encrypted using the AES algorithm and securely stored in the database.

In case of a suspicious login attempt, users are promptly notified via email and are required to confirm their identity to protect against unauthorized access.

User Roles
There are three distinct user roles within the system:

Admin: The admin role manages the overall system, including moderator management, community management, content moderation, monitoring user activity, and more.
Moderators: Moderators manage communities, manually review reported posts, and perform other moderation-related tasks.
General Users: General users have the ability to make posts, like comments, and perform other actions within the platform.
Features
 User authentication and authorization (JWT)
 User profile creation and management
 Post creation and management
 Commenting on posts
 Liking posts and comments
 Following/unfollowing users
 Reporting posts
 Content moderation
 Context-based authentication
 Device management
 Admin dashboard
 Moderator dashboard
 Email notifications
Technologies
React.js
Redux
Node.js
Express.js
MongoDB
Tailwind CSS
JWT Authentication
Passport.js
Nodemailer
Crypto-js
Azure Blob Storage
Flask
Hugging Face Transformers
