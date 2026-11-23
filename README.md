# STUDYHUB – Your Complete Study Partner
> **All-in-One Student Learning & Academic Resource Platform**

STUDYHUB is a modern, professional, fully responsive educational web platform designed to provide students with all their study materials in one place. It eliminates fragmented links and paywalls, delivering verified notes, textbooks, previous year questions (PYQs), formula cheat sheets, video lectures, and practical files through a clean, high-performance interface.

---

## 🌟 Key Features

### 1. Modern Design & User Experience
- **Color Palette:** Deep Navy (`#0B0F19`), Royal Purple (`#7C3AED`), Indigo (`#4F46E5`), and Cyan accents.
- **Glassmorphism & Micro-animations:** Translucent frosted panels, subtle gradient borders, and smooth hover elevations.
- **Dark & Light Mode:** Instant theme toggle with persistent memory.
- **Fully Responsive:** Flawless layout across smartphones, tablets, laptops, and 4K displays.

### 2. Comprehensive 12-Category Study Material System
1. **PDF Notes:** High-yield typed notes curated by educators.
2. **Handwritten Notes:** Clean topper notes with annotated diagrams and step derivations.
3. **Textbooks:** Standard reference books and open e-textbook summaries.
4. **Previous Year Question Papers (PYQs):** 10-year chapterwise solved board and university papers.
5. **Sample Papers:** Official exam pattern mock papers with marking schemes.
6. **Assignments:** Solved university semester problem sheets.
7. **Practical Files:** Lab manuals, SQL scripts, and experimental records.
8. **Important Questions:** High-probability exam questions with step solutions.
9. **Revision Notes:** One-shot summaries and mind maps for last-minute prep.
10. **Formula Sheets:** Pocket cheat sheets for mathematics and physics formulas.
11. **Video Lectures:** Interactive chapter-wise tutorials with an embedded video player.
12. **Study Guides:** Complete syllabi roadmaps and preparation blueprints.

### 3. Integrated PDF Reader & Download Engine
- **In-Browser Reading:** Preview notes right inside the app with page zoom (70% - 160%), Light / Dark / Sepia reading themes, and curriculum chapter navigation.
- **Real PDF Downloads:** Generates and saves authentic `.pdf` documents using client-side `jsPDF` with document headers, verification stamps, and academic text.

### 4. Smart Search & Multi-Dimensional Filters
- Instant search across titles, subjects, degrees, and authors with `Ctrl+K` shortcut support.
- Multi-parameter filters:
  - By Category (12 types)
  - By Level / Board / Degree (Class 10-12, CBSE, ICSE, BCA, B.Tech, BBA, B.Sc, B.Com, JEE, NEET, UPSC, SSC)
  - By Subject (Computer Science, Physics, Chemistry, Mathematics, Biology, Management, Commerce)
  - By Sort Order (Most Popular, Highest Rated, Newest, Title A-Z)

### 5. Student Dashboard
- **Profile Overview:** Target exams, college affiliation, and enrolled branches.
- **Saved Materials (Bookmarks):** Quick-access favorites list with instant toggle.
- **Download History:** Timestamped archive of downloaded notes.
- **Daily Study Goals:** Interactive checklist to track daily study targets.
- **Personalized Recommendations:** Algorithmic resource suggestions based on the student's enrolled stream.

### 6. Admin Panel & Resource Management
- **Instant Upload Form:** Upload notes, past papers, and lab files with titles, categories, and syllabus breakdowns.
- **Live Publishing:** Uploaded resources automatically appear in relevant categories, search, and recently uploaded feeds.
- **Catalog Management:** Search, review, preview, and delete study materials.
- **User Feedback & Reviews:** View and approve student ratings and suggestions.

---

## 🛠️ Technology Stack

