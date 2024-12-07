# Image Storage and Sharing Application

Your reliable, self-hosted solution for effortless photo and video management.

## Mission

To provide a reliable and intuitive self-hosted platform for effortless photo and video management, ensuring privacy, accessibility, and ease for every user.

## Vision

To create a platform that empowers users to share their digital assets with ease, ensuring privacy, accessibility, and ease for every user.

## Features

- [x] Organizing Memories - **Simplified Photo and Video Management.** Easily manage your photos and videos in one place with a user-friendly interface designed for seamless organization.

- [x] Prioritizing Privacy - **Your Data, Your Control.** Keep your data safe with a self-hosted solution that ensures complete control over your photos and videos. No third-party access, no compromises—your privacy is always the priority.

- [x] Enhancing Accessibility - **Seamless Sharing Made Easy.** Share your favorite moments with friends, family, or colleagues effortlessly.

- [x] Solving Affordability - **Cost-Effective Self-Hosting.** Enjoy a powerful photo and video management platform without the hefty price tag. By leveraging self-hosting, you can save costs while still enjoying top-tier features and performance.

## Key Components  

### 1. Technologies Used  

- **Frontend**:  
  - **Next.js**: A React-based framework for server-side rendering, static site generation, and enhanced routing.  
  - **Tailwind CSS**: A utility-first CSS framework for building fast and responsive designs.  
  - **TypeScript**: Adds static typing to JavaScript for improved code quality and maintainability.  

- **Backend**:  
  - **Java 18**: The core programming language used for backend development.  
  - **Spring Boot**: A framework to simplify backend setup with built-in features like dependency injection, REST APIs, and web services.  

- **Database**:  
  - **PostgreSQL**: A robust and scalable relational database system used for storing images, metadata, and user information.  
  - **Docker**: Used for containerizing the PostgreSQL database to ensure consistent and isolated environments for development and deployment.  

---

### 2. Project Structure  

**Frontend**:  
The frontend is built with Next.js, and it's organized as follows:

- **components/**: Contains reusable UI components like icons, modals, and carousels.  
- **pages/**: Contains the pages of the application, including dynamic routes for viewing individual photos.  
- **public/**: Stores static assets like the favicon and Open Graph images.  
- **styles/**: Holds global CSS styles for the application.  
- **utils/**: Utility functions and custom hooks for handling image management, caching, and more.

**Backend**:  
The backend is powered by Spring Boot and is organized into the following key packages:

- **controller/**: Manages API requests and handles user interactions.  
- **service/**: Contains business logic for image handling and user management.  
- **repository/**: Interfaces with the PostgreSQL database for image and user data storage.  
- **model/**: Defines data structures for images, users, etc.

**Database**:  
The PostgreSQL database is containerized using Docker to ensure easy deployment and consistency across environments.

This simplified structure provides a clean separation of concerns and ensures scalability as the application grows.

---

### 3. API Endpoints  

**General Endpoints**  

| HTTP Method | Endpoint         | Description                              |  
|-------------|------------------|------------------------------------------|  
| **GET**     | `/api/images`     | List all image information.              |  

**Upload Image Endpoints**  

| HTTP Method | Endpoint         | Description                              |  
|-------------|------------------|------------------------------------------|  
| **POST**    | `/api/upload`     | Upload a single image.                   |  
| **POST**    | `/api/uploads`    | Upload multiple images.                  |  

**Preview Endpoints**  

| HTTP Method | Endpoint                          | Description                              |  
|-------------|-----------------------------------|------------------------------------------|  
| **GET**     | `/api/show?name=FILE_NAME`        | Preview image by file name (query param).|  
| **GET**     | `/api/show?uuid=FILE_UUID`        | Preview image by file UUID (query param).|  
| **GET**     | `/api/show/150/200?uuid=FILE_UUID`| Preview image with specific dimensions (150x200) by UUID. |  
| **GET**     | `/api/show/300/200?name=FILE_NAME`| Preview image with specific dimensions (300x200) by file name. |  
<!-- | **GET**     | `/api/show/200/400/FILE_NAME`     | Preview image with specific dimensions (200x400) by file name. |   -->
<!-- | **GET**     | `/api/view/FILE_NAME`             | Preview image by file name.              |   -->

Delete Endpoints (Work in Progress)

| HTTP Method | Endpoint         | Description                              |  
|-------------|------------------|------------------------------------------|  
| **DELETE**  | `/api/delete/FILE_NAME`     | Delete an image by file name.            |

Download Endpoints (Work in Progress)

| HTTP Method | Endpoint         | Description                              |  
|-------------|------------------|------------------------------------------|  
| **GET**     | `/api/download?uuid=FILE_UUID`     | Download an image by file name.          |
| **GET**     | `/api/archive`        | Download all images in a zip file.       |

### Roadmap

- [ ] **Video Player**: Integrate a video player into the platform, enabling users to preview and play their video files directly within the app.

- [ ] **Multi-Select Operations**: Enable multi-selection of images or videos, allowing users to perform bulk actions like deletion, downloading, or sharing on multiple assets at once.  

- [ ] **Prevent Asset Duplication**: Implement a feature to automatically detect and prevent the duplication of uploaded photos and videos, ensuring the storage remains organized and efficient.  

- [ ] **View EXIF Data**: Provide users with the ability to view EXIF (Exchangeable Image File Format) data, giving them metadata about their photos such as camera settings and location.  

- [ ] **Admin Dashboard**: Develop a web-based admin portal that allows administrators to manage users, settings, and overall system configurations seamlessly.  

- [ ] **Album Sharing**: Introduce the ability for users to share entire albums with others, enabling collaboration and easy sharing of collections.  

- [ ] **Image Tagging**: Allow users to tag images with custom labels or keywords, improving the searchability and organization of their assets.  

### Best Practices

- **Code Documentation**: Ensure that all components, including frontend and backend code, are thoroughly documented to provide clarity on functionality and ease of future development.  
- **Error Handling**: Implement robust error handling across both the frontend and backend to manage unexpected issues and provide a seamless user experience.  
- **Security Practices**: Prioritize secure authentication and authorization mechanisms, ensuring that all user data, especially sensitive media, is protected.  
- **Responsive Design**: Ensure the frontend is responsive and optimized for various devices, enhancing accessibility for users across different platforms.  
- **Performance Optimization**: Optimize database queries and frontend rendering to ensure fast loading times, even with large media libraries.  
- **Unit and Integration Testing**: Maintain a high level of testing coverage, including unit tests for backend services and integration tests for full-stack functionality, to guarantee application stability.
