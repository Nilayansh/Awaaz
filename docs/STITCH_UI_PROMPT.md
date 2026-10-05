# Stitch UI Design Prompt: Awaaz

Use this prompt in **Stitch** to generate high-fidelity, production-grade UI mockups for **Awaaz** — an AI Requirements Engineering platform bridging citizens and civic institutions.

---

## 🎨 Design System & Visual Identity

- **Theme:** Modern, accessible, civic-tech platform tailored for Bharat. Clean, trustworthy, and high-contrast.
- **Color Palette:**
  - **Deep Civic Teal (Primary):** `#0E5E6F` (Navbar, primary headers, key accents)
  - **Warm Saffron / Amber (Action):** `#D97706` / `#E07A1E` (Record button, primary CTAs, key highlights)
  - **Evidence Tag Badges:**
    - 🟢 **Observed (Direct Evidence):** `#10B981` (Emerald green badge, dark green text)
    - 🟡 **Reported (Citizen Statement):** `#F59E0B` (Warm amber badge, dark amber text)
    - 🔵 **Hypothesis (AI Inference):** `#3B82F6` (Sky blue badge, dark blue text)
    - ⚪ **Unknown (Information Gap):** `#6B7280` (Neutral slate badge, dark gray text)
  - **Backgrounds:** Clean neutral canvas `#F8FAFC`, card surfaces `#FFFFFF`, borders `#E2E8F0`.
- **Typography:** Inter or Plus Jakarta Sans for clean readability; support for Indic font pairing (Noto Sans).
- **Iconography:** Lucide / Tabler style clean geometric icons (Microphone, Camera, MapPin, ShieldCheck, FileText, ChevronRight).

---

## Screen 1: Citizen Mobile PWA (Voice-First Reporting)

### Context & Goal
A mobile-first web app (390px × 844px) designed for everyday citizens across India with varying levels of literacy. The primary input is natural voice recording in their local language, with optional photo and location.

### Layout & Key Components:
1. **Header:**
   - Brand logo with small tricolor accent: `🇮🇳 Awaaz`.
   - Language selector dropdown chip: `Kannada (ಕನ್ನಡ) ▼` with quick-switch for Hindi, Tamil, Telugu, English.
2. **Hero Audio Input Card (Central Focal Point):**
   - Heading: *"Describe what you are facing"* / *"ನಿಮ್ಮ ಅನುಭವವನ್ನು ಹಂಚಿಕೊಳ್ಳಿ"*.
   - Subtext: *"Speak naturally in your mother tongue. We handle the rest."*
   - Large circular tactile Record Button (88px diameter, Vibrant Saffron `#D97706` with subtle pulsing soundwave ring).
   - Live waveform visualizer showing audio activity.
   - Status badge: *"Recording... 0:18 (Kannada auto-detected)"*.
3. **Evidence Attachments Strip:**
   - **Photo Upload Button:** Card showing thumbnail of uploaded road waterlogging with EXIF badge (`GPS: 12.9000, 77.6000 · 14 Aug 2026`).
   - **Location Pill:** Green toggle chip with pin icon: `📍 GPS Enabled (Ward 174, Bengaluru)`.
4. **Live Translation / Transcription Preview Card:**
   - Real-time speech transcript in Kannada: *"ಮಳೆ ಬಂದಾಗ ನಮ್ಮ ಶಾಲೆಯ ಮುಂದಿನ ರಸ್ತೆ ನೀರಿನಿಂದ ತುಂಬುತ್ತದೆ..."*
   - English subtitle: *"When it rains, the road in front of our school fills with water."*
5. **Submit Action:**
   - Full-width high-contrast button: `Submit Experience →`
   - Privacy reassurance subtext: *"🔒 Consent given. Personal names & phone numbers are automatically redacted before review."*
6. **Closed-Loop Feedback Toast (Post-Submission state):**
   - Notification card: *"Your report is linked to Problem Dossier #184 (23 reports total)."*
   - Audio playback bar: `▶ Listen to update in Kannada (0:24)` powered by Sarvam Bulbul TTS.

---

## Screen 2: Stakeholder Desktop Dashboard (Problem Dossier & BRD Agent)

### Context & Goal
A responsive desktop dashboard (1440px × 900px) used by municipal engineers, ward officers, and civic NGO leads. It transforms fragmented complaints into structured, evidence-backed requirements.

