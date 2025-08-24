## Overview

**Name:** Time-Off Tracker  
**Goal:** Analyze and visualize time-off data to support HR and team leaders in managing workforce availability, preventing burnout, and identifying seasonal patterns.  
**Dataset:** Synthetic/fake dataset stored as `time_off_data.csv`  

## Dataset Schema (`time_off_data.csv`)
| **Name** |  **Type**  | **Description** |
|:-----|:--------:|------:|
| employee_id   | integer | Unique employee identifier |
| name   |  string  |   Employee name |
| department   | string |    Employee's department |
| date   | date |    Date of time-off |
| type   | string |    Type of leave (e.g., PTO, Sick, Vacation) |
| hours   | float |    Number of hours taken off |

## Core Functionalities
### 1. Time-off totals by month
  - Aggregates total hours off per month
  - **Visualization**: Line chart or bar chart
  - **Filename**: `charts/time_off_by_month.png`

### 2. Frequency of leave types (PTO vs Sick vs Vacation) 
  - Count of each leave type
  - **Visualization**: Pie chart
  - **Filename**: `charts/pto_type_breakdown.png`

### 3. Department with most hours off
  - Grouped sum of hours_off by department
  - **Visualization**: Horizontal bar chart
  - **Filename**: `charts/time_off_by_department.png`

### 4. Seasonal trends
  - Overlays leave trends by month to identify peaks (e.g., summer vacations, winter flu season)
  - **Visualization**: Multi-year line plot or heatmap
  - **Filename**: `charts/seasonal_trends.png`

### 5. Employee time-off anomalies
  - Employees with:
    - **Excessive leave**: (e.g., > threshold per year)
    - **No leave**: (risk of burnout)
  - Flagged via summary tables or annotations




## Tools & Technologies
  - **Python:** Data analysis and visualization
        - `matplotlib / seaborn`: For charting
        - `pandas`: For data manipulation
  - **Data Source:** `time_off_data.csv` (Fake data generated from `generate-data/generate_employee_data.py`)

## Visualizations
| **Name** | **Description** |
|:-----|------:|
| **Bar Chart**   | Time-off hours by department |
| **Line Chart**   | Monthly time-off trends over the year |
| **Pie Chart**   | Proportional breakdown of leave types |
| **Heatmap/Calendar View**   | Day-wise leave usage to spot dense periods |


## Future Improvements
  - Add authentication and upload interface for real datasets
  - Interactive dashboard (Power BI/Tableau or Streamlit)
  - Alerts for anomalies (e.g., no time-off in 6+ months
  - Time-off forecasting using historical trends