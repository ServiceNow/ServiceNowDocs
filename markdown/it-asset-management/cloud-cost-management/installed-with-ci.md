---
title: Components installed with Cloud Cost Management
description: Several types of components are installed with activation of the Cloud Cost Management application, including tables, user roles, and scheduled jobs.
locale: en-US
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 13
breadcrumb: [Reference, Cloud Cost Management, IT Asset Management]
---

# Components installed with Cloud Cost Management

Several types of components are installed with activation of the Cloud Cost Management application, including tables, user roles, and scheduled jobs.

## Scheduled jobs installed

<table id="table_wzk_vfn_wwb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Price Sheet Table Cleaner

</td><td>

Cleans up AWS price sheet records.

</td></tr><tr><td>

Resource Group Table Cleaner

</td><td>

Cleans up Azure resource group records that are no longer required.

</td></tr><tr><td>

CCM CleanUp Inactive Aggregated Spend Records

</td><td>

Cleans up inactive aggregated spend records.

</td></tr><tr><td>

Cloud Insights Historical Data Collection

</td><td>

Collects GCP spend data.

</td></tr><tr><td>

Cloud Insights Saving Daily Data Collection

</td><td>

Collects potential savings and realized savings for spend.

</td></tr><tr><td>

Cloud Insights Spend Saving Data Collection

</td><td>

Collects cloud spend potential saving percentage.

</td></tr><tr><td>

Execute Tasks

</td><td>

Executes tasks associated with AWS billing download.

</td></tr><tr><td>

Flow Launcher and Hierarchical Flow Launcher Keep Alive

</td><td>

Cancels stale flow jobs.

</td></tr><tr><td>

GCP Price Sheet Table Cleaner

</td><td>

Cleans up GCP Price sheet table

</td></tr><tr><td>

Tag Categories Based Recommendation

</td><td>

Generates Tag Category based recommendations.

</td></tr><tr><td colspan="2">

**Important:** The following scheduled jobs are used only when the Cloud Cost Management Infra Stack application is installed in addition to Cloud Cost Management version 8.1.

</td></tr><tr><td>

Cumulus- Cancel stuck job

</td><td>

Monitors scheduled billing jobs and cancels the jobs that are stuck. This enables billing jobs in the queue to be processed.

</td></tr><tr><td>

Unsupported CI Type Placement

</td><td>

Places the CI types that aren’t used for daily recommendations.

</td></tr><tr><td>

CCM - Daily job

</td><td>

Performs daily maintenance activities such as cleanup of left-out attachments of AWS billing job \(with assume role authentication\).

</td></tr></tbody>
</table>## Tables installed

<table id="table_yzk_vfn_wwb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CI Placement Extension Progress Calculation \[sn\_cld\_intg\_aws\_ci\_placement\_extension\_progress\_calculation\]

</td><td>

Configuration Items placement progress for AWS. Contains number of records to be processed by the AWS extension.

</td></tr><tr><td>

CI Placement Stats \[sn\_cld\_intg\_aws\_ci\_placement\_stats\]

</td><td>

Status of bookmarks created during the Configuration Items placement for AWS.

</td></tr><tr><td>

AWS CI Placement Type Information \[sn\_cld\_intg\_aws\_ci\_placement\_type\]

</td><td>

All types of Configuration Items deployed byCloud Cost Management for AWS.

</td></tr><tr><td>

AWS Cost And Usage Bill Data \[sn\_cld\_intg\_aws\_cost\_usage\]

</td><td>

Cost and billing data for AWS.

</td></tr><tr><td>

Cost Usage Bookmarks \[sn\_cld\_intg\_aws\_cost\_usage\_bookmarks\]

</td><td>

Time stamp bookmarks created for the ingested Cloud Cost Management placement records.

</td></tr><tr><td>

CloudWatch Metric Association \[sn\_cld\_intg\_aws\_cw\_metric\_association\]

</td><td>

Custom metrics created by user.

</td></tr><tr><td>

AWS CloudWatch Metric Definition \[sn\_cld\_intg\_aws\_cw\_metric\_definition\]

</td><td>

Definitions for various AWS cloud watch metrics.

</td></tr><tr><td>

CloudWatch Metric Definition to Account \[sn\_cld\_intg\_aws\_cw\_metric\_definition\_account\_m2m\]

</td><td>

Metric to service account mapping information.

</td></tr><tr><td>

AWS Baseline Performance for EC2 Burstable Instances \[sn\_cld\_intg\_aws\_ec2\_burstable\_baseline\_perf\]

</td><td>

Baseline performance percentage for AWS EC2 burstable instances.

</td></tr><tr><td>

AWS Gov Accounts Mapping \[sn\_cld\_intg\_aws\_gov\_account\_mapping\]

</td><td>

AWS Gov accounts and linked accounts details.

</td></tr><tr><td>

AWS Instance details \[sn\_cld\_intg\_aws\_instance\_detail\]

