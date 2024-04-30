# HR-Dashboard

### Dashboard Link : https://app.powerbi.com/groups/me/reports/4321a68d-4149-4afb-88e2-9a7a0d063c15/ReportSection503991b6996c05eac47c?experience=power-bi



# Snapshot of Dashboard (Power BI Service)                                                               
 ![Screenshot 2024-04-29 163934](https://github.com/Smita-opp/Test/assets/159506053/1a925693-98e3-4ce3-9241-b3b5dbe7f5e5)





Main DAX Functioned used in the reports are mentioned below.

1. Active Employee.

        Active Employee = CALCULATE(
                        SUM('HR data'[Employee Count]))-
                          [Attrition Count] 


2. Attrition Count.

         Attrition Count = CALCULATE(
                       COUNT('HR data'[Attrition]),
                            'HR data'[Attrition]="YES")

3. Rate of Attrition
         
         Attrition rate = DIVIDE(
                    [Attrition Count],
                     CALCULATE(
                        SUM('HR data'[Employee Count])
                           )
                               )
