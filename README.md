# Solar Power Forecasting Using Deep Learning Techniques

## Project Overview
This project forecasts solar power generation in Malmö, Sweden, using various machine learning (ML) models. The models include Logistic Regression, Shallow Neural Networks, and Deep Neural Networks, optimized through hyperparameter tuning. The aim is to provide accurate forecasts that aid in sustainable energy management by improving the predictability of solar photovoltaic (PV) power generation.

## Case Study: Malmö, Sweden
- **Location:** Malmö, a city with a temperate oceanic climate and favorable conditions for solar power.
- **Goals:** Support Malmö’s initiative for a 70% CO2 reduction and climate neutrality by 2030, with solar PV installation on all new/remodeled roofs.

## Data Sources
- **Weather Data:** Collected from Visual Crossing.
- **Electricity Production Data:** Sourced from Renewables.ninja.
  
The dataset includes one year (2019) and three years (2019-2021) of hourly data, with the following features:
- Temperature
- Humidity
- Wind Speed
- Precipitation
- Wind Direction
- Cloud Cover
- Solar Radiation

Disregarded features include dew, snow, dust accumulation, bird droppings, and partial shading due to limited relevance.

## Data Preprocessing
- **Handling Missing Data:** Solar radiation missing values were filled using a combination of forward and backward filling.
- **Smoothing:** Applied rolling mean to smooth fluctuations.
- **Normalization:** All features were scaled using `MinMaxScaler` to ensure uniformity.

## Machine Learning Models

### 1. Logistic Regression
- **Train/Test Split:** 75%/25%
- **Number of Iterations:** 6800
- **Hyperparameters:** Learning rate between \(10^{-7}\) and 1.

### 2. Shallow Neural Network (SNN)
- **Hyperparameters:** 
    - Iterations: [100 - 10000]
    - Learning rate: [0.001 - 1]
    - Number of hidden units: [10 - 100]
    - Activation functions: ReLU, Tanh (Hidden layers), Sigmoid (Output layer)

### 3. Deep Neural Network (DNN)
- **Configurations:** 
    - Layers: 2 or 4 layers with ReLU/Tanh activations
    - Number of hidden units: [20 - 100]
    - Iterations: [2000 - 10000]
    - Learning rate: [0.01 - 1]

## Results

### Logistic Regression
- **Train Accuracy:** 88.30%
- **Test Accuracy:** 88.77%

### Shallow Neural Network
- **ReLU Activation (1 Year Data):**
  - Train Accuracy: 94.91%
  - Test Accuracy: 94.69%

- **Tanh Activation (1 Year Data):**
  - Train Accuracy: 95.37%
  - Test Accuracy: 93.33%

### Deep Neural Network
- **2-Layer ReLU:** 
  - Train Accuracy: 95.97%
  - Test Accuracy: 95.72%

- **4-Layer ReLU (1 Year Data):**
  - Train Accuracy: 96.45%
  - Test Accuracy: 95.89%

- **2-Layer Tanh:**
  - Train Accuracy: 95.31%
  - Test Accuracy: 95.14%

## Conclusion
Deep Neural Networks outperformed other models, achieving the highest accuracy, especially when trained on more complex patterns. The accuracy of the models improved with the increased quantity of training data (3-year dataset). Future studies can further refine model performance by incorporating additional input features and optimizing train/test splits.

## Future Work
- Use larger datasets and more input features.
- Explore different ML models.
- Experiment with different train-test splits and learning rate optimizations.

## References
- Trivedi S. (2021), "Evaluation of the Use of Artificial Neural Networks to Predict the Photovoltaic Power Generation..."
- Castillo-Rojas et al. (2023), "Photovoltaic Energy Forecast Using Weather Data through a Hybrid Model..."

---
