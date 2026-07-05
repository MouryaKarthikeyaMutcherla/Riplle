# Riplle 🌊
> **Pollution Tracker & Civic Action Hub for Mumbai's Coastline**

Riplle is a responsive, full-stack civic tech web application built during a fast-paced hackathon sprint. The platform empowers citizens and tourists to crowdsource environmental hazards along the Mumbai coastline, bridging the gap between civic awareness and municipal cleanup teams via an event-driven, real-time data layer.

---

## 🚀 The Core Problem

Scenic beaches, tourist hotspots, and marine ecosystems are under constant threat from severe pollution. Riplle targets **Water Body Pollution** as its primary threat vector while capturing and addressing the two critical upstream infrastructure failures that feed it:
1. **Water Body Pollution (Primary Focus):** Plastic accumulation, floating debris, and raw wastewater discharges ruining coastal tourist spots.
2. **Illegal Waste Dumping (Feeder 1):** Solid construction debris or household waste abandoned on roadsides or vacant plots before it washes into the sea.
3. **Broken Civic Infrastructure (Feeder 2):** Open manholes or damaged drain grates acting as open chutes that swallow street litter and funnel it directly out to the ocean during monsoons.

---

## ✨ Features

* **🔒 Mandatory Google Authentication:** Secures user accountability. Features an explicit entry gate ensuring all logged interactions, history, and profile metrics are bound to verified user accounts via Firebase Auth.
* **⚡ Live Real-Time Architecture:** Integrated directly with **Google Firebase Firestore** utilizing event-listeners (`onSnapshot`) to render new reports, dynamic charts, and stats instantly across all active clients without manual page refreshing.
* **🗺️ Interactive Threat Map:** Plots real-time coordinates over Mumbai's coast utilizing OpenStreetMap. Pins are color-coded dynamically based on the threat category (Orange for Dumping, Blue for Infrastructure, Green for General Pollution) with pulsing animations prioritizing highly critical, high-risk items.
* **📊 Live Impact & Analytics Dashboard:** Visualizes live database counts through interactive UI charts including a categorical breakdown pie chart, a 7-day activity tracking bar graph, and visual progress metrics mapping open vs. resolved cleanup pipelines.
* **🛠️ Authorities Hub & Action Gallery:** Features deep transparency charting pathways to regulatory bodies (MCGM, MPCB, BMC, CZMA, NGT) alongside an Action Gallery mapping community transformations, safety precautions, and active volunteer directives.
* **📰 Global Environmental Feed:** Aggregates real-time global news streams natively utilizing **The Guardian Environment API** and **BBC Science & Environment RSS feeds** directly into the platform context.

---

## 📁 Project File Structure

```text
Aqua-Pulse/
├── artifacts/                  # Generated build outputs and static deployment configurations
├── attached_assets/            # Mock assets, imagery, and static interface dependencies
├── lib/                        # Shared utility libraries and layout configurations
├── scripts/                    # Database seeding scripts and configuration macros
│
├── src/                        # Main Application Codebase
│   ├── components/            # Reusable UI Elements (Buttons, Cards, Loading States)
│   │   ├── AuthGate.tsx       # Secure Google Sign-In gate context barrier
│   │   ├── InteractiveMap.tsx # OpenStreetMap container with dynamic pulsing vector plotters
│   │   ├── ReportWizard.tsx  # 3-Step seamless reporting workflow with image attachment
│   │   └── AnalyticsCharts.tsx# Charting widgets for live metrics rendering
│   │
│   ├── pages/                 # Full Page Web Portal Modules
│   │   ├── Home.tsx           # Landing portal highlighting current active alerts feed
│   │   ├── Dashboard.tsx      # Analytics panel consuming reactive Firestore snapshots
│   │   ├── Profile.tsx        # Personal tracking portal displaying total user submissions
│   │   ├── Authorities.tsx    # Governance workflows and municipal data-export tooling
│   │   └── ActionGallery.tsx  # Interactive proof-of-work cleanups & safety guide lists
│   │
│   ├── firebase/              # Firebase configuration context, Storage, and Firestore listeners
│   ├── App.tsx                # Core application router and state manager
│   └── main.tsx               # Client bootstrap entrypoint
│
├── package.json                # Project script mappings and build dependencies
├── tsconfig.json               # TypeScript workspace configurations
└── replit.md                   # Replit build environment definitions