</td><td>

Details for various AWS instances present.

</td></tr><tr><td>

AWS Instance Price details \[sn\_cld\_intg\_aws\_instance\_price\_detail\]

</td><td>

Pricing and rate details for AWS instances.

</td></tr><tr><td>

AWS Offer Term \[sn\_cld\_intg\_aws\_offer\_term\]

</td><td>

Offer term details based on configurations of AWS products.

</td></tr><tr><td>

AWS Price Discount \[sn\_cld\_intg\_aws\_price\_discount\]

</td><td>

Price discounts for AWS service accounts.

</td></tr><tr><td>

AWS Price Sheet Information \[sn\_cld\_intg\_aws\_price\_sheet\_info\]

</td><td>

Price sheet details for AWS.

</td></tr><tr><td>

AWS Product Details Base \[sn\_cld\_intg\_aws\_product\_details\]

</td><td>

All product details or specifications for AWS.

</td></tr><tr><td>

AWS Product Details EC2 \[sn\_cld\_intg\_aws\_product\_details\_ec2\]

</td><td>

EC2 product details or specifications for AWS.

</td></tr><tr><td>

AWS Product Details RDS \[sn\_cld\_intg\_aws\_product\_details\_rds\]

</td><td>

RDS product details or specifications for AWS.

</td></tr><tr><td>

AWS Resource Hourly Usage Last Downloaded \[sn\_cld\_intg\_aws\_resource\_hourly\_usage\_last\_downloaded\]

</td><td>

Hourly usage download status for AWS resources.

</td></tr><tr><td>

AWS Resource Rate \[sn\_cld\_intg\_aws\_resource\_rate\]

</td><td>

Resource rates for AWS product SKUs.

</td></tr><tr><td>

AWS Billing Download Job \[sn\_cld\_intg\_aws\_schedule\]

</td><td>

Billing download jobs and their status for AWS.

</td></tr><tr><td>

AWS Storage Price Details \[sn\_cld\_intg\_aws\_storage\_price\_detail\]

</td><td>

Storage price sheet information for AWS.

</td></tr><tr><td>

Azure CI Placement Type Information \[sn\_cld\_intg\_azure\_ci\_placement\_type\]

</td><td>

Defines all types of Configuration Items deployed by Cloud Cost Management for Azure.

</td></tr><tr><td>

Azure Cost And Usage Bill Data \[sn\_cld\_intg\_azure\_cost\_usage\]

</td><td>

Cost and billing data for Azure.

</td></tr><tr><td>

Azure Database Price Sheet \[sn\_cld\_intg\_azure\_db\_price\_sheet\]

</td><td>

Price sheet details for Azure database.

</td></tr><tr><td>

Azure Database retail price detail \[sn\_cld\_intg\_azure\_db\_retail\_price\]

</td><td>

Retail price information for Azure database.

</td></tr><tr><td>

Azure Enrollment To Service Account Mapping \[sn\_cld\_intg\_azure\_ea\_sa\_mapping\]

</td><td>

Mapping information for enrollment account to the service accounts used by Cloud Cost Management.

</td></tr><tr><td>

Azure Instance Details \[sn\_cld\_intg\_azure\_instance\_detail\]

</td><td>

Details of various Azure instances present.

</td></tr><tr><td>

Azure Instance Price Details \[sn\_cld\_intg\_azure\_instance\_price\_detail\]

</td><td>

Pricing and rate details for Azure instances.

</td></tr><tr><td>

Azure Instance Series To Family Mapping \[sn\_cld\_intg\_azure\_instance\_series\_family\_mapping\]

</td><td>

Instance family to instance series mapping information for Azure.

</td></tr><tr><td>

Azure Instance Size Details \[sn\_cld\_intg\_azure\_instance\_size\_detail\]

</td><td>

Details about various Azure instances sizes &amp; their functionalities.

</td></tr><tr><td>

Azure Normalized Region \[sn\_cld\_intg\_azure\_normalized\_region\]

</td><td>

Resource location to a generic normalized location mapping information.

</td></tr><tr><td>

Azure Price Sheet Version \[sn\_cld\_intg\_azure\_price\_sheet\_version\]

</td><td>

Price sheet status and version for Azure.

</td></tr><tr><td>

Azure Product Details \[sn\_cld\_intg\_azure\_product\_details\]

</td><td>

All product details or specifications for Azure.

</td></tr><tr><td>

Azure Product Details VM \[sn\_cld\_intg\_azure\_product\_details\_vm\]

</td><td>

Virtual Machine product details or specifications for Azure.

</td></tr><tr><td>

Azure Product Offering VM \[sn\_cld\_intg\_azure\_product\_offering\_vm\]

</td><td>

Offer term details for Azure Virtual Machine service.

</td></tr><tr><td>

Azure Product Details Instance Type Map \[sn\_cld\_intg\_azure\_prod\_dtls\_inst\_type\_map\]

</td><td>

