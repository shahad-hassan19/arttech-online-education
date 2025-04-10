# 🎓 ArtTech Online Education – Learning Management System (LMS)

*Live Demo:* [https://online.arttechbsp.com/](https://online.arttechbsp.com/)  
*Deployed on:* Vercel  
*Stack:* Next.js (TypeScript), Tailwind CSS, MongoDB, Prisma, Clerk, UploadThing, Mux, PhonePe

---

## 🧠 Overview

**ArtTech Online Education** is an online learning platform built to offer industry-relevant courses in **Excel**, **Power BI**, and **Tally Prime**. It supports features like video-based lessons, chapter progress tracking, learner dashboards, role-based admin controls, and automatic certificate generation.

---

## 👥 Target Audience

It’s designed to be user-friendly and accessible to **anyone** interested in learning Excel, Power BI, or Tally Prime — whether they're students, beginners, or working professionals.

The platform is designed for:
- *Students*
- *Working professionals*
- *Beginners*

There is *no age restriction, and both **learners and administrators* are supported within the system.

---


## 🧩 Key Features

ArtTech Institute offers a range of essential features to ensure a seamless and efficient learning experience:

- **User Roles**: 
  - **Admin**: Full access to manage users, courses, and site settings.
  - **Learner**: Access to courses, progress tracking, and certifications.

- **Course & Chapter Creation**: 
  - Admins can create and manage courses with various content types, including videos, text, and downloadable files.
  - Chapters can be added within each course to organize learning materials effectively.

- **Enrollments & Purchases**: 
  - Learners can enroll in courses and make payments via **PhonePe** to unlock content.
  
- **Progress Tracking**: 
  - Learners have a dashboard to track their progress in each course, including completed lessons and pending tasks.

- **Certification**: 
  - Learners receive certificates upon successful completion of courses, enhancing their credentials.

- **Role-Based Dashboards**: 
  - **Admin Dashboard**: Manage all aspects of the platform, including users, courses, and payments.
  - **Learner Dashboard**: View enrolled courses, progress, and certificates.

---

### 🧱 Tech Stack Overview

ArtTech Institute leverages a modern and efficient tech stack to deliver a seamless learning experience:

- **Frontend**: Next.js (TypeScript), styled with Tailwind CSS for responsive and clean UI.
- **Backend**: Next.js API routes with TypeScript for full-stack integration.
- **Database**: MongoDB for flexible and scalable data storage.
- **ORM**: Prisma, ensuring type-safe and efficient database queries.
- **Authentication**: Clerk, offering secure and smooth user auth and session handling.
- **File Uploads & Storage**: UploadThing, used for handling course materials and related assets.
- **Video Handling**: Mux, enabling reliable and high-quality video streaming.
- **Payments**: PhonePe integration to manage course purchases and transactions.

---

## 🔐 Role-Based Access Control

Access is managed by identifying admin user IDs stored in .env and validating them via a utility function:
```javascript
export const isAdmin = (userId?: string | null): boolean => {
  if (!userId) return false;
  return [
    process.env.NEXT_PUBLIC_ADMIN_ID
  ].includes(userId);
};
```

Admin-only features (like course creation) are gated both at the UI level and route level.

---

### 🎯 Routing & Navigation

ArtTech Institute uses **Next.js’s built-in file-based routing system** to manage seamless navigation across the platform. Dynamic routes are utilized for pages like course details, chapter views, and user-specific dashboards. Routing is also protected and role-aware, ensuring that only authorized users can access certain pages (e.g., Admin dashboard vs Learner dashboard).

---

### 💻 Responsive & User-Friendly UI

ArtTech Institute's interface is built with **Tailwind CSS**, ensuring a fully responsive and mobile-friendly experience across all devices. The design follows a **mobile-first approach**, with utility classes used extensively to adapt layouts and components to different screen sizes. Special attention was given to keeping the UI clean, intuitive, and accessible for both admins and learners.

---

### 📦 Course Content Management

- **Admins** are responsible for creating and uploading all course content, including **videos, text lessons, and downloadable files**.
- Each **course is made up of modular chapters**, allowing admins to:
  - Add multiple chapters as structured learning units
  - Edit, rearrange, or delete chapters as needed
  - Provide a step-by-step learning path for learners
- **Storage**:
  - **Videos** are hosted on **Mux** for smooth streaming.
  - **Files and assets** are handled via **UploadThing** for secure and efficient uploads.
- Courses and their chapters can be **updated anytime**, keeping the content fresh and relevant.
  
---

### 📄 Certificate Generation

ArtTech Institute provides **auto-generated certificates** upon successful completion of a course. Each certificate includes:

- The **learner’s name**
- The **course title**
- The **completion date**

Certificates are generated using a **pre-designed template**, with JavaScript dynamically injecting the relevant learner and course data. This ensures every learner receives a **personalized, professional-looking certificate** that they can download and share.

---

## 🚀 Deployment

ArtTech Institute is deployed on *Vercel* with production optimizations for performance and stability.  
🔗 *Live URL:* [https://online.arttechbsp.com/](https://online.arttechbsp.com/)

---

### 🛠️ Challenges Faced

Building a full-fledged LMS like ArtTech Institute came with its share of challenges:

- **Payment Gateway Integration**:  
  Implementing **PhonePe** for payments was particularly challenging due to the **lack of experience**. It required significant trial and error to get the system fully functional and secure.

- **Video Streaming & Publishing**:  
  Setting up **Mux** for video handling was also complex. Challenges included:
  - Handling upload states and processing delays
  - Managing playback reliably across devices
  - Ensuring videos were properly linked and secured within course chapters

Overcoming these challenges strengthened the technical robustness of the platform and significantly enhanced the learning experience.

---

### 💡 Lessons Learned

Developing ArtTech Institute was a major learning experience. Key takeaways include:

- **Full-Stack Development**: Gained hands-on experience with a modern tech stack including **Next.js with TypeScript**, **MongoDB**, and **Prisma ORM**.
- **Third-Party Integrations**: Learned to work with powerful yet complex tools like:
  - **Mux** for scalable video streaming
  - **PhonePe** for payments
  - **Clerk** for authentication and session handling
- **Project Architecture**: Improved skills in project structuring, separating concerns, and building maintainable codebases.
- **Role-Based Access Control**: Built and enforced admin-specific capabilities throughout the app.
- **Problem Solving & Debugging**: Tackled real-world issues such as asynchronous media handling, payment flow validation, and file uploads.

---

### 🎯 Future Plans

While no concrete roadmap is defined yet, the project remains open for future improvements based on user feedback and evolving needs. Potential areas for expansion include:

- Interactive features like **quizzes or community forums**
- More **payment options**
- **Mobile app** adaptation for broader accessibility

---

Thank you!
**Shahad Hassan** 
Full Stack Developer
*Softles*


