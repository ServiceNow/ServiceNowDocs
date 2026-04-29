---
title: Confidential records
description: You can mark sensitive GRC records as confidential. You can then make sure that the right people have access to these records.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# Confidential records

You can mark sensitive GRC records as confidential. You can then make sure that the right people have access to these records.

You can mark sensitive GRC records as confidential by setting the confidential option for a record. By doing this action, you can ensure that only certain users or users from specific user groups can access these confidential records.

## Confidentiality property

A new option **Enable record level confidentiality** is available under GRC properties at the record level to enable confidentiality.

**Important:** The **Enable record level confidentiality** property is turned off by default. When it is enabled, it can't be turned off again.

The confidential records in GRC are listed under the GRC Confidential module. The GRC confidential records module is displayed in the application navigator only when you enable the **Enable record level confidentiality** property.

Starting with San Diego, the GRC Confidential Records module is available for the Audit Management, GRC core, Policy and Compliance Management, and Risk Management applications.

## Unmarking confidentiality on the record

When you unmark confidentiality on a record, allowed users and groups on that record will be removed and all the users will get access to the record based on ACL.

## User roles that are required to access the confidential records

Users with the GRC confidential user \(sn\_grc.confidential\_user\) role can access the confidential records. This role is for the users who are not GRC users but who want to access the GRC confidential records.

Users who have access and who are named in the record continue to have access to the record with the existing GRC role.

Consider the following examples for different roles:

-   You're a risk user and you were given access to a risk record earlier. Now, you're part of the allowed users list for the same record. Therefore, even if you don't have the sn\_grc.confidential\_user role, you can access the record because you had access to this record earlier and your name is now listed on the allowed users list.
-   Your name is listed on the record, but you don't have the sn\_grc.confidential\_user role. You must have the sn\_grc.confidential\_user role first to access the record.

When a record is marked as confidential, an email notification is sent out to the users and the user group members informing them about the assignment and the roles that are required to access the record. Every user that is listed in the Allowed users and Allowed groups list gets an email notification about the assignment of the record.

## Confidentiality tab on the form

The **Confidentiality** tab on the form displays the following lists and options:

-   Confidential option: Enabling the **Confidential** option on the Confidentiality tab displays the Allowed users and Allowed groups lists as shown in the following figure.

    **Note:** A user with write access to the record can enable the **Confidential** option.

    ![Confidential tab on a form.](../image/confidential-record-risk-event1.png "Confidentiality field on a form")

-   Allowed users list: When a record is marked as confidential, only the users in the Allowed users list have access to the record. A user who is listed in the Allowed users list should either have read access to the record or have the sn\_grc.confidential\_user role to access the confidential records.

    The logged-in user who enables the **Confidential** option gets auto-populated in the Allowed users list. The user who enables the **Confidential** option on the tab is auto-appended to the Allowed users list by default. Those users with write access to the record can unlock and update the Allowed users list.

    **Note:** There are no restrictions on which users can be added to the Allowed users list. A user who doesn't have the GRC role should have the sn\_grc.confidential\_user role to access the record. An email notification is also sent to the user about the role requirement.

-   Allowed groups list: When a record is marked as confidential, only the users that are listed in the Allowed groups list have access to the record. Those users with write access to the record can unlock and update the Allowed groups list.

    **Note:** Confidential records are visible to the users who are listed in the Allowed users or Allowed groups list. By default, the administrators can also view the confidential records. If you do not want the administrators to view the confidential records, follow the steps mentioned in [KB1497382](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1497382).


Users who don't have the GRC user role but are listed in the Allowed users list or Allowed groups list can be assigned with the sn\_grc.confidential\_user role to access the confidential records.

Confidentiality is supported on the following tables.