Product details for various instance types for Azure.

</td></tr><tr><td>

Azure Advisor Subscription Queue \[sn\_cld\_intg\_azure\_recommendation\_subscription\_queue\]

</td><td>

Stores the states of generate, get generate status and list recommendations flow launcher jobs, for provider based recommendations of Azure.

</td></tr><tr><td>

Azure resource hourly usage last downloaded \[sn\_cld\_intg\_azure\_resource\_hourly\_usage\_last\_downloaded\]

</td><td>

Hourly usage download status for Azure resources.

</td></tr><tr><td>

Azure Resource Rate \[sn\_cld\_intg\_azure\_resource\_rate\]

</td><td>

Resource rates for Azure meter IDs.

</td></tr><tr><td>

Azure Billing Download Job \[sn\_cld\_intg\_azure\_schedule\]

</td><td>

Billing download jobs and their status for Azure.

</td></tr><tr><td>

Azure Software Cost Details \[n\_cld\_intg\_azure\_software\_cost\_detail\]

</td><td>

Hourly cost details for Azure software.

</td></tr><tr><td>

Azure Storage Price Details \[sn\_cld\_intg\_azure\_storage\_price\_detail\]

</td><td>

Storage price sheet information for Azure.

</td></tr><tr><td>

Azure Storage Size Details \[sn\_cld\_intg\_azure\_storage\_size\_detail\]

</td><td>

Various Azure storage sizes &amp; their functionalities.

</td></tr><tr><td>

Cloud Action Execution \[sn\_cld\_intg\_core\_action\_exec\]

</td><td>

Execution details for various cloud actions.

</td></tr><tr><td>

Cloud Alias \[sn\_cld\_intg\_core\_alias\]

</td><td>

List of defined aliases.

</td></tr><tr><td>

Cloud Alias Mapping \[sn\_cld\_intg\_core\_alias\_mapping\]

</td><td>

Alias mapping to the script or action flow.

</td></tr><tr><td>

Cloud API Request \[sn\_cld\_intg\_core\_api\_request\]

</td><td>

API request &amp; parameters sent to the provider.

</td></tr><tr><td>

Cloud API Request Error \[sn\_cld\_intg\_core\_api\_request\_error\]

</td><td>

Error responses for failed request items.

</td></tr><tr><td>

Cloud API Request Item \[sn\_cld\_intg\_core\_api\_request\_item\]

</td><td>

API request item details sent to the provider.

</td></tr><tr><td>

Cloud API Response \[sn\_cld\_intg\_core\_api\_response\]

</td><td>

API responses for the API calls made to providers.

</td></tr><tr><td>

Cloud Availability Zones \[sn\_cld\_intg\_core\_availability\_zone\]

</td><td>

Availability zones for various providers.

</td></tr><tr><td>

Billing Report Information \[sn\_cld\_intg\_core\_billing\_report\_info\]

</td><td>

Billing summary reports for billing download jobs.

</td></tr><tr><td>

Billing Import Progress \[sn\_cld\_intg\_core\_bill\_imp\_progress\]

</td><td>

Import information for various extensions under billing download job.

</td></tr><tr><td>

CI Placement Stats \[sn\_cld\_intg\_core\_ci\_placement\_stats\]

</td><td>

Status of bookmarks created during Configuration Items placement.

</td></tr><tr><td>

CI Placement Status \[sn\_cld\_intg\_core\_ci\_placement\_status\]

</td><td>

Configuration Items placement status for extensions executed.

</td></tr><tr><td>

CI Placement Type Information \[sn\_cld\_intg\_core\_ci\_placement\_type\]

</td><td>

All types of Configuration Items deployed by our product for all providers.

</td></tr><tr><td>

Cost Tags \[sn\_cld\_intg\_core\_cost\_tags\]

</td><td>

Mapping information of tag category to cost hash.

</td></tr><tr><td>

Execution \[sn\_cld\_intg\_core\_execution\]

</td><td>

Execution details for all types of running IH flows.

</td></tr><tr><td>

Execution Batch \[sn\_cld\_intg\_core\_execution\_batch\]

</td><td>

Execution batches for running the flows.

</td></tr><tr><td>

Execution To Batch Map \[sn\_cld\_intg\_core\_execution\_batch\_map\]

</td><td>

Mapping information of execution jobs to the respective batches.

</td></tr><tr><td>

Execution Log \[sn\_cld\_intg\_core\_execution\_log\]

</td><td>

Log messages for all the executions.

</td></tr><tr><td>

Execution Metric \[sn\_cld\_intg\_core\_execution\_metric\]

</td><td>

Metrics for executions.

</td></tr><tr><td>

Execution Monitor \[sn\_cld\_intg\_core\_execution\_monitor\]

</td><td>

Live status of the ongoing execution.

</td></tr><tr><td>

Extension \[sn\_cld\_intg\_core\_ext\]

</td><td>

All the available extensions and their details.

</td></tr><tr><td>

