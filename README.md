# fiverrC

# Game Audio Outsourcing Platform

## Platform Introduction

This is a professional game audio(test level for now) outsourcing platform, primarily for game audio composition, sound effect design, and voice-over (in Chinese, English, and other languages). The goal of the platform is to connect game companies with audio professionals, providing an efficient environment for transactions and collaboration. The simple framework currently mimics Fiverr, and the main tech stack includes React and SCSS.

### Key Features
- **Modular Frontend**: Implemented using React and SCSS.
- **Showcase**:
  - Display of supplier works
  - Display of client needs
  - Search services (for both clients and suppliers)
  - Activity pages (collections)
- **Personal Pages**:
  - Post requirements (for both clients and suppliers)
  - Order page
  - Message page
- **Admin Panel**:
  - Review (AI + Manual)
  - Registration review (mandatory for suppliers, optional for clients)
  - Post review
- **Payment Integration**: Integrated with Stripe, supporting milestone payments.
- **Bilingual Support**: Support for English and Chinese switching.
- **AI Generation Features**: Generate images, text, etc., with source model attribution (potential collaboration with other AI teams).

## Deployment Instructions

### Local Environment Setup

1. **Install Dependencies**:
   - Run the following command in both `api` and `client` directories:
     ```bash
     yarn
     ```

2. **Configure Environment Variables**:
   - Create a `.env` file in the project root directory and add the following content:
     ```env
     MONGO=mongodb+srv://<your-mongo-username>:<your-mongo-password>@clusterfiverr.2hvwxpm.mongodb.net/?retryWrites=true&w=majority&appName=ClusterFiverr
     JWT_KEY=thisisasupersecretkey
     ```

3. **Configure MongoDB**:
   - Ensure the MongoDB connection URL is correct and points to your MongoDB cluster.

4. **Configure Cloudinary**:
   - Replace `https://api.cloudinary.com/v1_1/dkxsnqvqx/image/upload` in `utils/upload.js` with your Cloudinary user.
   - Create a new folder and set the Upload presets to unsigned.

### Running the Project

1. **Start Backend Server**:
   - Navigate to the `api` folder and run:
     ```bash
     npm run dev
     ```

2. **Start Frontend Server**:
   - Navigate to the `client` folder and run:
     ```bash
     npm run dev
     ```

## Changelog

### Sprint 1
- Confirmed tech stack (Next.js, React, Node.js, MongoDB, TailwindCSS, Stripe, NextAuth).
- Completed basic UI design.
- Set up development environments for both frontend and backend.

### Sprint 2
- **Modular Frontend**: Implemented using React and SCSS.
- **Showcase**:
  - Supplier service/work display using test data.
  - Detailed page access using test data.
  - Implemented messaging and rating on detailed pages.
  - Partially implemented client needs display.
  - Partially completed search functionality (keywords, price range, type).
- **Personal Pages**:
  - Completed supplier posting page, allowing users to post new services.
  - Partially completed Order page functionality, needs integration with payment system.
- **Registration**: Completed registration, allowing users to choose client or supplier role, using Cloudinary for test data storage.
- **Payment Integration**: Expected to be completed in Sprint 3.
- **Message Page**: Expected to be completed in Sprint 3.
- **Bilingual Support**: Expected to be completed in Sprint 4.

> Note: Payment and Order binding are not yet completed, hence Order page functionality is not fully implemented. The Message feature has bugs and is not yet functional.

## What to Do Next

- Fix various bugs and add testing to improve functionality.
- Use a React UI library such as Shadcn/UI to enhance the UI design and improve the overall aesthetics.
- Continue to develop and refine features based on user feedback and testing results.
- Integrate more comprehensive and automated testing to ensure the stability and reliability of the platform.