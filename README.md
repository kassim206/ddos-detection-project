# Hybrid CNN-LSTM for Real-Time DDoS Detection and Mitigation
### Master’s Thesis Research | Applied Informatics (2026)
**Author:** Mohammed Kassim Cherukodan  
**Supervisor:** Audrius Zajančkauskas  
**Status:** Midterm Defense Phase (~45% Complete)

---

## 🚀 Project Motivation: The "Why Now?"
In Q4 2025, the **Aisuru Botnet** set a world record with a **31.4 Tbps** DDoS attack. Modern "Cyber Warfare" has shifted toward sophisticated Layer 7 (Application Layer) attacks that mimic human behavior, making traditional firewalls and basic Machine Learning models (like SVM or Random Forest) ineffective due to high latency and low detection accuracy.

This project investigates a **Hybrid Deep Learning** approach to bridge the gap between high-speed spatial detection and long-term temporal pattern recognition.

---

## 🧠 Proposed Architecture (CNN-LSTM)
The model utilizes a sequential hybrid architecture to process network traffic:

1. **CNN Module (Spatial Analysis):** Uses 1D-Convolutional layers to extract "signatures" and specific packet header features.
2. **LSTM Module (Temporal Analysis):** Long Short-Term Memory units analyze the *sequence* and *timing* of those features to identify burst patterns over time.
3. **Dense Layer:** A final classification head to distinguish between "Normal" and "DDoS" traffic in milliseconds.



---

## 🛠️ Technical Stack
* **Deep Learning:** TensorFlow, Keras, Scikit-Learn
* **Environment:** Docker (Containerized Isolation), Kali Linux
* **Traffic Generation:** `hping3`, `Tshark`
* **Dataset:** CIC-DDoS2019 (A Comprehensive DDoS dataset)

---

## 📂 Repository Structure
* `/src`: Python implementation of the CNN-LSTM model.
* `/lab`: Dockerfiles and scripts for the isolated virtual laboratory.
* `/docs`: Project Presentation (PDF) and Literature Review analysis.
* `/data_science`: Jupyter Notebooks for Data Exploration (EDA) and Model Training.

---

## 📈 Midterm Progress & Results
| Task | Completion | Status |
| :--- | :--- | :--- |
| **Literature Review** | 85% | Advanced Stage (Incorporating 2026 threat reports) |
| **Environment Setup** | 100% | Isolated Docker/Kali Lab fully operational |
| **Hybrid Prototype** | 60% | 1D-CNN baseline established |
| **Initial Results** | **98.7%** | Accuracy achieved on CIC-DDoS2019 sample traces |

---

## 🔮 Phase 4: Future Work
* **Mitigation Integration:** Implementing real-time rate limiting and IP-filtering based on model output.
* **Latency Optimization:** Reducing inference time to <50ms for high-speed network compatibility.
* **Comparative Analysis:** Benchmarking the Hybrid model against traditional AI algorithms to prove efficiency gains.

---

## 📜 References
This research is based on the following key studies:
* [1] Sharafaldin et al. (2019) - CIC-DDoS2019 Dataset.
* [2] S. S. Shomron (2025) - Hybrid Deep Learning for DDoS.
* [3] Cloudflare Radar (2026) - Global DDoS Threat Reports.

---

### How to Run the Prototype
1. Clone the repo: `git clone https://github.com/kassim206/ddos-detection-project.git`
2. Build the environment: `docker-compose up --build`
3. Run the training script: `python src/train_model.py`