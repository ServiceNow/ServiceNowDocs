---
title: Defining filter and aggregation criteria
description: You can define and set filter conditions so that you can specify which incoming Microsoft Azure Sentinel incidents should create security incidents. You can also define additional incident field criteria that allows an incoming incident to be appended to an open security incident instead of creating an incident.Set the filtering conditions so that security incidents are created only when the filtering conditions match.Define additional incident aggregation criteria that aggregates an incoming incident to an existing SIR security incident instead of creating similar, potentially duplicate incidents. When you use field matching value criteria for each profile, this additional aggregation can reduce the number of active, overlapping security incidents by placing all related incidents data on a single security incident.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Microsoft Azure Sentinel integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Defining filter and aggregation criteria

You can define and set filter conditions so that you can specify which incoming Microsoft Azure Sentinel incidents should create security incidents. You can also define additional incident field criteria that allows an incoming incident to be appended to an open security incident instead of creating an incident.

**Important:**

Microsoft has extended the deprecation of the Azure Sentinel experience in the Azure portal from March 2026 to March 2027.

If you are currently using the Azure Sentinel integration with Security Incident Response \(SIR\), we strongly recommend migrating to the new Defender portal integration as soon as possible. The Defender integration includes a built-in migration utility that automatically converts your existing Sentinel profiles into Defender profiles, while ensuring continuity of incidents created through Sentinel after the transition. For more information, see [Microsoft Sentinel to Defender Migration Guide](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2795226).

## Set the filtering conditions for security incidents

Set the filtering conditions so that security incidents are created only when the filtering conditions match.

### Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

### About this task

This type of filtering helps you to isolate security incidents and limits the number of security incidents that you create. If you set additional filtering criteria, only the required incidents are ingested without having to change the query or the triggered incident configuration.

### Procedure

1.  To define the criteria that an incoming Microsoft Azure Sentinel incident must satisfy so that a security incident is created, select **Filter based on conditions**.

    The options in the first field in the Filter Conditions match the fields that are displayed on the Azure Sentinel Sample Incident Ingestion section for the incident that you ingested. These fields are dynamic and change depending on the incident that you ingest. The criteria that you enter is case-sensitive. Verify that the criteria that you define matches the values of the incident.

    Use the filter condition `contains` for the following fields with multiple values:

    -   properties\(labels\)
    -   properties\(additionalData\(alertProductNames\)\)
    -   properties\(relatedAnalyticRuleIds\)
    -   properties\(additionalData\(tactics\)\)
    Because the filter condition can retrieve only strings, you must use the `contains` filter condition for the above fields to ensure that the data is filtered correctly.

    ![Filter conditions builder.](../image/sentinel-filtering.png "Security incident generation conditions")

2.  Using the lists and fields of the conditions builder, set the filters for the first row.

3.  To add more conditions, click **AND** or **OR**.

    -   If **AND** is selected, all conditions must be matched.
    -   If **OR** is selected, either condition can be matched.
4.  To set a second filter condition, click **New Criteria**.


## Define aggregation conditions

Define additional incident aggregation criteria that aggregates an incoming incident to an existing SIR security incident instead of creating similar, potentially duplicate incidents. When you use field matching value criteria for each profile, this additional aggregation can reduce the number of active, overlapping security incidents by placing all related incidents data on a single security incident.

### Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

### About this task

If a new incident matches all the values that are selected in the aggregation field conditions in the mapping step, the incident is automatically added to the most recently opened security incident with the same field values. As a user with the sn\_si.analyst role working with security incidents, you can view all the added aggregate incidents on a related list on a security incident.

All the aggregated incidents on a security incident are displayed on the Azure Sentinel Aggregated Incidents related list. This list details the associated timestamps and aggregated field values. This information helps you understand why incidents are added to the existing security incidents.

### Procedure

1.  To define additional incident field criteria that allows an incoming Microsoft Azure Sentinel incident to be appended to an open security incident instead of creating a new incident, select the **Aggregation Conditions** option as shown in the following figure.

    ![Aggregation to define additional incident filtering criteria.](../image/sentinel-aggregation.png "Aggregation Conditions")

2.  In the **Incident fields with matching values** field, enter the field values that you want to match on existing security incidents in your ServiceNow AI Platform instance.

    All field values that you selected in the multi-selection input field must match so that the aggregation criteria is met and that this incoming incident can be appended to an existing security incident. This selection implies it is an `AND` condition where fields, such as Observables and Configuration Items that may have multiple field values, are mapped to them. If only a subset of the values is matched, the Azure Sentinel Incident aggregation conditions are not met and a new security incident is created.

3.  To add multiple field matching conditions, click **Add New Criteria**

    The aggregation occurs if any one of the multi-selection field conditions that you define are met. This selection implies the `OR` condition.

4.  To update the work note for a new incident when it is added to a security incident, select **Log work note for new Incident**.

    The work note logs that a new incident is added and includes a link to the incident details. The log work note also updates more details that you add to the work note field in your mapping section.

5.  To configure the schedule, click **Continue**.


### What to do next

Set a schedule to retrieve the incident data and ingested incidents that match the criteria in the profile.

