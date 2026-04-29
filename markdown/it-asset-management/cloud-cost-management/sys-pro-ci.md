---
title: System properties for Cloud Cost Management
description: These system properties are available for the Cloud Cost Management application.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Cloud Cost Management reference, Cloud Cost Management, IT Asset Management]
---

# System properties for Cloud Cost Management

These system properties are available for the Cloud Cost Management application.

Access system properties by navigating to **All** &gt; **System properties** &gt; **All properties.**. You can set some property values on the System Properties form, but other lesser-used properties are available only on the System Property \[sys\_properties\] table.

<table id="table_ays_hkm_ywb"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cld\_intg\_core.ci\_placement\_threads\_number

</td><td>

Number of threads that are used by CI placement flow to create CIs in the billing process.-   Type: integer
-   Default value: 4

</td></tr><tr><td>

sn\_cld\_intg\_aws.max\_unprocessed\_records\_for\_ci\_placement

</td><td>

Maximum number of records to read in one batch from the AWS Cost And Usage Bill Data table for CI Placement.-   Type: integer
-   Default value: 300000

</td></tr><tr><td>

sn\_cld\_intg\_aws.min\_unprocessed\_records\_for\_ci\_placement

</td><td>

Minimum number of records to read in one batch from the AWS Cost And Usage Bill Data table for CI Placement.-   Type: integer
-   Default value: 100000

</td></tr></tbody>
</table><table id="table_fkc_hlm_ywb"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cld\_spend\_core.metricbase\_transform\_limit

</td><td>

Maximum number of Billing records to use in one Metric Base transform.-   Type: integer
-   Default value: 20000

</td></tr><tr><td>

sn\_cld\_spend\_core.spend\_report\_flow\_launcher\_chunk\_size

</td><td>

Number of non-empty CI chunks to send to the spend flow launcher.-   Type: integer
-   Default value: 40

</td></tr><tr><td>

sn\_cld\_spend\_core.spend\_report\_per\_chunk\_workload\_size

</td><td>

Number of workloads \(CI ranges and metadata\) for each chunk in the spend flow launcher.-   Type: integer
-   Default value: 500

</td></tr><tr><td>

sn\_cld\_spend\_aws.num\_months\_forecast

</td><td>

Number of future months after the current month for which the AWS Forecast spend is retrieved during every execution of the Spend job.-   Type: integer
-   Default value: 2

</td></tr></tbody>
</table><table id="table_e52_trm_ywb"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_clin\_core.bh\_report.batch\_size

</td><td>

The number of resources to include in a Business Hours report batch.-   Type: integer
-   Default value: 5000

</td></tr><tr><td>

sn\_clin\_core.bh\_recom\_max\_chunk\_size

</td><td>

Number of records used to create workload chunks of rightsizing recommendations. If you set a value greater than glide.db.max\_view\_records, then the glide.db.max\_view\_records value is used instead. A smaller number means more chunks and a larger number means fewer chunks.Records considered in one execution of generating recommendations = \(number of chunks\) \* \(data records/chunk\)

-   Type: integer
-   Default value: 10000

</td></tr><tr><td>

sn\_clin\_core.bh\_recom\_num\_chunks\_per\_workload

</td><td>

Number of chunks per workload. This value times the value of sn\_clin\_core.bh\_recom\_max\_chunk\_size is the total number of records per workload when generating rightsizing recommendations.Records considered in one execution of generating recommendations = \(number of chunks\) \* \(data records/chunk\)

-   Type: integer
-   Default value: 10

</td></tr></tbody>
</table><table id="table_tc3_hsm_ywb"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

mid.azure\_action.batch\_size

</td><td>

Use `batch_size` to set the batch size to fewer than 20 for action calls like Stop, Start, Modify \(resize\), Terminate, and Describe.

 Cloud Cost Management uses the Azure Batch API to make a bulk request for the actions. By default, Azure Batch supports a maximum of 20 for the synchronous call.

 -   Type: integer
-   Default value: 20