| Layer | Technologies |
|---|---|
| **Frontend UI** | HTML5, CSS3, Tailwind CSS, JavaScript (ES6+), Font Awesome 6 Icons |
| **PDF Generation** | jsPDF (with automatic multi-page formatting and fallback) |
| **Client Storage** | LocalStorage & IndexedDB resilient offline engine |
| **Backend API** | Node.js, Express.js, RESTful Architecture, CORS, Multer |
| **Database** | MongoDB & Mongoose Schema (with automatic offline fallback) |
| **Authentication** | JWT (JSON Web Tokens), bcryptjs password hashing, Google OAuth simulation |

---

## 🚀 Getting Started

### Option A: Run Directly in Any Browser (Zero Installation Needed)
The frontend contains a built-in state engine and seed database. Simply open `index.html` in your web browser:
1. Navigate to the project folder:
   `C:\Users\a\.gemini\antigravity\scratch\studyhub\`
2. Double-click `index.html` or open it with Google Chrome, Microsoft Edge, or Mozilla Firefox.
3. Every button, filter, PDF preview, PDF download, login, dashboard, and admin upload works immediately.

---

### Option B: Run Full-Stack with Node.js & Express

#### 1. Prerequisites
- [Node.js](https://nodejs.org/) (v16 or higher)
- Optional: Local MongoDB or [MongoDB Atlas Free Cluster](https://www.mongodb.com/cloud/atlas)

#### 2. Install Backend Dependencies
```bash
cd backend
npm install
```

#### 3. Configure Environment Variables
Copy `.env.example` to `.env`:
```bash
cp .env.example .env
```
Update your MongoDB URI in `.env`:
```env
PORT=5000
MONGODB_URI=mongodb+srv://<username>:<password>@cluster0.mongodb.net/studyhub?retryWrites=true&w=majority
JWT_SECRET=your_jwt_secret_key_here
```

#### 4. Start the Server
```bash
npm start
```
The server will boot on `http://localhost:5000`:
- **Health Check:** `http://localhost:5000/api/health`
- **Materials API:** `http://localhost:5000/api/materials`
- **Frontend App:** `http://localhost:5000/`

---

## 🔐 Demo Credentials

Quick 1-click login buttons are provided on the Sign In modal:

| Role | Email | Password | Access |
|---|---|---|---|
| **Student Demo** | `student@studyhub.edu` | `demo123` | Full student dashboard, bookmarks, goals, ratings |
| **Admin Demo** | `admin@studyhub.edu` | `admin123` | Upload resources, delete materials, manage feedback |

---

## 📁 Project Directory Structure

```
studyhub/
├── index.html                   # Core single-page application & responsive views
├── README.md                    # Documentation & setup instructions
├── assets/
│   ├── css/
│   │   └── style.css            # Custom animations, glassmorphism, dark/light theme variables
│   └── js/
│       ├── data.js              # Comprehensive academic seed catalog (40+ items across all classes)
│       ├── pdf-generator.js     # Client-side PDF generation & download engine using jsPDF
│       ├── api.js               # Dual-Mode API connector (Express REST API + LocalStorage fallback)
│       └── app.js               # Central controller for navigation, search, filters, modals & admin
└── backend/
    ├── package.json             # Node.js dependencies
    ├── server.js                # Express REST API server
    ├── .env.example             # Environment template for MongoDB & Firebase
    ├── models/
    │   ├── Material.js          # Mongoose schema for study materials
    │   ├── User.js              # Mongoose schema for students and admins
    │   └── Feedback.js          # Mongoose schema for user inquiries and reviews
    └── routes/
        ├── materials.js         # Endpoints for CRUD materials and filtering
        ├── auth.js              # Endpoints for registration and JWT login
        └── feedback.js          # Endpoints for contact and reviews
```

---

## ⚖️ Copyright & Legal Compliance
STUDYHUB is dedicated to open educational access. All sample study materials, revision summaries, and exam guides are legally compliant educational notes and open-access curricula compiled strictly for non-commercial student learning.
