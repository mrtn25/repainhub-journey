# 🔧 RepairHub – Interactive Customer Journey

An interactive, scene-based customer journey game for the **RepairHub** smartphone repair concept — built as part of the Operations Management Capstone Project at **Católica Lisbon Business & Economics** (Postgraduate 2025/2026).

## 🎮 What is this?

A choose-your-own-path web experience that walks customers through the RepairHub process:

1. 😱 Your phone breaks
2. 🏪 You arrive at the store
3. 📷 Camera + tablet diagnosis at the counter
4. 🤖 AI checks parts & technician availability
5. 💬 You receive a personalised quote
6. ⚡ Decision: Same-day repair, schedule, or leave
7. 🔧 Repair in progress
8. 🎉 Pickup — phone is fixed!

Each step is annotated with its **Operations Management concept** (Flow Rate, Buffers, Activities, ROP, VUT Queueing, etc.)

## 🚀 Deploy

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/mrtn25/repainhub-journey)

## 📁 Structure

```
/
├── index.html            # Full interactive journey (self-contained)
├── public/
│   └── images/           # Drop Gemini scene images here
│       ├── scene-0-broken-phone.jpg
│       ├── scene-1-store-exterior.jpg
│       ├── scene-2-counter-camera.jpg
│       ├── scene-3-ai-check.jpg
│       ├── scene-4-quote-tablet.jpg
│       ├── scene-5-repair-workshop.jpg
│       ├── scene-6-pickup.jpg
│       ├── scene-7-scheduled.jpg
│       └── scene-8-decline.jpg
├── GEMINI_PROMPTS.md     # Image generation prompts for each scene
└── README.md
```

## 🎨 Adding Scene Images

Generate images using the prompts in `GEMINI_PROMPTS.md`, save them to `public/images/`, then update the `bg` field in each SCENES entry in `index.html`:
```js
bg: "url('/images/scene-0-broken-phone.jpg') center/cover"
```

## 📐 OM Concepts Covered

| Scene | OM Concept |
|---|---|
| Arrival Queue | Buffer (WIP) |
| Counter | Activity — Registration & AI Diagnosis |
| AI Check | ROP Inventory + VUT Queueing Model |
| Quote | Single Customer Decision Point |
| Repair | Capacity Management, Utilization ρ < 85% |
| Scheduled Path | Demand-triggered replenishment |

---
*Built with HTML/CSS/JS · Deployed on Vercel · Católica Lisbon OM Capstone 2025/2026*