# Phyisiological-Wellness-Dataset
Longitudinal multimodal dataset of physiological &amp; behavioral signals from Empatica Embrace Plus wearables (28 adults, 15 months).

# ZU-PW Dataset
**Longitudinal Multimodal Physiological and Behavioral Signals from Medical-Grade Wearables**

**Size**: 901,440 rows × 24 columns  
**Participants**: 28 adults  
**Duration**: March 2024 – May 2025  
**Device**: Empatica Embrace Plus  

---

## Overview
The **ZU-PW Dataset** provides synchronized, minute-level physiological and behavioral signals collected from **28 adults** wearing **Empatica Embrace Plus** wrist-worn devices over **15 months**.  
Unlike many existing wearable datasets, ZU-PW offers:

- **Longitudinal coverage** (10–30+ days per participant)  
- **Multimodal signals** across cardiovascular, respiratory, thermoregulatory, electrodermal, movement, sleep, and posture domains  
- **Ecological validity** with entirely free-living, unsupervised monitoring  
- **Analysis-ready schema** with explicit wear-time and missing value annotations  

This dataset is designed to support **digital phenotyping, behavioral health monitoring, circadian rhythm analysis, physical activity recognition, chronic disease modeling,** and **machine learning for multimodal sensor fusion**.

---

## Dataset Contents
- **`zu_pw_dataset.csv`** → Main dataset (`901,440 × 24` minute-level observations)  

---

## Variables
The dataset contains **24 variables**, grouped into functional domains:

- **Cardiovascular** → `pulse_rate_bpm`, `prv_rmssd_ms`  
- **Respiratory** → `respiratory_rate_brpm`  
- **Electrodermal** → `eda_scl_usiemens`  
- **Temperature** → `temperature_celsius`  
- **Movement & Activity** → `step_counts`, `vector_magnitude`, `activity_class`, `activity_intensity`, `met`  
- **Sleep & Posture** → `sleep_detection_stage`, `body_position_left`, `body_position_right`  
- **Quality & Metadata** → `wearing_detection_percentage`, `missing_value_reason`, `participant_id`, timestamps  

---

## Applications
- **Digital Phenotyping & Behavioral Health**: Stress, recovery, and autonomic function modeling  
- **Physical Activity Recognition**: Activity type, energy expenditure, sedentary time analysis  
- **Sleep & Circadian Rhythm Analysis**: Stage detection, rhythm profiling, chronotype estimation  
- **Chronic Disease Risk Monitoring**: Cardiovascular, respiratory, and metabolic health modeling  
- **Machine Learning & Sensor Fusion**: Benchmark dataset for multimodal AI models  

---

## Citation

If you use this dataset, please cite:

> Evangelista, E., Nazir, A., Bukhari, S. M. S., Dahmani, N., Tbaishat, D., & Sharma, R. (2025).  
> *ZU-PW Dataset: Longitudinal Multimodal Physiological and Behavioral Signals from Medical-Grade Wearables.*  
> Zayed University.

## Quick Start

### Python
```python
import pandas as pd

# Load dataset
df = pd.read_csv("zu_pw_dataset.csv")

# Inspect shape and first few rows
print(df.shape)
print(df.head())