|Table label|Table name|Application scope|Users that get auto-populated in the allowed users list|Groups that get auto-populated in the allowed groups list|
|-----------|----------|-----------------|-------------------------------------------------------|---------------------------------------------------------|
|Audit task|sn\_audit\_task|GRC: Audit Management|Assigned To, Engineering lead, Engineering auditors, Engineering approvers|Not applicable|
|Engagement|sn\_audit\_engagement|GRC: Audit Management|Auditors, Approvers, Engagement lead|Not applicable|
|Evidence request task|sn\_grc\_advanced\_evidence\_response|GRC: Advanced Core|Requester, Assigned To, Approvers, Watchlist, Requested on behalf of|Assignment Group|
|Issue|sn\_grc\_issue|GRC: Profiles|Assigned to, Issue Manager, Opened by|Issue Manager Group,Assignment Group|
|Observation|sn\_audit\_advanced\_observation|GRC: Advanced audit|Owner, Respondent, Peer Reviewer, Reviewer, Watch list Users, Engagement lead, Engineering auditor, Engineering approver|Assignment Group|
|Policy exception|sn\_compliance\_policy\_exception|GRC: Policy and Conformance Management|Requester, Approver, Watch list|Approval Group|
|Remediation task|sn\_grc\_task|GRC: Profiles|Assigned to, Watch list, Issue Manager, Issue Assigned To|Not applicable|
|Risk events|sn\_risk\_advanced\_event|GRC: Advanced Risk|Current logged in user, Owner, Approver|Owning group, Approval groups|
|Disclosure|sn\_esg\_disclosure|Operational Sustainability Management|Logged in user, reviewer, assigned to|Not applicable|
|Material topic|sn\_esg\_material\_topic|Operational Sustainability Management|Logged in user, reviewer|Not applicable|
|Metrics|sn\_grc\_metric|Operational Sustainability Management|Logged in user, enterprise owner, data owner|Enterprise owner group, data owner group|
|Metric definitions|sn\_grc\_metric\_definition|Operational Sustainability Management|Logged in user, enterprise owner, data owner|Enterprise owner group, data owner group|
|Composite metric definitions|sn\_grc\_composite\_metric\_definition|Operational Sustainability Management|Logged in user, enterprise owner|Enterprise owner group|

Starting with Utah, confidential configuration for all the default confidentiality enabled GRC tables except sn\_esg\_material\_topic, sn\_grc\_metric, sn\_grc\_metric\_definition, sn\_grc\_composite\_metric\_definition, are shipped to sn\_grc\_confidentiality\_configuration table. You can update and remove the user and group fields that are auto-populated into allowed users and groups of a record from this configuration.

To know more about the confidentiality feature, see [KB1218856](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1218856).

[Configure confidentiality in your GRC tables](../task/configure-confidentilaity-on-grc-tables.md)

To enable confidentiality in your GRC tables, you must perform additional configuration, such as updating the client scripts and updating access control lists \(ACLs\). After you update the configuration for a specific ServiceNow platform table, the confidentiality functionality can be used on those table's forms.

For information on how to enable confidentiality in your GRC tables, see [KB1497382](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1497382).

**Note:** You must log in to Now Support to view the Knowledge Base articles.

You can also enable Confidentiality on a form in the workspace view as shown in the following figure.

![Confidentiality section in the workspace view.](../image/confidentiality-fields-ws-view.png "Confidentiality in the workspace view")

-   **[Create a confidential record](../task/configure-confidential-record.md)**  
Create a record and mark it as confidential so that you can make sure that only the users with a specific role can access it.
-   **[Configure confidentiality in GRC tables](../task/configure-confidentilaity-on-grc-tables.md)**  
You can create a confidentiality configuration record in your GRC tables.
-   **[Configuring confidential inheritance in your tables](confidential-inheritance.md)**  
You can set up confidentiality inheritance in the tables that are already configured in the confidentiality configuration module. In the GRC application, whenever a parent record is marked or unmarked as confidential, its related table records are also marked or unmarked as confidential.

**Parent Topic:**[Common Governance, Risk, and Compliance features](common-grc-features.md)

