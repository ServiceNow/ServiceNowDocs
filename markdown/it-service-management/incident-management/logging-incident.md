---
title: Logging an incident
description: Log incident records from sources such as email, service desk, service catalog, or external applications as per your convenience. You can also generate incident using business rules or SOAP messaging.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Logging an incident

Log incident records from sources such as email, service desk, service catalog, or external applications as per your convenience. You can also generate incident using business rules or SOAP messaging.

<table id="table_w5s_p4x_bq"><thead><tr><th>

Where

</th><th>

How

</th></tr></thead><tbody><tr><td>

Service desk

</td><td>

User can call a service desk agent and the agent can log an incident based on the information provided by the user. Service desk \(ITIL\) agents can log an incident from the **Self-Service** &gt; **Incidents** &gt; **Create New** module.

</td></tr><tr><td>

Service catalog

</td><td>

User can log an incident in service catalog from the **Self-Service** &gt; **Service Catalog** &gt; **Can We Help You?** &gt; **Create Incident** record producer.

</td></tr><tr><td>

Email

</td><td>

User can send an email to the instance mailbox. An incident is created according to the inbound email actions.

</td></tr><tr><td>

SMS

</td><td>

User can send an SMS to ServiceNow Customer Service number and an incident is automatically created for the user.**Note:** The user must install the Notify plugin \(com.snc.notify\) and set up a Twilio account in order to avail the messaging service.

</td></tr><tr><td>

Chat window

</td><td>

User can request to create an incident using the Connect chat icon \(![Chat icon](../../../reuse/icons/brand-icons/bus-chat.svg)\) that appears on the upper-right corner of the instance. On the chat window, the user can add an ITIL user and also provide a short description of the issue. Based on the description, the ITIL user creates an appropriate incident.

</td></tr></tbody>
</table>**Note:** If you want to create a security incident, first activate the Security Incident Response Dependencies plugin \(com.snc.si\_dep\). You can then click **Create Security Incident** on a new incident form to create a security incident from the currently displayed incident.

ESS users can:

-   View the incidents they have opened. By default, the **Watch list**, **State**, and **Urgency** fields are available on the ESS view of the **Incident** form.
-   Update the **Watch list** and **Short Description** fields, and enter **Additional comments**. The administrator can configure other fields to be editable.

User who do not have the itil role can view an incident only if the user is the caller for that incident, has opened the incident, or is included in the watchlist. The **incident query** business rule controls this function.

## Automatically generated incidents

-   Incidents can be automatically generated using business rules. Business rules use JavaScript to generate an incident if pre-defined conditions are met.
-   Incidents can be generated from outside the platform with SOAP messaging. For more information, refer to [SOAP messaging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/c_DirectWebServices.md) .

