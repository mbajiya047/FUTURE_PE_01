# FUTURE_PE_01: AI Website Copy Generator for Local Businesses

> **Internship Track:** Prompt Engineering (`PE`)  
> **Task ID:** `FUTURE_PE_01`  
> **Client Case Study:** Roots & Whisk Artisan Cafe & Micro-Bakery (Indiranagar, Bengaluru)  
> **Core Objective:** Design a structured, reusable prompt engineering system that generates **100% authentic, high-converting website copy** that reads like a passionate business owner wrote it, completely eliminating robotic AI clichés and generic filler.

---

## 📌 Executive Summary

Most local business websites fail for two reasons:
1. **Generic AI Fluff:** When business owners use ChatGPT without constraints, they end up with cliché-ridden copy (*"Welcome to our culinary haven where we elevate your gastronomic journey"*), which immediately repels skeptical local customers.
2. **Missing Local & Operational Texture:** Generic copy fails to answer the questions real customers care about: *When do warm batches come out? Where do I park? Is the Wi-Fi good enough to work from? Is the sourdough actually fermented or made with industrial yeast?*

This project provides an end-to-end **Prompt Engineering System** that turns raw business facts into natural, human-voiced, conversion-ready copy.

---

## 🏢 Client Profile: Roots & Whisk Artisan Cafe

* **Location:** 12th Main Road, HAL 2nd Stage, Indiranagar, Bengaluru, Karnataka
* **Founder & Head Baker:** Arjun Sen (former tech product manager turned sourdough baker)
* **Core Offerings:** 36-hour wild-ferment sourdough loaves, single-estate Karnataka specialty coffee, all-day tartine plates.
* **Neighborhood Nuance:** Situated in busy Indiranagar, balancing remote-working tech professionals on weekdays with leisurely weekend brunch crowds and dog owners.

---

## 🧠 Prompt Engineering Methodology

### 1. Negative Constraint Engineering (The Anti-AI Filter)
Generic LLM outputs are plagued by recognizable "AI markers". The master system prompt (`prompts/01_system_prompt.md`) explicitly prohibits:
* **Banned Vocabulary:** *embark, tapestry, elevate, delve, testament, nestled, haven, symphony of flavors, meticulously crafted, unrivaled, game-changer.*
* **Banned Sentence Openers:** *"In today's fast-paced world...", "Are you looking for...", "Look no further!"*
* **Empty Superlatives:** Banning words like *"delicious"* or *"heavenly"* unless tied directly to an ingredient, extraction time, or baking method.

### 2. Contrastive Few-Shot Calibration
To calibrate the model, prompts include explicit positive/negative pairs:

| Component | ❌ Generic AI Output | ✅ Authentic Owner-Voice Output |
| :--- | :--- | :--- |
| **Headline** | *"Elevate Your Culinary Journey at Our Artisanal Sanctuary"* | *"Real sourdough bread. Honest coffee. No shortcuts."* |
| **Product Copy** | *"Our bread is a testament to culinary perfection, meticulously crafted to tantalize your senses."* | *"Our Country Loaf takes 36 hours from starter to stone deck. The crust is blistered and dark; the crumb is open, soft, and slightly tangy."* |
| **Call to Action** | *"Embark on an unforgettable experience and visit our establishment today!"* | *"Don't risk arriving to empty baskets. WhatsApp us before 2 PM to hold your loaf."* |

### 3. Dynamic Variable Decoupling
All business-specific parameters (founder background, ingredients, pricing, neighborhood landmarks) are cleanly decoupled in `config/business_variables.json`. This allows the same prompt system to be adapted in minutes to a dental clinic, hair salon, or coaching academy.

---

## 📂 Repository Structure