Extension Type \[sn\_cld\_intg\_core\_ext\_type\]

</td><td>

Types of extensions defined.

</td></tr><tr><td>

Flow Launcher Execution \[sn\_cld\_intg\_core\_flow\_launcher\_execution\]

</td><td>

Flow launcher job execution details.

</td></tr><tr><td>

Flow Launcher Job \[sn\_cld\_intg\_core\_flow\_launcher\_job\]

</td><td>

List of flow launcher jobs and their status.

</td></tr><tr><td>

Flow Launcher Job Configuration \[sn\_cld\_intg\_core\_flow\_launcher\_job\_config\]

</td><td>

Configurations for flow launcher jobs.

</td></tr><tr><td>

Flow Launcher Workload \[sn\_cld\_intg\_core\_flow\_launcher\_workload\]

</td><td>

Workload information for flow launcher executions.

</td></tr><tr><td>

Flow Map \[sn\_cld\_intg\_core\_flow\_map\]

</td><td>

Mapping information of input parameters to the flow workloads.

</td></tr><tr><td>

Flow Reflection \[sn\_cld\_intg\_core\_flow\_reflection\]

</td><td>

Flow reflection link in flow designer for given context.

</td></tr><tr><td>

Hierarchical Flow Launcher Execution \[sn\_cld\_intg\_core\_hierarchical\_flow\_launcher\_execution\]

</td><td>

Hierarchical flow launcher job execution details.

</td></tr><tr><td>

Imported Date Range \[sn\_cld\_intg\_core\_imported\_date\_range\]

</td><td>

Imported date range of data during billing download execution.

</td></tr><tr><td>

Instance Family \[sn\_cld\_intg\_core\_instance\_family\]

</td><td>

Instance families available for various providers.

</td></tr><tr><td>

Cloud Instance Types \[sn\_cld\_intg\_core\_instance\_type\]

</td><td>

Instance types &amp; details for various providers.

</td></tr><tr><td>

Cloud Instance Type Family \[sn\_cld\_intg\_core\_instance\_type\_family\]

</td><td>

Instance family types available for various providers.

</td></tr><tr><td>

Billing Line Item Types \[ sn\_cld\_intg\_core\_line\_item\_type\]

</td><td>

Types of billing charges for various providers.

</td></tr><tr><td>

Associated Flow Execution \[sn\_cld\_intg\_core\_m2m\_ext\_exec\_flow\_exec\]

</td><td>

Mapping information of extension execution to flow execution.

</td></tr><tr><td>

M2m Profile Exec Metrics Profile Table Metrics \[sn\_cld\_intg\_core\_m2m\_profile\_exec\_metrics\_profile\_table\_metrics\]

</td><td>

Mapping information of profile execution to profile table metrics.

</td></tr><tr><td>

Pipeline Stage Extension Type Map \[sn\_cld\_intg\_core\_map\_pp\_stage\_ext\_type\]

</td><td>

Mapping information of extension types to their respective stages.

</td></tr><tr><td>

Cloud Operating Systems \[sn\_cld\_intg\_core\_os\_type\]

</td><td>

Operating system details for various providers.

</td></tr><tr><td>

Pipeline Execution \[sn\_cld\_intg\_core\_pp\_exec\]

</td><td>

Contains all the pipeline executions for billing download.

</td></tr><tr><td>

Execution Stage \[sn\_cld\_intg\_core\_pp\_exec\_stage\]

</td><td>

Contains all the pipeline executions for each billing download stage.

</td></tr><tr><td>

Extension Execution \[sn\_cld\_intg\_core\_pp\_exec\_stage\_ext\_log\]

</td><td>

Pipeline execution logs.

</td></tr><tr><td>

Execution Stage Log \[sn\_cld\_intg\_core\_pp\_exec\_stage\_log\]

</td><td>

Pipeline execution logs for each stage.

</td></tr><tr><td>

Import Stage \[sn\_cld\_intg\_core\_pp\_import\_stage\]

</td><td>

Executions details for the import state of billing download.

</td></tr><tr><td>

Cloud Price Sheet Version \[sn\_cld\_intg\_core\_price\_sheet\_version\]

</td><td>

Price sheet status and version for providers.

</td></tr><tr><td>

sn\_cld\_intg\_azure\_storage\_ps

</td><td>

Store azure storage price sheet details.

</td></tr><tr><td>

Cloud Product Regions \[sn\_cld\_intg\_core\_product\_region\]

</td><td>

List of product regions for various providers.

</td></tr><tr><td>

Profile Execution Metrics \[sn\_cld\_intg\_core\_profile\_execution\_metrics\]

</td><td>

Execution metrics for performance profiling.

</td></tr><tr><td>

Profile Flow Launcher Job Metrics \[sn\_cld\_intg\_core\_profile\_flow\_launcher\_job\_metrics\]

</td><td>

Flow launcher execution metrics for performance profiling.

