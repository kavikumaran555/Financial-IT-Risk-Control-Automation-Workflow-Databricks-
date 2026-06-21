Financial Risk Control Automation Workflow (Databricks)
Overview

Simple financial risk analysis workflow using Databricks and PySpark.

Combines:

system logs
transactions data
holdings data

Goal:
detect IT risk, banking risk, financial risk using login behavior + transaction activity

Step 1: Import libraries and load system log data

load sys_logs_record table
rename Location → Log_Location
Step 2: Load transactions and holdings data

load transactions_record
load holdings_record
Step 3: Analyze login activity and failures

filter only Login actions
create success / failure flags

calculate:

total_logins
failed_logins
avg_failure_per_login
Step 4: Create mapping table (connect all datasets)

generate:

User_ID
Transaction_ID
Portfolio_ID

helps join all 3 datasets

Step 5: Join all datasets

join logs + mapping + transactions + holdings
create one combined dataset
Step 6: Add login risk metrics
left join with login result using IP_Address

adds:

total_logins
failed_logins
avg_failure_per_login
Step 7: Risk classification logic

Rules:

CRITICAL → high failures + high trade amount
HIGH → high failures
MEDIUM → high asset risk
LOW → others
Step 8: Create final output table

select important columns
remove duplicates
save as table: final_risk_table
Step 9: Risk visualization
Overall risk volume

Risk by location

Risk by device type

Risk by merchant type

Risk by asset type

Risk by sector

Risk by user