</td></tr></tbody>
</table><table id="table_drz_msm_ywb"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cld\_intg\_azure.az\_rs\_recommendation\_queue\_orchestrator\_polling\_time

</td><td>

Polling time for the Microsoft Azure recommendation orchestrator to check the status of the `generate`, `get generate status`, `list recommendation`, or `process recommendation` call and move it to the next stage for processing.**Note:** A short polling time is better if there are fewer subscriptions.

-   Type: integer
-   Default value: 5000 \(ms\)

</td></tr><tr><td>

sn\_cld\_intg\_azure.chunk\_size\_generate\_recommendation\_subscriptions

</td><td>

Number of subscriptions to be processed by each workload. Each workload creates a maximum of 5 threads to process 10 subscriptions in parallel based on the available MID Server worker threads.

Changing the setting to lower number increases the number of workloads created. `Generate Recommendation` is an asynchronous API call that quickly returns the generate recommendation operation ID.**Note:** For fewer than 50 subscriptions, you can decrease the value to enable parallel processing. For example, for 40 subscriptions, changing the chunk size to 10 allows 4 workloads to process subscriptions. By default, a maximum of 3 parallel workload executions are allowed. The maximum is configured in the flow launcher job that is defined in the `sn_cld_intg_core_flow_launcher_job_config` table.

-   Type: integer
-   Default value: 5

</td></tr><tr><td>

sn\_cld\_intg\_azure.advisor\_get\_status\_min\_chunk\_size

</td><td>

Minimum number of subscriptions to process in a workload for `Get generate status` API call.

 The call creates a workload when the specified minimum chunk size is met and, after all subscriptions are processed, doesn’t create another workload.

 **Note:** By default, a maximum of 4 parallel workload executions are allowed. The maximum is configured in the flow launcher job that is defined in the `sn_cld_intg_core_flow_launcher_job_config` table.

 -   Type: integer
-   Default value: 5

</td></tr><tr><td>

sn\_cld\_intg\_azure.advisor\_list\_recommendation\_min\_chunk\_size

</td><td>

Minimum number of subscriptions to process in a workload for the `list recommendation` API call.The call creates a workload when the specified minimum chunk size is met and, after all subscriptions are processed, doesn’t create another workload.

**Note:** Increasing the chunk size might increase the overall processing time because subscriptions are processed sequentially. By default, a maximum of 4 parallel workload executions are allowed. The maximum is configured in the flow launcher job that is defined in the `sn_cld_intg_core_flow_launcher_job_config` table.

-   Type: integer
-   Default value: 1

</td></tr><tr><td>

sn\_clin\_azure.advisor\_process\_recommendation\_min\_chunk\_size

</td><td>

The number of recommendation responses that should be processed in a workload for the API call and persisted in the Rightsizing or Unused Machines recommendation table.

 The call creates a workload when the specified minimum chunk size is met and, after all subscriptions are processed, doesn’t create another workload.

 **Note:** Increasing the chunk size might increase the overall processing time because subscriptions are processed sequentially. By default, a maximum of 4 parallel workload executions are allowed. The maximum is configured in the flow launcher job that is defined in the `sn_cld_intg_core_flow_launcher_job_config` table.

 -   Type: integer
-   Default value: 20

</td></tr></tbody>
</table><table id="table_mhq_gtr_nbc"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cld\_intg\_aws.pricesheet\_timeout\_aws

</td><td>

Controls AWS price sheet download flow time out duration.-   Value format: DD HH:MM:SS
-   Default value: 2 days

</td></tr></tbody>
</table><table id="table_bmd_bgv_gdc"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cld\_intg\_core.optimize\_pivot\_keys

</td><td>

Enables the option to limit the columns used for pivot key generation so that multiple cost line items map to a single pivot key, which decreases the number of entries in the cost usage table. -   Type: true \| false
-   Default value: false

</td></tr><tr><td>

sn\_cld\_intg\_core.sink\_only\_required\_ci\_types

</td><td>

Enables the option that only the line items that have the CI types - cmdb\_ci\_vm\_instance, cmdb\_ci\_database, cmdb\_ci\_cloud\_database, cmdb\_ci\_storage\_volume, cmdb\_ci\_storage\_vol\_snapshot, are sent to Glide for storage in the cost usage table, reducing the data that is transmitted.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

