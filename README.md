# Amsterdam Airbnb Price Prediction
https://www.kaggle.com/datasets/thedevastator/airbnb-prices-in-european-cities?select=amsterdam_weekdays.csv

## Project Overview
A machine learning project to predict Airbnb rental prices in Amsterdam based on various features such as location, property type, and amenities. The model helps hosts price their properties competitively and assists travelers in finding fairly priced accommodations.

## Table of Contents
- [Dataset](#dataset)
- [Features](#features)
- [Models](#models)
- [Results](#results)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Dataset
The analysis uses the Amsterdam Airbnb dataset containing information about weekday listings. Key features include:
- Room types (Entire home/apt, Private room, Shared room)
- Property characteristics (bedrooms, capacity)
- Host information (superhost status)
- Location metrics (distance to metro, attractions)
- Quality indicators (cleanliness rating, guest satisfaction)

## Features
The project implements several key features:
- Data preprocessing and cleaning
- Feature engineering and selection
- Multiple prediction models (Linear Regression, Random Forest)
- Cross-validation and model evaluation
- Price prediction for new listings

### Key Findings
- Room type is a significant predictor of price
- Location (distance to attractions) impacts pricing
- Superhost status correlates with higher prices
- Cleanliness ratings show strong correlation with pricing


## Models
The project implements and compares multiple models:

### Linear Regression
- Training RMSE: 0.298
- Test RMSE: 0.306
- R² (Train): 0.704
- R² (Test): 0.644

### Random Forest
- Training RMSE: 0.248
- Test RMSE: 0.312
- R² (Train): 0.795
- R² (Test): 0.629

## Results
- Model achieves ~63% accuracy in price prediction
- Cross-validation shows stable performance across different data splits
- Average RMSE from cross-validation: 0.306

### Feature Importance
1. Room type
2. Person capacity
3. Location metrics
4. Host status
5. Quality ratings

## Usage
To use the price prediction model:

```python
from src.modeling import predict_price

# Example input
features = {
    'room_type': 'Private room',
    'person_capacity': 2,
    'cleanliness_rating': 9,
    'distance_to_metro': 1.5
    # ... other features
}

predicted_price = predict_price(features)
print(f"Predicted price: €{predicted_price:.2f}")
```

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.


## License
This project is licensed under the MIT License 

## Acknowledgments
- Data source: Inside Airbnb
- Libraries used: scikit-learn, pandas, numpy, seaborn

