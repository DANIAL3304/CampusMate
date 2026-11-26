# CampusMate – The Universal Wayfinder for International Newcomers

**A high-fidelity UI/UX prototype for campus navigation at Universiti Putra Malaysia (UPM).**

CampusMate helps international students navigate campus with ease. It combines **outdoor + indoor navigation**, **real-time sign translation** and a **campus glossary** in one app, so newcomers can overcome language barriers and understand an unfamiliar campus environment.


---


##  The Problem

International students at UPM face three recurring frustrations:

- **"I found the building, but not the room."** Google Maps stops being useful at the building entrance, leaving students lost inside multi-level buildings and late for class.
- **"I can't read the signs."** Campus signage is mostly in Malay (*Bilik Kuliah*, *Tingkat*, *Sayap Timur*).
- **"What is DKAP? What is BK?"** Local acronyms make room codes and directions hard to understand.

On top of that, students juggle **Google Maps + Google Translate + the university portal** just to get to one class.

---

##  Target Users & Persona

**Primary persona — Alex**, an international student who mainly uses Google Maps, switches to Google Translate for signs, and checks the portal for class locations.

| Persona need / pain | Design response |
|---|---|
| Feels frustrated after finding the building but not the room | Multi-floor indoor floor plans with a blue route that continues from the outdoor map into the building |
| Struggles to understand Malay words on campus signs | Dark-themed **Lens Translate** camera view with a one-tap language dropdown inside the viewfinder |
| Does not understand terms like *BK-1* or *DKAP* | **Campus Glossary & Search** card directly on the home screen with expanding definition cards |

---

##  Pain → Feature Crosswalk

| User pain point | Root cause | Feature | How it works |
|---|---|---|---|
| "Google Maps is not reliable for indoor navigation" | GPS signal drops at building thresholds | **Dual-Phase Navigation Engine** | Auto-switches from outdoor route tracking to indoor floor plans on arrival |
| "Language barriers make signboards hard to understand" | Signage is printed only in the local language | **Live Camera Translation Viewfinder** | Point-and-translate lens tool built into the main app |
| "Campus directions are confusing… unfamiliar terminology" | Local acronyms (FSKTM, DKAP) | **Terminology Decoupling Cards** | Expandable glossary definitions in the search results |
| "Alex uses Google Maps, then switches to Google Translate…" | App-switching fatigue | **Unified Navigation Suite** | Schedule, map and translation in one persistent bottom tab bar |

