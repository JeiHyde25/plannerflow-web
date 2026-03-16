
# 📅 PlannerFlow Web

![MIT License](https://img.shields.io/badge/License-MIT-yellow.svg)
![Next.js](https://img.shields.io/badge/Framework-Next.js-black)
![TypeScript](https://img.shields.io/badge/Language-TypeScript-blue)
![TailwindCSS](https://img.shields.io/badge/Style-TailwindCSS-38B2AC)

PlannerFlow Web is the frontend application for **PlannerFlow**, an AI‑powered productivity system that converts handwritten planner pages into structured digital schedules and calendar events.

The web app allows users to scan their planner, review AI‑extracted schedules, edit time blocks, and export their day into calendar systems.

---

# 📌 Project Overview

Many professionals prefer writing their daily plans in physical planners because it feels more natural and flexible. However, handwritten plans are disconnected from digital tools such as calendars, reminders, and productivity apps.

PlannerFlow bridges this gap.

Workflow:

Write planner → Scan planner → AI extraction → Review & edit → Export to calendar

This repository contains the **frontend application responsible for**:

- Planner scanning interface
- Schedule preview editor
- Timeline editing UI
- Planner history views
- Calendar export actions

---

# 📁 Project Structure

plannerflow-web/
├── app/
│   ├── page.tsx
│   ├── scan/
│   ├── preview/
│   └── history/
│
├── components/
│   ├── planner/
│   └── ui/
│
├── lib/
│   └── api.ts
│
├── public/
│
├── styles/
│
├── .gitignore
├── next.config.ts
├── package.json
├── tailwind.config.ts
├── tsconfig.json
└── README.md

---

# 🔧 Features

- 📷 Capture planner pages using the device camera
- 🧠 Send planner images to the PlannerFlow API for AI extraction
- 📅 Visual timeline editor for schedule blocks
- ✏️ Edit event titles, times, and tasks
- 🗂 Planner history view
- 📤 Export schedules to calendar files

---

# 🚀 Tech Stack

- **Next.js**
- **React**
- **TypeScript**
- **TailwindCSS**
- **PlannerFlow API (FastAPI backend)**

---

# 🛠️ Getting Started (Local)

## 1. Clone the repository

git clone https://github.com/JeiHyde25/plannerflow-web.git  
cd plannerflow-web

---

## 2. Install dependencies

npm install

---

## 3. Run the development server

npm run dev

Open:

http://localhost:3000

---

# 🔌 Backend Integration

The frontend communicates with the **PlannerFlow API**.

Default development endpoint:

http://localhost:8000

Example API flow:

POST /planner/extract  
→ send planner image  
→ receive structured planner JSON

---

# 🧪 Future Improvements

- Mobile‑optimized planner scanning
- Drag‑and‑drop schedule editing
- Real‑time calendar sync
- Planner analytics
- Offline PWA support

---

# 📄 License

This project is licensed under the MIT License.

---

# 👤 Author

Harold Tago  
GitHub: https://github.com/JeiHyde25
