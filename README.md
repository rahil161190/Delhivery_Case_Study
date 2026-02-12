# Logistics Network Optimization: Data Processing & Forecasting

## 📊 Dashboard Link
**[View the Logistics Dashboard Here!](https://rahil161190.github.io/Logistics_Network_Optimization/)**


---

## 🔍 Project Overview
This project focuses on optimizing logistics operations for a large-scale integrated provider. It leverages advanced data processing and analytical techniques to understand complex freight movement patterns, analyze trip duration trends, and identify optimal routing strategies. The study delivers actionable recommendations aimed at enhancing overall operational efficiency and service quality within the logistics network.

---

## 🎯 Purpose of the Case Study
This case study provides a practical framework for **understanding and processing raw logistics data**, which is integral to modern supply chain operations. By applying data engineering pipelines and advanced analytics, the project aims to achieve several critical goals:
* **Ensure data integrity and quality** by addressing missing values and structuring datasets.
* **Extract valuable features** from raw data for building accurate forecasting models.
* Facilitate the **identification of patterns, insights, and actionable recommendations** to optimize logistics operations.
* Refine processes through **hypothesis testing and outlier detection**, ultimately enhancing service quality.

---

## 💡 The Business Challenge
The client sought to improve its data processing and forecasting capabilities to address key operational challenges. The core objectives included:
* **Cleaning, sanitizing, and transforming raw logistics data** to ensure high data quality.
* **Identifying critical demand variables** that impact operational efficiency and delivery timelines.
* Generating **forecasting insights** to enable proactive decision-making and continuous operational enhancements.

---

## 📊 Operational Snapshot
* **14.5K Trips Analyzed:** Data collected between Sept 22 - Oct 8, 2018.
* **FTL & Carting:** Utilization of Full Truck Load for inter-city and Carting for intra-city logistics.
* **Early Morning Starts:** Most trips commence early to optimize for traffic conditions.

---
Dataset:
https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/001/551/original/delhivery_data.csv?
1642751181
Instructions to download the dataset:

Column Profiling:
1. data - tells whether the data is testing or training data
2. trip_creation_time – Timestamp of trip creation
3. route_schedule_uuid – Unique ID for a particular route schedule
4. route_type – Transportation type
a. FTL – Full Truck Load: FTL shipments get to the destination sooner, as the truck
is making no other pickups or drop-offs along the way
b. Carting: Handling system consisting of small vehicles (carts)
5. trip_uuid - Unique ID given to a particular trip (A trip may include different source and
destination centers)
6. source_center - Source ID of trip origin
7. source_name - Source Name of trip origin
8. destination_cente – Destination ID
9. destination_name – Destination Name
10. od_start_time – Trip start time
11. od_end_time – Trip end time
12. start_scan_to_end_scan – Time taken to deliver from source to destination
13. is_cutoff – Unknown field
14. cutoff_factor – Unknown field
15. cutoff_timestamp – Unknown field
16. actual_distance_to_destination – Distance in kms between source and destination
warehouse
17. actual_time – Actual time taken to complete the delivery (Cumulative)
18. osrm_time – An open-source routing engine time calculator which computes the
shortest path between points in a given map (Includes usual traffic, distance through
major and minor roads) and gives the time (Cumulative)
19. osrm_distance – An open-source routing engine which computes the shortest path
between points in a given map (Includes usual traffic, distance through major and minor
roads) (Cumulative)
20. factor – Unknown field
21. segment_actual_time – This is a segment time. Time taken by the subset of the
package delivery
22. segment_osrm_time – This is the OSRM segment time. Time taken by the subset of the
package delivery
23. segment_osrm_distance – This is the OSRM distance. Distance covered by subset of
the package delivery
24. segment_factor – Unknown field

## 🌐 Warehouse & Regional Performance

### Major Sourcing & Delivery Hubs
Our analysis pinpointed major **sourcing hubs** in metropolitan areas like **Bengaluru and Gurgaon**, suggesting these are critical points for freight origination and large warehouse operations. Correspondingly, **high delivery concentrations** were noted in cities such as **Bengaluru, Gurgaon, and Mumbai**, reflecting significant regional demand.

### Crucial Interstate Corridors
Frequent **cross-state deliveries** in corridors like **Haryana, Punjab, and Delhi** underscore their importance as vital interstate logistics arteries, facilitating significant freight movement across regions.

---

## 🛣️ Route Efficiency & Traffic Impact

### Fastest Routes (km/hr)
These routes demonstrate high operational efficiency, likely due to better road conditions and lower traffic. Key examples include:
* **Abohar - Malout:** 69.83 km/hr
* **Shahdol - Anuppur:** 68.78 km/hr
* **Jaisalmer - Pokhran:** 59.89 km/hr

### Slowest Routes (km/hr)
These routes represent major bottlenecks, significantly impacted by high congestion or poor infrastructure, leading to considerably lower speeds:
* **Khatra - Hura:** 1.88 km/hr
* **Malvan - Sawantwadi:** 2.14 km/hr
* **Mariani - Jorhat:** 2.16 km/hr

Insights from hypothesis testing indicated that the **average actual time taken by trips is often more than the estimated OSRM time**, while the **actual distance covered is less than the OSRM distance**, suggesting discrepancies that impact efficiency.
*(**What is OSRM Time?** OSRM (Open Source Routing Machine) time is a calculated estimate of the shortest path travel time between two points on a map, considering typical traffic conditions and road networks. It serves as a benchmark for ideal route duration.)*

---

## 🛠️ Our Analytical Approach
Our comprehensive data analysis pipeline included:
1.  **Data Collection & Setup:** Ingesting raw data and initial structural examination.
2.  **Exploratory Data Analysis (EDA):** Analyzing data distributions, identifying patterns, and deriving preliminary insights.
3.  **Feature Engineering:** Transforming raw data into meaningful features, including datetime and location splits, and aggregating segment-level data to trip-level.
4.  **Data Preprocessing & Outlier Handling:** Cleaning data by managing missing values, detecting/treating outliers (IQR method), and preparing numerical/categorical features for modeling (scaling, one-hot encoding).
5.  **Hypothesis Testing:** Statistically validating assumptions and comparing actual vs. OSRM time/distance metrics, including assessing data normality.
6.  **Insights & Recommendations:** Translating analytical findings into actionable business strategies and observed patterns.

---

## 📈 Strategic Recommendations
Based on the insights, the following strategic recommendations are proposed:

1.  **Optimize Warehouse Infrastructure:**
    Strategically **expand hubs in high-demand cities** (e.g., Bengaluru, Gurgaon, Mumbai) to boost capacity and **reduce transit times**, improving service and cost-effectiveness.

2.  **Implement Dynamic Route Optimization:**
    Leverage real-time data and historical performance (fastest/slowest routes) to **proactively adjust delivery paths**, enhancing speed, fuel efficiency, and fleet utilization.

3.  **Enhance Intra-City Logistics:**
    Develop **specialized strategies for "Carting" operations**, optimizing routes and schedules based on local traffic and precise delivery windows to improve urban efficiency and customer satisfaction.

4.  **Conduct Root Cause Analysis for Delays:**
    Systematically investigate the underlying reasons for consistent delays and discrepancies between actual and OSRM times, especially on identified slow routes. This deep dive will uncover operational inefficiencies, infrastructure issues, or external factors, allowing for targeted interventions and process improvements to **minimize future delays across the network.**

5.  **Invest in Predictive Analytics for Demand Forecasting:**
    Utilize the processed and engineered features to build and deploy **predictive models for demand forecasting**. This will enable proactive resource allocation, optimize fleet sizing, and anticipate logistical bottlenecks, leading to **improved planning and reduced operational costs.**

---

## 💻 Technical Stack
* **Python**: Primary language for data processing and analysis.
* **Pandas**: For data manipulation and analysis.
* **NumPy**: For numerical operations.
* **Scikit-learn**: For data preprocessing tasks (e.g., scaling, encoding).
* **Matplotlib / Seaborn**: For data visualization and exploratory analysis.
