# **HR-DASHBOARD-using-Power-BI**
----

**Power BI Project**
-----

![Intro](https://github.com/soma-ramesh/HR-DASHBOARD-using-Power-BI/assets/143477687/e05af4e2-4cc4-496f-b329-64a2be6e8505)

**_Disclaimer_**:
The Dataset, which is used for this project is took from **Codebasics** an online educational platform.

-----
## Skills Used:
The following Power BI features were incorporated.
1. **ETL**
2. **Dax** 
3. **Measures**
4. **Dashboard**
-----


## DAX:
1. Total Days = count('Final Data'[Value])
2. NonWorkDays = CALCULATE(COUNT('Final Data'[Value]), ('Final Data'[Value] IN {"WO","HO"}))
3. Total Working Days = [Total Days]-[NonWorkDays]
4. WFH Count = sum('Final Data'[WFH])
5. Present Days = CALCULATE(COUNT('Final Data'[Value]),('Final Data'[Value]="P"))+[WFH Count]
6. WFH % = DIVIDE([WFH Count],[Present Days])
7. Present % = DIVIDE([Present Days],[Total Working Days])
8. SL % = DIVIDE(SUM('Final Data'[SL]),[Total Working Days])
9. Total Employee = DISTINCTCOUNT('Final Data'[Employee Name])

-------


**HR Dashboard**

https://github.com/soma-ramesh/HR-DASHBOARD-using-Power-BI/blob/main/HR%20Analytics.pbix

