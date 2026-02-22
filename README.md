# Project: Drone Delivery Business Analysis
# Author: BBA Student (Marketing & Logistics)
# Goal: Comparing the cost efficiency between Human and Drone delivery.

def calculate_delivery_roi(distance_km):
    # Standard rates (can be adjusted for research)
    drone_cost_per_km = 0.5   # Energy and maintenance cost
    human_labor_per_km = 3.0  # Considering vehicle fuel and time cost

    # Calculation logic
    total_drone_cost = distance_km * drone_cost_per_km
    total_human_cost = distance_km * human_labor_per_km
    
    savings = total_human_cost - total_drone_cost
    efficiency_percent = ((total_human_cost - total_drone_cost) / total_human_cost) * 100

    print(f"--- Marketing & Logistics Analysis ---")
    print(f"Distance: {distance_km} KM")
    print(f"Estimated Savings with Drone: ${savings:.2f}")
    print(f"Efficiency Improvement: {efficiency_percent:.1f}%")

    if savings > 0:
        return "Recommendation: Implement drone delivery for this route."
    else:
        return "Recommendation: Continue with traditional delivery."

# Running a sample test for 10 Kilometers
print(calculate_delivery_roi(10))