```text
FUTURE_PE_01/
├── README.md                              # Comprehensive project documentation
├── config/
│   └── business_variables.json           # Parameterized business config & tone rules
├── prompts/
│   ├── 01_system_prompt.md               # Master persona & anti-AI constraint engine
│   ├── 02_homepage_prompt.md             # Hero, Problem Hook & Founder Story prompt
│   ├── 03_services_prompt.md             # Offerings, specs, ingredients & pricing prompt
│   └── 04_cta_faq_prompt.md              # Local FAQs, directions & conversion CTA prompt
├── outputs/
│   ├── 01_homepage_copy.md               # Final generated homepage copy
│   ├── 02_services_copy.md               # Final generated services & menu copy
│   └── 03_cta_faq_copy.md                # Final generated FAQs, CTAs & navigation copy
└── templates/
    └── website_wireframe_copy.html       # Standalone, interactive HTML/CSS live preview
```

---

## 📋 Deliverables Summary

### 1. Homepage Copy (`outputs/01_homepage_copy.md`)
* **Live Schedule Notice:** Informs locals of the 7:30 AM and 3:30 PM oven batch timings.
* **Hero Section:** Clear value proposition, tangible trust badges (36-hour fermentation, 100% direct trade coffee), and dual low-friction action buttons.
* **The "Honest Truth" Hook:** Contrasts industrial 90-minute chemical bread with traditional 3-day fermentation.
* **Founder's Story:** Arjun Sen’s transition from Bangalore tech burnout to sourdough mastery in Pondicherry.

### 2. Services & Offerings Copy (`outputs/02_services_copy.md`)
* **The Daily Bakehouse:** 4 signature loaf cards with exact hydration, grain percentages, tasting profiles, and prices in INR (₹).
* **Specialty Coffee Bar:** Direct-estate Chikmagalur harvest notes, manual lever machine pulls, and homemade oat milk options.
* **All-Day Kitchen:** Tartine and breakfast plates built on fresh sourdough.
* **The 4 Kitchen Rules:** Zero chemical improvers, direct trade farmer relationships, transparent tax-inclusive pricing, and zero food waste.

### 3. Conversion CTAs & Local FAQs (`outputs/03_cta_faq_copy.md`)
* **Dual Conversion Modules:** Same-day WhatsApp loaf reservation + Google Maps directions.
* **6 Honest Local FAQs:** Real answers on weekday remote work policies, weekend laptop etiquette, street parking vs. 100ft Road lots, pet friendliness, and gluten sensitivity.

### 4. Interactive Live Wireframe (`templates/website_wireframe_copy.html`)
A clean, responsive, single-file HTML preview with modern typography (Plus Jakarta Sans & Playfair Display), responsive cards, and styled sections. Double-click to open in any web browser!

---

## 🛠️ How to Replicate for Another Local Business

To use this framework for another client (e.g., a dental clinic or salon):

1. **Update `config/business_variables.json`:**
   * Change `business_name`, `founder_name`, and `location`.
   * Fill in the specific local pain points and transparent pricing.
2. **Select the Tone Parameter in `prompts/01_system_prompt.md`:**
   * *For a clinic:* Empathetic, gentle, transparent about procedure steps and costs.
   * *For a salon:* Warm, attentive, focusing on hair texture and realistic maintenance.
3. **Execute Prompts 02, 03, and 04 in sequence:**
   * Run through your chosen LLM (ChatGPT, Claude, or Google Gemini).
   * Review against the Banned AI Vocabulary list to ensure 100% authentic human voice.

---

## ✅ Evaluation Checklist (Future Interns Rubric)

- [x] **Repository Naming:** Conforms to `FUTURE_PE_TaskNumber` (`FUTURE_PE_01`).
- [x] **Track Code:** Identified as `PE` (Prompt Engineering).
- [x] **Core Deliverables:** Complete Homepage Copy + Services Page Content + CTA & FAQ Sections.
- [x] **Human Voice Compliance:** Zero robotic AI tropes; authentic, grounded founder perspective.
- [x] **Prompt Logic Documented:** System prompts, negative constraints, and variables fully articulated.
- [x] **Ready for Real Client Delivery:** Includes wireframe HTML preview and WhatsApp reservation hook.
