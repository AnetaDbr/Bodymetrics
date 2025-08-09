# Bolt.new Vision Prompt – Ultimate Body Measurement & Weight Tracker

You are building **the ultimate mobile app for tracking body measurements, weight, and progress photos**.  
It must be **futuristic, clean, professional, and non-AI-looking**, with a focus on **simplicity and motivation**.

## Core Purpose
This app does one thing perfectly: tracks weight, measurements, and body photos to help fitness enthusiasts reach their goals.

## Target Audience
Fitness enthusiasts who want a **simple, beautiful, focused tool** without the clutter of larger fitness apps.  
They are tired of calorie counters and irrelevant stats — they want **pure measurement tracking**.

---

## Architecture & Tech Setup
You must create a **scalable architecture from day one**:

**Framework**
- Cross-platform mobile app (React Native or Expo).
- Strict separation of concerns: components, services, models.

**Authentication**
- Email/password + social login (Google, Apple).
- Authentication required for cloud sync, but **not required** to use the app initially.

**Database**
- Cloud database (Firebase Firestore or Supabase) for:
  - User profile
  - Measurements
  - Photos
  - Reminders
  - Subscription status
- Local SQLite or AsyncStorage for offline-first experience.
- Implement hybrid model: save locally first → sync to cloud when user is online/logged in.

**Storage**
- Cloud storage (Firebase Storage or Supabase Storage) for user photos.
- Private buckets only — no public access URLs.
- Store images compressed and optimized.

**Premium Management**
- Store subscription status in DB.
- Lifetime premium flag for one-time payment users.
- Gated features check subscription status before access.

---

## Data Model

### User
- id
- name
- sex
- age
- height
- unit system (kg/cm or lb/in)
- goal weight
- subscription status (free/premium)
- lifetime premium flag

### Measurement
- id
- userId
- type (waist, thigh, arm, custom, etc.)
- value
- goalValue
- date

### PhotoEntry
- id
- userId
- date
- frontImage
- sideImage
- backImage

### Reminder
- id
- userId
- time
- repeatPattern

---

## App Flow

### Onboarding
1. Step 1: Sex, age, height, name
2. Step 2: Units (kg/cm or lb/in)
3. Step 3: Weight + goal weight
4. Step 4: Measurements + goals (suggest waist, thigh, arm; allow skip)
5. Immediately after onboarding: **Paywall with 5-min countdown** → lifetime premium offer.

### Main Navigation (Bottom Tabs)
1. **Dashboard**
   - Current weight + change indicator (green/red).
   - Progress bar toward goal.
   - BMI with color-coded health status.
   - Favourite measurements (Premium unlock for >3).
2. **Progress**
   - Graphs for weight & measurements.
   - Goal line + predicted trend.
3. **Photos**
   - View/add photo sets (front, side, back).
   - Date list of entries.
   - Premium: compare mode (side-by-side, switch between angles).
4. **Profile**
   - Edit info, metrics, measurements (Premium for >3).
   - Change units.
   - Set reminders (Premium).
   - Manage subscription.

---

## Monetization
- Free tier:
  - Weight + 3 fixed measurements
  - Graphs with prediction
  - Photos (no compare)
  - BMI calc
- Premium tier:
  - Unlimited measurements & favourites
  - Reminders
  - Photo comparison
  - Ad-free
  - Priority support

---

## Design Guidelines

**Colors**
- Primary: Electric Blue `#0A84FF`
- Secondary: Neon Green `#34D399`
- Accent Red: `#EF4444`
- Dark BG: `#0E0E10`
- Light BG: `#FFFFFF`
- Text Dark Mode: `#FFFFFF`
- Text Light Mode: `#111827`
- Neutral Gray: `#9CA3AF`

**Typography**
- Headings: Inter / SF Pro Display Bold, 20–28px
- Body: Inter Regular, 14–16px
- Numbers: Monospaced font (JetBrains Mono or similar)

**UI**
- Buttons: Rounded corners (8px), subtle shadow, scale-up 1.03 on press
- Graphs: Minimal gridlines, smooth animations
- Cards: Elevated, 16px horizontal padding

**Theme**
- Dark mode default, light mode optional toggle

---

## Non-Negotiables
- No bloated extra features (calorie counting, workouts, chat, etc.)
- UI must match modern professional fitness app quality
- Every screen must load instantly with offline-first capability
- All data stored locally first, then synced to cloud
- Premium checks must be enforced at the feature level

---

## Development Phases
**Phase 1:** Onboarding, dashboard, progress graphs, photo add/view, profile edits, hybrid storage.  
**Phase 2:** Premium layer (unlimited measurements, reminders, compare mode, ad-free).  
**Phase 3:** Light/dark toggle, animations, optimization.

---

**Final Goal:** Deliver the cleanest, most motivational body tracking app on the market, with architecture ready for scaling from day one.
