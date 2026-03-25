━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  ⚡ CIVICINSIGHT — SmartGov: Citizen-State Connectivity Redefined
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  The right action, at the right time — for every citizen.
  Our Intelligent Engine analyzes public grievances and eliminates
  the need to navigate bureaucratic loops.

  Live Demo   →  https://civic-insight.vercel.app
  Stack       →  Spring Boot  ·  MongoDB  ·  Llama 3.2 (Live AI)  ·  JWT
  Frontend    →  Vanilla HTML / CSS / JS  ·  No build step required


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  01  OVERVIEW
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  CivicInsight is a full-stack AI-powered grievance redressal portal where
  citizens can describe civic problems — electricity, water, roads, sanitation
  — in Hindi or English. The AI engine analyzes the complaint, automatically
  assigns the correct government department, sets an urgency level, and
  notifies the responsible officer.

  The Problem
  ───────────
  Millions of civic complaints in India either never reach the right
  department or sit unattended for hours. CivicInsight bridges this gap
  through intelligent routing, real-time tracking, and officer accountability.

  The Solution
  ────────────
  A unified portal powered by Llama 3.2 that handles routing, prioritization,
  and assignment — giving citizens transparency and giving officials clarity.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  02  KEY FEATURES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  🧭  Intelligent Routing       AI automatically determines whether a
                                complaint belongs to Jal Board, PWD, DISCOM,
                                or another department — correctly, the first
                                time, every time.

  🚨  Life-Saving Priority      Not all complaints are equal. Exposed wiring
                                or open sewers are instantly identified and
                                pushed to the Emergency Queue.

  📊  Political Intelligence    A real-time dashboard showing elected
                                representatives and officers the ground
                                reality of their ward — live data and
                                sentiment analysis included.

  🔐  JWT Authentication        Separate secure login flows for Citizens,
                                Officers, and Admins. Every API call is
                                protected with a Bearer token.

  🌐  Multi-lingual Support     Hindi and English both supported. The AI
                                engine picks up keywords from either language.

  📱  Responsive UI             Mobile-first dark interface. No build tools
                                required — runs directly in any browser.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  03  PROJECT STRUCTURE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  civic-insight/
  │
  ├── frontend/
  │   ├── index.html                  Public landing page
  │   ├── login.html                  Login (Citizen, Officer, Admin)
  │   ├── signup.html                 Registration page
  │   ├── complaint-portal.html       File a complaint + status check
  │   ├── officer-dashboard.html      Officer: fetch, analyze, reply
  │   └── admin-dashboard.html        Admin analytics panel
  │
  └── backend/                        Spring Boot Application
      ├── controllers/
      ├── services/
      ├── models/
      ├── security/
      └── SmartGovApplication.java


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  04  USER FLOW
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  index.html  (Landing Page)
        │
        ▼  Already logged in? → auto-redirect based on role
        │
        ▼  "File a Complaint" button
        │
  complaint-portal.html
    ├── Login / Register             POST /create/login/user
    ├── File Complaint               POST /user/complaint/submit
    └── Check Status                 POST /user/complaint/check/status?Id=

  login.html  (All Roles)
    ├── Citizen   ──→  complaint-portal.html
    ├── Officer   ──→  officer-dashboard.html
    └── Admin     ──→  admin-dashboard.html


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  05  GETTING STARTED
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  Prerequisites
  ─────────────
  · Java 17+
  · Maven 3.8+
  · MongoDB (local or Atlas)
  · Any modern browser

  Backend Setup
  ─────────────
  git clone https://github.com/your-username/civic-insight.git
  cd civic-insight

  # Configure src/main/resources/application.properties:
  spring.data.mongodb.uri = mongodb://localhost:27017/civicinsight
  jwt.secret              = your_secret_key_here

  mvn clean install
  mvn spring-boot:run

  # Backend will start at http://localhost:8080

  Frontend Setup
  ──────────────
  cd frontend/
  open index.html
  # Or use VS Code Live Server — no build step needed.

  NOTE: All frontend files contain  const BASE = 'http://localhost:8080'
        Update this to your production server URL before deploying.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  06  API ENDPOINTS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  All protected endpoints require:
  Authorization: Bearer <jwt_token>

  ── Citizen ───────────────────────────────────────────────────────────────

  POST  /create/signup/user
        Body: { name, username, email, password }

  POST  /create/login/user
        Body: { username, password }  →  returns plain JWT string

  ── Officer ───────────────────────────────────────────────────────────────

  POST  /create/department_user/signup
        Body: { name, username, email, password, department, city }

  POST  /create/department_user/login/officer
        Body: { username, password }  →  JWT

  ── Admin ─────────────────────────────────────────────────────────────────

  POST  /admin/signup/crateAdmin
        Body: { Name, username, email, password, city }
        Note: "Name" uses a capital N — matches the Admin entity field.

  POST  /admin/signup/login/admin
        Body: { username, password }  →  JWT

  ── Complaints  [Auth Required] ───────────────────────────────────────────

  POST  /user/complaint/submit
        Body: { Name, city, ward_number, complaint }
        Note: "Name" uses a capital N. AI analysis runs automatically.

  POST  /user/complaint/check/status?Id=
        Query param: Id

  ── Officer Analysis  [Auth Required] ─────────────────────────────────────

  POST  /department_officer/Analysis/fetch/complaint?Id=
        Query param: Id — returns full complaint details

  POST  /department_officer/Analysis/analysis/complaint?Id=&message=
        Query params: Id, message — submit official reply

  POST  /department_officer/Analysis/find/Officer?Id=
        Query param: Id — returns officer profile


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  07  DATA MODELS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  Complaints Entity
  ─────────────────
  {
    "Name"           : "Ramesh Kumar",           // capital N — required
    "city"           : "Lucknow",
    "ward_number"    : "Ward No. 12",
    "complaint"      : "Complaint text here...", // required

    // Auto-filled by AI and Backend:
    "urgency"        : "HIGH | MEDIUM | LOW",
    "status"         : "PENDING | IN_PROGRESS | RESOLVED",
    "departmentName" : "Nagar Nigam",
    "OfficerName"    : "Assigned Officer",
    "officerId"      : "...",
    "createdAt"      : "2025-01-01T00:00:00Z"
  }

  Frontend localStorage Keys
  ──────────────────────────
  jwt_token         Bearer token used in all protected API calls
  logged_role       "user" | "officer" | "admin"
  logged_username   Username of the logged-in user
  logged_dept       Officer's department (officer role only)


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  08  AI ENGINE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  Production uses Llama 3.2 for live complaint analysis and routing.

  When the backend is unavailable, the frontend falls back to a local
  keyword-based engine:

  Keywords                          Department               Urgency
  ───────────────────────────────  ──────────────────────  ──────────
  bijli, wire, electricity          Electricity / DISCOM     HIGH
  paani, water, jal, nalka          Jal Board                HIGH
  police, crime, theft              Local Police Station     HIGH
  sadak, road, pothole              PWD (Roads)              MEDIUM
  jaanwar, dog, stray animals       Animal Control           MEDIUM
  kachra, garbage, sanitation       Nagar Nigam              LOW


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  09  ROADMAP
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  [✓]  Citizen, Officer, Admin registration and login (JWT)
  [✓]  Llama 3.2 powered complaint routing and urgency detection
  [✓]  Real-time complaint status tracking
  [✓]  Officer dashboard — fetch, analyze, reply
  [✓]  Constituency Health and Sentiment Monitor for politicians
  [✓]  Responsive dark UI — no build tools needed
  [ ]  Admin dashboard (full analytics and officer management)
  [ ]  Push notifications for citizens on status updates
  [ ]  Ward-level heatmap for political dashboard
  [ ]  Mobile app (React Native)
  [ ]  Expanded regional language support (Tamil, Bengali, Marathi)


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  10  CONTRIBUTING
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  Pull requests are welcome. Open an issue for feature suggestions or
  bug reports.

  git checkout -b feature/your-feature-name
  git commit -m "Add your feature"
  git push origin feature/your-feature-name

  Then open a Pull Request on GitHub.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  LICENSE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  MIT License — see the LICENSE file for details.

  Made with ❤️  for Bharat 🇮🇳
  Every complaint deserves to be heard. That is the purpose of CivicInsight.
