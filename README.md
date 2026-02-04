# Gas Leak Detection System

## Overview
**Developed an industrial safety monitoring system using Random Forest classifier to detect and classify gas leak severity across 5 levels (Normal to Severe).** The system analyzes sensor data including gas concentration, temperature, pressure, proximity, humidity, and acoustic readings to provide real-time safety assessments with detailed risk protocols.

## Key Features
- **5-Level Severity Classification**: Normal, Minor, Moderate, Significant, Severe
- **Real-time Prediction**: Instant severity assessment from sensor inputs
- **Complete Probability Distribution**: Shows confidence across all 5 levels
- **Safety Protocol Recommendations**: Automated action plans for each severity level
- **Interactive Test Scenarios**: Pre-built and custom test cases
- **Visual Analytics**: Probability charts and sensor value graphs

## Model Performance
- **Algorithm**: Random Forest Classifier with 100 estimators
- **Data Split**: 80% training, 20% testing with stratified sampling
- **Class Balancing**: Weighted training to handle severity level distribution
- **Accuracy**: [Training/Testing accuracy displayed after training]
- **Features**: 6 sensor parameters from industrial gas monitoring

## Data Pipeline
1. **CSV Upload**: Gas leak detection dataset with 7 columns
2. **Preprocessing**: StandardScaler normalization
3. **Feature Engineering**: All 6 sensor features used
4. **Model Training**: Random Forest with balanced class weights
5. **Prediction**: Real-time classification with probability scores

## Sensor Parameters
- **gas_concentration_ppm**: 0-911 ppm (Primary indicator)
- **temperature_c**: 1416-1577°C
- **pressure_psi**: 11-104 psi
- **proximity_cm**: 9.5-16.9 cm
- **humidity_percent**: 23-79%
- **acoustic_db**: 58-150 dB

## Severity Levels & Actions
| Level | Color | Description | Immediate Action |
|-------|-------|-------------|------------------|
| **0** | 🟢 | Normal (No leak) | Continue operations |
| **1** | 🟡 | Minor (Slight presence) | Increase monitoring |
| **2** | 🟠 | Moderate (Minor leak) | Schedule inspection |
| **3** | 🔴 | Significant (Safety concern) | Isolate area |
| **4** | ⚫ | Severe (Emergency) | EVACUATE & shutdown |

## Technical Implementation
```python
# Core Components
- RandomForestClassifier(n_estimators=100, class_weight='balanced')
- StandardScaler for feature normalization
- Train-test split with stratification
- Probability predictions for all 5 classes
- Interactive user input system
- Visualization with Matplotlib
```

## Installation & Usage
1. **Upload CSV file** with required columns
2. **Run training** or load existing model
3. **Enter sensor values** manually or use test scenarios
4. **View predictions** with detailed analysis
5. **Follow safety protocols** based on severity level

## Output Includes
1. **Final Prediction** with severity level
2. **All 5 probability scores** with visual bars
3. **Confidence analysis** and alternatives
4. **Safety protocols** with specific actions
5. **Visual charts** saved as PNG files

## Safety Applications
- Industrial plant monitoring
- Pipeline safety systems
- Hazardous material storage
- Emergency response planning
- Worker safety protocols

## File Structure
```
├── gas_leak_detection_dataset.csv  # Uploaded data
├── gas_leak_model_real.pkl         # Trained model
├── gas_leak_scaler_real.pkl        # Feature scaler
├── gas_leak_features_real.pkl      # Feature names
└── gas_leak_prediction_results.png # Output visualization
```

## Requirements
- Python 3.7+
- scikit-learn, pandas, numpy
- matplotlib, joblib
- Google Colab environment

## Future Enhancements
- Real-time sensor integration
- Historical trend analysis
- Multiple leak point detection
- Mobile alert system
- Regulatory compliance reporting

**Note**: System accuracy depends on quality of training data.
