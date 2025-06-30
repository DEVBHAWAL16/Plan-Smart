# PlanSmart

## 📍 Overview

**PlanSmart** is a Python-based AI logic-driven Event Cost Estimator and Negotiation Advisor designed for the **event management industry**.

It helps users:  
- Estimate total event costs based on **guest count** and **selected services**  
- Compare **user budget vs actual estimated cost**  
- Run a **negotiation simulation** that offers smart, tiered discounts  
- Make **vendor-level pricing decisions**  
- Provide **cost-saving recommendations** like dropping optional services  


## Concept: "AI Thinking for Event Cost Negotiation"

**Business Problem:**  
Event planners often struggle to balance client budgets with actual service costs, especially when guest counts are large.

**Solution Approach:**  
PlanSmart simulates an AI negotiation advisor by:  
- Dynamically scaling certain service costs based on **number of guests**  
- Keeping **Venue Rental cost fixed by default**, but making it negotiable for **large guest lists (more than 500 guests)**  
- Running a **tiered negotiation logic** offering discounts based on how far the budget falls short  
- Suggesting **removal of low-priority services** like Entertainment or Decoration when needed  


## Features

**Dynamic Pricing Logic**  
- Catering, Decoration, Entertainment → Scale with guest count  
- Photography, Venue Rental → Fixed (Venue Rental becomes negotiable for big events)  

**Budget Comparison**  
- Clearly displays budget shortfall (or surplus) before negotiation  

**Negotiation Simulation Logic**  
- Offers discounts:  
  - 5% for minor budget gaps  
  - 8% for medium gaps  
  - 10%-12% for larger gaps  
- Additional **10% Venue Rental discount if guests > 500**

**Service Drop Recommendations**  
- For extreme budget gaps, suggests removing low-priority services  

**Mock Vendor Details**  
- Vendor names used (mock data only) for realism  


## 📋 Mock Vendor Data (Internal to Code)

| Service       | Base Price (for 500 guests) | Vendor        | Scales with Guests |
|---------------|-----------------------------|---------------|--------------------|
| Catering      | ₹50,000                     | Foodies Hub   | Yes                |
| Decoration    | ₹25,000                     | Dream Decor   | Yes                |
| Photography   | ₹20,000                     | SnapShots     | No                 |
| Venue Rental  | ₹1,25,000                   | Royal Palace  | No (negotiable only for >500 guests) |
| Entertainment | ₹30,000                     | Fun Events    | Yes                |

---

## Workflow Summary

1. **User Inputs:**
   - Event Type (Wedding / Birthday / Corporate)
   - Total Number of Guests
   - Services Required (chosen via menu selection)
   - Total Budget

2. **System Calculates:**
   - Total Service Cost (with guest scaling for relevant services)

3. **Budget Comparison:**
   - Shows the difference between budget and total estimated cost

4. **Negotiation Simulation:**
   - Offers smart discounts
   - Provides special large-event negotiation for Venue Rental if guests >500
   - Suggests dropping optional services if needed

5. **Final Output:**
   - Displays final payable cost after negotiation logic
