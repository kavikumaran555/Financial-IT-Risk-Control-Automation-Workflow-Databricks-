Financial IT Risk Control Automation Workflow (Databricks)
Overview

Simple financial risk analysis workflow using Databricks and PySpark.

Combines:

system logs
transactions data
holdings data

Goal: detect IT risk, banking risk, financial risk using login behavior + transaction activity

Step 1: Import libraries and load system log data

![Step 1](./importing_libraries_and_creating_spark_dataframe_for_sys_log_dataset_in_databricks_notebook.PNG)

Step 2: Load transactions and holdings data

![Step 2](./loading_transactions_and_holdings_dataset.PNG)

Step 3: Analyze login activity and failures

![Step 3](./showing_login_status_and_failure_average_per_login.PNG)

Step 4: Create mapping table

![Step 4](./creating_mapping_table_with_key_columns_to_connect_all_three_tables_together.PNG)

Step 5: Join all datasets

![Step 5](./inner_joining_all_three_tables_using_key_columns.PNG)

Step 6: Risk logic

![Step 6](./risk_classification_using_average_login_failure_and_trade_amount.PNG)

Step 7: Final output table creation

![Step 7](./creating_final_output_table_with_feature_engineered_columns_for_visualization.PNG)

Step 8: Visualizations

Risk volume

![Chart 1](./showing_final_risk_volume_in_bar_chart.PNG)

By location

![Chart 2](./showing_final_risk_classification_by_location_using_pie_chart.PNG)

By device type

![Chart 3](./showing_final_risk_classification_by_device_type_in_bar_chart.PNG)

By merchant type

![Chart 4](./showing_final_risk_classification_by_merchant_type_using_pie_chart.PNG)

By asset type

![Chart 5](./showing_final_risk_classification_by_asset_type_using_pie_chart.PNG)

By sector

![Chart 6](./showing_final_risk_classification_by_sector_using_area_chart.PNG)

By user

![Chart 7](./showing_final_risk_classification_by_user_id_in_table_view.PNG)


Final Output

Table: final_risk_table

![Dashboard](./databricks_dashboard_showing_risk_classification.PNG)

Finally, automated the workflow using Databricks Jobs section to refresh data daily at 9 AM IST.

Contains:

user activity
transaction data
holdings data
calculated risk level
Summary
automated workflow
joins 3 datasets
detects IT + financial risk
rule-based risk scoring
ready for dashboard use
