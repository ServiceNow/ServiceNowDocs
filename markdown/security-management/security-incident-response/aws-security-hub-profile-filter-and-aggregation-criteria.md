---
title: Define filter and aggregation criteria for AWS Security Hub findings ingestion
description: You can define and set filter conditions so that you can specify which incoming findings should create security incidents. You can also define additional incident field criteria that allows an incoming finding to be appended to an open security incident instead of creating an another security incident for the same finding.Set the filtering conditions so that security incidents are created only when the filtering conditions match.Define additional incident aggregation criteria that aggregates an incoming AWS Security Hub finding to an existing SIR security incident instead of creating similar, potentially duplicate incidents. When you use field matching value criteria for each profile, this additional aggregation can reduce the number of active, overlapping security incidents by placing all related incidents data on a single security incident.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Amazon Web Services \(AWS\) Security Hub integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Define filter and aggregation criteria for AWS Security Hub findings ingestion

You can define and set filter conditions so that you can specify which incoming findings should create security incidents. You can also define additional incident field criteria that allows an incoming finding to be appended to an open security incident instead of creating an another security incident for the same finding.

## Set the filtering conditions for AWS Security Hub findings to create security incidents

Set the filtering conditions so that security incidents are created only when the filtering conditions match.

### Before you begin

Role required: sn\_si.admin

### About this task

This type of filtering helps you to isolate security incidents and limits the number of security incidents that you create. If you set additional filtering criteria, only the required findings are ingested without having to change the query or the triggered incident configuration.

Perform the following steps to define the criteria that an incoming AWS Security Hub finding must satisfy so that a security incident is created:

### Procedure

1.  Select **Apply Pre-Filter** in the Pre-Filtering section.

    You can use this option to filter specific findings and reduce the load of findings ingestion.

    In the **API Filter** field, enter a JSON condition as per your requirement that filters out specific findings based on the condition. For example, enter the following value to filter out findings that have Workflow Status as Resolved in Security Hub:

    ```
    {"Filters"{
      "WorkflowStatus":[{
      "Comparison":"NOT_EQUALS",
      "Value": "RESOLVED"}]
     }
    }
    ```

    Based on the provided condition, AWS Security Hub findings are ingested and displayed in the AWS Security Hub findings raw table.

    Navigate to **All** &gt; **AWS Security Hub Findings Integration** &gt; **AWS Security Hub findings raw** to view the raw findings data.

2.  In the Select Finding fields for filter conditions section, select **Display available finding fields** to display a list of all available fields in a AWS Security Hub finding.

    From **All finding fields** list, select the finding fields which you want to be displayed in the Security incident generation conditions section.

    **Note:** An AWS Security Hub finding contains multiple fields and values. In the **All finding fields** list, you can search for a finding field as per your requirement and select it.

3.  In the Security incident generation conditions section, select **Filter based on conditions** to define the criteria that an incoming AWS Security Hub finding must satisfy so that a security incident is created.

    The first field in the Filter Conditions contains a default list of two hundred fields that are available on a AWS Security Hub finding and the finding fields you selected in the Select Finding fields for filter conditions section.

    The second field in the Filter Conditions contain conditional operators. The option you choose determines the condition that must be fulfilled to ingest a finding.

    The third field in the Filter Conditions contain values supported by the available finding fields. Verify that the finding field that you enter matches the values of the findings.

    For example, use the filter condition `contains` for the following fields with multiple values:

    -   Workflow\(Status\)
    -   WorkflowState
4.  Using the lists and fields of the conditions builder, set the filters for the first row.

5.  To add more conditions, click **AND** or **OR**.

    -   If **AND** is selected, all conditions must be matched.
    -   If **OR** is selected, either condition can be matched.
6.  To set a second filter condition, click **New Criteria**.


### Result

Based on the filtering conditions, AWS Security Hub findings are imported to SIR. Navigate to **All** &gt; **AWS Security Hub Findings Integration** &gt; **AWS Security Hub findings import** to view the imported findings.

## Define conditions to aggregate AWS Security Hub findings to a security incident

Define additional incident aggregation criteria that aggregates an incoming AWS Security Hub finding to an existing SIR security incident instead of creating similar, potentially duplicate incidents. When you use field matching value criteria for each profile, this additional aggregation can reduce the number of active, overlapping security incidents by placing all related incidents data on a single security incident.

### Before you begin

Role required: sn\_si.admin

### About this task

If a new incident matches all the values that are selected in the aggregation field conditions in the mapping step, the incident is automatically added to the most recently opened security incident with the same field values. As a user with the sn\_si.analyst role working with security incidents, you can view all the added aggregate incidents on a related list on a security incident.

All the aggregated AWS Security Hub findings on a security incident are displayed on the AWS Security Hub related list. This list details the associated timestamps and aggregated field values. This information helps you understand why AWS Security Hub findings are added to the existing security incidents.

### Procedure

1.  To define additional incident field criteria that allows an incoming AWS Security Hub finding to be appended to an open security incident instead of creating a new incident, select the **Aggregation Conditions** option.

2.  In the **Incident fields with matching values** field, enter the field values that you want to match on existing security incidents in your ServiceNow AI Platform instance.

    All field values that you selected in the multi-selection input field must match so that the aggregation criteria is met and that this incoming incident can be appended to an existing security incident. This selection implies it is an `AND` condition where fields, such as Observables and Configuration Items that may have multiple field values, are mapped to them. If only a subset of the values is matched, the AWS Security Hub findings aggregation conditions are not met and a new security incident is created.

3.  To add multiple field matching conditions, click **Add New Criteria**.

    The aggregation occurs if any one of the multi-selection field conditions that you define are met. This selection implies the `OR` condition.

4.  To update the work note for a new finding when it is added to a security incident, select **Log work note for new finding**.

    The work note logs that a new finding is added and includes a link to the finding details. The log work note also updates more details that you add to the work note field in your mapping section.

5.  To configure the schedule, click **Continue**.


### Result

Based on the aggregation conditions, AWS Security Hub findings are are aggregated to create to create a SIR incident. Navigate to **All** &gt; **AWS Security Hub Findings Integration** &gt; **AWS Security Hub findings to task** to view the list of security incidents that have been created.

### What to do next

Set a schedule to retrieve the finding data and finding incidents that match the criteria in the profile.

