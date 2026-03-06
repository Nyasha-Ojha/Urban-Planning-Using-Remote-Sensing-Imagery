# Urban Planning using Remote Sensing Image Interpretation

## 📌 Project Overview
This project, developed as part of the **Engineering Project in Community Service (EPICS)** at **VIT Bhopal University**, presents a data-driven urban planning model for **Sehore** and the surrounding districts of Madhya Pradesh. By leveraging satellite imagery, Geographic Information Systems (GIS), and Machine Learning, the system provides actionable insights for sustainable growth, efficient resource allocation, and infrastructure development.

---

## 🗺️ The Madhya Pradesh Context: Why This Project Matters
The terrain of Madhya Pradesh (MP) presents unique geographical and structural challenges that necessitated a specialized approach:

* **Topographical Diversity:** MP features a mix of the Malwa Plateau, the Narmada Valley, and rugged hill ranges. These variations mean that a "one size fits all" urban plan is impossible. Our project uses Remote Sensing to identify specific land suitability based on these terrains.
* **Water Scarcity & Drainage:** With its central location, the state relies heavily on groundwater and seasonal rivers. The terrain's natural slope and soil composition require precise mapping to ensure new urban settlements have sustainable water access and proper drainage to prevent flooding.
* **Rapid Semi-Urban Transition:** Regions like Sehore are transitioning from agricultural hubs to industrial/residential extensions of Bhopal. Without the GIS-based monitoring used in this project, this "urban sprawl" risks destroying fertile land and depleting the local water table.
* **Resource Distribution:** The vast, often uneven landscape makes traditional physical surveying slow and expensive. Remote Sensing provides a cost-effective way to monitor forest cover, wasteland, and built-up areas across the state’s challenging terrain.



---

## 🧪 Personal Case Study: The Catalyst for Change
This project is born out of a direct response to the infrastructural challenges we witness daily. Our primary inspiration stems from the **Bhopal-Indore corridor**, a critical lifeline for the state.

While official reports designate this as a 6-lane highway, the reality on the ground is far different. Large sections operate effectively as a one-way highway being used for two-way traffic. This misalignment creates:
* **High Accident Risks:** The bottlenecking and improper lane usage make it extremely accident-prone.
* **Congestion Crisis:** During university vacations and peak hours, the area suffers from debilitating traffic jams that stall regional productivity.
* **Resource Scarcity:** Beyond transport, the area faces severe water shortages due to insufficient resources and poor distribution networks.
* **Institutional Gaps:** Despite rapid growth, there is a visible lack of properly planned educational institutions, healthcare facilities, and designated industrial zones.

The haphazard infrastructural design of this area highlights the urgent need for a scientific, data-backed approach to urban planning rather than reactive construction.

---

## 🚀 Key Modules & Features
1.  **Population Forecasting:** Uses Gradient Boosting Regression and historical census data to predict growth trends and future infrastructure needs.
2.  **Land Use & Land Cover (LULC) Analysis:** Utilizes **Sentinel-2A** satellite imagery and **QGIS** (Semi-Automatic Classification Plugin) to classify land into vegetation, water bodies, and built-up areas.
3.  **Water Resource Management:** Employs Multilayer Perceptron (MLP) and Ridge Regression models to forecast groundwater availability and identify scarcity-prone zones.
4.  **Traffic & Road Planning:** Analyzes vehicle run rates (AVRR) and Peak Hour Factors (PHF) to determine where new lanes or roads are required to prevent future congestion.



---

## 🛠️ Tech Stack
* **GIS Tools:** QGIS, Bhuvan NRSC Geoportal.
* **Data Sources:** Sentinel-2A Satellite Imagery, Census of India (1961–2011).
* **Programming:** Python (Pandas, Scikit-learn, XGBoost, LightGBM).
* **Machine Learning:** Multilayer Perceptron (MLP), SVM, Ridge Regression.

---

## 👥 Team Members (Group EPICS226)
* **Nyasha Ojha:** Project Lead & Population Forecasting.
* **Anushka Mandekar:** LULC Classification & Mapping.
* **Dhaani Bahl:** Model Optimization & Research.
* **Riya Mandaogade:** Traffic Forecasting & Road Analysis.
* **Aastha Pancholi:** Traffic Data Structuring.
* **Devansh Kalura:** MLP Model Development (Healthcare/Schools).
* **Parth Sharma:** Data Normalization & Error Handling.
* **Namrata Bhutani:** Groundwater Assessment & Research.
* **Suhani Tiwari:** Water Management & ML Pipeline.
* **Divyansh Sinha:** Data Collection & Integration.

---

## 📈 Future Scope
* Integration of real-time traffic data via APIs.
* Implementation of **ConvLSTM** (Deep Learning) for more accurate spatio-temporal land growth predictions.
* Developing a public-facing dashboard for local municipal authorities in Sehore and Bhopal.

  # 🤖 Machine Learning Pipeline Architecture

```mermaid
flowchart TD

A[Raw Data Sources]
A --> B1[Census Data 1961-2011]
A --> B2[Satellite Imagery Sentinel-2A]
A --> B3[Traffic Data AVRR & PHF]
A --> B4[Groundwater Records]

B1 --> C[Data Cleaning & Preprocessing]
B2 --> C
B3 --> C
B4 --> C

C --> D[Feature Engineering & Normalization]

D --> E[Population Forecasting Model]
E --> F[Gradient Boosting Regression]

F --> G[Predicted Population Growth]

G --> H1[Groundwater Prediction Model]
G --> H2[Water Allocation Model]
G --> H3[Road & Traffic Infrastructure Model]

H1 --> I1[MLP + Ridge Regression]
H2 --> I2[Water Demand Estimation]
H3 --> I3[Traffic Capacity Prediction using AVRR & PHF]

I1 --> J[Urban Planning Insights]
I2 --> J
I3 --> J

J --> K[GIS Spatial Mapping]
K --> L[QGIS / Tableau / Power BI Dashboards]
