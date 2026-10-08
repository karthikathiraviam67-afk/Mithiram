# 🌿 MITHRAM (மித்ரம்) — Senior-Centric Medication Management & Caregiver Support Platform

> *"Mithram means friendship and companion. Designed as a trusted friend supporting elderly citizens in their everyday health, safety, routines, and social connection."*

---

## 🌟 1. Product Philosophy & Core Objectives

**Mithram** is built senior-first, extremely simple, warm, human, accessible, multilingual, and emotionally supportive. It moves away from cold, complex hospital dashboards toward a comforting digital companion.

### Target Users & Roles:
1. **👵 Senior Citizen (Primary User):**
   - **Today's Routine Timeline** (8:00 AM Morning, 12:30 PM Afternoon, 5:00 PM Evening, 9:00 PM Night).
   - **Interactive Checklist:** Large, tremor-friendly tappable task cards.
   - **Visual Pill Identifier:** Scored tablets, two-tone capsules, and caplets with anti-double-dosing safety lockouts.
   - **Hydration & Mood Tracking:** 1-tap water logging & emotional health check-in.
   - **🗣️ Thunai AI Companion:** Empathetic voice-guided health & emotional care.
   - **👥 Community Circles:** Suprabhatam yoga, Bhajans & devotional music, walking buddies, gardening.
2. **👨‍👩‍👧 Family Member:**
   - Real-time routine adherence & medicine intake confirmation.
   - Live mood & hydration updates.
   - Prescription stock monitoring with refill alerts.
   - Direct note composer that pins loving reminders directly onto the senior's tablet screen.
3. **🤝 Professional Caregiver:**
   - Multi-tier delay escalation matrix (15 min in-app chime ➔ 30 min SMS/Push ➔ 60 min emergency dispatch).
   - Routine & medication administration logs.
   - Pharmacy stock replenishment (+30 pills button).
4. **🩺 Healthcare Professional / Doctor:**
   - 30-day compliance percentages and vitals (Blood Pressure, Fasting Sugar, Restorative Sleep).
   - Medication regimen adjustments.
   - 1-click printable Clinical Continuity & Physician Adherence Report.

---

## 🌐 2. Multilingual Support
Built with native localization for five Indian languages:
- 🇬🇧 **English**
- 🇮🇳 **Tamil (தமிழ்)**
- 🇮🇳 **Malayalam (മലയാളം)**
- 🇮🇳 **Telugu (తెలుగు)**
- 🇮🇳 **Kannada (ಕನ್ನಡ)**

---

## 🧭 3. Mandated 5-Button Senior Bottom Navigation
1. 🏠 **Home:** "Today's Routine" timeline, hero upcoming action, water tracker, and mood check-in.
2. 💊 **Medicines:** Schedule, 3D SVG pills, food/water instructions, and anti-double-dose lockout.
3. 🗣️ **Thunai:** AI voice companion with 4-step comforting protocol & Gemini AI integration.
4. 👥 **Community:** Elder friends, morning yoga circle, bhajans, walking club, and words of wisdom.
5. 👤 **Profile:** Personal details, emergency circle, text size scaler (`A` / `A+` / `A++`), and high-contrast toggle.

---

## 🤖 4. Thunai — AI Companion (Gemini 2.5 Integration)

Thunai ("துணை" meaning companion/support) is powered dynamically via the backend endpoint `/api/chat` with Google Gemini:
- **Package:** `@google/genai`
- **Model:** `gemini-2.5-flash`
- **Environment Variable:** `GEMINI_API_KEY` (configured in `.env.local` or `.env`)

### 4-Step Critical Emotional & Health Response Protocol:
When a senior expresses physical or emotional pain (*"I am not feeling well"*, *"Udambu mudiyala"*, *"I feel sick"*, *"I am scared"*):
1. **Immediate Comfort:** Validates feelings with instant emotional warmth (*"Oh dear, I am so sorry you are feeling unwell. Please don't worry, I am right here with you."*).
2. **Gentle Inquiries:** Asks simple, non-overwhelming questions (*"Are you feeling dizzy, having body pain, or feeling tired?"*).
3. **Comforting Guidance:** Step-by-step calming instructions (*"Please sit or lie down comfortably. Take a slow, deep breath and sip a little warm water."*).
4. **Caregiver Alert Offer:** Offers to alert family or caregiver without stressing them (*"Would you like me to send a gentle message to your daughter Ananya?"*), with a 1-tap alert button!

---

## 🚀 5. Getting Started & Running Locally

### Start Dev Server:
```bash
npm run dev
```
Open **`http://localhost:5173/`** in your browser.

### Add Gemini API Key:
Create or edit `.env.local`:
```bash
GEMINI_API_KEY=your_google_gemini_api_key_here
```
*(If no API key is provided, Thunai operates in built-in offline compassionate mode with full Tamil/English 4-step protocol support).*

### Production Build:
```bash
npm run build
```
Compiled bundle in `./dist` in ~100ms.
