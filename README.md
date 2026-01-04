# 🍎 **NutriScan AI - Food Label Analyzer**

## 🚀 **Live Application**
- **Frontend App**: https://encode26.lovable.app/
- **Backend API**: `https://encode26-production.up.railway.app`
- **API Documentation**: `https://encode26-production.up.railway.app/docs`

### ✅ **IMPLEMENTED & WORKING**
1. **Backend API** (FastAPI on Railway) - Complete
2. **Image Processing** - Google Vision API OCR
3. **AI Analysis** - Gemini AI for ingredient categorization
4. **6 Health Personas** - Pre-defined profiles
5. **RESTful API** - All endpoints functional

## 🏗️ **Architecture**
```
### 📊 Data Flow Diagram
┌─────────┐ POST /analyze ┌─────────┐ Vision API ┌─────────┐
│ User │ ──────────────────▶ │ Backend │ ───────────────▶ │ Google │
│ │ │ │ │ Vision │
│ Browser │ ◀───────────────── │ FastAPI │ ◀────────────── │ API │
└─────────┘ JSON Response │ Railway │ Extracted └─────────┘
│ Text
│
│ Gemini AI ┌─────────┐
└─────────────────▶ │ Google │
│ Gemini │
│ AI │
Analysis Results │ │
◀───────────────── │ │
└─────────┘

yaml
Copy code

```

---

## 🧰 Technology Stack

### Frontend
- React with TypeScript  
- Tailwind CSS  
- Hosted on Lovable  

### Backend
- FastAPI (Python)  
- Hosted on Railway  

### AI & Cloud Services
- Google Vision API – OCR (text extraction)  
- Google Gemini AI – Ingredient analysis  

### Infrastructure
- Railway – Backend deployment  
- Lovable – Frontend hosting & CDN  

---

## 🔁 Complete Request Cycle
1. User uploads a food label image via the web interface  
2. Frontend converts the image into FormData and sends a POST request  
3. Backend calls Google Vision API for OCR  
4. Extracted text is sent to Gemini AI for analysis  
5. Backend formats results into structured JSON  
6. Frontend parses JSON and renders an interactive dashboard  
7. User views personalized ingredient analysis with scores and charts  

---

## 🧩 Component Overview
- Frontend (Lovable): Image upload, UI, charts, and results  
- Backend (Railway): FastAPI server with AI integrations  
- Google Vision API: Optical Character Recognition  
- Google Gemini AI: Natural language ingredient analysis  
- Railway: Container-based backend hosting  
- Lovable: Frontend hosting with CDN  

---

## 📈 Scalability Features
- Stateless backend containers for horizontal scaling  
- Auto-scaling Google Cloud AI services  
- Frontend served via global CDN  
- Planned:
  - Redis caching  
  - PostgreSQL database  

---

## 🔐 Security Measures
- HTTPS encryption for all connections  
- CORS restricted to frontend domains  
- API keys stored as environment variables  
- Input validation and sanitization  
- Planned:
  - Rate limiting  
  - Authentication 

### **Local Development**
```bash
# Clone repo
git clone https://github.com/dikshaparulekar/Encode26
cd Encode26/backend

# Install dependencies
pip install -r requirements.txt

# Run server
uvicorn main:app --reload --port 8000
```

## 📊 **API Endpoints**

| Method | Endpoint | Description | Status |
|--------|----------|-------------|--------|
| `GET` | `/` | API info | ✅ |
| `GET` | `/health` | Health check | ✅ |
| `GET` | `/personas` | Get health profiles | ✅ |
| `POST` | `/analyze` | Image analysis | ✅ |
| `POST` | `/analyze/text` | Text analysis | ✅ *(frontend missing)* |
| `POST` | `/custom-profile` | Create profile | ✅ |
| `GET` | `/history` | Recent scans | ✅ *(in-memory only)* |

## 🎯 **Future Features (Planned)**
### **Short-term **
- [ ] **Text Input Interface** - Paste ingredient lists directly
- [ ] **Database Integration** - PostgreSQL for user history
- [ ] **User Accounts** - Save preferences and history
- [ ] **Export Reports** - PDF/CSV download of analysis

- [ ] **Mobile App** - React Native version
- [ ] **Barcode Scanner** - Scan products for automatic lookup
- [ ] **Recipe Analysis** - Analyze full recipes, not just ingredients
- [ ] **Multi-language Support** - Spanish, French, German

### **Long-term **
- [ ] **Allergy Alerts** - Real-time allergy warnings
- [ ] **Meal Planning** - Weekly meal suggestions
- [ ] **Grocery Integration** - Connect with Instacart/Amazon
- [ ] **Community Features** - Share safe products


## ⚠️ **Important Notes for Judges/Reviewers**
> **Note: This repository contains BACKEND ONLY.** The frontend is hosted separately on Lovable.

---
