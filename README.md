📘 Smart Billing Control System – README
💡 Overview
The Smart Billing Control System is a C++ console application designed to calculate and suggest improvements for monthly electricity usage. It supports both residential and commercial users, including those with solar panels, and provides:

Bill estimation based on energy consumption.

Suggestions to reduce electricity usage.

Solar energy impact analysis.

Account management for returning users.

🔧 Features
👤 User Authentication
Register/Login using a reference number and password.

New users can register; existing users can log in to proceed.

🔋 Appliance Tracking
Users can enter multiple appliances with:

Name

Quantity (max 10)

Daily usage hours (max 24)

Power in watts

Calculates monthly unit consumption for each appliance.

📈 Bill Calculation
Calculates monthly bills based on slabs:

Residential slabs: Rs. 10, 15, and 20/kWh

Commercial slabs: Rs. 12, 18, and 25/kWh

☀️ Solar Integration
Users with solar panels can input:

Monthly solar generation

Last month’s solar profit (if any)

Desired profit

Calculates net billable units and potential profits from surplus energy.

💬 Suggestions Engine
Based on high-consuming appliances, suggests:

Reduced daily usage

Switching to energy-efficient models

📁 Class Descriptions
Appliance
Holds appliance details.

Calculates monthly energy usage in kWh.

BillCalculator
Static class that calculates bills based on user type (residential/commercial).

SuggestionEngine
Suggests ways to reduce energy usage based on target unit reduction.

UserAccount
Stores reference number and password.

Used for user login/registration.

SolarUser
Handles all solar-related details and profit/billable calculations.

Residential / Commercial
Handles user input, appliance data entry, billing, and summary display for each type.

🖥️ Running the Program
Compile using a C++ compiler:

bash
Copy
Edit
g++ -o billing_app billing.cpp
./billing_app
Follow prompts:

Register or log in.

Enter customer and solar panel details.

Input appliances.

View energy usage, estimated bill, and reduction tips.

✅ Sample Output (Summary)
yaml
Copy
Edit
--- Usage Summary ---
Total Units Used by Appliances: 432.00 kWh
Estimated Bill after Solar Adjustment: Rs. 6200

--- Suggestions to Reduce Your Bill ---
- Use Air Conditioner for 1 hour less/day. Saves ~90.0 units/month.
- Use Geyser for 1 hour less/day. Saves ~60.0 units/month.

--- Solar Energy Summary ---
Total Consumption: 500 kWh
Solar Generation: 600 kWh
Surplus Energy: 100 kWh
Profit Earned: Rs. 1200

