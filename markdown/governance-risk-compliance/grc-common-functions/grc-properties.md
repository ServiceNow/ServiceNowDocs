---
title: Governance, Risk, and Compliance properties
description: The following are the common GRC properties under Policy and Compliance and Risk Management.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [GRC reference, Common GRC features, Governance, Risk, and Compliance]
---

# Governance, Risk, and Compliance properties

The following are the common GRC properties under Policy and Compliance and Risk Management.

## Common GRC properties

Navigate to **Policy and Compliance** &gt; **Administration** &gt; **GRC Properties**. Alternatively, you can navigate to **Risk** &gt; **Administration** &gt; **GRC Properties**.

<table id="table_dhr_rjk_3jb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Consider executing indicator result business rules on indicator job runsn\_grc.indicator\_result\_execute\_business\_rules\_on\_indicator\_job\_run

</td><td>

The property is a GRC indicator for the executed result business rules on the indicator job run and is in GRC: Profiles.-   Type: true or false
-   Default value: false

</td></tr><tr><td>

Consider executing indicator task business rules on indicator job runsn\_grc.indicator\_task\_execute\_business\_rules\_on\_indicator\_job\_run

</td><td>

The property is a GRC indicator for the executed task business rules on the indicator job run and is in GRC: Profiles.-   Type: true or false
-   Default value: false

</td></tr><tr><td>

Consider executing indicator business rules on indicator job runsn\_grc.indicator\_execute\_business\_rules\_on\_indicator\_job\_run

</td><td>

The property is a GRC indicator for the executed business rules on the indicator job run and is in GRC: Profiles.-   Type: true or false
-   Default value: false

</td></tr><tr><td>

Enable same response assessment grouping option. sn\_grc.enable\_consolidate\_asmt

</td><td>

This property is used by the feature “Attestation Response Consolidation​.“ When this is set to true, an additional option “Provide same response for all assessments” is added to the grouping choices.-   Type: Yes or No
-   Default value: Yes

</td></tr><tr><td>

Total number of questions allowed in a different response type grouped assessment = number of questions in one assessment \* number of selected assessments. sn\_grc.grouped\_questions\_limit

</td><td>

This property is used when creating a group \(different response type\) of attestations/risk assessments. If total number according to formula exceeds it throws an error to restrict group creation to prevent too many questions in a group. If this property is increased by customer it may impact performance.

</td></tr><tr><td>

Automatically make indicators for item. sn\_grc.auto\_create\_indicator

</td><td>

If this property is set to true indicators are automatically generated once the content\(Risk statement/Control objective\) is linked to indicator template.-   Type: Yes or No
-   Default value: Yes

</td></tr><tr><td>

Maximum number of indicator events allowed. sn\_grc.indicator\_max\_events

</td><td>

These are the maximum number of indicator run related events that are allowed to be fired during a scheduled indicator run. Typically the no of events to be fired is determined by Total no of indicators/Batch size of indicator to run. If the result event count exceeds Maximum number of indicator events allowed then the batch size id adjusted to total indicators/ Maximum number of indicator events allowed.

</td></tr><tr><td>

Batch size of indicator to run. sn\_grc.indicator\_min\_batch\_size

</td><td>

This property controls how many indicators must run in a batch. Indicators are always run in batches. For each batch there is an event fired with sys\_ids of the indicators to be run. For example, if the total number of indicators are 10000 and the batch size is 1000 there will be 10 events fired and each event has list of 1000 indicators to be run.

</td></tr><tr><td>

Total number of questions allowed in a same response type grouped assessment = number of questions in one assessment \* number of selected assessments. sn\_grc.consolidated\_questions\_limit

</td><td>

This property is used when creating a group \(same response type\) of attestations/risk assessments. If total number as per formula exceeds it throws an error to restrict group creation to prevent too many questions in a group. If this property is increased by customer it may impact performance.

</td></tr><tr><td>

Maximum number of open indicator tasks. sn\_grc.max\_open\_indicator\_tasks

</td><td>

Each indicator that is run will have an associated task created in the sn\_grc\_indicator\_task table. This property controls the number of indicator tasks active at any point of time. If the indicators exceed the count, a sn\_grc.max\_tasks\_exceeded event is fired.For more information, see [KB0788099](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0788099).

</td></tr><tr><td>

Automatically close a issue when all its related remediation tasks are closed. sn\_grc.automatically\_close\_all\_issues\_when\_all\_tasks\_closed

</td><td>

When this property is set to true, an issue will be automatically closed when all its children tasks are closed. Otherwise, the user has to manually close the issue.-   Type: Yes or No
-   Default value: Yes

