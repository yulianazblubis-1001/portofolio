# How to Edit Your Portfolio Content

You can edit any `.html` file with a text editor (VS Code, Notepad, or even TextEdit).
Just search (Ctrl+F / Cmd+F) for the text you want to change, edit it, save, and refresh the browser.

---

## Quick Reference: What's Where

### index.html (Main Page)

| Section | What to search for | What you can change |
|---|---|---|
| Name/title in nav | `YULIANA LUBIS` | Your name |
| Hero headline | `drive real results` | Main headline text |
| Hero subtitle | `Senior Product Manager with 8+` | Your intro paragraph |
| Status badge | `Open to Senior PM` | Your current job status |
| Video | `Video Coming Soon` | Replace the whole div with a YouTube/Loom iframe |
| Metric: Experience | `8+` and `Years of Experience` | Number and label |
| Metric: Farmers | `9,300+` and `Farmers Served` | Number and label |
| Metric: Cashless | `1st` and `Real-time Cashless` | Number and label |
| Case Study 1 title | `Building a Complete Claim` | Rey.id card title |
| Case Study 2 title | `Collection System for 9,300+` | Rize Farm card title |
| Case Study 3 title | `A POS That Feels Like` | Zeepos card title |
| Working Together subtitle | `Every team is different` | Process section intro |
| Product DNA chips | Search for `chip` in the DNA section | Add/remove skill chips |
| Contact email | `yuliana.zb.lubis@gmail.com` | Your email |
| LinkedIn | `linkedin.com/in/yuliana-lubis` | Your LinkedIn URL |
| Calendly | `Book a Chat` section | Replace placeholder div with Calendly iframe |
| CV download | `cv.pdf` | Make sure cv.pdf file exists in folder |

### rey-id.html (Rey.id Case Study)

| Section | What to search for |
|---|---|
| Hero title | `Building a Complete Claim Ecosystem` |
| Hero description | `As PM, I owned the entire` |
| Problem section | `The Chicken-and-Egg Problem` |
| Decisions | `Decision 1:`, `Decision 2:`, `Decision 3:` |
| Results | `50%`, `+30%`, `-60%` |
| Learnings | `WHAT I LEARNED` |

### zeepos.html (Zeepos Case Study)

| Section | What to search for |
|---|---|
| Hero title | `A POS That Feels Like a Calculator` |
| Hero description | `This project changed my career` |
| Problem cards | `Cashiers have high school`, `High turnover`, `Internet = extra cost` |
| Key decision | `Make it feel like a calculator` |
| Trade-off | `The trade-off I accepted` |
| Edge cases | `EDGE CASES I HANDLED` |
| Learnings | `WHAT I LEARNED` |

### rize-collection.html (Rize Farm Case Study)

| Section | What to search for |
|---|---|
| Hero title | `From Reactive to Proactive` |
| Hero description | `Rize Farm provides seeds` |
| Problem section | `THE PROBLEM` |
| Key insight | `DAP 80` |
| What I Built | `WHAT I BUILT` |
| Pre-harvest meeting | `Pre-harvest Meeting` |
| Agronomist app | `Agronomist App` |
| Cohortly dashboard | `Cohortly Dashboard` |
| Key decisions | `Decision 1:`, `Decision 2:`, `Decision 3:` |
| Edge cases | `EDGE CASES I HANDLED` |
| Learnings | `WHAT I LEARNED` |

---

## How to Add Calendly

Replace the "Book a Chat" placeholder in index.html with:

```html
<iframe src="https://calendly.com/YOUR-USERNAME/30min"
  style="width: 100%; height: 480px; border: none; border-radius: 2rem;"
  loading="lazy">
</iframe>
```

## How to Add Video

Replace the "Video Coming Soon" placeholder in index.html with:

```html
<div class="bg-surface-container-lowest rounded-[2rem] overflow-hidden" style="min-height: 320px;">
  <iframe src="https://www.youtube.com/embed/YOUR-VIDEO-ID"
    style="width: 100%; height: 320px; border: none;"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>
```

## How to Add a New Case Study

1. Copy `zeepos.html` and rename it (e.g. `rize-farm.html`)
2. Edit the content inside
3. In `index.html`, find the matching case study card and update:
   - Change `href="#"` to `href="rize-farm.html"`
   - Change `Coming soon` to `Read case study`
   - Update the title and description

---

## File Names Reference

| File | What it is |
|---|---|
| `yuliana-sketch.png` | Profile sketch (hero banner) |
| `mindmap-transparent.png` | Process mind map (Working Together) |
| `intools-preadmission.png` | InTools screenshot 1 |
| `intools-admission.png` | InTools screenshot 2 |
| `intools-monitoring.png` | InTools screenshot 3 |
| `intools-payment.png` | InTools screenshot 4 |
| `reyid-mobile-app.jpeg` | Rey.id mobile app main menu |
| `reyid-outpatient.jpeg` | Rey.id outpatient flow |
| `reyid-inpatient.jpeg` | Rey.id inpatient flow |
| `reycard-blurred.jpeg` | ReyCard (digits blurred) |
| `zeepos-order.png` | Zeepos calculator screen |
| `zeepos-history.png` | Zeepos history screen |
| `cohortly-overview.jpeg` | Cohortly dashboard overview (blurred) |
| `cohortly-detail.jpeg` | Cohortly collection details (blurred) |