</td></tr><tr><td>

Profile Flow Metrics \[sn\_cld\_intg\_core\_profile\_flow\_metrics\]

</td><td>

Flow metrics for performance profiling.

</td></tr><tr><td>

Profile Table Metrics \[sn\_cld\_intg\_core\_profile\_table\_metrics\]

</td><td>

Table metrics for performance profiling.

</td></tr><tr><td>

Cloud Provider Service \[sn\_cld\_intg\_core\_provider\_service\]

</td><td>

List of services provided by various cloud providers &amp; their end points.

</td></tr><tr><td>

Cloud Provider Service Action \[sn\_cld\_intg\_core\_provider\_service\_action\]

</td><td>

Script include actions for the cloud services provided.

</td></tr><tr><td>

Price Sheet Execution \[sn\_cld\_intg\_core\_ps\_download\_request\]

</td><td>

Price sheet job status and summary.

</td></tr><tr><td>

Execution Item \[n\_cld\_intg\_core\_ps\_download\_request\_items\]

</td><td>

List of items fetched for every price sheet execution.

</td></tr><tr><td>

Price Sheet Download Execution \[sn\_cld\_intg\_core\_ps\_execution\]

</td><td>

Price sheet execution and download information for all scheduled job.

</td></tr><tr><td>

Price Sheet Download Job \[sn\_cld\_intg\_core\_ps\_schedule\]

</td><td>

List of the price sheet download jobs created.

</td></tr><tr><td>

Cloud Purchase Options \[n\_cld\_intg\_core\_purchase\_option\]

</td><td>

Various purchase options available for providers.

</td></tr><tr><td>

Cloud Regions \[sn\_cld\_intg\_core\_region\]

</td><td>

List of cloud regions available for various providers

</td></tr><tr><td>

Resource Group \[sn\_cld\_intg\_core\_resource\_group\]

</td><td>

List of resource groups.

</td></tr><tr><td>

RS Metrics Configuration \[sn\_cld\_intg\_core\_rs\_metrics\_configuration\]

</td><td>

Metric configurations for rightsizing.

</td></tr><tr><td>

Cloud Billing Schedule \[sn\_cld\_intg\_core\_schedule\]

</td><td>

List of billing download jobs created.

</td></tr><tr><td>

Billing Download Execution \[sn\_cld\_intg\_core\_scheduled\_exec\]

</td><td>

Billing download execution and download information for all scheduled jobs.

</td></tr><tr><td>

Cloud Integration Action Schedule Job \[sn\_cld\_intg\_core\_schedule\_job\]

</td><td>

Scheduled jobs for invoking cloud actions.

</td></tr><tr><td>

Cloud Integration Action Schedule Trigger \[sn\_cld\_intg\_core\_schedule\_trigger\]

</td><td>

Triggers for invoking clod actions scheduled jobs

</td></tr><tr><td>

Storage Details Base \[sn\_cld\_intg\_core\_storage\_detail\]

</td><td>

Available storage details for providers.

</td></tr><tr><td>

Storage Option \[sn\_cld\_intg\_core\_storage\_option\]

</td><td>

Available storage options for providers

</td></tr><tr><td>

Tag Category \[sn\_cld\_intg\_core\_tag\_category\]

</td><td>

List of tag categories having various tags under them.

</td></tr><tr><td>

Tag Name \[sn\_cld\_intg\_core\_tag\_name\]

</td><td>

Tag names from the billing data or user generated names.

</td></tr><tr><td>

Tag Name-Category \[sn\_cld\_intg\_core\_tag\_name\_category\]

</td><td>

Mapping of tag name to category.

</td></tr><tr><td>

Tag Name-Value \[sn\_cld\_intg\_core\_tag\_name\_value\]

</td><td>

Mapping of tag name to value.

</td></tr><tr><td>

Tag Resource \[sn\_cld\_intg\_core\_tag\_resource\]

</td><td>

Tag value pairs associated with a resource.

</td></tr><tr><td>

Tag Value \[sn\_cld\_intg\_core\_tag\_value\]

</td><td>

Tag values from the billing data or user generated values.

</td></tr><tr><td>

Test Connection Execution \[sn\_cld\_intg\_core\_test\_connection\_execution\]

</td><td>

Test connection execution details

</td></tr><tr><td>

Variable \[sn\_cld\_intg\_core\_variable\]

</td><td>

Local variables for integrations core.

</td></tr><tr><td>

GCP CI Placement Type Information \[sn\_cld\_intg\_gcp\_ci\_placement\_type\]

</td><td>

All types of Configuration Items deployed by Cloud Cost Management for Google Cloud Platform \(GCP\).

</td></tr><tr><td>

GCP Cost And Usage Bill Data \[sn\_cld\_intg\_gcp\_cost\_usage\]

</td><td>

Cost and billing data for GCP.

</td></tr><tr><td>

GCP Product Details \[sn\_cld\_intg\_gcp\_product\_details\]

