#Industrial Gas Leak Detection System
A real-time machine learning system for detecting and classifying gas leak severity levels from sensor data. Built with Python and scikit-learn, this tool helps industrial facilities monitor safety conditions and respond appropriately to potential gas leaks.

Gas Leak Detection Python License ML

Features
5-Level Severity Classification: Normal → Minor → Moderate → Significant → Severe
Real-time Prediction: Enter current sensor readings for immediate analysis
Visual Dashboard: Color-coded results with probability bars and charts
Safety Protocols: Actionable recommendations for each severity level
Test Scenarios: Pre-defined scenarios for training and demonstration
Model Management: Train, save, load, and retrain models
Data Logging: Automatic logging of all assessments
Quick Start
1. Upload Your Data
The system expects a CSV file with the following columns:

gas_concentration_ppm (0-911 ppm typical)
temperature_c (1416-1577°C typical)
pressure_psi (11-104 psi typical)
proximity_cm (9.5-16.9 cm typical)
humidity_percent (23-79% typical)
acoustic_db (58-150 dB typical)
leak_severity (0-4: Normal to Severe)
2. Run the System
# Simply run the entire script
python gas_leak_detection.py

3. Follow the Interactive Menu
Upload your CSV file

Train a new model or load existing

Enter current sensor values or run test scenarios

View detailed analysis with safety recommendations

📊 Severity Levels
Level	Name	Color	Action Required
0	Normal	🟢	Continue monitoring
1	Minor	🟡	Increase monitoring frequency
2	Moderate	🟠	Schedule inspection within 12h
3	Significant	🔴	Immediate inspection & isolation
4	Severe	⚫	EMERGENCY SHUTDOWN & Evacuation
🛠️ Technical Implementation
Model Architecture
Algorithm: Random Forest Classifier

Preprocessing: StandardScaler for feature normalization

Validation: 80-20 train-test split with stratification

Features: 6 sensor inputs

Output: 5-class probability distribution

Key Components
Data Loading: Automatic CSV detection and validation

Model Training: Balanced class weighting for imbalanced data

Interactive Interface: Menu-driven user experience

Visualization: Matplotlib charts for probabilities and sensor values

Persistence: Save/load models using joblib