### Layout & Key Components:

1. **Sidebar Navigation (Left, 260px):**
   - Logo: `Awaaz Admin`
   - Menu items:
     - 📁 **Problem Dossiers** *(Active - Badge: 14)*
     - 📋 **Generated BRDs** *(Badge: 6 Pending Review)*
     - 🗺️ **Ward Geographic Map**
     - 📊 **Civic Analytics**
     - ⚙️ **Settings & API Keys**
   - User profile chip: *Ward 174 Engineering Desk*

2. **Dossier Header & Key Metrics (Top Content Area):**
   - Dossier ID & Title: **Dossier #184: Recurring School Road Waterlogging**
   - Location: *Ward 174, South Bengaluru · Last updated: 2 hrs ago*
   - KPI metric stat cards:
     - **23** Independent Citizen Reports (Voice: 17, Text: 6)
     - **14** Verified Photo Uploads (Metadata matched)
     - **3** Wards Impacted
     - **1** Unified BRD Draft Generated

3. **Two-Column Core Workspace:**

   #### Left Column (60%): Structured Claim Ledger
   - Header with filter chips: `All Claims (12)`, `🟢 Observed (4)`, `🟡 Reported (5)`, `🔵 Hypothesis (2)`, `⚪ Unknown (1)`.
   - Interactive Claim Cards:
     - **Card 1 (Observed):**
       - Badge: `🟢 OBSERVED` · Basis: `Photo evidence + EXIF (Report #031)`
       - Text: *"Water level on road surface exceeds 30cm during rainfall."*
       - Attachment thumbnail with photo viewer toggle.
     - **Card 2 (Reported):**
       - Badge: `🟡 REPORTED` · Basis: `Citizen statements (Reports #018, #044)`
       - Text: *"Children are unable to access the government school during monsoon mornings."*
     - **Card 3 (Hypothesis):**
       - Badge: `🔵 HYPOTHESIS` · Basis: `AI inference (Sarvam-M)`
       - Text: *"Road gradient depression combined with blocked side drains is likely causing stagnant accumulation."*
       - Note: *"⚠️ Unverified inference. Requires physical site inspection."*
     - **Card 4 (Unknown):**
       - Badge: `⚪ UNKNOWN` · Basis: `Data gap`
       - Text: *"Total number of households and commercial shops cut off during storm surges."*

   #### Right Column (40%): Live BRD Preview & "Prove This Claim" Drawer
   - Card container with document header: `Business Requirements Document (Draft v1.2)`
   - Generated sections with source tags:
     - **1. Problem Statement:** Recurring access disruption due to seasonal waterlogging on 80-foot School Link Road. `[claims: c1, c2]`
     - **2. Scope & Stakeholders:** School students, local shopkeepers, BMTC route 201.
     - **3. Functional Requirements:**
       - FR-1: Conduct topographic drainage survey within 200m radius.
       - FR-2: Assess storm-water drain culvert capacity.
     - **4. Acceptance Criteria:** Complete drainage assessment and publish mitigation plan before monsoon onset.
   - **"Prove This Claim" Interactive Inspector:**
     - Callout box triggered on claim click:
       ```
       CLAIM: 23 independent reports indicate recurring waterlogging
       SUPPORTED BY:
       ├─ Report #018 · Kannada Voice (0:45) · GPS: 12.9000, 77.6000
       ├─ Report #031 · Hindi Voice + Photo (3.2MB) · GPS: 12.9003, 77.6002
       ├─ Report #044 · English Voice · GPS: 12.8998, 77.5999
       └─ +20 more linked source events [View Full Audit Trail]
       ```
   - **Footer Action Bar:**
     - `Review & Approve BRD` (Primary Teal button)
     - `Export as PDF` (Outlined secondary button)
     - `Broadcast Voice Update to 23 Citizens` (Amber audio icon button)

---

## 💡 Key Design Instructions for Stitch:
- Prioritize high visual fidelity, modern card shadows (`shadow-sm` / `shadow-md`), smooth rounded corners (`rounded-xl` / `rounded-2xl`).
- Ensure contrast ratios satisfy WCAG AA standards.
- Give the citizen view a warm, trustworthy, mobile-optimized tactile feel.
- Give the stakeholder dashboard an enterprise-grade, clean analytical SaaS layout.
