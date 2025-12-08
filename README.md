

# 🌾 **CropAI – Intelligent Crop Disease Detection & Smart Recommendation System**

<p align="center">
  <img src="https://github.com/AKHIL-SAURABH/CropAI-Project/blob/master/ChatGPT%20Image%20Dec%208,%202025,%2002_39_04%20AM.png?raw=true" alt="CropAI Banner" width="800"/>
</p>



---

## 🏗️ **Project Architecture**

```mermaid
graph TD
    A["PlantVillage Image Dataset"] --> B["Crop Disease Model (MobileNetV2)"]
    C["Crop & Fertilizer Datasets"] --> D["Tabular ML Models"]

    B --> E["Saved Models Folder"]
    D --> E

    E --> F["FastAPI Backend"]

    F --> G["Streamlit Dashboard"]
    F --> H["Mobile App (Future)"]
    F --> I["Cloud Deployment (Render/AWS/Railway)"]

```

---

# 🧠 **Features**

---

## **1️⃣ Crop Disease Detection (Deep Learning)**

* Built using **MobileNetV2** (Transfer Learning)
* Trained on the **PlantVillage** dataset
* Detects crop disease from leaf image
* Returns:

  * Disease label
  * Confidence score

**API Endpoint:** `POST /predict-disease`

### **Output Example**

```json
{
  "predicted_class_index": 14,
  "disease_label": "Tomato___Early_blight",
  "confidence": 0.83
}
```

---

## **2️⃣ Crop Recommendation System**

* Inputs:

  * N, P, K
  * Temperature, Humidity
  * pH, Rainfall
* Predicts the best crop to grow

**API Endpoint:** `POST /recommend-crop`

```json
{
  "recommended_crop": "rice"
}
```

---

## **3️⃣ Fertilizer Recommendation System**

* Inputs:

  * Temperature, Humidity, Moisture
  * Soil Type, Crop Type
  * Nitrogen, Phosphorous, Potassium
* Predicts the best fertilizer

**API Endpoint:** `POST /recommend-fertilizer`

```json
{
  "recommended_fertilizer": "Urea"
}
```

---

# 🚀 **How to Run Locally**

### **1️⃣ Environment Setup**

```bash
conda create -n cropai python=3.10
conda activate cropai
pip install -r requirements.txt
```

---

### **2️⃣ Run Backend (FastAPI)**

```bash
cd backend
uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

API Docs:
👉 [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

---

### **3️⃣ Run Dashboard (Streamlit)**

```bash
cd dashboard
streamlit run app.py
```

Dashboard:
👉 [http://localhost:8501](http://localhost:8501)

---

# 📸 **Screenshots (Add Later)**

Create `/screenshots` and upload images.
Then embed like this:

```markdown
![Dashboard Home](https://github.com/AKHIL-SAURABH/CropAI-Project/blob/master/screenschots/dashboard_homepage.jpg)

![Disease Prediction](./screenshots/disease_result.png)
![Crop Recommendation](./screenshots/crop_result.png)
![Fertilizer Recommendation](./screenshots/fertilizer_result.png)
```

---

# 🎯 **Future Enhancements**

* Improve accuracy with heavy fine-tuning
* Add multilingual UI for farmers
* Build a mobile app (Flutter/React Native)
* Deploy backend + dashboard to Render/Railway/AWS
* Add real-time weather API integration
* Build farmer login + recommendation history

---

# 💼 **Why This Project Matters**

This project demonstrates:

* 🧠 Deep Learning (CV with MobileNetV2)
* 📊 Machine Learning (RandomForest, preprocessing)
* ⚙️ API engineering (FastAPI, Pydantic, CORS)
* 🖥️ Interactive dashboards (Streamlit)
* 🧩 Full end-to-end design (data → model → API → UI)
* 🧱 Production-ready architecture

Perfect for:

* Resume
* LinkedIn posts
* Interviews
* Final-year projects
* ML engineering portfolios

---

# 👤 **Author**

**Akhil Saurabh**

---

