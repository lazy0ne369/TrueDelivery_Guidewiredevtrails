<div align="center">

<img src="https://img.shields.io/badge/TrueDelivery-Parametric%20Income%20Insurance-f97316?style=for-the-badge&logo=shield&logoColor=white" alt="TrueDelivery"/>

# TrueDelivery

### *Your Earnings, Truly Protected.*

> **AI-native parametric income insurance engineered for India's 5+ million food delivery workers.**
> Zero forms. Zero calls. Zero waiting. When a verified disruption hits your zone — heavy rain, AQI spike, curfew, platform outage — your lost income is restored to your UPI **automatically**, in under 3 minutes.

<br/>

[![Phase](https://img.shields.io/badge/Phase%201-Complete-22c55e?style=flat-square)](https://github.com)
[![Hackathon](https://img.shields.io/badge/Guidewire-DEVTrails%202026-f97316?style=flat-square)](https://github.com)
[![Coverage](https://img.shields.io/badge/Coverage-Income%20Loss%20Only-60a5fa?style=flat-square)](https://github.com)
[![Model](https://img.shields.io/badge/Model-Weekly%20Parametric-a78bfa?style=flat-square)](https://github.com)
[![Stack](https://img.shields.io/badge/AI-Fraud%20Detection%20%2B%20Risk%20Engine-ef4444?style=flat-square)](https://github.com)
[![Market](https://img.shields.io/badge/TAM-₹2%2C400Cr%2Fyr-facc15?style=flat-square)](https://github.com)

<br/>

[Crisis](#-the-crisis-no-one-is-insuring) · [How It Works](#-how-truedelivery-works) · [Architecture](#-system-architecture-overview) · [Triggers](#%EF%B8%8F-parametric-trigger-engine) · [Fraud Defense](#%EF%B8%8F-adversarial-defense--anti-spoofing) · [AI/ML](#-aiml-architecture) · [UX Features](#-worker-experience--app-features) · [Business Model](#-business-model--unit-economics) · [Stack](#-tech-stack) · [Roadmap](#%EF%B8%8F-development-roadmap) · [Team](#-team)

---

</div>

## 🚨 The Crisis No One Is Insuring

India's gig economy is the world's largest informal workforce with zero systemic protection. **5.5 million food delivery partners** on Zomato and Swiggy earn their entire livelihood on two wheels — no fixed salary, no paid leave, no sick days, no insurance of any kind.

Every rupee they earn requires them to physically be able to ride. When external disruptions strike — events entirely outside their control — they bear 100% of the financial loss. Alone.

### The Disruption Tax Delivery Partners Pay Every Month

| Disruption Event | Mechanism of Income Loss | Avg. Monthly Loss |
|:---|:---|:---|
| 🌧️ Heavy Rain / Red Alert Flooding | Roads submerged, platform suspends order assignments | ₹1,500 – ₹3,000 |
| 🌡️ Extreme Heat Wave (>43°C) | Outdoor work becomes physically unsafe, voluntary withdrawal | ₹800 – ₹1,500 |
| 🌫️ AQI Severe+ Pollution Event | Government advisory triggers platform-level halt | ₹600 – ₹1,200 |
| 🚫 Curfew / Bandh / Strike | Zone access blocked, movement restricted citywide | ₹500 – ₹2,000 |
| 📵 Platform Technical Outage | Order queues drop >80%, workers idle for hours | ₹300 – ₹800 |

> **These five disruptions cause delivery partners to lose 20–30% of their monthly earnings — and every single rupee of that loss falls on them.**

### Why Existing Solutions Fail

| Solution | Why It Falls Short |
|:---|:---|
| Government welfare schemes | Require permanent employment proof; gig workers explicitly excluded |
| Traditional health/accident insurance | Covers body, not income; claims require documentation, weeks of processing |
| Platform "partner benefits" | Cosmetic; do not cover income disruption from external events |
| Personal savings | Median delivery partner has <₹3,000 liquid savings at any time |
| Microloans | Debt-based; transforms income loss into long-term financial burden |

**TrueDelivery is the only solution built specifically for this gap: external-event-triggered income loss, resolved in minutes, not months.**

> ⚠️ **Scope Boundary:** TrueDelivery covers **income loss only** from verified, objective, third-party-confirmed external disruptions. Health, life, accident, and vehicle repair coverage are explicitly excluded by design to maintain parametric integrity and regulatory clarity.

---

## 📖 Table of Contents

1. [The Crisis No One Is Insuring](#-the-crisis-no-one-is-insuring)
2. [Real-World Scenarios](#-real-world-scenarios--personas)
3. [How TrueDelivery Works](#-how-truedelivery-works)
4. [System Architecture Overview](#-system-architecture-overview)
5. [Payment Models](#-payment-models)
6. [Application Workflow](#-application-workflow--user-journey)
7. [Weekly Premium Model](#-weekly-premium-model--pricing-engine)
8. [Parametric Trigger Engine](#%EF%B8%8F-parametric-trigger-engine)
9. [Worker Experience & App Features](#-worker-experience--app-features)
10. [AI/ML Architecture](#-aiml-architecture)
11. [Adversarial Defense & Anti-Spoofing](#%EF%B8%8F-adversarial-defense--anti-spoofing)
12. [Business Model & Unit Economics](#-business-model--unit-economics)
13. [Tech Stack](#-tech-stack)
14. [Development Roadmap](#%EF%B8%8F-development-roadmap)
15. [Target Market & Expansion](#-target-market--expansion-strategy)
16. [Regulatory & Compliance Considerations](#-regulatory--compliance-considerations)
17. [Team](#-team)
18. [Pitch Deck](#-pitch-deck)

---

## 🎭 Real-World Scenarios & Personas

### The TrueDelivery Worker Profile

| Attribute | Details |
|:---|:---|
| Platforms | Zomato and/or Swiggy (dual-app workers common) |
| Weekly earnings | ₹3,500 – ₹7,000 depending on city tier and hours worked |
| Daily hours | 8 – 12 hrs/day, 6 – 7 days/week |
| Geography | Urban metros, tier-2 cities, semi-urban zones with active platform coverage |
| Current safety net | **None.** |
| Financial literacy | Variable; majority prefer voice UI and regional language |
| Device | Android smartphone, often entry-to-mid segment |

---

### Scenario 1 — The Monsoon Blackout 🌧️

**Ravi · Swiggy Partner · Bengaluru · Standard Shield subscriber**

IMD issues a Red Alert. Bengaluru receives 180mm rainfall in 6 hours. Roads flood across South and East zones. Swiggy suspends order dispatch. Ravi parks his bike and waits.

| | Without TrueDelivery | With TrueDelivery |
|:---|:---|:---|
| Income loss | ₹375 gone permanently | ₹375 returned to UPI — automatically |
| Effort required | None (still loses money) | Zero — no claim filed |
| Time to payout | Never | 2 min 43 sec |
| Ravi's action required | N/A | Open his phone. See ₹375 arrive. |

**What happened under the hood:**
```
OpenWeatherMap API → Red Alert confirmed, rainfall > 50mm/hr
HyperZone engine → Ravi's registered zone matches affected pin codes
Fraud Detection → Behavioral Twin check: PASS (Ravi's zone history: 94 days)
Risk Score: 18 → 🟢 Auto-Approve
UPI payout: ₹375 → Ravi's PhonePe in 2 min 43 sec
```

---

### Scenario 2 — The Curfew Shutdown 🚫

**Meena · Zomato Partner · East Delhi · Standard Shield subscriber**

6:00 AM: A bandh is called across East Delhi. Movement restricted. Platforms reduce order volume 90%+ in affected zones. Meena has been awake since 5 AM planning her morning rush.

**What happened:**
```
Govt Alert Mock API → Bandh advisory detected for East Delhi pin codes
Order Volume Monitor → Zomato orders in zone: dropped 91% (threshold: 80%)
Dual-signal confirmation → Both triggers agree; claim auto-initiated
Risk Score: 22 → 🟢 Auto-Approve
Payout: ₹480 → Meena's GPay — before she even left her house
```

Meena didn't file a claim. She didn't call anyone. Her phone buzzed with a ₹480 credit — income she lost before she even lost it.

---

### Scenario 3 — The Pollution Shutdown 🌫️

**Arjun · Swiggy Partner · Delhi · Pro Shield subscriber**

AQI crosses 450 — Severe+ category. Delhi government issues an outdoor activity advisory. Multiple platforms announce voluntary halt on outdoor deliveries citing worker safety. Arjun would have earned ₹680 across the afternoon.

**What happened:**
```
AQICN API → AQI: 463 (threshold: >400 Severe+)
Platform activity log → Swiggy confirmed reduced order volume (simulated)
Zone match → Arjun's registered North Delhi zone within affected radius
Risk Score: 31 → 🟢 Auto-Approve
Payout: ₹680 → Arjun's UPI, 1 min 54 sec post-trigger
```

---

### Scenario 4 — The Coordinated Fraud Attempt 🚨

**Telegram Syndicate · 47 workers · Mumbai**

A WhatsApp/Telegram group sends a blast: *"RAIN ALERT ZONE 4 — CLAIM NOW — FOLLOW THESE STEPS."* 47 accounts simultaneously submit claims from GPS coordinates inside a rain-affected zone. Many are sitting at home in clear weather across a different part of the city.

**What TrueDelivery's Syndicate Detection Layer saw:**
```
47 claims — same GPS pin (19.0456°N, 72.8778°E) — within 4 minutes 12 seconds
Mock Location API flag: ACTIVE on 39 of 47 devices
Cell tower triangulation: Contradicts GPS coordinates for 41 of 47 workers
WiFi SSID analysis: 34 of 47 connected to residential broadband (not mobile data)
Zone history check: 29 of 47 workers have never delivered in claimed zone
Digital Twin match: 0 of 47 pass behavioral consistency check

RESULT: All 47 claims → 🔴 FREEZE
ACTION: Syndicate alert raised. Claims pending human investigation.
```

**Meanwhile:** 312 genuine delivery workers caught in the actual rain zone received automatic payouts without interruption. The fraud ring caused zero false positives. The system's discriminatory precision is its core value to the insurer.

---

## ⚡ How TrueDelivery Works

Think of it like a **Jio recharge for your income** — pay a small amount on Monday, get full income protection for the week. No paperwork. No phone calls. No waiting for an adjuster.

```
┌─────────────────────────────────────────────────────────────────────┐
│  WEEK CYCLE: MONDAY → SUNDAY                                        │
│                                                                     │
│  MON   Worker pays ₹49 weekly premium (or auto-deducted)           │
│        ↓ Policy activated for 7 days                                │
│                                                                     │
│  TUE–SUN  TrueDelivery monitors 5 disruption triggers in real time │
│           HyperZone Map shows live zone status                      │
│           Earnings Forecast shows tomorrow's risk level             │
│                                                                     │
│  ANY DAY  Disruption detected → Claim auto-initiated               │
│           Fraud check runs silently in background                   │
│           ┌───────────────────────────────────────────────┐        │
│           │ Risk 0–40:   💸 Instant UPI payout            │        │
│           │ Risk 41–70:  ⏳ 2-hour soft hold → Auto-pay   │        │
│           │ Risk 71–100: 📱 10-sec selfie → Manual review  │        │
│           └───────────────────────────────────────────────┘        │
│                                                                     │
│  NEXT MON  Worker renews. Streak discount applied if eligible.     │
└─────────────────────────────────────────────────────────────────────┘
```

### The Numbers, Demystified

**Ravi pays ₹49 on Monday. Heavy rain hits Thursday — 5 hours lost.**

| Item | Value |
|:---|:---|
| Hours disrupted | 5 hours |
| Hourly earnings (₹4,200/week ÷ 7 ÷ 8hrs) | ₹75/hr |
| Income lost to disruption | ₹375 |
| **TrueDelivery payout → Ravi's UPI** | **₹375** ✅ |
| Premium paid | ₹49 |
| **Net protection value** | **₹326 saved from total loss** |

### Does Ravi Repay ₹375? No. Never.

This is the fundamental insurance principle — the many fund the few:

```
Pool Mechanics (1,000 workers, 1 week):
────────────────────────────────────────
Premiums collected:   1,000 × ₹49          = ₹49,000
Claims paid out:      100 workers × ₹375   = ₹37,500
Operating margin:                          = ₹11,500
Loss ratio:                                  76.5% (healthy for micro-insurance)
```

The 900 workers who had a disruption-free week fund the 100 who were affected. Nobody repays anything. This is 200-year-old insurance logic — TrueDelivery makes it instant, automated, and built natively for gig work patterns.

### Payout vs. Premium at a Glance

| Week Scenario | Premium Paid | Payout Received | Outcome |
|:---|:---|:---|:---|
| No disruptions | ₹49 | ₹0 | Peace of mind. Full earnings kept. |
| 3-hour rain event | ₹49 | ₹225 | **+₹176 net recovery** |
| Full-day curfew | ₹49 | ₹600 | **+₹551 net recovery** |
| Two-day flood | ₹49 | ₹1,200 | **+₹1,151 net recovery** |
| Major outage (8 hrs) | ₹49 | ₹600 | **+₹551 net recovery** |

> **No repayment. No loans. No fine print. No exceptions.**

---

## 🏗️ System Architecture Overview

```
┌──────────────────────────────────────────────────────────────────────────────┐
│                         TRUEDELIVERY ARCHITECTURE                            │
│                                                                              │
│  ┌────────────────────┐    ┌──────────────────────────────────────────────┐ │
│  │   WORKER LAYER     │    │              DATA INGESTION LAYER             │ │
│  │                    │    │                                              │ │
│  │  Flutter Mobile    │    │  OpenWeatherMap   AQICN    Govt Alert Mock   │ │
│  │  App (Android/iOS) │    │  (Rain/Heat)      (AQI)   (Curfew/Bandh)    │ │
│  │                    │    │       ↓             ↓            ↓            │ │
│  │  • HyperZone Map   │    │  ┌─────────────────────────────────────────┐ │ │
│  │  • Premium Portal  │    │  │      PARAMETRIC TRIGGER ENGINE          │ │ │
│  │  • Payout Feed     │    │  │  Real-time threshold evaluation         │ │ │
│  │  • Voice Assistant │    │  │  Zone-level pin code matching           │ │ │
│  │  • Streak Rewards  │    │  │  Multi-signal event confirmation        │ │ │
│  └────────┬───────────┘    │  └──────────────────┬──────────────────────┘ │ │
│           │                │                     │                          │ │
│           ▼                └─────────────────────│──────────────────────────┘ │
│  ┌────────────────────┐                          │                            │
│  │   API GATEWAY      │◄─────────────────────────┘                            │
│  │   Node.js/Express  │                                                        │
│  │                    │    ┌──────────────────────────────────────────────┐   │
│  │  • Auth routes     │───►│           AI/ML MICROSERVICE LAYER           │   │
│  │  • Policy mgmt     │    │  (Python · scikit-learn · XGBoost)           │   │
│  │  • Claim pipeline  │    │                                              │   │
│  │  • UPI payout      │    │  ┌────────────────┐  ┌────────────────────┐  │   │
│  │  • Admin dashboard │    │  │  Risk Profiler  │  │  Fraud Detector   │  │   │
│  └────────┬───────────┘    │  │  (XGBoost)      │  │  (Isolation Forest│  │   │
│           │                │  │  Risk Score 0–100│  │  + rule engine)   │  │   │
│           ▼                │  └────────────────┘  └────────────────────┘  │   │
│  ┌────────────────────┐    │  ┌────────────────┐  ┌────────────────────┐  │   │
│  │   Firebase Layer   │    │  │ Digital Twin   │  │  Premium Calculator│  │   │
│  │                    │    │  │ (Behavioral    │  │  (Regression +     │  │   │
│  │  • Firestore DB    │    │  │  Clustering)   │  │   zone weighting)  │  │   │
│  │  • Firebase Auth   │    │  └────────────────┘  └────────────────────┘  │   │
│  │  • Real-time sync  │    │  ┌────────────────────────────────────────┐  │   │
│  └────────────────────┘    │  │  Predictive Disruption Model (Prophet) │  │   │
│                            │  └────────────────────────────────────────┘  │   │
│                            └──────────────────────────────────────────────┘   │
└────────────────────────────────────────────────────────────────────────────────┘
```

### Core Data Flows

**Happy Path (Genuine Claim, No Fraud):**
```
External Event → Trigger Engine → Zone Match → Risk Profiling → 
Fraud Score: LOW → UPI Payout Initiated → Razorpay → Worker's UPI
(Total time: < 3 minutes)
```

**Fraud Path (GPS Spoofer):**
```
Spoofed GPS Claim → Trigger Engine → Zone Match (PASS) → 
Device Intelligence (FAIL: Mock Location API ON) → 
Behavioral Twin (FAIL: Never worked this zone) → 
Syndicate Check (FAIL: 23 claims same pin) → FREEZE → Investigation Queue
(Worker notified: "Signal verification in progress")
```

---

## 💳 Payment Models

### Model 1 — Worker Self-Pay

```
Ravi earns ₹4,200 this week from Swiggy
→ Opens TrueDelivery app on Monday morning
→ Taps "Activate This Week" → UPI payment ₹49
→ Policy live for 7 days. No commitment beyond this week.
```

Zero lock-in. The worker chooses week by week. Designed to match the mental model of a Jio recharge.

---

### Model 2 — Platform Co-Pay ⭐ Recommended B2B2C Model

```
Swiggy contributes   ₹25  (employer share — 51%)
Ravi pays            ₹24  (worker share — 49%)
                     ────
Total premium:       ₹49 → Full coverage activated
```

**The business case for Swiggy/Zomato co-paying:**

| Metric | Implication |
|:---|:---|
| Avg. worker acquisition cost | ₹800–₹1,200 per new partner |
| Avg. churn during monsoon season | 18–22% of active partners |
| TrueDelivery co-pay cost to platform | ₹25/worker/week (₹100/month) |
| Churn reduction (estimated) | 8–12% through weather disruptions |
| Net saving per retained worker | ₹700–₹1,100 vs. recruiting cost |

Platforms save more money retaining protected workers than they spend co-paying premiums. The business case writes itself — and TrueDelivery's **B2B2C distribution model** turns platforms into the primary distribution channel, dramatically reducing customer acquisition cost.

---

### Model 3 — Earnings Auto-Deduct (Zero Friction)

```
Ravi earns ₹4,200 this week
Swiggy auto-deducts ₹49 before weekly settlement
Ravi receives ₹4,151 — already fully insured. Zero decision required.
```

Functionally identical to how EPF works. The worker is permanently protected with no active thought required. Opt-out is available but requires deliberate action — behavioral inertia works in the worker's favor.

---

### 🛟 Zero-Balance Safety Net

A worker lets their policy lapse due to a lean week. A disruption hits anyway.

- TrueDelivery issues a **one-time emergency micro-payout of ₹100** — no premium on file
- Recovered automatically from their next premium payment
- No worker is ever left completely without a safety net

> This is not charity — it is a retention mechanism and a human-dignity design principle.

---

## 🔄 Application Workflow & User Journey

```
┌──────────────────────────────────────────────────────────────────┐
│                        WORKER JOURNEY                             │
├──────────────────────────────────────────────────────────────────┤
│                                                                  │
│  STEP 1 · ONBOARD                                                │
│  ─────────────────                                               │
│  Mobile OTP login → Link Swiggy/Zomato Worker ID                 │
│  Select operating zones on HyperZone Map                         │
│  Declare average weekly earnings                                 │
│  AI generates personalized Risk Profile Score (0–100)            │
│  System recommends coverage tier based on zone + earnings        │
│                                                                  │
│  STEP 2 · SUBSCRIBE                                              │
│  ──────────────────                                              │
│  View AI-calculated weekly premium (with full factor breakdown)  │
│  Pay via UPI / auto-deduct from platform earnings                │
│  Policy confirmation sent via SMS + in-app notification          │
│  Policy active for exactly 7 days from payment                   │
│                                                                  │
│  STEP 3 · WORK NORMALLY                                          │
│  ─────────────────────                                           │
│  TrueDelivery silently monitors 5 triggers in real time          │
│  HyperZone Map shows live zone color status                      │
│  Earnings Forecast Widget shows tomorrow's disruption risk       │
│  Weekly streak counter visible on home screen                    │
│                                                                  │
│  STEP 4 · DISRUPTION DETECTED (happens without worker action)    │
│  ──────────────────────────────────────────────────────────────  │
│  Parametric trigger crosses verified threshold                   │
│  Worker zone confirmed as affected by pin code matching          │
│  Fraud check pipeline runs silently (<5 seconds)                 │
│  Claim auto-initiated — worker receives notification             │
│  Message: "Rain disruption detected in your zone. Processing     │
│            your income protection payout now."                   │
│                                                                  │
│  STEP 5 · PAYOUT DECISION                                        │
│  ────────────────────────                                        │
│  🟢 Risk Score 0–40:   Instant UPI payout (~80% of all claims)  │
│  🟡 Risk Score 41–70:  2-hour soft hold → Auto-approved          │
│  🔴 Risk Score 71–100: One 10-second selfie video verification   │
│                                                                  │
│  STEP 6 · POST-PAYOUT DASHBOARD                                  │
│  ────────────────────────────                                    │
│  Earnings protected this week · Active policy status             │
│  Payout history · Zone safety alerts · Streak progress           │
│  Next week's weather risk forecast                               │
│  Payout Split Intelligence — worker controls routing rules       │
│                                                                  │
└──────────────────────────────────────────────────────────────────┘
```

---

## 📊 Weekly Premium Model & Pricing Engine

TrueDelivery uses a **dynamic weekly premium** model synchronized with the gig economy's natural weekly earnings cycle.

### Design Philosophy: Why Weekly?

Traditional insurance operates on annual or monthly cycles — entirely misaligned with how gig workers earn and budget. Delivery partners are settled **weekly** by Zomato and Swiggy. A weekly premium:

- Aligns with actual cash flow patterns — no annual commitment anxiety
- Allows workers to pause during personal leave or low-earning weeks without penalty
- Creates a "recharge" mental model that India's smartphone users already understand deeply
- Enables dynamic premium adjustment week-over-week based on real-time conditions

### Premium Formula

```
Weekly Premium = Base Premium
              × Zone Risk Factor        (flood history, elevation, topology)
              × Seasonal Multiplier     (monsoon +, summer heat +, winter -)
              × Claim History Factor    (past 12 weeks rolling window)
              × Coverage Tier Modifier  (Basic / Standard / Pro)
```

All factors visible to the worker — no black box. Every rupee of premium change explained in plain Hinglish.

### Coverage Tiers

| Tier | Weekly Premium | Max Weekly Payout | Hourly Rate Coverage | Best For |
|:---|:---|:---|:---|:---|
| Basic Shield | ₹35 – ₹49 | ₹1,800 | Up to ₹60/hr | Part-time / new workers |
| Standard Shield ⭐ | ₹49 – ₹89 | ₹2,700 | Up to ₹80/hr | Full-time partners (most common) |
| Pro Shield | ₹89 – ₹120 | ₹4,000 | Up to ₹120/hr | High-earning veterans |

> **All tiers capped at under 2% of average weekly declared earnings** — affordability is a first-class constraint in the pricing model, not an afterthought.

### Dynamic Premium Adjustment Matrix

| Factor | Direction | Premium Impact |
|:---|:---|:---|
| Flood-prone zone (e.g. Old City Hyderabad, Dharavi Mumbai) | ↑ | +₹5 to +₹15/week |
| Active monsoon season (June – September) | ↑ | +₹8/week |
| High-disruption city tier (Delhi, Mumbai, Chennai) | ↑ | +₹10/week |
| Loyalty: 3+ consecutive months active | ↓ | −₹5/week |
| No-claim streak: 4 consecutive weeks | ↓ | −₹3/week |
| No-claim streak: 8+ consecutive weeks | ↓ | −₹6/week |
| Worker refers a new subscriber | ↓ | −₹4 one-time |

### Payout Calculation Formula

```
Hourly Rate = Weekly Earnings ÷ 7 days ÷ Daily working hours declared

Payout = Hourly Rate × Disrupted Hours (verified by trigger timestamps)

Example:
  Worker earns ₹4,200/week, works 8 hrs/day
  Disruption lasts 4 hours (confirmed by trigger end signal)
  
  Hourly rate = ₹4,200 ÷ 7 ÷ 8 = ₹75/hr
  Payout = ₹75 × 4 = ₹300
```

Maximum weekly payout is capped at tier limit. Partial disruptions are calculated pro-rata to the hour. There is no minimum disruption threshold below which a claim is denied — if a trigger fires for 45 minutes, 45 minutes is paid.

---

## ⚙️ Parametric Trigger Engine

Five automated, real-time triggers continuously monitor environmental and platform conditions. The moment any threshold is breached within a worker's registered zone, a claim pipeline is initiated **without any action from the worker**. No form. No upload. No call.

### Trigger Specifications

| # | Trigger | Primary Source | Secondary Validation | Threshold | Impact |
|:---|:---|:---|:---|:---|:---|
| 1 | Heavy Rainfall | OpenWeatherMap API | IMD Alert feed | >50mm/hr **OR** Official Red Alert issued | Deliveries halted, roads impassable |
| 2 | Extreme Heat | OpenWeatherMap API | Feels-like index | >43°C sustained for 2+ hours | Outdoor work unsafe, advisory issued |
| 3 | Severe AQI | AQICN.org API | PM2.5 sensor cross-check | AQI >400 (Severe+ category) | Platform suspends outdoor operations |
| 4 | Curfew / Bandh / Strike | Govt Alert Mock API | News API cross-signal | Official advisory published | Zone access blocked by authorities |
| 5 | Platform Outage | Zomato/Swiggy Mock API | Order volume analytics | Order volume drops >80% in zone for 2+ hrs | No orders available; workers idle |

### Multi-Signal Confirmation (Anti-False-Positive Design)

For Triggers 1–4, a single API signal alone does not initiate a claim. TrueDelivery requires **dual-signal confirmation** — the primary source must be validated by at least one secondary signal before the claim pipeline fires. This prevents API errors, data anomalies, or brief sensor glitches from generating false payouts.

For Trigger 5 (Platform Outage), order volume data serves as the primary and the platform's own status communication serves as secondary.

### Zone Matching Engine

Every trigger event is mapped to a set of affected pin codes. When a trigger fires:

1. Affected pin codes are extracted from the event's geographic boundary
2. TrueDelivery's worker registry is queried for all policy-holders with registered zones overlapping the affected area
3. Only matching workers enter the claim pipeline
4. Workers outside the geographic impact area are explicitly excluded — preventing false claims from adjacent zones

---

## 🚀 Worker Experience & App Features

### 1. HyperZone Live Map 🗺️

A real-time color-coded map overlay of the worker's city, updated every 5 minutes during active monitoring windows.

| Zone Color | Status | Worker Meaning |
|:---|:---|:---|
| 🟢 Green | Clear | Safe to work; full earnings expected |
| 🟡 Yellow | Watch | Mild disruption forming; monitoring active |
| 🔴 Red | Active Disruption | Claim auto-triggered; payout processing |
| ⬛ Grey | No Coverage | Outside worker's registered zones |

Workers can tap any zone for a tooltip: *"Heavy rain detected. Payout threshold reached. ₹225 processing to your UPI now."*

The HyperZone Map also serves as a **planning tool** — before starting a shift, workers can see which zones are forecast to be disrupted, enabling smarter routing decisions.

---

### 2. Earnings Forecast Widget 📈

A predictive widget on the app's home screen that surfaces tomorrow's risk before it becomes today's problem.

Example outputs:
- *"Tomorrow: 68% chance of heavy rain in your registered zone (6 AM – 2 PM)"*
- *"High disruption week ahead. Recommend upgrading to Pro Shield — extra ₹800 coverage for ₹40 more."*
- *"This weekend looks clear. Great week to ride."*

Powered by OpenWeatherMap forecast API + proprietary disruption ML model. The Forecast Widget turns TrueDelivery from a passive insurance product into an **active financial planning companion** for delivery partners.

---

### 3. Hinglish Voice Assistant 🎙️

Full accessibility for the 60%+ of delivery partners who are low-literacy or prefer audio interfaces. Workers can ask questions naturally in Hindi, Hinglish, or regional language.

**Example interactions:**

> Worker: *"Aaj kitna milega agar barish ho?"*
> App: *"Bhai, agar 3 ghante rain disruption hoti hai aur aap Standard Shield pe ho, toh ₹225 directly aapke UPI mein aa jayega!"*

> Worker: *"Mera claim kab tak aayega?"*
> App: *"Aapka claim processing mein hai. 2 minute mein paise aapke PhonePe mein honge."*

> Worker: *"Is hafte premium kitna katega?"*
> App: *"₹49 — monsoon season ki wajah se ₹8 zyada hai is hafte. Aapki loyalty discount bhi apply hui hai."*

Powered by device speech-to-text + Claude API for natural language understanding and response generation.

---

### 4. Instant Payout Countdown ⏱️

```
╔════════════════════════════════════════╗
║  ✅  CLAIM APPROVED                    ║
║                                        ║
║  💰  ₹285 incoming to your UPI         ║
║                                        ║
║  [████████████░░░░░░] 67%              ║
║                                        ║
║  Arriving in:    00:43 seconds         ║
║  Account:        Ravi Kumar — SBI UPI  ║
║  Reference:      TD-BLR-20260418-4821  ║
╚════════════════════════════════════════╝
```

The countdown creates a tangible, visceral sense of the product working. This is not a confirmation email. This is money arriving in real time, on screen, while the worker watches.

---

### 5. Weekly Streak Rewards 🏆

Gamified retention system that rewards loyalty with tangible financial benefits:

| Streak Milestone | Status Badge | Benefit |
|:---|:---|:---|
| 4 consecutive weeks | 🥉 Loyal Rider | −₹5 discount on next week's premium |
| 8 consecutive weeks | 🥈 TrueWarrior | Priority payout (30-second guarantee) |
| 12 consecutive weeks | 🥇 TrueChampion | One free premium week annually + referral bonus |

Streaks are preserved even in weeks where a disruption occurs — only voluntary non-renewal breaks a streak. Workers are never penalized for receiving a payout.

---

### 6. Payout Split Intelligence 💳

Workers define custom financial routing rules for their payouts — bringing basic wealth management tools to people who have never had access to them.

Examples of split rules a worker can set:
- *"Send ₹200 to PhonePe (fuel), remainder to savings account"*
- *"If payout > ₹500, move 20% to my savings jar automatically"*
- *"Send entire payout to family account if disruption is more than 6 hours"*

Financial wellness infrastructure built natively into an insurance product — not bolted on as an afterthought.

---

### 7. Admin & Insurer Dashboard 📊

A separate web-based dashboard (React + Tailwind) for the insurer/admin operator:

- Real-time claim pipeline visualization by city and zone
- Fraud alert queue with investigation tools
- Weekly premium pool vs. payout liability tracking
- Loss ratio by city, tier, and season
- Predictive disruption forecast for next 7 days (liquidity planning)
- Worker cohort analysis — churn risk, upgrade opportunities, streak patterns

---

## 🧠 AI/ML Architecture

### Module 1 — Risk Profiling Engine

| Property | Detail |
|:---|:---|
| Algorithm | Gradient Boosted Decision Tree (XGBoost) |
| Training inputs | Worker zone history, city tier, platform affiliation, seasonal patterns, historical claim rate per zone, weather volatility index |
| Output | Risk Score 0–100 → feeds weekly premium calculation and payout tier routing |
| Update cadence | Retrained every Sunday night; applied Monday morning for the new week |
| Transparency layer | Every score is explainable — each factor's contribution shown to worker on request |

---

### Module 2 — Dynamic Premium Calculator

| Property | Detail |
|:---|:---|
| Model type | Constrained regression with zone-level multiplicative weighting |
| Hard constraint | Premium never exceeds 2% of declared weekly earnings |
| Transparency | Worker sees a factor-by-factor premium breakdown on subscription screen |
| Edge case handling | New workers with no zone history receive the city-level base rate for 4 weeks before personalization kicks in |

---

### Module 3 — Fraud Detection Model

| Property | Detail |
|:---|:---|
| Algorithms | Isolation Forest (anomaly detection) + deterministic rule engine |
| Signal inputs | Device fingerprint, GPS vs. cell tower delta, accelerometer, WiFi SSID, Mock Location API flag, behavioral history, zone history, claim timing patterns |
| Output | Fraud Risk Score → 🟢 Auto-approve / 🟡 Soft hold / 🔴 Verification required |
| Processing time | < 5 seconds from claim initiation to decision |
| False positive design | Tuned to minimize false positives; genuine workers in storm conditions may show weak device signals — this alone is never grounds for denial |

---

### Module 4 — Digital Twin Behavioral Model

| Property | Detail |
|:---|:---|
| Model type | Unsupervised behavioral clustering (k-means / DBSCAN) per worker ID |
| Training window | Rolling 4-week zone activity history |
| Features tracked | Zone frequency, working hours, movement speed distribution, battery usage patterns, delivery platform login sessions |
| Purpose | Claims that are behaviorally inconsistent with a worker's established profile are flagged — a worker who has never delivered in a zone for 6 weeks suddenly claiming from that zone is a strong signal |
| Privacy note | Behavioral data is aggregated and anonymized for model training; individual profiles are used only for claim verification |

---

### Module 5 — Predictive Disruption Forecasting (Admin)

| Property | Detail |
|:---|:---|
| Algorithms | Facebook Prophet (time-series) + LSTM for extreme event detection |
| Purpose | Predict next 7 days' likely claim volume by city and zone for liquidity reserve management |
| Consumer | Insurer admin dashboard — proactive capital allocation |
| Inputs | Historical disruption data, IMD seasonal forecasts, city-level weather patterns, platform outage history |

---

## 🛡️ Adversarial Defense & Anti-Spoofing

> This section directly addresses the GPS-spoofing syndicate attack vector outlined in the Guidewire DEVTrails 2026 problem document.

### The Threat Model

Organized fraud rings coordinate via Telegram and WhatsApp to mass-spoof GPS coordinates into verified disruption zones, triggering false parametric payouts and draining the shared insurance pool — without any members leaving home. Because parametric insurance triggers automatically on data, the attack surface is different from traditional claims fraud.

**The attacker's advantages:**
- GPS can be spoofed cheaply with freely available apps
- Parametric triggers fire automatically — no human adjuster to deceive
- Coordinated timing exploits pool mechanics

**The attacker's fundamental limitation:**
> A fraudster can fake GPS. They cannot simultaneously fake GPS, device sensors, network environment, behavioral history, zone history, and cell tower location — all of which are independently logged and cross-referenced.

---

### The Seven-Layer Anti-Spoofing Stack

| Layer | Signal | Genuine Worker | Spoofer |
|:---|:---|:---|:---|
| **L1** Device | Mock Location API flag | OFF | ON (detected immediately) |
| **L2** Network | WiFi SSID type | Mobile data (storm degrades signal) | Home broadband SSID |
| **L3** Hardware | Accelerometer / gyroscope | Movement patterns consistent with sheltering outdoors | Stationary at home |
| **L4** Telecom | Cell tower triangulation | Consistent with GPS zone | Contradicts GPS coordinates |
| **L5** Platform | Delivery app activity | Logged in; no orders in queue | App may be closed or inactive |
| **L6** Behavioral | 4-week zone history | Has delivered in this zone regularly | May have never worked there |
| **L7** AI Twin | Digital Twin consistency | Behavioral profile matches | Statistically inconsistent |

**Key insight:** No single signal is definitive. The system requires corroboration across independent layers. A genuine worker caught in a storm may fail one or two checks (e.g., weak mobile signal, slower movement). They will not fail six of seven.

---

### Defense Architecture (Four Layers)

**Layer 1 — Device Intelligence**

- Android Mock Location API flag (OS-level detection, not spoofable without root)
- WiFi SSID type analysis — outdoor workers during disruptions are on mobile data, not home WiFi
- Accelerometer and gyroscope pattern analysis — stationary vs. movement profile matching
- Battery drain pattern profiling — storm conditions affect battery differently
- IP geolocation cross-verification against GPS coordinates

**Layer 2 — Behavioral & Historical Intelligence**

- Rolling 4-week zone delivery history per worker
- Sudden first-time claims from previously unvisited zones: immediate flag
- Time-of-day pattern matching against established work schedule
- Platform login session verification — is the delivery app open and actively waiting for orders?
- Digital Twin behavioral consistency score

**Layer 3 — Environmental Cross-Validation**

- Weather API confirmation: does the claimed disruption actually exist at the claimed pin code?
- Order volume analysis: did platform orders actually decrease in the claimed zone and time window?
- Independent news API signal: is the disruption independently reportable?
- Spatial propagation check: is the weather event consistent with its claimed boundaries?

**Layer 4 — Syndicate Detection (Coordination Attack Defense)**

- Cluster analysis: 15+ claims within 100m of the same GPS coordinate within 5 minutes → auto-freeze all
- Device fingerprint deduplication: same physical device registered under multiple Worker IDs
- IP subnet analysis: multiple simultaneous claimers sharing the same internet connection
- Temporal clustering: statistically impossible claim submission timing (all within 90 seconds from a Telegram blast)
- Network graph analysis: shared device IDs, linked phone numbers, or shared payment accounts across a cluster

> **The fundamental detection heuristic:** In a genuine flood event, hundreds of workers file claims from different GPS coordinates across a zone, over a period of 30–120 minutes, on different network connections. In a coordinated fraud ring, claims arrive from a single coordinate within seconds, often from the same subnet. This statistical pattern is the system's strongest and most reliable signal.

---

### Fraud Risk Tier UX Design

**Core principle: Innocent until data proves otherwise. Verify silently. Never accuse.**

> ⚠️ Network degradation during a genuine storm is expected and normal. A failed WiFi check alone is never grounds for denial. The system is calibrated to accept imperfect signals from genuine workers under difficult conditions.

| Tier | Risk Score | Action | Worker Experience | % of Total Claims |
|:---|:---|:---|:---|:---|
| 🟢 Auto-Approve | 0–40 | Instant UPI payout | Countdown timer. Done. | ~80% |
| 🟡 Soft Hold | 41–70 | 2-hour hold → Auto-approved | "Confirming your location signal. Payment in ~2 hours." | ~15% |
| 🔴 Verify | 71–100 | 10-second selfie video | "Quick signal check needed. Record 10 sec showing your surroundings." | ~5% |

**Worker-Facing Language Policy**

The language of fraud detection is never exposed to the worker. The system's internal classifications remain internal.

| Internal Term | Worker-Facing Term |
|:---|:---|
| Fraud score elevated | Signal verification in progress |
| GPS spoofing suspected | Confirming your location |
| Syndicate detection triggered | Processing with additional checks |
| Claim frozen | Your payment is being processed — this can take up to 2 hours |

A genuine worker held at the 🟡 tier experiences a 2-hour delay — inconvenient, not devastating. A fraudster at the 🔴 tier cannot produce a 10-second video of a flooded street from their dry apartment.

---

## 💼 Business Model & Unit Economics

### Revenue Architecture

| Revenue Stream | Mechanism | Margin Profile |
|:---|:---|:---|
| Premium float | Collect weekly premiums; invest float in short-duration instruments | 4–6% annualized on float |
| Operational margin on loss ratio | Claims paid < premiums collected; target loss ratio 70–80% | 20–30% gross margin |
| Platform co-pay SaaS fee | B2B2C licensing fee for platform integration and co-pay program management | High-margin recurring |
| Data licensing (anonymized) | Disruption pattern analytics sold to insurers and urban planners (opt-in) | Pure margin |

### Unit Economics (Per Worker, Steady State)

| Metric | Value |
|:---|:---|
| Average weekly premium (Standard Shield) | ₹60 |
| Expected claim rate per worker per year | 6–8 weeks of disruption |
| Average payout per disruption event | ₹350 |
| Annual premium collected per worker | ₹3,120 |
| Annual claims paid per worker | ₹2,450 |
| **Gross margin per worker per year** | **₹670 (~21%)** |
| Customer acquisition cost (platform B2B2C) | ₹0 – ₹120 (platform-subsidized) |
| LTV (3-year assumed) | ₹2,010 |
| **LTV/CAC ratio** | **>16x** |

### Market Size

| Segment | Size |
|:---|:---|
| Total active food delivery workers (India) | ~5.5 million |
| Addressable via platform partnerships (Zomato + Swiggy) | ~4.2 million |
| Year 1 target (8 cities, Standard Shield) | 50,000 workers |
| Year 1 premium revenue target | ₹9.4 Cr |
| Year 3 target | 500,000 workers |
| Year 3 premium revenue target | ₹94 Cr |
| **Total Addressable Market (India, all gig verticals)** | **₹2,400 Cr/year** |

---

## 🔧 Tech Stack

| Layer | Technology | Rationale |
|:---|:---|:---|
| Mobile App | Flutter | Single codebase for iOS + Android; high performance on entry-level Android |
| Web Dashboard | React + Tailwind CSS | Component-based, fast iteration, real-time dashboard rendering |
| Backend | Node.js + Express | Lightweight, non-blocking I/O ideal for high-concurrency claim pipeline |
| Database | Firebase Firestore | Real-time sync, sub-100ms reads for live claim status updates |
| AI/ML Service | Python · scikit-learn · XGBoost | Fraud detection and risk scoring as isolated microservice |
| Weather Data | OpenWeatherMap API (free tier) | Real-time precipitation, temperature, alerts; pin code–level resolution |
| Air Quality | AQICN.org API (free tier) | City and zone-level AQI; supports Delhi, Mumbai, Hyderabad, all Tier-1 cities |
| Alerts | NewsAPI + Govt. alert mock | Curfew, bandh, and strike event detection |
| Platform Data | Simulated/Mock API | Zomato/Swiggy order volume simulation (pending partnership for live data) |
| Payments | Razorpay Test Mode | UPI payout simulation, countdown, and split routing |
| Maps | Google Maps API | HyperZone visualization, zone drawing, GPS validation |
| Authentication | Firebase Auth (OTP) | Mobile number–based login; no email required for accessibility |
| Voice Assistant | Claude API + Device STT | Hinglish natural language queries and dynamic response generation |
| Hosting | Vercel (frontend) + Railway/Render (backend) | Zero-DevOps deployment for hackathon phase; scalable on GCP post-validation |

---

## 🗓️ Development Roadmap

### Phase 1 — Ideation & Foundation `March 4–20, 2026` ✅ COMPLETE

- [x] Deep research into delivery partner income patterns and disruption frequency
- [x] Core architecture and system design (parametric + fraud hybrid)
- [x] Weekly premium model and all three payment model designs
- [x] Parametric trigger identification, threshold research, and API source validation
- [x] Feature ideation — HyperZone Map, Voice Assistant, Streak Rewards, Payout Split
- [x] Adversarial threat modeling and seven-layer anti-spoofing defense design
- [x] Full README documentation and project scaffolding

### Phase 2 — Build & Protect `March 21 – April 4, 2026`

- [ ] Worker onboarding flow (Flutter mobile app — OTP login, zone selection, tier selection)
- [ ] HyperZone Live Map integration (Google Maps + real-time trigger overlay)
- [ ] AI weekly premium calculator with full risk scoring and factor breakdown display
- [ ] Policy creation, management, and cancellation screens
- [ ] All 5 parametric trigger integrations (Weather, AQI, Govt alerts, Platform mock, News)
- [ ] Three-tier fraud detection pipeline (Green / Yellow / Red routing)
- [ ] Claims pipeline and claim status screens
- [ ] Instant payout countdown (Razorpay test mode + UPI split routing)
- [ ] Earnings Forecast Widget with 7-day weather integration

### Phase 3 — Scale & Differentiate `April 5–17, 2026`

- [ ] Digital Twin fraud detection model (4-week behavioral profile per worker)
- [ ] Telegram Honeypot Monitor and syndicate cluster detection (simulated)
- [ ] Crowd Consensus Validator (zone-level claim density analysis)
- [ ] Hinglish Voice Assistant full integration (Claude API + STT)
- [ ] Weekly Streak Rewards system and loyalty discount engine
- [ ] Payout Split Intelligence (custom routing rules per worker)
- [ ] Zero-Balance Safety Net (emergency micro-payout flow)
- [ ] Worker dashboard (complete — earnings, coverage, forecast, payout history)
- [ ] Admin/insurer dashboard (claim pipeline, fraud queue, loss ratio, predictive analytics)
- [ ] Final 5-minute demo video production
- [ ] Final pitch deck (PDF, investor-ready)

---

## 🎯 Target Market & Expansion Strategy

### Launch Market

| Dimension | Details |
|:---|:---|
| Geography | 8 Tier-1 Indian cities: Delhi · Mumbai · Bengaluru · Hyderabad · Chennai · Pune · Kolkata · Ahmedabad |
| Platform partners | Zomato and Swiggy (combined ~85% market share in food delivery) |
| Target segment | Active full-time delivery partners earning ₹3,000–₹7,000/week |
| Distribution | B2C (self-enroll via app) + B2B2C (platform co-pay partnership) |
| Revenue model | Weekly premium + platform SaaS licensing fee |

### Expansion Roadmap

| Phase | Timeline | Scope |
|:---|:---|:---|
| 🏙️ Metro 8 Launch | Year 1 | 50,000 workers across 8 cities; Zomato/Swiggy integration |
| 🌆 Tier-2 Expansion | Year 2 | Jaipur, Lucknow, Chandigarh, Indore, Bhubaneswar + 20 cities |
| 🛵 Vertical Expansion | Year 2–3 | Blinkit / Zepto (quick commerce), Rapido, Porter, Dunzo couriers |
| 🌏 SEA Expansion | Year 3–4 | Indonesia (GoFood / ShopeeFood), Vietnam (GrabFood), Bangladesh |
| 🏗️ Product Extension | Year 3+ | Parametric income insurance for auto-rickshaw drivers, domestic workers, daily wage laborers |

---

## ⚖️ Regulatory & Compliance Considerations

### Insurance Regulatory Context

TrueDelivery operates in a space that intersects insurance regulation, fintech, and gig economy policy in India. Key considerations for the production path:

| Requirement | Status | Notes |
|:---|:---|:---|
| IRDAI Micro-Insurance Product Framework | Required | TrueDelivery fits the IRDAI micro-insurance category (sum assured < ₹50,000); special dispensation pathway exists |
| Insurance Intermediary License | Required | TrueDelivery can operate as a distribution platform for a licensed insurer as the underwriter |
| UPI payout compliance | Required | Razorpay and PhonePe have existing NPCI compliance; partnership model avoids direct licensing |
| DPDP Act 2023 (data privacy) | Required | Behavioral data collection requires explicit consent; handled at onboarding with clear opt-in UI |
| Gig Worker Code (Draft) | Monitor | India's draft social security code for gig workers, if passed, creates formal mandate for income protection — tailwind for TrueDelivery's adoption |

### Underwriting Partnership Model

For the hackathon demo, TrueDelivery simulates the full stack. In production, TrueDelivery operates as:

```
TrueDelivery (InsurTech Distribution + AI Platform)
      ↓
Partner Insurer (Licensed underwriter — e.g. ICICI Lombard, New India Assurance, Digit Insurance)
      ↓
Delivery Workers (Policy holders)
```

This separation allows TrueDelivery to focus on technology, distribution, and fraud detection while the licensed partner carries the regulatory liability for actual insurance products.

---

## 👥 Team

| Name | Role |
|:---|:---|
| **Sohan Kumar Sahu** | **Product Architect & Data Systems Lead (Team Lead)** |
| **Abu Sufian Choudhury** | **Backend & DevOps Engineer** |
| **Samarth V Ratnam** | **Product Strategist & UI/UX Designer (Pitch Lead)** |
| **T Deepak Kumar Patro** | **Frontend Engineer** |
| **Salagrama Shanmukha Chintamani Sharma** | **Backend API Engineer** |

---

*A cross-functional team specializing in scalable system architecture, API-driven backend services, intuitive frontend design, and impactful product storytelling.*

---

## 🔗 Pitch Deck

| Resource | Link |
|:---|:---|
| 🌐 Deployed App | [true-delivery-frontend.vercel.app](https://true-delivery-frontend.vercel.app) |
| 📊 Pitch Video | [Google Drive — Demo & Pitch](https://drive.google.com/drive/folders/1yeAbwHa1GqDLBN3__cqnex91eQciRlng?usp=sharing) |
| 🔗 GitHub Repository | [TrueDelivery — Guidewire DEVTrails](https://github.com/lazy0ne369/TrueDelivery_Guidewiredevtrails.git) |

---

<div align="center">

**Built for Guidewire DEVTrails 2026 University Hackathon**

*Theme: Seed. Scale. Soar.*

<br/>

*TrueDelivery — because every ride deserves a safety net.*

</div>