[User Journey Map](https://www.figma.com/make/IZLSv6wk4b6yZomZ0h7Tnv/User-Journey-Map?p=f&t=qXCZeD5yKBZHO2kn-0)

---

##  Key Features

### 🏠 Home
- **Up Next** card with the next class and a one-tap **Route Me to Class** button
- **Campus Glossary & Search** for acronyms (BK, DKAP, FSKTM)
- Quick Tools: Navigate (Outdoor + Indoor) and Translate Sign

### 🗺️ Dual-Phase Navigation
- Search with category filter pills (Classrooms, Faculties, Services)
- Route planning sheet with time and distance; **Walk** or **Accessible** mode
- **Outdoor phase:** turn-by-turn steps with an animated position dot and route line
- **Indoor phase:** floor plans for DKAP (Ground, Level 2, Level 3) and FSKTM (Ground, Level 1)
- **Lift / Stairs** toggle that rebuilds the indoor route instantly
- Step progress tracker, direction banner, Back / Next / Stop, and **Back to Outdoor Route**

### 📅 Schedule
- Daily timetable with a **Navigate to Class** shortcut on every class

### 📷 Lens Translate
- Google Lens–style camera view with scanning animation and AR translation bubbles
- One-tap language dropdown (English, Malay, Chinese, Japanese, Tamil)

---

##  Design System

### Colour palette

| Role | Colour | Hex | Used for | Why |
|---|---|---|---|---|
| **Primary** | Deep Royal Violet | `#4B3BC8` | App headers, high-emphasis action buttons | Builds a strong brand identity and draws attention to the main action on each screen |
| **Secondary** | Electric Blue | `#1E88E5` | Navigation controls (Next, step titles) | Contrasts with the primary colour to guide users through multi-step flows without competing with headers |
| **Success** | Growth Green | `#2E7D32` | Direction banners, arrival states, "Continue Indoor Navigation" | Reassures the student they are on the right path or have arrived |
| **Warning** | Amber Gold | `#FFA726` | Map highlights for facilities (e.g. FSKTM, café) | Isolates key landmarks so they are identifiable at a glance |
| **Error** | Coral Crimson | `#E05555` | Stop button, destructive actions | Demands attention for high-alert actions such as stopping active navigation |

### Typography & visual scale

| Level | Style | Example |
|---|---|---|
| Heading | Bold 32px | Screen entry points – *My Schedule* |
| Sub-heading | Semi-Bold 24px | Module containers and destinations – *Linear Algebra* |
| Body | Regular 16px | Status updates and instructions – *"Point your camera…"* |
| Caption | Regular 12px | Metadata and micro-copy – *DKAP · BK-10, Level 2* |

A single typeface is used throughout for consistency (see Heuristic #4 below).

### Iconography
Tabler Icons provide a consistent line-icon style across navigation, directions (turn arrows, lift, stairs, flag) and tools.

---

##  Component Library

| Component | Purpose |
|---|---|
| **Navigation search bar** | Find rooms, faculties and services |
| **Glossary search bar** | Look up campus terms such as BK, DKAP, FSKTM |
| **Category filter pills** | Classrooms / Faculties / Services |
| **Primary action buttons** | *Route Me to Class*, *Navigate to Class*, *Search a Destination*, *Choose Destination* |
| **Phase switch buttons** | *Continue Indoor Navigation* / *Back to Outdoor Route* |
| **Step controls** | Back · Next · Stop |
| **Lift / Stairs toggle** | Choose how to change floors |
| **Language dropdown** | Select translation language in the camera view |
| **Map direction banner** | Shows the current instruction on top of the map |
| **Step progress tracker** | Shows progress through the route |
| **Route tracking line** | Dashed path and moving dot on outdoor and indoor maps |
| **Bottom tab bar** | Home · Schedule · Translate · Map |

---
##  Wireframae - [FigmaWireframe](https://www.figma.com/proto/HLSG9lD5sMqzTciZ4nO11k/SWE3307?node-id=1-887&starting-point-node-id=1%3A887)
##  Usability Fixes (Low-Fi → Hi-Fi)

Problems found during wireframe testing were fixed using **Nielsen's 10 Usability Heuristics**.

| Heuristic | Problem in wireframe | Fix in hi-fi prototype | Impact |
|---|---|---|---|
| **#4 Consistency & Standards** | Inconsistent fonts confused users and broke visual hierarchy | Standardised all typography to one typeface with a clear type scale | Easier to scan; users can tell clickable elements from static text |
| **#7 Flexibility & Efficiency of Use** | No shortcut; users had to search manually every time | Added a **Schedule** tab with one-tap *Navigate to Class* | Much faster task completion, while search remains available for new users |
| **#3 User Control & Freedom** | No back button; users got stuck and tapped screen edges | Added a visible back action on every sub-screen | Users can undo mistakes and never feel trapped |
| **#4 Consistency & Standards** | Lens Translate supported only one language | Added a multi-language dropdown | Removes language barriers for a diverse student base |
| **#8 Aesthetic & Minimalist Design** | Map screen was crowded with room chips and extra elements | Removed redundant elements, added whitespace, used progressive disclosure | Lower cognitive load; focus on the map and the main search action |

---

##  Usability Testing

### DECIDE framework

| Step | Plan |
|---|---|
| **D**etermine the goal | Evaluate whether CampusMate helps international students find locations easily and reduces navigation difficulty |
| **E**xplore the questions | Is it easy to use? Can users find locations? Does translation help? Is timetable integration useful? |
| **C**hoose methods | Task-based testing with the prototype, followed by a **SUS questionnaire** and feedback session |
| **I**dentify practical issues | Recruit 5 international students to test remotely via video call |
| **D**ecide on ethics | Academic purpose only; voluntary participation; confidential responses |
| **E**valuate data | Analyse SUS scores and qualitative feedback to find strengths and improvements |

### Participants
5 international students, all Computer Science students with high digital literacy. Common behaviours:
- Use Google Maps first, then ask other students when confused
- Manage outdoors well but struggle **inside large buildings**
- Want **timetable integration**, clear distance indicators and visual (not text-heavy) guidance
- Interested in translation and voice guidance

### SUS method
- Odd questions (1, 3, 5, 7, 9): score = response − 1
- Even questions (2, 4, 6, 8, 10): score = 5 − response
- Sum of adjusted scores × 2.5 = SUS score per user

---

## 📊 Results & Insights

### SUS scores

| Participant | SUS score |
|---|---|
| P1 | 87.5 |
| P2 | 85.0 |
| P3 | 85.0 |
| P4 | 82.5 |
| P5 | 80.0 |
| **Average** | **84.0** |

| Benchmark | Score | Grade |
|---|---|---|
| Industry average | 68 | C – Okay |
| **CampusMate** | **84** | **A – Excellent** |

Highlights from the questionnaire:
- **100%** agreed or strongly agreed the system was **easy to use**
- **100%** disagreed that it was **unnecessarily complex** or **cumbersome**
- **100%** agreed they felt **confident** using it
- **100%** agreed most people would **learn it quickly**

### Affinity diagram (qualitative feedback)

| Theme | What users said |
|---|---|
| **Tool reliability & integration** | Saves time finding classes · Timetable integration is useful · No need to open the student portal separately · Easy to use |
| **Language & semantics** | Translate Sign made campus terms easier to understand · Easier to follow locations and terminology |
| **Emotional impact** | Reduced stress during navigation · Navigation was easy to understand · More confident finding places independently |
| **Navigation accuracy** | Helped find class quickly · ⚠️ Large buildings remain confusing · ⚠️ Building layouts lack detail · ⚠️ Indoor directions are unclear |

**Takeaway:** Users valued the timetable integration, guided navigation and translation the most. The main weakness is **indoor detail in large buildings**, which drives the roadmap below.

---

##  What's Next

1. **Improve indoor navigation accuracy** – more detailed floor maps and additional landmarks
2. **AR-assisted wayfinding** – camera-based arrows and real-world navigation overlays
3. **Better building visualisation** – 3D building maps and interactive floor navigation

---

##  Run the Prototype

The prototype is a single HTML file with no build step.

1. Clone the repo and open `campusmate.html` in Chrome, Edge, Safari or Firefox.
2. For the camera in Lens Translate, serve it over `localhost` or `https`:
   ```bash
   python -m http.server 8000
   ```
   then open `http://localhost:8000/campusmate.html`.

**Try this flow:** Home → *Route Me to Class* → *Start Navigation* → tap **Next** through the outdoor steps → the app switches to indoor → toggle **Lift / Stairs** → arrive at BK-10.

**Deploy on GitHub Pages:** rename the file to `index.html`, then enable **Settings → Pages** on the main branch.

### Tech stack
HTML5 · CSS3 · vanilla JavaScript · SVG maps · `getUserMedia` camera API · Tabler Icons · Google Fonts

### Prototype scope
This is a hi-fi UX prototype. Routes, floor plans and the schedule use sample data, and Lens Translate simulates text detection with predefined signboards rather than real OCR.

---
