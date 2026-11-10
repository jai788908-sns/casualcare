# CasualCare™ - Continuous Remote Healthcare Platform

A comprehensive, production-ready healthcare application featuring bilingual (Tamil & English) remote patient monitoring, doctor tele-consultations, AI Care triage, automated SMS & WhatsApp multi-tier escalation, and real-time GPS emergency SOS ambulance dispatch.

---

## 🚀 Key Modules & Features Implemented

1. **Patient Dashboard (`src/components/Dashboard.jsx`)**
   - Live telemetry vitals (Heart rate, Blood Pressure, Blood Sugar, SpO2, Temperature).
   - "I Am OK" one-click check-in.
   - Quick medicine adherence progress & emergency status banner.

2. **Doctor Portal (`src/components/DoctorPortal.jsx`)**
   - Attending physician profile switcher (Cardiology, Endocrinology, Geriatrics).
   - Real-time patient telemetry monitoring and interactive clinical directive notes.
   - Medication adherence review table and direct caregiver contact links.

3. **AI Care Assistant (`src/components/AIAssistant.jsx`)**
   - Hybrid **English & Tamil (தமிழ்)** clinical prompt and symptom checking.
   - Smart triage: detects critical warning symptoms (chest pain, shortness of breath) and triggers immediate emergency recommendations.

4. **Medicine Tracker (`src/components/MedicineTracker.jsx`)**
   - Real-time dose completion toggle with progress percentage.
   - Refill alerts countdown and custom medicine addition modal.

5. **Recovery Tracker (`src/components/RecoveryTracker.jsx`)**
   - Step-by-step post-surgical rehabilitation milestones with dates and status.
   - Interactive daily self-assessment (mood, pain index 0–10, and notes) synced to clinical feed.

6. **Family Care Circle (`src/components/FamilyCircle.jsx`)**
   - Designated family guardians with emergency authorization badges.
   - 1-click test ping and telephone calling for primary caregivers.

7. **Digital Health Records (`src/components/MedicalRecords.jsx`)**
   - Category filters (Discharge & Surgery, Laboratory, Diagnostics, Ophthalmology).
   - Real-time search, interactive record preview modal, and PDF upload modal.

8. **Automated Check-up Reminders & Escalation (`src/components/CheckupReminders.jsx`)**
   - Multi-channel scheduled reminders (SMS & WhatsApp).
   - **No-Response 3-Tier Escalation Ladder Simulator**:
     - *Level 0*: Normal Acknowledged
     - *Level 1*: First reminder SMS/WhatsApp dispatched
     - *Level 2*: 45-minute timeout alerts primary family circle
     - *Level 3*: Paramedics and ACLS emergency services triggered
   - Live simulated terminal log showing real-time gateway dispatches.

9. **GPS-Based Emergency SOS & Ambulance Assistance (`src/components/EmergencySOS.jsx`)**
   - High-precision GPS satellite telemetry view (Anna Nagar, Chennai coordinates).
   - ACLS Ambulance unit tracking (`TN-01-AMB-8420`), dynamic ETA countdown, and driver calling.
   - Nearest hospital ICU availability and instant panic button.

10. **Tamil-English Language Switcher (`Navbar.jsx` & `mockData.js`)**
    - Seamless 1-click language switcher with dual-language dictionary.

---

## 📁 Project Architecture

```
CasualCare/
├── backend/
│   ├── package.json
│   └── server.js               # Express REST API for vitals, medications, escalation, and SOS
├── frontend/
│   ├── package.json
│   ├── vite.config.js          # Vite with Tailwind v4 plugin
│   ├── src/
│   │   ├── main.jsx
│   │   ├── App.jsx             # Main application container & state management
│   │   ├── index.css           # Tailwind CSS directives
│   │   ├── data/
│   │   │   └── mockData.js     # Full bilingual dataset, patient records, doctors, milestones
│   │   └── components/
│   │       ├── Navbar.jsx
│   │       ├── Dashboard.jsx
│   │       ├── DoctorPortal.jsx
│   │       ├── AIAssistant.jsx
│   │       ├── MedicineTracker.jsx
│   │       ├── RecoveryTracker.jsx
│   │       ├── FamilyCircle.jsx
│   │       ├── MedicalRecords.jsx
│   │       ├── CheckupReminders.jsx
│   │       └── EmergencySOS.jsx
```

---

## 💻 How to Run the Platform

### Frontend Development Server:
```bash
cd frontend
npm run dev
```

### Backend API Server:
```bash
cd backend
npm start
```
The backend API starts on port `5000` with endpoints for `/api/patient`, `/api/medicines`, `/api/escalation/trigger`, and `/api/emergency/sos`.
