# 🎓 ArtTech Institute – Learning Management System (LMS)

*Live Demo:* [https://online.arttechbsp.com/](https://online.arttechbsp.com/)  
*Deployed on:* Vercel  
*Stack:* Next.js (TypeScript), Tailwind CSS, MongoDB, Prisma, Clerk, UploadThing, Mux, PhonePe

---

## 🧠 Overview

*ArtTech Institute* is an online learning platform built to offer industry-relevant courses in *Excel, **Power BI, and **Tally Prime*. It supports features like video-based lessons, chapter progress tracking, learner dashboards, role-based admin controls, and automatic certificate generation.

---

## 👥 Target Audience

The platform is designed for:
- *Students*
- *Working professionals*
- *Beginners*

There is *no age restriction, and both **learners and administrators* are supported within the system.

---

## 🧩 Key Features

- 🔐 Role-based access (Admin & Learner)
- 📚 Course & chapter creation with support for videos, text, and downloadable files
- 🛒 Enrollments and payment-based course purchases
- 📈 Learner progress tracking
- 🧾 Auto-generated certificates on course completion
- 📊 Dedicated dashboards for both learners and admins

---

## ⚙ Tech Stack

| Layer            | Tools/Tech Used              |
|------------------|------------------------------|
| *Frontend*     | Next.js with TypeScript      |
| *Styling*      | Tailwind CSS                 |
| *Backend*      | Next.js API routes (server-side logic) |
| *Database*     | MongoDB                      |
| *ORM*          | Prisma                       |
| *Authentication* | Clerk                    |
| *File Uploads* | UploadThing                  |
| *Video Hosting*| Mux                          |
| *Payments*     | PhonePe                      |

---

## 🔐 Role-Based Access Control

Access is managed by identifying admin user IDs stored in .env and validating them via a utility function:

ts
export const isTeacher = (userId?: string | null): boolean => {
  if (!userId) return false;
  return [
    process.env.NEXT_PUBLIC_TEACHER_ID_1,
    process.env.NEXT_PUBLIC_TEACHER_ID_2,
  ].includes(userId);
};


Admin-only features (like course creation) are gated both at the UI level and route level.

---

## 💻 Responsive Design

Using *Tailwind CSS, the UI is built with a **mobile-first approach*. All layouts and components adapt seamlessly to various screen sizes, ensuring accessibility across smartphones, tablets, and desktops.

---

## 📦 Course Content Management

- Admins can *create and update* courses at any time.
- Each course includes *modular chapters*, allowing:
  - Multiple lessons per course
  - Editing, reordering, or deleting chapters
- *Content Storage*:
  - Videos → *Mux*
  - Files → *UploadThing*

---

## 🧾 Certificate Generation

Upon course completion, learners receive a downloadable certificate that includes:

- Learner's name
- Course title
- Completion date

Certificates are *auto-generated* using a *pre-designed template*, with JavaScript injecting dynamic data.

---

## 🚀 Deployment

ArtTech Institute is deployed on *Vercel* with production optimizations for performance and stability.  
🔗 *Live URL:* [https://online.arttechbsp.com/](https://online.arttechbsp.com/)

---

## 🛠 Challenges Faced

1. *Payment Integration with PhonePe*:  
   Due to limited online documentation and examples, integration was difficult and required significant research and experimentation.

2. *Video Streaming with Mux*:  
   Setting up reliable video upload and playback was complex, involving asynchronous video processing and linking Mux assets correctly.

---

## 💡 Lessons Learned

- Deepened understanding of *full-stack web development* using modern tools
- Practical experience with *Mux, Clerk, PhonePe, and Prisma*
- Learned effective *project structuring*, admin role implementation, and large-scale state handling
- Overcame challenges related to *media, payments, and access control*

---

## 🎯 Future Plans

No fixed roadmap yet, but potential future upgrades include:

- Interactive *quizzes* and *forums*
- More *payment gateways*
- A *mobile application* for learners
