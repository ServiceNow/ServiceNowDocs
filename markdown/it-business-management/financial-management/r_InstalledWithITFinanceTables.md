---
title: Tables installed with Financial Management - Legacy
description: Financial Management adds the following tables.
locale: en-US
release: australia
product: Financial Management
classification: financial-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Installed with Financial Management - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Tables installed with Financial Management - Legacy

Financial Management adds the following tables.

|Table|Description|
|-----|-----------|
|Actuals Log \[itfm\_actuals\_run\_log\]|Logs of actuals generated and keys generated for the associated plan definition.|
|Base Statement Item Breakdown \[itfm\_charge\_item\_breakdown\]|Statement item breakdown definitions.|
|Breakdown Relationship \[itfm\_breakdown\]|Statement item breakdown definitions.|
|Bucket \[itfm\_bucket\]|Buckets used in the allocation workbench to group similar expenses.|
|Bucket Account Allocation \[itfm\_bucket\_account\_allocation\]|Bucket assignment information.|
|Bucket Allocation Account \[itfm\_bucket\_allocation\_account\]|A reference link among buckets, accounts, and cost models.|
|Bucket Allocation Rule \[itfm\_bucket\_allocation\_rule\]|Allocates expenses to buckets.|
|Budget \[itfm\_budget\]|Final budgets.|
|Budget Actual \[itfm\_gl\_actuals\]|Actual expenses.|
|Budget Definitions \[itfm\_plan\_definition\]|Parent table for budgeting that holds the metadata such as name, budget plan year span, forecast time span, ownership, and frequency of forecasting.|
|Budget Forecast \[itfm\_budget\_forecast\]|All budget forecasts.|
|Budget Forecast Items \[itfm\_bf\_item\]|All items on the budget forecast.|
|Budget Keys \[itfm\_plan\_key\]|The key used to identify forecasts and plans.|
|Budget Notes \[itfm\_budget\_note\]|Notes for budgets that you enter in the budget variance report.|
|Budget Override Categories \[itfm\_budget\_override\_categories\]|Categories that you use to classify budget overrides.|
|Budget Period \[itfm\_budget\_period\]|Budget periods.|
|Budget Reference Rate Configuration \[itfm\_fx\_config\]|Exchange rate / fiscal period relationships.|
|Budget Reference Rates \[itfm\_fx\_rate\]|The exchange rates that budgets use.|
|Budget Segment Map \[itfm\_budget\_segment\_map\]|A relationship between segments that budgets use and a budget key.|
|Budget Targets \[itfm\_budget\_target\]|All budget target values.|
|Budget Task \[itfm\_budget\_task\]|Budget tasks.|
|Business Unit \[business\_unit\]|All business units.|
|Cleansing Condition \[itfm\_cleansing\_condition\]|Conditions that the application automatically generates when you clean data in the workbench.|
|Consumption Breakdown \[itfm\_charge\_item\_breakdown\_cons\]|Breakdown definitions for statement items that are based on a user-defined consumption table.|
|Consumption Statement Item \[itfm\_charge\_item\_cons\]|Showback source definitions for statement items that are based on a user-defined consumption table.|
|Cost Allocation \[itfm\_account\_allocation\]|An all-around view of the allocations going to and from each account.|
|Cost Allocation \[itfm\_allocation\]|All allocation lines that are processed from allocations. This table holds a more detailed level of allocation lines as compared to the Cost Allocation Aggregate table.|
|Cost Allocation Breakdown Aggregate \[itfm\_allocation\_breakdown\]|Allocation lines created based on cost allocation breakdown relationships.|
|Cost Allocation Group \[itfm\_cost\_allocation\_group\]|Groups that can be associated with allocations.|
|Cost Allocation Metric \[itfm\_cost\_allocation\_metric\]|Metrics that weighted and custom allocation methods use.|
|Cost Allocation Aggregate \[itfm\_allocation\_aggregate\]|A more brief set of allocation line data than is saved in the Cost Allocation \[itfm\_allocation\] table.|
|Cost Allocation Rollup \[itfm\_rollup\]|Rollups that the application creates when you use the workbench.|
|Cost Allocation Rollup Override \[itfm\_rollup\_override\]|Values that you can use to override allocation rollups.|
|Cost Allocation Runs Log \[itfm\_ca\_run\_log\]|A log of all allocations that have been run.|
|Cost Model Breakdown \[itfm\_charge\_item\_breakdown\_cm\]|Breakdown definitions for statement items that are based on the Financial Modeling output.|
|Cost Model Statement Item \[itfm\_charge\_item\_cm\]|Showback source definitions for statement items that are based on the financial modeling output.|
|Financial Data Source \[itfm\_data\_source\]|The source of the financial data: the staged general ledger or the cost plan breakdown.|
|Financial Data Source Field Map \[itfm\_data\_source\_field\_map\]|Individual fields mapped to the sources of financial data.|
|Financial Model \[itfm\_cost\_model\]|Financial cost models.|
|FM Report \[itfm\_report\]|Finance reports.|
|Forecast Period \[itfm\_forecast\_period\]|Forecast periods.|
|General Ledger Accounts \[itfm\_gl\_accounts\]|Accounts and associated account numbers.|
|General Ledger Cleansed Data \[itfm\_gl\_data\_cleansed\]|Expenses in the general ledger that is cleansed.|
|General Ledger Log \[itfm\_gl\_log\]|Log records that are created when expenses are added to the general ledger for a fiscal period.|
|General Ledger Staged Data \[itfm\_gl\_data\_staged\]|Imported expenses that have not been cleansed or groomed.|
|Groomed General Ledger Data \[itfm\_gl\_data\_groomed\]|Expenses in the general ledger that have been groomed.|
|Grooming Condition \[itfm\_grooming\_condition\]|Conditions that the application creates during the financial grooming process in the workbench.|
|ITCOA Definition \[itfm\_itcoa\_definition\]|Reference field mappings for cost models.|
|IT Shared Service \[itfm\_shared\_service\]|Services shared across the IT infrastructure.|
|IT Shared Service Type \[itfm\_shared\_service\_type\]|Categories that are associated with IT shared services.|
|ITFM Session \[itfm\_session\]|Saves session information for the workbench.|
|Main Report Configuration \[itfm\_ca\_main\_config\]|Configuration settings for the main Financial Management report.|
|Plan Actuals \[itfm\_plan\_actuals\]|Actual items created based on budget definition from staged source expense lines.|
|Plan Actual Breakdowns \[itfm\_ai\_breakdown\]|Actual amount breakdowns of the item for each fiscal period.|
|Plan Core \[itfm\_plan\_core\]|Meta information such as name, original plan, budget currency of a plan. itfm\_plan and itfm\_plan\_versions extend from the table.|
|Plan Item Breakdown \[itfm\_pi\_breakdown\]|Breakdowns of costs for a given plan item.|
|Plan Item Execution \[itfm\_plan\_item\_execution\]|Unit cost and its validity of plan item.|
|Plan Items \[itfm\_plan\_item\]|Financial details such as account number, budgeted amount, forecast amount, actual amount, and attributes associated to asset, project, catalog, and contract.|
|Plans \[itfm\_plan\]|Associates a budget key and the fiscal yearly details of the plan.|
|Planner \[itfm\_planner\]|Owners of budget keys.|
|Plan Template Column \[itfm\_plan\_template\_column\]|Defines columns as template columns for budget definition.|
|Plan Versions \[itfm\_plan\_versions\]|Plans that are created during promotion of each plan.|
|Plan Viewer \[itfm\_plan\_viewer\]|Access to view the plans.|
|Plan Yearly Details \[itfm\_plan\_year\_details\]|Yearly plan details.|
|Planning Data Source Field Map \[itfm\_plan\_data\_source\_field\_map\]|Planning data source field map.|
|Planning Log \[itfm\_plan\_run\_log\]|Planning log.|
|Reporting Entity \[itfm\_reporting\_entity\]|Reporting entity assigned to a user or group.|
|Segment Definition \[itfm\_ca\_segment\_map\]|Segments specified in the hierarchy of segments.|
|Segment Group Accounts \[itfm\_group\_segment\_acct\]|Grouped ITCOA accounts.|
|Segment Relationship \[itfm\_itcoa\_hierarchy\]|Relationships between segments in the segment hierarchy as defined in the Data Definition stage of the workbench.|
|Service Catalog Breakdown \[itfm\_charge\_item\_breakdown\_sc\]|Breakdown definitions for statement items that are based on Service Catalog requests.|
|Service Catalog Statement Item \[itfm\_charge\_item\_sc\]|Showback source definitions for statement items that are based on Service Catalog requests.|
|Service Charge Line \[itfm\_charge\_line\]|Individual showback lines.|
|Service Charge Line Drilldown \[itfm\_charge\_line\_drilldown\]|Individual showback line drilldowns.|
|Service Charge Price Ratecard \[itfm\_sc\_price\_rate\_card\]|Showback price rate card.|
|Showback Statement \[itfm\_sb\_stmt\]|Showback statements.|
|Showback Statement Definition \[itfm\_sb\_stmt\_def\]|Showback statement definitions.|
|Showback Statement Line Definition \[itfm\_sb\_stmt\_line\_def\]|Showback statement line definitions.|
|Showback Statement Line Unit Cost Definition \[itfm\_sb\_stmt\_line\_unit\_cost\_def\]|Showback statement line unit cost definitions.|
|Sibling Rollup Relationship \[itfm\_sibling\_relationship\]|Sibling segment rollup relationship definitions.|
|Statement Dispute \[itfm\_dispute\]|Showback disputes.|
|Statement Expense Line \[itfm\_charge\_expense\_line\]|Individual showback statement expense items.|
|Statement Expense Line Details \[itfm\_charge\_expense\_line\_details\]|Detailed showback expense information.|
|Statement Item \[itfm\_charge\_item\]|Showback source definitions.|
|Statement Item Drilldown \[itfm\_chg\_item\_drilldown\]|Statement item drilldown definitions.|
|Unit Cost Metrics \[itfm\_segment\_unit\_metrics\]|Unit cost metric definitions.|
|Unit Costs \[itfm\_unit\_cost\]|Unit cost lines generated by cost allocation.|
|Weight Map Run Log \[itfm\_weight\_map\_run\_log\]|Weight map generation log.|
|Weight Maps \[itfm\_weight\_map\]|Weight relationships that the application uses to calculate weighted metrics.|

The application also uses this table created by the Fiscal Calendar.

|Table|Description|
|-----|-----------|
|Fiscal period \[fiscal\_period\]|Fiscal calendars and the periods used by fiscal calendars.|

**Parent Topic:**[Installed with Financial Management - Legacy](r_InstalledWithITFinance.md)

**Related topics**  


[User roles installed with Financial Management - Legacy](r_InstalledWithITFinanceUserRoles.md)

