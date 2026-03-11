━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  ⚡ SMART-GOV — AI-Powered Citizen Grievance Redressal System
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  Aam nagrik apni pareshani seedha sahi vibhag tak pahuncha sake —
  bina kisi chakkar ke, bina kisi sifaarish ke.

  Stack  →  Spring Boot  ·  MongoDB  ·  JWT Auth  ·  Vanilla JS
  Live Demo  →  [your-link-here]


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  01  OVERVIEW
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  Smart-Gov ek full-stack AI-powered portal hai jahan nagrik apni civic
  problems — bijli, paani, sadak, kachra — Hindi ya English mein likh sakte
  hain. Backend ka AI engine complaint analyze karke automatically sahi
  department assign karta hai, urgency set karta hai, aur officer ko notify
  karta hai.

  Problem  →  India mein lakho civic complaints sahi jagah nahi pahunchti ya
              ghanton tak unattended rehti hain. Smart-Gov is gap ko bridge
              karta hai — intelligent routing, real-time tracking, aur officer
              accountability ke saath.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  02  KEY FEATURES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  🤖  AI Routing          Complaint text se department, urgency aur action
                          auto-detect — Hindi ya English dono mein.

  🔐  JWT Auth            Citizen, Officer aur Admin — teeno ke liye alag
                          secure login. Har API Bearer token se protect hai.

  🏛  Officer Dashboard   Complaints fetch, official reply submit, aur
                          officer profile dekh sakte hain.

  🔍  Live Tracking       Citizen Complaint ID se kabhi bhi status check
                          kar sakta hai.

  🌐  Bilingual Support   Hindi aur English dono supported. AI dono languages
                          se keywords pick karta hai.

  📱  Responsive UI       Mobile-first dark UI. Koi build step nahi —
                          seedha browser mein chalega.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  03  PROJECT STRUCTURE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  smart-gov/
  │
  ├── frontend/
  │   ├── smart-gov-portal.html       Public landing page
  │   ├── login.html                  Login / Register (User, Officer, Admin)
  │   ├── complaint-portal.html       User: Login + Complaint on same page
  │   ├── officer-dashboard.html      Officer: Fetch, Analyze, Profile
  │   └── admin-dashboard.html        Admin panel (coming soon)
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

  smart-gov-portal.html
        │
        ▼  (JWT already saved? → auto redirect)
        │
        ▼  "Shikayat Darj Karein" button
        │
  complaint-portal.html
    ├── 🔐 Login / Register       POST /create/login/user
    ├── 📝 File Complaint         POST /user/complaint/submit
    └── 🔍 Status Check           POST /user/complaint/check/status?Id=

  login.html  (all 3 roles)
    ├── 👤 User     ──→  complaint-portal.html
    ├── 🏛 Officer  ──→  officer-dashboard.html
    └── ⚙  Admin   ──→  admin-dashboard.html


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  05  GETTING STARTED
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  Prerequisites
  ─────────────
  · Java 17+
  · Maven 3.8+
  · MongoDB (local ya Atlas)
  · Koi bhi modern browser

  Backend Setup
  ─────────────
  git clone https://github.com/your-username/smart-gov.git
  cd smart-gov

  # src/main/resources/application.properties mein ye daalo:
  spring.data.mongodb.uri = mongodb://localhost:27017/smartgov
  jwt.secret              = your_secret_key_here

  mvn clean install
  mvn spring-boot:run

  # Backend http://localhost:8080 pe start hoga.

  Frontend Setup
  ──────────────
  cd frontend/
  open smart-gov-portal.html
  # Ya VS Code Live Server use karo — koi build nahi chahiye.

  NOTE: Sabhi frontend files mein  const BASE = 'http://localhost:8080'  hai.
        Production deploy karte waqt apna server URL yahan update karo.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  06  API ENDPOINTS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  Auth header (sabhi protected endpoints pe zaroori):
  Authorization: Bearer <jwt_token>

  ── User ──────────────────────────────────────────────────────────────────

  POST  /create/signup/user
        Body: { name, username, email, password }
        Register karo.

  POST  /create/login/user
        Body: { username, password }
        Login karo → plain JWT string milega.

  ── Officer ───────────────────────────────────────────────────────────────

  POST  /create/department_user/signup
        Body: { name, username, email, password, department, city }

  POST  /create/department_user/login/officer
        Body: { username, password }  →  JWT

  ── Admin ─────────────────────────────────────────────────────────────────

  POST  /admin/signup/crateAdmin
        Body: { Name, username, email, password, city }
        Note: "Name" capital N hai — Admin entity ka field.

  POST  /admin/signup/login/admin
        Body: { username, password }  →  JWT

  ── Complaints  [Auth Required] ───────────────────────────────────────────

  POST  /user/complaint/submit
        Body: { Name, city, ward_number, complaint }
        Note: "Name" capital N. AI analysis automatic hogi.

  POST  /user/complaint/check/status?Id=
        Query param: Id
        Complaint ka live status milega.

  ── Officer Analysis  [Auth Required] ─────────────────────────────────────

  POST  /department_officer/Analysis/fetch/complaint?Id=
        Query param: Id
        Complaint ki poori detail fetch karo.

  POST  /department_officer/Analysis/analysis/complaint?Id=&message=
        Query params: Id, message
        Official reply aur analysis submit karo.

  POST  /department_officer/Analysis/find/Officer?Id=
        Query param: Id
        Officer ka profile aur details fetch karo.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  07  DATA MODELS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  Complaints Entity
  ─────────────────
  {
    "Name"           : "Ramesh Kumar",        // capital N — required
    "city"           : "Lucknow",
    "ward_number"    : "Ward No. 12",
    "complaint"      : "Pareshani ka text...", // required

    // Auto-filled by AI & Backend:
    "urgency"        : "HIGH | MEDIUM | LOW",
    "status"         : "PENDING | IN_PROGRESS | RESOLVED",
    "departmentName" : "Nagar Nigam",
    "OfficerName"    : "Assigned Officer",
    "officerId"      : "...",
    "createdAt"      : "2025-01-01T00:00:00Z"
  }

  localStorage Keys  (frontend)
  ──────────────────────────────
  jwt_token         Bearer token — sabhi API calls mein use hota hai
  logged_role       "user" | "officer" | "admin"
  logged_username   Logged-in user ka username
  logged_dept       Officer ka department (officer only)


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  08  AI DEMO MODE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  Jab backend available nahi hota, frontend keyword-based AI se complaint
  analyze karta hai:

  Keywords                          Department               Urgency
  ────────────────────────────────  ───────────────────────  ──────────
  bijli, wire, electricity          Electricity / DISCOM     HIGH
  paani, water, jal, nalka          Jal Board                HIGH
  police, crime, theft, chori       Local Police Station     HIGH
  sadak, road, pothole, gaddha      PWD (Roads)              MEDIUM
  jaanwar, dog, kutte, saanp        Animal Control           MEDIUM
  kachra, garbage, safai, waste     Nagar Nigam              LOW


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  09  ROADMAP
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  [✓]  User / Officer / Admin registration & login (JWT)
  [✓]  AI-based complaint routing & urgency detection
  [✓]  Real-time complaint status tracking
  [✓]  Officer dashboard — fetch, analyze, reply
  [✓]  Responsive dark UI (no build tools needed)
  [ ]  Admin dashboard (analytics + officer management)
  [ ]  Push notifications for citizens
  [ ]  Politician analytics panel (ward-wise heatmap)
  [ ]  Mobile app (React Native)
  [ ]  Regional language support (Bhojpuri, Maithili, Tamil)


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  10  CONTRIBUTING
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  Pull requests welcome hain. Naya feature ya bug report ke liye issue kholo.

  git checkout -b feature/AmazingFeature
  git commit -m "Add some AmazingFeature"
  git push origin feature/AmazingFeature

  Phir GitHub pe Pull Request submit karo.


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  LICENSE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  MIT License — details ke liye LICENSE file dekhein.

  Made with ❤️  for Bharat 🇮🇳
  Har shikayat ki sunwaai ho — yahi hai Smart-Gov ka iraada.