</td><td>

All product details or specifications for GCP.

</td></tr><tr><td>

Google Billing Download Job \[sn\_cld\_intg\_gcp\_schedule\]

</td><td>

Billing download jobs and their status for GCP.

</td></tr><tr><td>

GCP Services \[sn\_cld\_intg\_gcp\_services\]

</td><td>

List of services provided by GCP.

</td></tr><tr><td>

AWS Spend Report Finalization Information \[sn\_cld\_spend\_aws\_report\_finalization\_info\]

</td><td>

Spend reports finalization status for AWS.

</td></tr><tr><td>

Spend Report Daily Aggregated Cost \[sn\_cld\_spend\_core\_daily\_aggregated\_cost\]

</td><td>

Spend report on daily basis aggregated on resources.

</td></tr><tr><td>

Spend Report Daily Cost \[sn\_cld\_spend\_core\_daily\_cost\]

</td><td>

Spend report for resource usage on daily basis.

</td></tr><tr><td>

Spend Report Forecast Cost \[n\_cld\_spend\_core\_forecast\_cost\]

</td><td>

Forecasted spend information.

</td></tr><tr><td>

Spend Report Monthly Cost \[sn\_cld\_spend\_core\_monthly\_cost\]

</td><td>

Monthly spend report for resource usage.**Important:** From Cloud Cost Management version 8.1 onward, if you have installed the Cloud Cost Management Infra Stack application, this table won't be populated.

</td></tr><tr><td>

Spend Report Execution Info \[sn\_cld\_spend\_core\_report\_info\]

</td><td>

Spend report execution details.

</td></tr><tr><td>

AWS Rightsizing Analytics Report \[sn\_clin\_aws\_rs\_analytics\_report\]

</td><td>

Rightsizing report for AWS.

</td></tr><tr><td>

AWS Rightsizing Skipped Instance Families \[sn\_clin\_aws\_rs\_skipped\_instance\_family\]

</td><td>

AWS instance families that are not considered in rightsizing recommendations.

</td></tr><tr><td>

Azure Rightsizing Analytics Report \[sn\_clin\_azure\_rs\_analytics\_report\]

</td><td>

Rightsizing report for Azure.

</td></tr><tr><td>

Cloud Insights Aggregated Cost Saving Snapshot \[sn\_clin\_core\_aggregated\_cost\_saving\_snapshot\]

</td><td>

Snapshot of aggregated cost for different service accounts.

</td></tr><tr><td>

Cloud Insights Aggregated Potential Saving Snapshot \[sn\_clin\_core\_aggregated\_potential\_saving\_snapshot\]

</td><td>

Snapshot of aggregated potential savings from various recommendations.

</td></tr><tr><td>

Cloud Insights Aggregated Realized Saving Snapshot \[sn\_clin\_core\_aggregated\_realized\_saving\_snapshot\]

</td><td>

Snapshot of the actual realised aggregated savings.

</td></tr><tr><td>

Business Hours Cost \[sn\_clin\_core\_bh\_cost\]

</td><td>

Business hours vs non business hours cost for a resource.

</td></tr><tr><td>

Business Hours Policy \[sn\_clin\_core\_bh\_policy\]

</td><td>

List of policies configured for business hours.

</td></tr><tr><td>

Business Hours Policy Execution \[sn\_clin\_core\_bh\_policy\_execution\]

</td><td>

Business hours policy execution information.

</td></tr><tr><td>

Business Hours Policy Match \[sn\_clin\_core\_bh\_policy\_match \]

</td><td>

Policy matches for various resources in the Business hours cost table.

</td></tr><tr><td>

Business Hours Policy Summary \[sn\_clin\_core\_bh\_policy\_summary\]

</td><td>

Information summary for the business hour policies.

</td></tr><tr><td>

Cloud Insights Business Hour Recommendations \[n\_clin\_core\_bh\_recommendation\]

</td><td>

Recommendations for business hours.

</td></tr><tr><td>

Business Hours Settings \[sn\_clin\_core\_bh\_settings\]

</td><td>

Settings record for Business hours module.

</td></tr><tr><td>

Budget \[sn\_clin\_core\_budget\_policy\]

</td><td>

List of budget policies &amp; details.

</td></tr><tr><td>

Budget Report Forecast Cost \[sn\_clin\_core\_budget\_report\_forecast\_cost\]

</td><td>

Spend calculation for the budget.

</td></tr><tr><td>

Budgets Policy Summary \[sn\_clin\_core\_budget\_summary\]

</td><td>

Summaries of budget policies with stats.

</td></tr><tr><td>

Cloud Insights realized saving snapshot \[sn\_clin\_core\_daily\_realized\_saving\_snapshot\]

</td><td>

Snapshot of the actual realised daily savings.

</td></tr><tr><td>

Excluded Resources Report Mapping \[sn\_clin\_core\_exclusion\_mapping\]

</td><td>

