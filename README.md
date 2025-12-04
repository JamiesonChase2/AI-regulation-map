[Screenshot-2025-12-03-at-6-53-05-PM.png](https://postimg.cc/hfvy6gZg)

# AI Regulation Map & Scorecard

A data visualization dashboard tracking the landscape of Artificial Intelligence regulation in the United States.

This project provides an interactive interface for exploring state and federal AI policies, visualizing legislative activity across the country, and evaluating current regulatory frameworks against core ethical principles (such as the **AI Bill of Rights**).

---

## 🚀 Features

### 1. Interactive US Map (Geospatial Data)
- **Dynamic Visualization:** A D3.js-powered map of the United States where users can click individual states to load their legislative timelines.  
- **Visual Cues:** States with active data are highlighted, making regulatory hotspots obvious at a glance.

### 2. Dual Timeline Architecture
- **State Legislation:** Scrollable panel with dynamic bill summaries, status tags, and source links.  
- **Federal Timeline:** Animated vertical timeline showing major executive actions, guidance documents, and national AI milestones.

### 3. AI Bill of Rights Scorecard
- **Compliance Assessment:** A visual scorecard measuring national AI governance against the 5 principles of the AI Bill of Rights.  
- **5‑Tier Rating System:** Color‑coded scale (Green → Red) to reflect alignment.  
- **Rationale Section:** Card‑based explanations supporting each score.

### 4. Decoupled Data Architecture
- **JSON‑Driven:** All data lives in external files (`state-ai-legislation.json`, `federal-ai-events.json`), enabling updates without touching source code.

---

## 🛠️ Tech Stack

**Core:**  
- HTML5  
- CSS3 (custom properties)  
- Vanilla JavaScript (ES6+)

**Libraries:**  
- **D3.js** — renders the interactive US map  
- **TopoJSON** — lightweight map topology  
- **ScrollReveal** — scroll‑triggered animations  
- **Lucide Icons** — sharp SVG iconography  

---

## 📦 Setup & Usage

Because the site fetches local JSON files, it must run on a **local server** to avoid CORS issues.

### 1. Clone the Repository
```bash
git clone https://github.com/JamiesonChase2/AI-regulation-map.git
cd AI-regulation-map
```

### 2. Run a Local Server

**Python (recommended):**
```bash
python3 -m http.server 8000
```

**Node.js:**
```bash
npx serve
```

### 3. Open in Browser
Visit:  
```
http://localhost:8000
```

---

## 📂 Project Structure
```
├── index.html                 # Main UI shell & JS logic
├── state-ai-legislation.json  # State-level bills and events
├── federal-ai-events.json     # Federal AI actions & milestones
└── README.md                  # Documentation
```

---

## ✏️ Customization

### Updating Data

Edit the JSON files to add new legislation or events.

#### Example: `state-ai-legislation.json`
```json
"CA": {
  "name": "California",
  "events": [
    {
      "date": "2024-01-01",
      "title": "New Bill Title",
      "status": "Passed",
      "summary": "Description of the bill...",
      "links": [
        { "label": "Read Text", "url": "..." }
      ]
    }
  ]
}
```

#### Example: `federal-ai-events.json`
```json
[
  {
    "date": "2024-05-15",
    "title": "New Executive Order",
    "status": "Executive Action",
    "summary": "Details about the order...",
    "links": []
  }
]
```

---

## 📄 License
This project is open‑source and available under the **MIT License**.
