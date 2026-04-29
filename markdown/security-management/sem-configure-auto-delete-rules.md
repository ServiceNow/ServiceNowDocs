---
title: Configuring auto-delete rules
description: By configuring auto-delete rules, you can automate the process of deleting older findings and remediation tasks.Create rules to delete findings and remediation tasks automatically based on specific filter conditions. These rules help remove older records from the Findings and Remediation Task tables.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure rules to manage findings, Implement, Unified Security Exposure Management, Security Operations]
---

# Configuring auto-delete rules

By configuring auto-delete rules, you can automate the process of deleting older findings and remediation tasks.

The base system provides two preconfigured auto-delete rules that automatically remove closed records and any related records. One rule targets findings, and the other targets remediation tasks. These rules are inactive by default, so you must activate them manually before they can delete any records. You can use the two preconfigured rules or create your own to suit your specific needs.

Configuration of auto-delete rules includes the following steps.

**Parent Topic:**[Configure rules to manage findings](../task/sem-configure-rules-manage-findings.md)

**Related topics**  


[Deleting stale findings automatically using auto-delete rules](sem-deleting-stale-findings-automatically.md)

## Create or edit auto-delete rules

Create rules to delete findings and remediation tasks automatically based on specific filter conditions. These rules help remove older records from the Findings and Remediation Task tables.

### Before you begin

Role required: See [Access control lists \(ACLs\) for administration rules](sem-acls-for-admin-rules.md)

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Select **Review** on the **Auto delete rules** tile.

4.  On the Rules page, select **Auto delete** in the navigation pane.

5.  Select **New** and fill in the fields on the form:

    |Field|Description|
    |-----|-----------|
    |Details|
    |Tablename|Name of the table for which the rule is being applied.|
    |Matchfield|Field for which the system monitors the duration.|
    |Age in seconds|Age of the vulnerability record to be deleted. For both findings and remediation task rules, the age is 365 days. This age is displayed in seconds.|
    |Active|Indicates whether the rule is active.|
    |Cascade delete|Option to delete all matching records, plus any records referring to them. If this option isn’t selected, only matching records are deleted, but not the records that refer to them.|
    |Conditions|
    |Condition fields|Filter conditions defining the records in the Findings and Remediation Task tables to which the rules apply.|
    |New condition set|Adds more condition filter fields to choose from.|

6.  Select **Set conditions**.

7.  Select the conditions.

8.  Select **Set**.

9.  Select **Save**.

    Once the rule is activated, the hourly platform function, **Auto flush** deletes those records from the table for which the rule is activated.

    If your environment contains millions of records that match your delete criteria, it's advisable to consult with ServiceNow Customer Support before enabling the auto-delete rules. They can assist you in deleting records through a phased process to ensure smooth and efficient data management.


