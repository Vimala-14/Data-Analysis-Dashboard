# 🌾 Farmer and Land Records Analysis Dashboard

## 📌 Project Overview
The **Farmer and Land Records Analysis Dashboard** is an interactive Power BI project designed to analyze farming patterns, land usage, crop distribution, soil quality, irrigation methods, and seasonal agricultural insights.

This dashboard helps:
- Understand district-wise land distribution  
- Compare crops and their cultivation patterns  
- Analyze soil types and irrigation methods  
- Track seasonal farming trends  
- Support agricultural decision-making using data

---

## 📊 Features of the Dashboard

### ✅ **1. District-Level Insights**
- Total land area by district  
- Farmer count distribution  
- Regional crop performance  

### ✅ **2. Crop Analysis**
- Crop-wise land usage  
- Season-wise crop distribution  
- Comparison of major and minor crops  

### ✅ **3. Soil Type Insights**
- Soil quality distribution across regions  
- Crop vs Soil compatibility trends  

### ✅ **4. Irrigation Method Analysis**
- Usage of drip, canal, borewell, and rain-fed irrigation  
- Irrigation effectiveness by crop  

### ✅ **5. Seasonal Farming Patterns**
- Kharif, Rabi, Summer season analysis  
- Year-round cultivation insights  

### ✅ **6. Interactive Slicers**
The dashboard includes slicers for smooth filtering:
- **District**
- **Crop Type**
- **Season**
- **Soil Type**
- **Irrigation Method**

## DAX Measures Used

Total_Farmers = DISTINCTCOUNT(FarmerID)

Total_Land_Area = SUM(LandArea)

Total_Crop_Count = DISTINCTCOUNT(CropType)

Average_Land_Per_Farmer = DIVIDE([Total_Land_Area], [Total_Farmers])

Season_Wise_Area = CALCULATE([Total_Land_Area], ALLEXCEPT(FarmerData, Season))

Crop_Wise_Land = CALCULATE([Total_Land_Area], ALLEXCEPT(FarmerData, CropType))





