import pandas as pd
import random

# Define sample data
weather_conditions = ['Clear', 'Rainy', 'Snowy', 'Foggy']
road_types = ['Highway', 'City Street', 'Rural Road']
traffic_volumes = ['Low', 'Medium', 'High']
driver_behaviors = ['Normal', 'Reckless', 'Distracted']

# Generate random sample data
data = {
    'Weather': random.choices(weather_conditions, k=100),
    'Road_Type': random.choices(road_types, k=100),
    'Traffic_Volume': random.choices(traffic_volumes, k=100),
    'Driver_Behavior': random.choices(driver_behaviors, k=100),
    'Accident_Severity': random.choices([1, 2, 3], k=100)  # 1: Minor, 2: Moderate, 3: Severe
}

# Create a DataFrame
df = pd.DataFrame(data)

# Save the dataset to a CSV file
df.to_csv('accident_dataset.csv', index=False)
