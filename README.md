# 🚨 Crime Analytics & Prediction Using NLP + AI for Emergency Call and FIR Data
Project Type: Full-stack AI System for Law & Order Forecasting
Technologies Used: Python, Streamlit, Scikit-learn, Prophet, CesiumJS, NLP, LLMs, GeoPandas, PyDeck, Plotly.

🔍 Project Objective
The primary goal of this project is to transform unstructured emergency call records (Dial‑112) and FIR datasets into structured, actionable insights for police and law enforcement leadership. The solution empowers district-level officials such as SPs (Superintendents of Police) and Commandants with real-time decision-making tools by:

✔️Automating classification of calls and incident reports using Natural Language Processing (NLP) and LLMs

✔️Identifying location-based crime hotspots and time-based risk zones

✔️Visualizing crimes on a 3D interactive globe using CesiumJS

✔️Predicting crime probabilities using AI/ML models

✔️Forecasting crime counts using time series models like Facebook Prophet

🧠 Core Functionalities
✅ 1. NLP-Driven Classification of Emergency Calls
Using LLM and text analysis methods, raw call logs and FIR descriptions are converted into structured categories such as:

🛡️ Theft

🛡️ Assault

🛡️ Burglary

🛡️ Vandalism

🛡️ Domestic Violence

The classification model flags low-confidence predictions for manual review through a role-based correction interface, enabling continuous model retraining via retrain_model.py.

📊 2. Crime Forecasting with Prophet
Utilizing historical FIR data, the system predicts the number of crimes per day/week/month using Prophet, a powerful time-series forecasting library. Forecasts are visualized with:

🎯 Confidence intervals

🎯 Future trendlines

🎯 Actual vs predicted overlays

🗺️ 3. Interactive Geospatial Visualization
Through Streamlit + CesiumJS + PyDeck, the system offers:

➤ Real-time 3D globe with Cesium

➤ Crime location clustering via heatmaps and hexbin layers

➤ Time-based toggling with day/night cycles and Cesium terrain layers

🧭 4. Predictive Crime Probability by Location & Time
Using a trained Random Forest classifier, users can predict:

➤ Likely crime types based on hour, day, month, latitude, and longitude

➤ Top 3 probable crimes with their respective confidence scores

➤ Spatial probability patterns in high-risk areas

📌 5. Error Handling and Resilience
The backend is equipped with robust error-handling mechanisms to:

➤ Flag malformed or unprocessable records

➤ Retry failed classification attempts

➤ Log and trace model prediction anomalies

🧩 Architecture Overview
Frontend UI: Streamlit dashboard with map filters, time selectors, and forecast tools

Backend Logic:

🚀 ml_logic.py: Model inference and classification

🚀 forecast.py: Time series modeling and visualization

🚀 retrain_model.py: Retraining pipeline with updated labeled data

Data Inputs:

➡️ Dial_112_10K_India_Locations.csv – emergency call logs

➡️ FIR_Dataset_10K_India_Locations.csv – registered FIRs with timestamps and geocoordinates

🧪 Results
Precision and recall of crime classification exceeded expectations after iterative model refinement.

💡 Interactive map successfully visualized:

💡 Real-time FIR locations

💡 High-confidence predicted hotspots

💡 Cesium globe allowed officials to zoom in to city-level clusters and understand daily escalation patterns.

💡 Forecasting accuracy (MAE) was within acceptable operational limits for most major crime categories.

🎯 Impact
This solution bridges operational gaps in law enforcement by:

💡 Replacing manual review with automated intelligent classification

💡 Enabling evidence-based resource deployment

💡 Providing daily and weekly summaries of critical crime zones

💡 Offering a scalable foundation for integrating CCTV, social media feeds, and call-center metadata

📦 Files & Modules

📋 app.py – Main Streamlit interface

📋 ml_logic.py – Crime type prediction logic

📋 forecast.py – Time series forecasting using Prophet

📋 retrain_model.py – Live model improvement pipeline

📋 cesium_utils.py – CesiumJS viewer configuration

📋 requirements.txt – All dependencies

*.csv – Datasets for Dial-112 and FIRs (10K+ records each)

📍 Sample Visuals (Uploaded):
🌟Heatmaps of crime activity in every state of India 

🌟Predicted hotspots with probability scoring

🌟Forecasted crime counts over time

🌟Cesium globe with historical and predictive overlays

I Have completed my project in some phases:

<img width="940" height="497" alt="1" src="https://github.com/user-attachments/assets/1139ae17-5663-4ec2-99d0-00b970bcb886" />
<figcaption>This is first phase of my project, here only on majority basis of level it just showing the historical crime at certain percentage of level on location for Delhi only </figcaption>

<img width="940" height="498" alt="2" src="https://github.com/user-attachments/assets/1a3043f6-aa6f-4859-b2f7-b9340d9889d0" />
<figcaption>This is second phase of my project, here only on majority basis of level it just showing the historical crime at certain percentage of level on location for whole India </figcaption>

<img width="940" height="498" alt="3" src="https://github.com/user-attachments/assets/f5946390-ff67-4081-9275-000cd35d3396" />
<figcaption>This is third phase of my project, here only on majority basis of level it just showing the historical crime and also predicting the future crime at certain percentage of level on location for whole India </figcaption>

<img width="942" height="502" alt="4" src="https://github.com/user-attachments/assets/fb03becd-49b9-4bb9-a643-5fb78643bbc7" />
<figcaption>This is Fourth phase of my project, here  it is showing the red spots for historical crime and also predicting the future crime by flags at every respective location on location for whole India. If the flag is above 80% it shows through Green Flag, if above than 65% and in between 80% it denotes through Orange Flag otherwise below than this is shown from Yellow Flag. </figcaption>

<img width="1366" height="725" alt="5" src="https://github.com/user-attachments/assets/b32eaff1-09a3-40b4-a8b3-7edce04f68df" />
<figcaption>This is Fifth and Final phase of my project, here  it is showing the grey spots for historical crime and also predicting the future crime by red Spots at every respective location on location for whole India in 3d Full visualisation, we can also do zooming over the globe to see the detailed location over the map to know the precise location of Hotspot.  </figcaption>

