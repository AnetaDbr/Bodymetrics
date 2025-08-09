# Masterplan – Ultimate Body Measurement & Weight Tracker

## 1. App Overview & Mission
This is **the ultimate body measurement & weight tracker** — nothing else, no fluff, no calorie counting, no chatbots, no social feeds. It solves *one problem perfectly*: tracking weight, measurements, and photos in a way that motivates and inspires users to reach their physical goals.

Where other apps overwhelm with 1000 tabs and irrelevant stats, this app is pure focus:
- **Beautiful** (futuristic, non-AI-looking, professionally designed).
- **Simple** (anyone can use it without a manual).
- **Motivational** (users see and feel progress every time they open it).

This app should *outperform competition* by being cleaner, faster, and visually superior.

---

## 2. Target Audience
- Fitness enthusiasts who want *simplicity with polish*.
- People on a weight-loss, muscle-gain, or body recomposition journey.
- Those tired of big fitness apps that bury their core need under dozens of extra features.

These users will choose this app because it *does exactly what they need and nothing they don’t*, while making progress tracking **addictive in a positive way**.

---

## 3. The Experience Promise
From the moment the app is opened:
1. No noise — the user is guided through a smooth, 4-step onboarding.
2. They instantly see *their* data visualized beautifully.
3. They feel emotionally invested before they’ve even signed up.
4. They’re presented with a *real* one-time offer for lifetime premium — with urgency that feels authentic.
5. They stay motivated through clean dashboards, goal-based progress bars, and photo comparisons that *look like professional fitness transformations*.

---

## 4. Monetization Model
- **Post-onboarding flash offer** (5-minute countdown) → lifetime premium.
- If declined, premium is only available as monthly/annual subscription.
- Free tier is actually useful — enough to keep users engaged, but clearly missing the extras that make premium irresistible.

---

## 5. Free vs Premium (V1)
**Free**
- Weight + 3 fixed measurements (waist, thigh, arm).
- Graphs for weight + 3 measurements, including goal prediction line.
- Add/view photos (no comparison mode).
- BMI calculation.

**Premium**
- Unlimited measurements & favourites.
- Custom reminders/notifications.
- Photo comparison mode (side-by-side front, side, back).
- Ad-free experience.
- Priority support.

---

## 6. Design Philosophy
- **Futuristic** but *not* “AI-generated” — no overused gradients, no bloated neon blobs, no cheap 3D renders.
- Inspired by *Samsung Health*’s clarity in data visualization, but with **tighter typography and modern card-based layouts**.
- High-contrast theme toggle: **dark mode default** (deep blacks, electric blue accents) and **light mode alternative** (clean whites, subtle grays).
- Minimal friction — *users always see their data in as few taps as possible*.

---

## 7. Data & Technical Approach
- **Hybrid storage:** Instant local save + cloud sync when logged in.
- Cloud storage for photos (private buckets, compression for cost).
- Cross-platform mobile build (React Native or Flutter).
- Lightweight backend (Firebase or Supabase) for auth, storage, and DB.

---

## 8. Development Phases
**Phase 1 (MVP)**
- Onboarding → dashboard → graphs → photo add/view → profile edits.
- Core data model for weight, measurements, photos.

**Phase 2 (Premium Layer)**
- Unlimited measurements, favourites, reminders, photo compare.
- Ads-free toggle.

**Phase 3 (Polish)**
- Light/dark toggle, animations, performance optimizations.

---

## 9. Future Expansion
- Google Fit / Apple Health sync.
- Data export & sharing.
- Web app companion for larger screen progress viewing.

---

# Implementation Plan & Scope

## Phase 1 — Core Product (Scalable MVP)
1. **Onboarding**
   - Step 1: Sex, age, height, name.
   - Step 2: Units (kg/cm or lb/in).
   - Step 3: Weight + goal weight.
   - Step 4: Measurements + goals (suggest waist, thigh, arm; skip option).
2. **Paywall**
   - Countdown: 5:00, “One-time lifetime premium offer”.
3. **Dashboard**
   - Current weight + change indicator (color-coded).
   - Goal progress bar (% complete).
   - BMI with health color band.
   - Favourite measurements (Premium unlock for >3).
4. **Progress Page**
   - Graph switcher (weight & measurements).
   - Goal line + predicted path to goal.
5. **Photos**
   - Add/view photo sets (front, side, back).
   - List view by date.
6. **Profile**
   - Edit personal info, metric system, measurements (Premium for >3).
   - Manage subscription.

## Phase 2 — Premium Layer
- Unlimited measurements/favourites.
- Custom reminders.
- Photo comparison mode.
- Ad-free toggle.

## Phase 3 — Polish & Scaling
- Light/dark theme toggle.
- UI animations.
- Sync optimizations.

---

# Design Guidelines

**Primary Theme Colors**
- Electric Blue `#0A84FF` → Key buttons, active graph lines.
- Neon Green `#34D399` → Success/goal achieved cues.
- Red `#EF4444` → Negative progress.
- Dark Background `#0E0E10` (Dark mode default).
- Light Background `#FFFFFF` (Light mode).

**Typography**
- Headings: Inter / SF Pro Display Bold, 20–28px.
- Body: Inter Regular, 14–16px.
- Numeric data: Monospaced font for perfect column alignment.

**UI Components**
- **Buttons:** Rounded corners (8px), subtle shadow, primary filled for key actions.
- **Graphs:** Minimal gridlines, clean legends, smooth animations.
- **Cards:** Elevated, with consistent padding (16px horizontal).

**Spacing & Layout**
- Touch targets: min 44px height.
- Vertical spacing between elements: 12–16px.

**Effects**
- Button press: 1.03 scale + slight shadow increase.
- Graph data points: subtle glow on hover/tap.

---

# App Flow, Pages & Roles

**Role:** All users are equal (no admin).

## Flow
1. App opens → Onboarding (4 steps) → Paywall → Dashboard.
2. Dashboard → See stats + measurements.
3. Progress → Graphs (weight + measurements).
4. Photos → Add/view photos, compare (Premium).
5. Profile → Edit info, units, measurements, reminders, subscription.

## Pages
- **Onboarding1:** Sex, age, height, name.
- **Onboarding2:** Unit selection.
- **Onboarding3:** Weight & goal.
- **Onboarding4:** Measurements & goals (skipable).
- **Paywall:** Lifetime premium offer (5-min timer).
- **Dashboard:** Current weight, BMI, favourites.
- **Progress:** Graphs + predictions.
- **Photos:** Photo history + add, compare (Premium).
- **Profile:** Settings, measurements, reminders (Premium).