Excluded resource mapping to the type report or recommendation it belongs to.

</td></tr><tr><td>

Excluded Resources \[sn\_clin\_core\_excl\_res\]

</td><td>

List of excluded resources from the Cloud Cost Management modules for different service accounts and providers.

</td></tr><tr><td>

Insights Alias \[sn\_clin\_core\_insights\_alias\]

</td><td>

List of defined aliases for Cloud Cost Management scope.

</td></tr><tr><td>

Insights Alias Mapping \[sn\_clin\_core\_insights\_alias\_mapping\]

</td><td>

Alias mapping to the script or action flow for Cloud Cost Management scope.

</td></tr><tr><td>

Insights Execution \[sn\_clin\_core\_insights\_execution\]

</td><td>

Execution details for all Cloud Cost Management executions.

</td></tr><tr><td>

Insights Type \[sn\_clin\_core\_insights\_type\]

</td><td>

List of insights types available for Cloud Cost Management.

</td></tr><tr><td>

M2m Insights Exec Profile Flow Metrics \[sn\_clin\_core\_m2m\_insights\_exec\_profile\_flow\_metrics\]

</td><td>

Insights execution to profile flow metrics.

</td></tr><tr><td>

Cloud Insights Policy Action \[sn\_clin\_core\_policy\_action\]

</td><td>

Actions and flows to be executed for a policy.

</td></tr><tr><td>

Policy Change Request Templates \[sn\_clin\_core\_policy\_change\_request\_template\]

</td><td>

Change request templates for business hours and unassigned recommendations.

</td></tr><tr><td>

Cloud Insights Policy Match \[sn\_clin\_core\_policy\_match\]

</td><td>

Policy matches for various resources and modules.

</td></tr><tr><td>

Policy Summary \[sn\_clin\_core\_policy\_summary\]

</td><td>

Summary of all the policies available

</td></tr><tr><td>

Policy \[sn\_clin\_core\_pol\_policy\]

</td><td>

Policies to be applied on various modules.

</td></tr><tr><td>

Cloud Insights potential saving snapshot \[sn\_clin\_core\_potential\_saving\_snapshot\]

</td><td>

Snapshot of the actual realised savings.

</td></tr><tr><td>

Cloud Insights Recommendations \[sn\_clin\_core\_recommendation\]

</td><td>

Recommendations for Cloud Cost Management modules.

</td></tr><tr><td>

Recommendation Action Job Execution \[sn\_clin\_core\_recommendation\_action\_job\_execution\]

</td><td>

Job execution status for recommendations.

</td></tr><tr><td>

Reserved Instance Settings \[sn\_clin\_core\_reserved\_instance\_settings\]

</td><td>

Settings record for Reserved Instance module.

</td></tr><tr><td>

Reserved Instance Recommendation \[sn\_clin\_core\_ri\_recommendation\]

</td><td>

Recommendations for reserved instances modules.

</td></tr><tr><td>

Rightsizing Analytics Report \[sn\_clin\_core\_rs\_analytics\_report\_base\]

</td><td>

Potential resources for rightsizing recommendations.

</td></tr><tr><td>

Cloud Insights Job \[sn\_clin\_core\_rs\_job\]

</td><td>

List of jobs for rightsizing or unused machines module.

</td></tr><tr><td>

Cloud Insights Rightsizing Recommendation Automatic \[sn\_clin\_core\_rs\_recommendation\_automatic\]

</td><td>

Rightsizing recommendations.

</td></tr><tr><td>

Cloud Insights Rightsizing Recommendation \[sn\_clin\_core\_rs\_recommendation\_base\]

</td><td>

Parent table for rightsizing or unused recommendations.

</td></tr><tr><td>

Rightsizing Settings \[sn\_clin\_core\_rs\_settings\]

</td><td>

Settings record for Rightsizing module.

</td></tr><tr><td>

Cloud Insights Unused Recommendation \[sn\_clin\_core\_rs\_unused\_recommendation\]

</td><td>

Unused resources recommendations.

</td></tr><tr><td>

Service Account Owner Update Policy \[sn\_clin\_core\_sa\_owner\_policy\]

</td><td>

Policies to update the service account owners.

</td></tr><tr><td>

Insights Settings\[sn\_clin\_core\_settings\]

</td><td>

Settings for various Cloud Cost Management modules.

</td></tr><tr><td>

Tag key \[sn\_clin\_core\_tag\_key\]

</td><td>

Tag keys derived from billing data as well as user generated keys.

</td></tr><tr><td>

Unassigned Resources Count \[sn\_clin\_core\_unassigned\_count\]

</td><td>

Count of unassigned resources for various service accounts.

</td></tr><tr><td>

Cloud Insights Unassigned Policies \[sn\_clin\_core\_unassigned\_policy\]

</td><td>

Policies available for unassigned resources.

</td></tr><tr><td>

Policy CI View \[sn\_clin\_core\_unassigned\_policy\_ci\_view\_list\]

