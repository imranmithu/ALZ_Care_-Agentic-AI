# 🧠 ALZ-CARE: Adaptive Resilience Ecosystem

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Status: Prototype](https://img.shields.io/badge/Status-Prototype-orange.svg)]()
[![Agents: 5](https://img.shields.io/badge/AI%20Agents-5-green.svg)]()
[![Bilingual: EN/ES](https://img.shields.io/badge/Bilingual-EN%20%7C%20ES-purple.svg)]()

**An Agentic AI System for Rural ADRD Caregiver Support**

ALZ-CARE is a multi-agent artificial intelligence platform designed to support caregivers of individuals with Alzheimer's Disease and Related Dementias (ADRD), particularly in rural and underserved communities. The system integrates environmental monitoring, wearable vital signs, telemedicine interoperability, and community resources through five specialized AI agents coordinated by a central orchestration layer.

### Demo Mode
The current version runs in demo mode with sample patient data (Eleanor Mitchell). All features are fully interactive for testing and demonstration purposes.

Demo Link:https://imranmithu.github.io/ALZ_Care_-Agentic-AI/
---

## 📋 Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [The Five AI Agents](#the-five-ai-agents)
- [Technology Stack](#technology-stack)
- [Installation](#installation)
- [Usage](#usage)
- [API Integrations](#api-integrations)
- [Bilingual Support](#bilingual-support)
- [Research Background](#research-background)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

---

## 🎯 Overview

### The Problem

- **11.5 million Americans** provide **18.4 billion hours** of unpaid ADRD care annually
- Rural caregivers face geographic isolation, limited healthcare access, and heavy reliance on telemedicine
- Extreme heat increases ADRD-related ED visits by **18-24%**
- Telemedicine data remains siloed and inaccessible to local emergency providers
- Existing digital tools offer static resources without real-time, personalized support

### Our Solution

ALZ-CARE deploys five specialized AI agents that work collaboratively to:
- Monitor environmental threats and translate them into personalized caregiving guidance
- Continuously track patient vital signs and detect early warning signs
- Provide multilingual decision support and telemedicine visit preparation
- Integrate health data across providers using FHIR interoperability standards
- Connect households to local resources and community health workers

---

## ✨ Key Features

### Real-Time Monitoring
- Live environmental data (AQI, heat index, UV, pollen)
- Continuous vital signs from smartwatch integration
- Behavioral pattern detection and correlation analysis

### Intelligent Alerts
- Personalized heat and air quality advisories
- Early warning detection for health deterioration
- Proactive care recommendations based on multi-source data

### Telemedicine Integration
- FHIR R4 compliant data exchange
- Automated visit summaries for providers
- Unified patient record across care settings

### Caregiver Support
- Multilingual interface (English/Spanish)
- Daily care tips based on environmental and health data
- One-click concern reporting to community health workers
- ADRD education resources

### Agent Orchestration
- Visual real-time agent activity monitoring
- Cross-agent communication and coordination
- Data flow visualization

---

## 🤖 The Five AI Agents

### 1. 🌡️ Environmental Sentinel Agent
Continuously monitors hyperlocal environmental conditions and translates population-level alerts into personalized caregiving recommendations.

**Data Sources:**
- EPA AirNow API (Air Quality Index)
- National Weather Service API (Heat advisories, weather alerts)
- UV Index data
- Pollen forecasts

**Outputs:**
- Personalized outdoor activity windows
- Heat safety recommendations
- Air quality alerts with actionable guidance

---

### 2. ❤️ Vital Signs Monitoring Agent
Collects and interprets physiological data from smartwatches, correlating changes with environmental conditions and behavioral patterns.

**Data Sources:**
- Apple HealthKit / Google Health Connect
- Smartwatch sensors (heart rate, HRV, accelerometer)

**Metrics Tracked:**
- Heart rate and heart rate variability (HRV)
- Sleep quality and patterns
- Activity levels and step count
- Correlation with environmental triggers

---

### 3. 💬 Caregiver Navigation Agent
A multilingual copilot providing real-time decision support, education, and telemedicine visit preparation.

**Features:**
- Symptom triage and guidance
- Structured visit summaries for providers
- Daily personalized care recommendations
- ADRD education modules
- Concern reporting workflow

**Languages:** English, Spanish (extensible)

---

### 4. 🏥 Telemedicine Data Integration Agent
The interoperability engine that aggregates and shares health data across providers using FHIR standards.

**Capabilities:**
- FHIR R4 compliant data exchange
- Visit summary aggregation
- Medication reconciliation
- Care plan synchronization
- EHR integration with rural clinics

**Connected Systems:**
- Telehealth platforms
- Critical Access Hospitals
- Federally Qualified Health Centers (FQHCs)
- Emergency departments

---

### 5. 🤝 Community Health Connector Agent
Links households to local resources, community health workers, and support services.

**Resources:**
- Respite care centers
- Cooling/warming centers
- Caregiver support groups
- Area Agencies on Aging
- Community health worker coordination

---

## 🛠️ Technology Stack

### Frontend
```
- HTML5 / CSS3 / JavaScript (ES6+)
- Responsive design with CSS Grid/Flexbox
- Real-time animations and data visualization
- Progressive Web App (PWA) ready
```

### Backend (Planned)
```
- Python 3.10+
- LangGraph (Multi-agent orchestration)
- FastAPI (REST API)
- PostgreSQL (Data persistence)
- Redis (Real-time caching)
```

### AI/ML
```
- LangChain / LangGraph (Agent framework)
- OpenAI GPT-4 / Claude API (LLM backbone)
- Custom NLP models for symptom extraction
```

### Integrations
```
- FHIR R4 (Healthcare interoperability)
- Apple HealthKit / Google Health Connect
- EPA AirNow API
- National Weather Service API
```

---

## 📦 Installation

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Node.js 18+ (for development server)
- Python 3.10+ (for backend, coming soon)

### Quick Start (Prototype)

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/alz-care.git
cd alz-care
```

2. **Open the prototype**
```bash
# Simply open the HTML file in your browser
open prototype/alz-care-realtime.html

# Or use a local server
npx serve prototype
```

3. **View the dashboard**
- Navigate to `http://localhost:3000` (if using serve)
- Or open `alz-care-realtime.html` directly in browser

### Development Setup (Coming Soon)
```bash
# Install dependencies
pip install -r requirements.txt
npm install

# Configure environment
cp .env.example .env
# Edit .env with your API keys

# Run development server
python -m uvicorn main:app --reload
```

---

## 🚀 Usage

### Dashboard Overview

The main dashboard displays all five agents with real-time activity:

1. **Patient Banner** - Shows patient info, days tracked, routine score, alerts
2. **Agent Panels** - Each agent has its own panel with live data
3. **Orchestration Bar** - Visual representation of agent coordination
4. **Live Feed** - Scrolling ticker of all agent activities

### Interactive Features

| Button | Action |
|--------|--------|
| 📋 View Visit Summary | Opens telemedicine visit preparation |
| 💡 Care Tips for Today | Time-based care recommendations |
| 🆘 Report a Concern | Submit concerns to CHW |
| 📚 ADRD Education | Educational resources |
| 🌐 Language Toggle | Switch between English/Spanish |

### Real-Time Simulation

The prototype simulates real-time agent activity:
- **Environmental Agent**: Updates every 8 seconds
- **Vitals Agent**: Updates every 5 seconds
- **Caregiver Agent**: Updates every 10 seconds
- **Telemedicine Agent**: Updates every 12 seconds
- **Community Agent**: Updates every 15 seconds
- **Cross-Agent Events**: Every 20 seconds

---

## 🔌 API Integrations

### Environmental Data
```javascript
// EPA AirNow API
GET https://www.airnowapi.org/aq/observation/zipCode/current/
Parameters: zipCode, API_KEY

// National Weather Service
GET https://api.weather.gov/alerts/active
Parameters: area (state code)
```

### Health Data (FHIR R4)
```javascript
// Patient vitals
GET /fhir/Observation?patient={id}&category=vital-signs

// Care plans
GET /fhir/CarePlan?patient={id}&status=active

// Medications
GET /fhir/MedicationRequest?patient={id}
```

### Wearable Integration
```javascript
// Apple HealthKit (via HealthKit.js)
HKHealthStore.requestAuthorization(toShare: [], read: [
  HKQuantityType.heartRate,
  HKQuantityType.heartRateVariability,
  HKCategoryType.sleepAnalysis,
  HKQuantityType.stepCount
])
```

---

## 🌐 Bilingual Support

ALZ-CARE supports English and Spanish with full UI translation:

### Supported Elements
- All navigation and buttons
- Agent status messages
- Modal content
- Care recommendations
- Alert notifications
- Form labels and placeholders

### Adding New Languages

1. Add translations to the `translations` object:
```javascript
const translations = {
  en: { /* English strings */ },
  es: { /* Spanish strings */ },
  // Add new language:
  fr: { 
    subtitle: "Écosystème de Résilience Adaptative",
    // ... more translations
  }
};
```

2. Add language button:
```html
<button class="lang-btn" onclick="setLang('fr')">Français</button>
```

---

## 📚 Research Background

### Target Population
- Rural ADRD caregivers in Arizona, New Mexico, and border regions
- Underserved communities with limited healthcare access
- Populations vulnerable to extreme heat and environmental hazards

### Evidence Base
- Heat exposure increases ADRD ED visits by 18-24% (EPA Climate Change Indicators)
- Poor air quality exacerbates cognitive decline (Lancet Neurology, 2020)
- Rural caregivers report higher depression and mortality rates (AARP, 2023)

### Pilot Study Design
- **Participants**: 20 caregiver-patient dyads
- **Duration**: 12 months
- **Measures**: Zarit Burden Interview, early warning detection accuracy, healthcare utilization, system usability

---

## 🗺️ Roadmap

### Phase 1: Prototype (Current)
- [x] Interactive HTML/CSS/JS prototype
- [x] All 5 agent visualizations
- [x] Real-time simulation
- [x] Bilingual support (EN/ES)
- [x] Modal interactions

### Phase 2: Backend Development (Q2 2026)
- [ ] LangGraph multi-agent architecture
- [ ] API integrations (EPA, NWS, FHIR)
- [ ] PostgreSQL data persistence
- [ ] User authentication

### Phase 3: Wearable Integration (Q3 2026)
- [ ] Apple HealthKit integration
- [ ] Google Health Connect integration
- [ ] Real-time vital signs streaming
- [ ] Anomaly detection models

### Phase 4: Pilot Deployment (Q4 2026)
- [ ] Rural community partnerships
- [ ] CHW training program
- [ ] IRB approval and pilot launch
- [ ] Outcome measurement

### Phase 5: Scale & Sustainability (2027)
- [ ] Multi-site expansion
- [ ] B2C/B2B2C revenue model
- [ ] NIH R21 submission
- [ ] Policy recommendations

---

## 🤝 Contributing

We welcome contributions from researchers, developers, healthcare professionals, and caregivers!

### How to Contribute

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Make your changes**
4. **Run tests** (when available)
   ```bash
   npm test
   ```
5. **Submit a pull request**

### Contribution Areas
- 🐛 Bug fixes and improvements
- 🌐 Language translations
- 📊 Data visualization enhancements
- 🔌 API integrations
- 📝 Documentation
- 🧪 Testing

### Code Style
- Use meaningful variable names
- Comment complex logic
- Follow existing patterns
- Write accessible HTML

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2026 ALZ-CARE Project

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software...
```

---

## 🙏 Acknowledgments

### Research Team
- Principal Investigator: [Imran Hossain Mithu]
- Co-Investigators: [Onicio Leal Neto]

---

<p align="center">
  <b>Built with ❤️ for caregivers everywhere</b>
  <br>
  <i>Empowering families. Connecting communities. Transforming care.</i>
</p>

---

## 📊 Project Stats

![GitHub stars](https://img.shields.io/github/stars/yourusername/alz-care?style=social)
![GitHub forks](https://img.shields.io/github/forks/yourusername/alz-care?style=social)
![GitHub issues](https://img.shields.io/github/issues/yourusername/alz-care)
![GitHub pull requests](https://img.shields.io/github/issues-pr/yourusername/alz-care)
