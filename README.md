# Road Safety: ML/DL Approach to Accident Prediction and Prevention

**Team:** WUZZI-WUZZI  
**Members:** Abhijnan Maji, Adarsh Pratap Singh, Prakhar Namdeo

---

## Overview

This project addresses critical road safety challenges through a comprehensive machine learning and deep learning approach. We combine statistical accident analysis with real-time computer vision technologies to predict, analyze, and prevent vehicular accidents.

### Project Objectives

1. **Identify Common Accident Causes** - Analyze historical patterns to prevent accidents before they occur
2. **Predict Accident Severity** - Assess severity levels to enable proper emergency response and victim protection
3. **Visualize Accident Hotspots** - Use QGIS to generate heatmaps of high-risk areas for targeted interventions

---

## Data Introduction

### Data Sources

The project utilizes:
- **UK Road Accident Dataset** - 33 features covering accident details
- **Vehicle Information Dataset** - 24 features for corresponding accident records

### Selected Features (11 Key Features)

- Engine Capacity
- Daytime (temporal analysis)
- Speed Limit
- Vehicle Maneuver
- Urban/Rural Area Classification
- Driver Age
- Vehicle Age
- Driver Sex
- Number of Casualties
- Road Condition

---

## Data Exploration Insights

Our exploratory data analysis (EDA) revealed critical patterns:

### Speed Limit Impact

Analysis of speed-related accidents demonstrated strong correlation between posted speed limits and accident occurrence, with higher speeds showing increased severity.

![Speed Limit Analysis](speed_limit_analysis.png)

*Figure 1: Accident Severity vs Speed Limit - Higher speed limits correlate with increased accident severity*

### Junction & Vehicle Analysis

Detailed junction type analysis revealed that certain intersection configurations are more prone to specific accident types. The analysis included both casualty and vehicle involvement patterns.

![Junction vs Casualties](junction_casualties.png)

*Figure 2: Junction Detail vs Number of Casualties - Distribution of accident severity across different junction types*

![Junction vs Vehicles](junction_vehicles.png)

*Figure 3: Junction Detail vs Number of Vehicles - Vehicle involvement patterns at different junction configurations*

---

## Machine Learning Models

### Model 1: Random Forest Classifier
- **Strengths:** Handles non-linear relationships, feature importance analysis
- **Application:** Primary classification model for severity prediction
- **Benefits:** Interpretability and robust performance across various feature distributions

### Model 2: Neural Networks (Deep Learning)
- **Architecture:** Multi-layer dense networks with TensorFlow/Keras
- **Strengths:** Captures complex patterns in high-dimensional data
- **Application:** Advanced severity classification and accident prediction
- **Optimization:** Cross-validation using KFold for robust model evaluation

---

## Computer Vision: Traffic Analysis

### Hardware Setup
**DJI Mavic Mini 3 Pro Drone**
- 4K@60fps video recording capability
- 3-axis mechanical gimbal for video stabilization
- Exceptionally reliable performance for extended operations

### Data Collection Period
- **Timeline:** August-October 2023
- **Frequency:** Multiple days across different times
- **Conditions:** Clear weather recordings only
- **Strategy:** Collection timing aligned with accident hotspot hours

### Real-Time Traffic Monitoring
Drone footage provides high-resolution aerial views of traffic patterns, enabling precise analysis of vehicle movements and conflict zones.

![Drone ROI Detection](drone_roi_detection.png)

*Figure 4: Region of Interest (ROI) Detection - Drone view with marked traffic flow paths and conflict zones at a roundabout in Greater Noida*

---

## Traffic Data Extraction Methodology

### Processing Pipeline

#### 1. Region of Interest (ROI) Setup
- Defined ROI boundaries over roundabout/intersection areas
- Masked ROI for focused analysis

![ROI Tracking](roi_tracking.png)

*Figure 5: ROI Definition - Aerial view showing defined region boundaries (purple outline) for traffic analysis at Greater Noida intersection*

#### 2. Vehicle Detection & Tracking
- Trained deep learning detection model for vehicle identification
- Implemented tracking algorithms for trajectory analysis
- Generated continuous vehicle paths for motion analysis

#### 3. Speed Extraction & Trajectory Analysis
- Positioned 7 counter lines across intersection legs
- Measured vehicle speeds while crossing each line
- Generated speed profiles for analysis

![Speed Trajectory Analysis](speed_trajectory_analysis.png)

*Figure 6: Speed & Trajectory Mapping - Vehicle trajectories with speed measurements and origin-destination counting showing vehicle IDs, speeds (km/h), and routing patterns*

#### 4. Traffic Flow Analysis
- Virtual line counters on each intersection leg
- Measured traffic volume entering/exiting
- Generated Origin-Destination (OD) matrices for traffic patterns

### Key Findings

**Origin-Destination Matrix Analysis:**
- Identified primary traffic generators and attractors
- Example: 15-minute analysis at Greater Noida site showed west side as major activity hub
- Revealed vehicular trip generation patterns critical for safety planning

---

## Results & Discussion

### Traffic Volume Monitoring
Virtual counters provided precise vehicle counts, enabling:
- Quantification of traffic flow patterns
- Identification of peak hour traffic
- Analysis of directional traffic distribution

### Conflict Point Analysis
Computer vision analysis identified:
- High-risk interaction zones
- Vehicular conflict points requiring intervention
- Critical decision points in driver behavior

---

## Extended Futuristic Work

### Phase 2 Implementation Plans

1. **Conflict Analysis for Network Prioritization**
   - Prioritize intersection/network upgrades based on conflict data
   - Direct resources to highest-risk areas

2. **Real-Time Driver Warning System**
   - Implement alerts for dangerous driving patterns
   - Provide live feedback at critical conflict points

3. **Traffic Safety Interventions**
   - Data-driven infrastructure modifications
   - Traffic management strategies to reduce crash numbers
   - Evidence-based policy recommendations

4. **Vehicle Adhoc Network (VANET)**
   - Develop connected vehicle communication systems
   - Utilize prolonged surveillance for continuous safety improvement
   - Enable vehicle-to-vehicle and vehicle-to-infrastructure communication

---

## Technologies & Libraries

### Data Processing
- `pandas` - Data manipulation and analysis
- `numpy` - Numerical computing

### Machine Learning
- `scikit-learn` - Random Forest, preprocessing, metrics
- `tensorflow`/`keras` - Neural network implementation

### Visualization
- `matplotlib` - Data visualization
- `seaborn` - Statistical visualizations
- `QGIS` - Geospatial heatmap generation

### Computer Vision
- Deep learning-based object detection
- Vehicle tracking algorithms

---

## Project References

**Data Source:** Road Accidents in India - Ministry of Road Transport & Highways, 2022

---

## Key Insights

1. **Speed is a Critical Factor** - Consistently emerges as major predictor of accident severity
2. **Location Matters** - Certain junction types and urban/rural settings show distinct accident patterns
3. **Temporal Patterns** - Daytime analysis reveals peak accident hours correlating with traffic volume
4. **Computer Vision is Essential** - Real-time video analysis provides actionable insights beyond historical data
5. **Holistic Approach Required** - Combining ML predictions with geospatial analysis and computer vision enables comprehensive safety interventions



## Contact & Contributions

For questions or contributions regarding this project, please contact the WUZZI-WUZZI team.

**Project Status:**  Complete (Phase 1 - Analysis & Modeling)

---

*Last Updated: 2023-2024*