</td><td>

Used for generating unassigned resources count. Contains information about the table to be queried and the encoded query and the columns to be queried in the specified table. The records in this table are manually hardcoded.

</td></tr><tr><td>

Unassigned Policy Summary \[sn\_clin\_core\_unassigned\_policy\_summary\]

</td><td>

Policy summaries available for unassigned resources.

</td></tr><tr><td>

Unassigned Recommendations \[sn\_clin\_core\_unassigned\_recommendation\]

</td><td>

Unassigned recommendations with assignment group, generated based on matched policies.

</td></tr><tr><td>

Unassigned Report \[sn\_clin\_core\_unassigned\_report\]

</td><td>

Reports or policy match for various unassigned resources.

</td></tr><tr><td>

Unassigned Resources \[sn\_clin\_core\_unassigned\_resource\]

</td><td>

List of unassigned resources on which policies can be applied.

</td></tr><tr><td>

Unassigned Resource Settings \[sn\_clin\_core\_unassigned\_settings\]

</td><td>

Settings record for Unassigned resources module.

</td></tr><tr><td>

Unused Machine Settings \[sn\_clin\_core\_unused\_settings\]

</td><td>

Settings record for Unused machines module.

</td></tr><tr><td>

Spend Report Monthly Aggregated Costs \[sn\_cld\_spend\_core\_monthly\_aggregated\_cost\]

</td><td>

Stores spend for all resources over a time range or a cost type.

</td></tr><tr><td>

Multi currency setups \[sn\_cld\_spend\_core\_multi\_currency\_setup\]

</td><td>

Stores currency options for the Multi-currency setup.

</td></tr><tr><td colspan="2">

**Important:** The following tables are used only when the Cloud Cost Management Infra Stack application is installed in addition to Cloud Cost Management version 8.1.

</td></tr><tr><td>

Resource Average Costs

 \[sn\_cld\_intg\_core\_resource\_avg\_cost\_list\]

</td><td>

Average daily cost of the resource. This average daily cost is used to calculate savings for unused recommendations.

</td></tr><tr><td>

Google Policy Usage Last Downloaded

 \[sn\_cld\_intg\_gcp\_resource\_usage\_last\_downloaded\]

</td><td>

Usage last downloaded timestamp of the resources. This helps in downloading only the delta usage for Business hours.

</td></tr><tr><td>

AWS billing job files

 \[sn\_cld\_intg\_aws\_billing\_files\]

</td><td>

Reference and status of the attachments of billing CSV files downloaded for a corresponding billing job of AWS assume role setup.

</td></tr><tr><td>

Azure billing Job chunk blob detail

 \[sn\_cld\_intg\_azure\_job\_chunk\_blob\_detail\]

</td><td>

Tracking and download URLs of Azure billing CSV data for a given date range corresponding to a billing job. Blobs are generated on Glide and download URLs are passed to the backend.

</td></tr><tr><td>

Resource Latest Usage

 sn\_cld\_intg\_core\_resource\_latest\_usage

</td><td>

Latest usage date and corresponding pivot key of the supported resources like VM, DB, storage, and snapshots for a specific provider. Resources used on the previous day are used for license calculation.

</td></tr><tr><td>

Spend Report Monthly Provider Agg Cost

 sn\_cld\_spend\_core\_monthly\_provider\_agg\_cost

</td><td rowspan="9">

Cloud Cost Management Workspace loads data from these tables when a user logs in with the insights\_admin role. These tables contain monthly aggregated spend data based on various categories such as Provider and Region.

</td></tr><tr><td>

Spend Report Monthly Master Account Agg Cost

 sn\_cld\_spend\_core\_monthly\_master\_account\_agg\_cost

</td></tr><tr><td>

Spend Report Monthly Service Account Agg Cost

 sn\_cld\_spend\_core\_monthly\_service\_account\_agg\_cost

</td></tr><tr><td>

Spend Report Monthly Purchase Option Agg Cost

 sn\_cld\_spend\_core\_monthly\_purchase\_option\_agg\_cost

</td></tr><tr><td>

Spend Report Monthly Region Agg Cost

 sn\_cld\_spend\_core\_monthly\_region\_agg\_cost

</td></tr><tr><td>

Spend Report Monthly Cloud Category Agg Cost

 sn\_cld\_spend\_core\_monthly\_cloud\_category\_agg\_cost

</td></tr><tr><td>

Spend Report Monthly Service Category Agg Cost

 sn\_cld\_spend\_core\_monthly\_service\_category\_agg\_cost

</td></tr><tr><td>

Spend Report Monthly Resource Group Agg Cost

 sn\_cld\_spend\_core\_monthly\_resource\_group\_agg\_cost

</td></tr><tr><td>

Spend Report Monthly Tag Agg Cost

 sn\_cld\_spend\_core\_monthly\_tag\_agg\_cost

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Cost Management reference](../concept/reference-cloudinsights.md)

