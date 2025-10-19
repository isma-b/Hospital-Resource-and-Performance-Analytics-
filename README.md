# Hospital Resource and Performance Analytics Using SQL

## Overview
This project analyzes hospital operations using SQL inside Python to understand how healthcare systems manage limited resources, staff performance, and patient experience.

By connecting multiple datasets (patients, staff, and weekly service reports) into a relational SQL database, this project explores efficiency, bottlenecks, and morale across departments.

---

## Objectives
- Evaluate hospital bed capacity and shortage patterns  
- Identify weekly utilization trends  
- Assess staff morale and attendance consistency  
- Measure patient satisfaction and length of stay  
- Understand the operational impact of seasonal events (e.g., flu outbreaks or strikes)

---

## Tools and Technologies
- Python (Pandas, SQLite3)
- SQL for relational analysis
- KaggleHub for dataset access  
- Jupyter Notebook / Google Colab for workflow execution

Dataset: [Hospital Beds Management – Kaggle](https://www.kaggle.com/datasets/jaderz/hospital-beds-management)

---

## Database Model
The SQL database includes four connected tables:

| Table | Description |
|--------|-------------|
| patients | Contains patient demographics, satisfaction scores, and length of stay |
| services_weekly | Weekly records of bed usage, admissions, refusals, morale, and satisfaction |
| staff | Lists staff members, roles, and assigned departments |
| staff_schedule | Tracks weekly staff attendance |

---

## Key Insights

### 1. Bed Occupancy by Service
| Service | Average Occupancy Rate |
|----------|------------------------|
| Emergency | 100% |
| General Medicine | 97.3% |
| Surgery | 88.2% |
| ICU | 84.4% |

**Observation:**  
Emergency and General Medicine consistently run at near full capacity, leaving little margin for unexpected surges or crises.

---

### 2. Bed Shortage Index
| Service | Refusal Rate |
|----------|--------------|
| Emergency | 80.9% |
| General Medicine | 45.4% |
| Surgery | 24.8% |
| ICU | 17.9% |

**Observation:**  
The emergency department rejects approximately four out of five patient requests, showing the most severe capacity constraint.

---

### 3. Staff Morale and Patient Satisfaction
| Service | Staff Morale | Patient Satisfaction |
|----------|---------------|----------------------|
| ICU | 71.0 | 81.6 |
| General Medicine | 73.1 | 81.2 |
| Surgery | 72.6 | 79.3 |
| Emergency | 73.6 | 77.9 |

**Observation:**  
Patient satisfaction scores remain high despite relatively low staff morale, suggesting professional resilience under pressure.

---

### 4. Event Impact Analysis
| Event | Avg Refusals | Avg Morale | Avg Satisfaction |
|--------|---------------|-------------|------------------|
| Flu | 126 | 72.9 | 78.7 |
| Donation Drive | 29 | 80.1 | 82.7 |
| Strike | 17 | 53.7 | 82.8 |

**Observation:**  
Flu events cause the highest refusal rates and reduced morale. Strikes drop morale sharply but do not immediately affect patient satisfaction, possibly due to reduced admissions.

---

### 5. Patient Experience
| Service | Avg Satisfaction | Avg Length of Stay (days) |
|----------|------------------|---------------------------|
| Surgery | 80.3 | 7.9 |
| ICU | 79.9 | 7.6 |
| Emergency | 79.5 | 7.2 |
| General Medicine | 78.6 | 7.0 |

**Observation:**  
Surgical patients have the longest stays and highest satisfaction, suggesting structured care and good recovery environments.

---

### 6. Attendance vs. Bed Shortage
Lower staff attendance correlates with higher patient refusal rates, especially in emergency and general medicine services. This connection emphasizes the importance of maintaining consistent staffing levels.

---

### 7. Top Performing Services
| Service | Satisfaction | Morale | Occupancy |
|----------|--------------|---------|------------|
| ICU | 81.6 | 71.0 | 84.4% |
| General Medicine | 81.2 | 73.1 | 97.3% |
| Surgery | 79.3 | 72.6 | 88.2% |
| Emergency | 77.9 | 73.6 | 100% |

**Observation:**  
ICU and General Medicine demonstrate strong performance balance between patient satisfaction, morale, and efficiency.  
Emergency remains the most overextended department.

---

## Recommendations
1. **Expand Emergency Capacity**  
   Increase bed availability and staffing to reduce refusals.
2. **Support Staff Well-being**  
   Implement programs that boost morale and address fatigue.
3. **Plan for Seasonal Surges**  
   Allocate temporary staff and resources during flu outbreaks or high-demand periods.
4. **Leverage Real-Time Data Monitoring**  
   Build SQL-based dashboards to detect capacity stress before it impacts outcomes.
5. **Preserve Communication and Care Quality**  
   Maintain patient-centered practices that sustain satisfaction even during operational strain.

---

## Conclusion
This analysis demonstrates how SQL-based data science can transform hospital data into actionable insights.  
By linking patient records, staffing data, and operational metrics, we can clearly observe how **efficiency, morale, and satisfaction** are interdependent.  
The findings highlight a well-functioning but overstretched system where sustainable improvements depend on capacity management and staff support.

---


