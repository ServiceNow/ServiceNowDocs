---
title: Report\_view access control
description: The report\_view operation is a record type ACL that restricts access to data visualizations and Core UI reports. Only users who have one of the required roles can view visualizations that contain the restricted resource.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/report-view-access-control.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Report\_view access control

The report\_view operation is a record type ACL that restricts access to data visualizations and Core UI reports. Only users who have one of the required roles can view visualizations that contain the restricted resource.

To create a report\_view ACL, follow the [general procedure for creating an ACL rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/t_CreateAnACLRule.md). Create an ACL rule with the following settings:

-   Type: record
-   Operation: report\_view
-   First table field: Required. Enter the name of the table on which to apply the ACL rule.
-   Second \(unlabeled\) table field: If you want the ACL rule to apply to a specific field on the table, select the field name here. Select a wildcard \(\*\) to give access to all fields on the table. Leave this field empty to create a row-level ACL rule, which gives access to the table records.
-   Conditions: Specify at least one role OR at least one security attribute condition. Data conditions and advanced conditions are not supported.

Set the other options freely.

## Table vs field report\_view rules

Record-type ACL rules can apply to either a table or a field \(or all fields\) on a table. For report\_view operations, a table rule allows only users with the specified roles to see the contents of visualizations of that table. A field rule allows only users with the specified roles to see visualization contents that show the field. A field rule also restricts all content of a visualization that has that field in its data source conditions. Field report\_view rules also apply to reference \(dot-walked\) fields.

For example, a report\_view field ACL requires that users have the chat\_admin role to view the Assignment Group field in visualizations of the Chat Queue table. This table is readable to all internal users. Two single-score visualizations are created that show the count of records on Chat Queue. One visualization has no conditions, and the other has Assignment Group = Database. Both visualizations are shared with a user who doesn't have the chat\_admin role. This user can see the metric in the visualization without conditions. However, when they open the visualization with the condition on the Assignment Group field, they see that their access is restricted by the report\_view ACL.

## Report\_view operation design considerations

Use these guidelines when creating your own report\_view operation access controls.

-   **Restrict access to visualizations by a required role**

    The report\_view operation usually has an Allow If decision type, granting view access to visualizations to users with specified roles.

-   **Require conditions to be met to view a visualization**

    Instead of requiring user roles, a report\_view operation can require conditions to be met. These conditions are defined by security attributes. Often these are basic conditions that must be met, so the report\_view rule has the Deny Unless decision type.

-   **Restrict access to list visualizations with a read operation**

    List data visualizations and Core UI list reports do not follow report\_view ACLs. Instead, they use record access controls that determine who can access data in a table or field. To restrict access to record data in lists, create a read operation access control. For more information about record access controls, see [Access control list rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control-rules.md).


## Report\_view field ACL rule with roles

You need to grant access to visualizations of all fields on the Performance Analytics cached forecast table to users with the pa\_admin role. Therefore you create an ACL rule. The rule affects visualization access, so you create a rule where type=record and operation=report\_view. You specify the Cached forecast \[cached\_forecast\] table. For the field, you specify the wildcard \(\*\). Doing so means that the rule grants viewing rights to visualizations of all fields on cached\_forecast to users with the specified roles. Finally, you specify the pa\_admin role.

\[Omitted image "report-view-acl-rule.png"\] Alt text: Report\_view rule with a wildcard in the Field field, giving access to all fields on the specified table to the selected roles.

## Report\_view table ACL rule with security access condition

You want only logged-in users with roles to be able to see visualizations of the Incident \[incident\] table. You can't set these conditions with role requirements, but fortunately there is an existing [compound security attribute](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/compound-security-attributes.md) called UserIsAuthenticated for this situation. Therefore, you create a report\_view table ACL on Incident that uses this security attribute condition. You also set the decision type to Deny Unless. Doing so prohibits any user not logged in with a role from viewing visualizations of the Incident table, regardless of any other report\_view ACL rules they satisfy.

\[Omitted image "report-view-sec-access-con.png"\] Alt text: Report\_view rule with a security attribute condition instead of a required role.

-   **[Fallback ACL evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/read-access-control.md)**  
When a data visualization is run, report\_view access control lists \(ACLs\) are evaluated on the table and table fields that the report is based on. If no report\_view ACL exists, there is a fallback check on table-level read ACL roles.

**Parent Topic:**[Configure data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/configure-data-visualizations.md)

**Related topics**  


[Configure an ACL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/t_CreateAnACLRule.md)

[Security Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-attributes-landing.md)

