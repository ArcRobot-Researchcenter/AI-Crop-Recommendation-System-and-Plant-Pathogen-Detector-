# AI-Crop-Recommendation-System-and-Plant-Pathogen-Detector-
This PHP + Python-based system allows users to upload plant leaf images and detect diseases using a trained deep learning model (TensorFlow/Keras).
This project combines IoT-based soil analysiswith deep learning leaf disease detection to assist farmers in making smart, data-driven agricultural decisions. It leverages a 7-in-1 Soil Tester Sensor and custom-trained CNN models to provide accurate crop recommendations and identify plant pathogens.
## 📽️ YouTube Demo  
[![Watch the demo](https://img.shields.io/badge/YouTube-Watch%20Demo-red)](https://www.youtube.com/watch?v=your-demo-link)

---

## 🖼️ Program Interface Screenshot  
![Interface](leaf_disease/uploads/interface_screenshot.png)

---

## 🌱 What the System Does

✅ **Analyze soil fertility** — Nitrogen (N), Phosphorus (P), Potassium (K), Temperature, Moisture, Humidity, pH, and Conductivity  
✅ **Recommend crops** — Based on real-time soil data from the 7-in-1 soil sensor  
✅ **Detect leaf diseases** — AI-based detection of diseases in Tomato, Rice, Maize, Potato, Orange, and Grapes  
✅ **Identify pathogens** — Determines if the disease is caused by fungi, bacteria, or virus  
✅ **Recommend solutions** — Smart suggestions for treatment and control

---
## 🛠️ Technologies Used

- PHP (backend)
- Python 3.9+ (TensorFlow, NumPy)
- MySQL (database)
- HTML/CSS/JS + DataTables
- Bootstrap-style UI (optional)

## 📂 Project Structure

```
crop_recommender_system/
├── index.php
├── style.css
├── crop_form.php
├── crop_result.php
├── train_crop_model.py
├── crop_model.pkl
├── leaf_disease/
│   ├── leaf_form.php
│   ├── leaf_result.php
│   ├── prediction_log.php
│   ├── predict_disease.py
│   ├── train_leaf_model.py
│   ├── models/
│   │   ├── tomato_model.h5
│   │   ├── rice_model.h5
│   │   └── ...
│   ├── uploads/
│   └── style.css
└── README.md
```

---

## 🧠 Features

- 🌱 Real-time crop recommendation based on soil readings
- 📸 Upload any leaf image and get results with:

Disease name

Pathogen type

Confidence score

Suggested solution
- 🌿 Leaf disease detection using CNN
- 🧬 Pathogen identification: fungal, bacterial, viral
- 💡 Treatment advice and best-practice suggestions
- 📊 Prediction log with DataTables and export (PDF/CSV/Excel)
- 🌀 Animated feedback while processing
- 📤 Upload interface and full prediction history

---

## 🚀 How to Run the Project

### 1. Clone the Repository
```bash
git clone (https://github.com/ArcRobot-Researchcenter/AI-Crop-Recommendation-System-and-Plant-Pathogen-Detector)
cd AI-Crop-Recommendation-System-and-Plant-Pathogen-Detector
```

### 2. Python Environment
```bash
pip install -r requirements.txt
```
**Recommended Libraries 
**
pip install matplotlib
pip install scikit-learn
pip install pandas
pip install opencv-python
pip install tensorflow-addons

### 3. Start the Local PHP Server
```bash
cd crop_recommender_system
php -S localhost:8000
```

### 4. Visit the App
Go to [http://localhost:8000](http://localhost:8000)

---

## 📦 Model Info

- 📁 Each plant has a dedicated `.h5` deep learning model (CNN)
- 🎯 Trained on PlantVillage dataset + custom images
- ✅ Output includes: `Disease | Solution | Pathogen | Confidence`
- 🧪 Example: `Tomato_Leaf_Mold | Improve air circulation | Fungal | 97.23%`

---

## 🧰 Requirements

Install with:

```bash
pip install tensorflow numpy pillow
```

Add if using Flask or serial input:

```bash
pip install flask pyserial
```

---

## 🗃️ Database Structure (MySQL)

```sql
CREATE TABLE leaf_disease_predictions (
    id INT AUTO_INCREMENT PRIMARY KEY,
    image_name VARCHAR(255) NOT NULL,
    plant_type VARCHAR(100) NOT NULL,
    disease_detected VARCHAR(100) NOT NULL,
    solution TEXT NOT NULL,
    pathogen_type VARCHAR(100),
    confidence_score DECIMAL(5,2),
    timestamp TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

---

## 💡 Future Enhancements

- Expand model to support 20+ plant species  
- Add REST API for mobile apps  
- Integrate IoT hardware for real-time field deployment  
- Add voice alerts or SMS reminders to farmers

---

## 🧑‍💻 Author

**Abdulrahaman Raji** — _AI & Agriculture Enthusiast_  
GitHub: [@ArcRobot-Researchcenter] (https://academicprojectworld.com)
