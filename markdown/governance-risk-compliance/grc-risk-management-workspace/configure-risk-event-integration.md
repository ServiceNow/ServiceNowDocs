---
title: Configure risk event integration
description: Configure risk event integration with other upstream ServiceNow applications. This integration enables all users in an organization to report and track the risk events.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use Risk Events, Use, Risk Management, Governance, Risk, and Compliance]
---

# Configure risk event integration

Configure risk event integration with other upstream ServiceNow applications. This integration enables all users in an organization to report and track the risk events.

## Before you begin

Role required: sn\_risk.admin and user\_admin

## About this task

When you configure the risk event integration with another upstream application, then users of that application can directly report risk events from the application. For example, if you configure risk event integration in the ServiceNow® IT Service Management \(ITSM\) application, all users of ITSM can report risk events from the ITSM application. By default, this configuration is provided for the IT Incidents application and the Security incidents application.

The two modes that enable the creation of a risk event are **Simple** and **Advanced**. The **Simple** mode enables you to define filter conditions on the application table so that users of the Incidents application can report a risk event. For example, you can define that a financial event with a high impact must be reported as a risk event. In contrast, the **Advanced** mode enables users with GRC developer role to write scripts.

Incident managers with the incident\_manager role are able to see the **Report Risk Event** option in an incident, whereas Security Managers with the sn\_si.manager role are able to see the **Report Risk Event** option in a security incident.

## Procedure

1.  Navigate to **Risk Events** &gt; **Administration** &gt; **Integration Configuration**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_yxw_n1t_3jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Configuration number. This field is automatically set.

</td></tr><tr><td>

Active

</td><td>

Option to enable the creation of a risk event from the application table.

</td></tr><tr><td>

Integration name

</td><td>

Short and unique title for the integration. For example, to report a risk event from an incident table, you can type `Incident-risk-event-integration`.

</td></tr><tr><td>

Application table

</td><td>

Application table that is used for reporting risk events. The table determines the upstream application that will be used for reporting risk events.

</td></tr><tr><td>

Source for name

</td><td>

How the name of risk events are set. The choices are as follows:-   **Form field**: Select this option if you want the value from a specific selected field to be used as the risk event name.
-   **Default value**: Enter a custom value. The risk event is created with the name you enter here.


</td></tr><tr><td>

Source for description

</td><td>

How the description of risk events are set.

</td></tr><tr><td>

Source for entity

</td><td>

How the entity of risk events are set.

</td></tr><tr><td>

Source for date of discovery

</td><td>

How the date of discovery for risk events are set.

</td></tr><tr><td>

Name

</td><td>

Field in the application table that is used to set the name of risk events. This field appears only when **Form field** is selected from the **Source of name** field.

</td></tr><tr><td>

Default Name

</td><td>

Default name for risk events. This field appears only when **Default value** is selected from the **Source of name** field.

</td></tr><tr><td>

Description

</td><td>

Field in the application table that is used to set the description of risk events. This field appears only when **Form field** is selected from the **Source of description** field.

</td></tr><tr><td>

Default description

</td><td>

Default description for risk events. This field appears only when the **Default value** is selected from the **Source of description** field.

</td></tr><tr><td>

Entity

</td><td>

Field from the application table that refers to a GRC entity or to a record in a GRC entity. This field appears only when **Form field** is selected from the **Source of entity** field.

</td></tr><tr><td>

Default Entity

</td><td>

Default entity for risk events. Default entities are created from the table in the **Application table** field. This field appears only when **Default value** is selected from the **Source of entity** field.

</td></tr><tr><td>

Date of discovery

</td><td>

Field in the application table that is used to set the date of discovery of risk events. This field is visible only when **Form field** is selected from the **Source of date of discovery** field.

</td></tr><tr><td>

Default date of discovery

</td><td>

Default date of discovery of risk events.

</td></tr><tr><td>

Default event type

</td><td>

Default event type of risk events. For example, if the event is financial or non-financial.

</td></tr><tr><td>

Event subtype

</td><td>

Subtype of the risk event. For example, if the event is actual or potential.

</td></tr><tr><td>

Source for Non-Financial impact

</td><td>

How the non-financial impact of risk events is set.

</td></tr><tr><td>

Non-Financial impact

</td><td>

Field in the application table that is used to set the non-financial impact of risk events. This field appears only when **Form field** is selected from the **Source of non-financial field** field.

</td></tr><tr><td>

Default non-financial impact

</td><td>

Default severity of risk events. The choices are **Low**, **Medium**, or **High**.

</td></tr><tr><td>

Source for expected loss

</td><td>

How the expected loss of risks events is set.

</td></tr><tr><td>

Expected loss

</td><td>

Field in the application table that is used to set the expected loss of risk events. This field appears only when **Financial impact** is selected from the **Default event type** is field and only when **Form field** is selected from the **Source of expected loss** field.

</td></tr><tr><td>

Default expected loss

</td><td>

Default monetary value of the loss. This field appears only when the **Financial impact** is selected from the **Default event type** field and only when **Default value** is selected from the **Source of expected loss** field.

</td></tr><tr><td class="sub-head" colspan="2">

Display UI Action Based On

</td></tr><tr><td>

Mode

</td><td>

Mode that is used to create the UI action. The choices are as follows:-   **Simple**: Mode to set simple filter conditions. For example, if the impact of an incident is **High**, the **Report a Risk Event** UI action must be created.
-   **Advanced**: Mode to write a script to query tables, including the table from the **Application table** field.


</td></tr><tr><td>

Role condition

</td><td>

Roles that can report risk events from the upstream application.

</td></tr><tr><td>

Filter condition

</td><td>

Build the filters as per the requirement.

</td></tr><tr><td>

Script

</td><td>

Field to write a custom script to query any table. **Note:** The option to write a script is only available to users who also have the sn\_grc.developer role. This field appears when the **Mode** field has **Advanced**.

</td></tr></tbody>
</table>4.  Click **Submit**.

    Any other application table which extends the task table can configure this integration. For details, see the [Risk Event Ingestion \[KB0780985\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0780985) article in the Now Support Knowledge Base. You must log in to view the article.


## Result

The application that is configured to report risk events displays the **Create Risk Event** button.

**Parent Topic:**[Use Risk Events](../concept/use-risk-events.md)

