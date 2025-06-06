Wind Fluctuation Prediction with MLP
This project is a part of an ongoing research initiative focused on predicting the fluctuating wind pressure coefficient on high-rise building façades using machine learning.

Although wind pressure prediction for buildings has been widely studied, our team is exploring a custom architecture tailored to predicting fluctuating pressure behavior (standard deviation of pressure) at façade points, influenced by various interference configurations.

🔬 Research Scope
At the current stage, we are developing a baseline MLP (Multilayer Perceptron) model. This will serve as a foundational step before transitioning to more advanced and modern architectures.

📊 Dataset Overview
The model is trained on a proprietary dataset derived from wind tunnel tests of high-rise building models.

Building Models
Both primary and interfering buildings are made of ABS plastic

Model dimensions: 30.48 × 30.48 × 182.88 cm

Measurement Points
Pressure measured at uniformly distributed points on all façades

Wind Test Conditions
Wind angles from 0° to 180° in 10° increments

32 spatial configurations of the interfering building

Target and Features
Target variable: Fluctuating pressure coefficient at a façade point (StdDev)

Input features:

Coordinates of the interfering building: X_int, Y_int

Coordinates of façade measurement point: X_fac, Y_fac

Wind direction angle: Ang

📁 Project Structure
bash
Copy
Edit
wind_fluctuation_prediction_mlp/
│
├── data/                            # Dataset storage
│   └── windloading_interference_base.csv
│
├── results/
│   └── figures/                     # Visualizations (mean & stddev maps)
│
├── src/
│   ├── model/                       # MLP architecture
│   ├── tuning/                      # Training scripts
│   ├── utils/                       # Metrics, helpers
│
├── notebooks/                       # Development notebooks
├── final_models/                   # Saved models & configs
├── requirements.txt                # Dependencies
└── README.md