</td></tr><tr><td>

Issue assignee suggestion based on. sn\_grc\_pred\_intel.issue\_assignee\_suggest

</td><td>

If this property is set to “None” the Suggest icon wouldn’t be available beside the Assigned To field on the issue form. If it is set to “Similarity Analysis” then the suggest icon would be available and the assignment predictions would happen based on the similarity solution definition name provided in the property " Machine learning solution for prediction of issue assignees”, when the user clicks the suggest icon.

</td></tr><tr><td>

Machine learning solution for prediction of issue assignees. sn\_grc\_pred\_intel.ml\_solution\_for\_issue\_assigned\_to

</td><td>

This property is used for mentioning the name of the Similarity solution definition that would be used for prediction of issue assigned to. If this field is left blank or has an incorrect/non-existent Similarity solution definition name then the user would get an error on clicking the suggest icon next to the issue assigned to field. The user could have many existing similar solutions on their instance. This provides some amount of flexibility to select the appropriate solution definition name.

</td></tr><tr><td>

Default sample size of indicator templates and indicators. sn\_grc.indicator.default.sample\_size

</td><td>

The property is used to set the default sample size of indicator templates and indicators.

</td></tr><tr><td>

Max number of records to be processed by indicator supporting data collection job. sn\_grc.max\_supporting\_data\_records\_to\_process

</td><td>

The property is used to collect the configured number of records from the supporting data statistics table whenever the supporting data collection job runs. The default value is 500.

</td></tr><tr><td>

Supporting data limit for indicators with % based sampling. sn\_grc.supporting\_data\_percentage\_max\_records\_limit

</td><td>

The property is used to set an upper limit in collecting supporting data although you have set a percentage of records to be collected when you select **Percentage** as the **Sample collection type** in the Supporting Data tab of the Indicator Template or Indicator forms.

</td></tr><tr><td>

Advanced issue grouping functionality

</td><td>

This property is used to enable advanced issue grouping functionalities, such as management methods for issue grouping and issue grouping within workspaces. After you enable this property the following changes occur:-   All grouped issues in the system will be updated with the management method set to Manage child.
-   Parent issues without child issues will be marked as standalone issues.
-   Confidential child issues under non-confidential parent issues will be removed from the group and marked as standalone issues.
-   Confidential parent issues that are marked as non-confidential will have their confidential child issues moved out of the group and marked as standalone issues.
-   The default management method for the issue auto-grouping functionality will be Manage child.
-   When closing child issues, the parent issue won’t be closed automatically if the management method is Manage child.
-   If the management method is Manage parent, fields such as **State**, **Response**, and **Explanation** will be non-editable on child issues.
-   If the management method is Manage parent, the **State**, **Response**, and **Explanation** fields are inherited by the child issues from the parent issue.

**Note:** If the mandatory fields, such as **Assigned to** and **Issue manager** fields are empty in the child issues, the child issues will inherit those fields from the parent issue.


**Note:** After you enable this property, you can't disable it.

</td></tr><tr><td>

Execute pending actions asynchronously post indicator run. sn\_grc.execute\_indicator\_next\_actions\_async

</td><td>

If the property is set to True, then the two custom queues are leveraged to process indicators at a high level. If the property is set to False, then the indicator processing is done by the default queue processor.

</td></tr><tr><td>

Collect supporting data asynchronously for an indicator using collection job. sn\_grc.process\_indicator\_supporting\_data\_async

</td><td>

If True, then the supporting data collection job collects the supporting data into the supporting data statistics table. If False, then the supporting data are collected from the Default queue. The supporting data collection job isn’t leveraged in this case.

</td></tr><tr><td>

Number of days after indicator task due date to send overdue notification.

</td><td>

This property is used to notify the users of the number of days lapsed since the due date.

</td></tr><tr><td>

Number of days before indicator task due date to send reminder notification.

</td><td>

The property is used to notify the users of the upcoming due date for an indicator task.

</td></tr></tbody>
</table>## Composite Entity properties

Navigate to **All** &gt; **Composite Entities** &gt; **Properties**.

|Property|Description|
|--------|-----------|
|Separator used to auto-generate the name of composite entity and composite entity classes \[sn\_grc\_comp\_ent.name\_separator\]|Property to specify the separator that is used for the composite entity and composite entity class name.|
|Maximum number of entities that can be rendered inside the content tree \[sn\_grc\_comp\_ent.max\_content\_tree\_entity\_count\]|Property to define the maximum number of entities displayed in the content tree during an entity search.|

**Parent Topic:**[Governance, Risk, and Compliance reference](../concept/grc-reference.md)

