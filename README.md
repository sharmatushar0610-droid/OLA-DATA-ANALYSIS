# 🚕 OLA Cab Booking Analysis | SQL + Power BI

### 📌 Project Overview
This is an end-to-end Data Analyst project on OLA Cabs booking data (103K+ records). The goal of this project was to analyze booking behavior, identify reasons for ride cancellations & incomplete rides, and find revenue and customer trends using SQL and Power BI.

### 🎯 Business Problem Statement
OLA is facing business challenges:
- High cancellation rate by Customers and Drivers
- Revenue loss due to incomplete rides
- Need to understand peak demand hours, top customers, and best-performing vehicle types
This project provides data-driven insights to solve these problems.

### 📂 Files in this Repository
- All `.sql` files - Contains 10 Business Questions solved using SQL
- `OLA-Dashboard.png` - Power BI Dashboard Screenshot
- `Bookings.csv` - Raw Dataset (100K+ rows)

### 🛠️ Tools & Technologies Used
- **SQL (MySQL):** Data Extraction & Business Problem Solving
- **Power BI:** Interactive Dashboard & Visualizations
- **DAX:** For Creating Measures (Total Revenue, Success Rate)
- **Excel:** Data Cleaning

### 🔍 10 Business Questions Solved with SQL
1. Retrieve all successful bookings:
2. Find the average ride distance for each vehicle type:
3. Get the total number of cancelled rides by customers:
4. List the top 5 customers who booked the highest number of rides:
5. Get the number of rides cancelled by drivers due to personal and car-related issues:
6. Find the maximum and minimum driver ratings for Prime Sedan bookings:
7. Retrieve all rides where payment was made using UPI:
8. Find the average customer rating per vehicle type:
9. Calculate the total booking value of rides completed successfully:
10. List all incomplete rides along with the reason

### 📊 10 Business Questions Solved with Power BI 
1. Ride Volume Over Time
2. Booking Status Breakdown
3. Top 5 Vehicle Types by Ride Distance
4. Average Customer Ratings by Vehicle Type
5. cancelled Rides Reasons
6. Revenue by Payment Method
7. Top 5 Customers by Total Booking Value
8. Ride Distance Distribution Per Day
9. Driver Ratings Distribution
10. Customer vs. Driver Ratings
### 📊 Power BI Dashboard Preview
![OLA Dashboard](OLA-Dashboard.png)

### 💡 Key Insights & Findings
- **Success Rate:** 62% rides are successful, 28% cancelled by customers/drivers, 10% incomplete.
- **Cancellation Reason:** Top reason for customer cancellation is "Driver asked to cancel".
- **Revenue Driver:** Prime Sedan category generated the highest total booking value.
- **Peak Time:** Highest bookings are observed between 6 PM to 9 PM.
- **Payment Method:** 55% customers still prefer Cash payment.
- **Customer Loyalty:** Top 5 customers contribute to more than 500+ bookings.

### 📈 DAX Measures Created
```DAX
Total Bookings = COUNT(Bookings[Booking_ID])
Successful Rides = CALCULATE(COUNT(Bookings[Booking_ID]), Bookings[Booking_Status]="Success")
Total Revenue = SUM(Bookings[Booking_Value])
Success Rate % = DIVIDE([Successful Rides], [Total Bookings])
