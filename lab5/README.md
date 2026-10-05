Task 1 (Feature Engineering): Created new features such as price per item (price_per_item), calculated geographical distances using the Haversine formula (haversine_rest_to_cust_km), and categorized price tiers (price_tier).

Task 2 (Peak Hours Evaluation): Tested alternative peak-hour definitions and evaluated their impact on predicting order status (Order_Status).

Task 3 (Categorical Reduction): Implemented Top-K reduction on item names, noting that the dataset contains 9 unique items.

Task 4 (Feature Selection): Applied feature selection using SelectFromModel to reduce model complexity and dimensions while maintaining baseline accuracy (~85.2%).