sn\_cld\_intg\_core.enable\_tag\_filtering

</td><td>

Enables the option that only the tag names that are mapped to tag categories in the Cloud Cost Management Workspace are considered to save the tag values. This verification optimizes the memory requirement to transfer the tags to Glide.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

ready.job.files.timeout

</td><td>

Maximum time in minutes to generate billing files for AWS assume role setup or blobs for Azure on Glide.You can monitor the AWS billing job files \[sn\_cld\_intg\_aws\_billing\_files\] table for AWS and the Azure billing Job chunk blob detail \[sn\_cld\_intg\_azure\_job\_chunk\_blob\_detail\] table for Azure only when the download is in progress and the time-out condition is met.

-   Type: String
-   Default value: 180

</td></tr><tr><td>

ready.job.nofiles.timeout

</td><td>

Maximum time in minutes to wait for the backend to pick up the job when there’s no other job being processed for the same provider. **Important:** To configure this system property, contact your support team. Don't configure it on your own.

-   Type: String
-   Default value: 10

</td></tr><tr><td>

reserved.job.timeout

</td><td>

Maximum time in minutes to wait for the job to change from Reserved to In progress state. **Important:** To configure this system property, contact your support team. Don't configure it on your own.

-   Type: String
-   Default value: 5

</td></tr><tr><td>

inprogress.job.timeout

</td><td>

Maximum time in minutes to wait for the job to change from In progress to Sink complete state.**Important:** To configure this system property, contact your support team. Don't configure it on your own.

-   Type: String
-   Default value: 10

</td></tr><tr><td>

sinkcomplete.job.timeout

</td><td>

Maximum time in minutes to wait for the job to change from Sink begin to Sink complete state.**Important:** To configure this system property, contact your support team. Don't configure it on your own.

-   Type: String
-   Default value: 20

</td></tr><tr><td>

billing.data.post.processing.timeout

</td><td>

Maximum waiting time in minutes for billing from Post processing to Complete phase. The final stage of billing job includes inserting spend data into Glide. During the Post processing phase, the newly inserted data is activated and the existing data is inactivated. Increasing the time out value gives more time for the activation flow to complete.

-   Type: String
-   Default value: 30

</td></tr><tr><td>

retry.cred.failed.billing.job.timeout

</td><td>

Maximum time in minutes to wait before canceling a job that's in the Requested state due to credential failure. When you add a credential, it’s sent to the backend only in the next billing run, resulting in a temporary failure. However, retries are made to establish a connection. This property specifies how long to wait before canceling the reattempted job.

-   Type: String
-   Default value: 30

</td></tr><tr><td>

sn\_cld\_intg\_azure.billing\_chunk\_duration

</td><td>

Defines the chunk size for Azure billing blob in days. By default, each blob contains billing data for three days.

-   Type: Number
-   Default value: 3

</td></tr></tbody>
</table><table id="table_kvf_lvr_yhc"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cld\_intg\_core.enable\_multicurrency\_setup

</td><td>

Enables the multi-currency setup feature for users.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

sn\_cld\_spend\_core.aws\_exchange\_rate\_date

</td><td>

Sets up the currency exchange rate date for AWS.

 Type: integer

</td></tr><tr><td>

glide.currency2.system\_rate\_&lt;table&gt;

</td><td>

Eliminates the need to maintain a separate custom exchange rate table exclusively for Cloud Cost Management. To use an existing exchange rate table from another application, enter its name as the value for this property.-   Type: String
-   Value: name of the table

</td></tr><tr><td>

sn\_cld\_spend\_core.ccm\_custom\_conversion\_rate\_&lt;table&gt;

</td><td>

Sets up the currency exchange rates based on the preferred currency. The table to be used for conversion should extend to the System Currency Conversion Rates \[fx\_conversion\_rate\] table.-   Type: String
-   Value: name of the table

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Cost Management reference](../concept/reference-cloudinsights.md)

