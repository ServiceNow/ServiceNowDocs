---
title: Logging an incident
description: Users and agents log incidents from sources such as email, the service desk, the service catalog, or external applications. Business rules and SOAP messaging can also generate incidents automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/logging-incident.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Logging an incident

Users and agents log incidents from sources such as email, the service desk, the service catalog, or external applications. Business rules and SOAP messaging can also generate incidents automatically.

<table id="table_w5s_p4x_bq"><thead><tr><th>

Where

</th><th>

How

</th></tr></thead><tbody><tr><td>

Service desk

</td><td>

Users can call a service desk agent, who logs an incident based on the information the user provides. Service desk \(ITIL\) agents can log an incident from the **Self-Service** &gt; **Incidents** &gt; **Create New** module.

</td></tr><tr><td>

Service catalog

</td><td>

Users can log an incident in the service catalog from the **Self-Service** &gt; **Service Catalog** &gt; **Can We Help You?** &gt; **Create Incident** record producer.

</td></tr><tr><td>

Email

</td><td>

Users can send an email to the instance mailbox. Inbound email actions create an incident from the email.

</td></tr><tr><td>

SMS

</td><td>

Users can send an SMS to the ServiceNow Customer Service number, which automatically creates an incident for the user.**Note:** To use the messaging service, an administrator must activate the Notify plugin \(com.snc.notify\) and set up a Twilio account.

</td></tr><tr><td>

Chat window

</td><td>

Users can request to create an incident using the Connect chat icon \[Omitted image "bus-chat.svg"\] Alt text: that appears in the header of the instance. In the chat window, the user can add an ITIL user and also provide a short description of the issue. Based on the description, the ITIL user creates an appropriate incident.

</td></tr></tbody>
</table>**Note:** To create a security incident, first activate the Security Incident Response Dependencies plugin \(com.snc.si\_dep\). You can then select **Create Security Incident** on a new incident form to create a security incident from the currently displayed incident.

Employee self-service \(ESS\) users can:

-   View the incidents they have opened. By default, the **Watch list**, **State**, and **Urgency** fields are available on the ESS view of the **Incident** form.
-   Update the **Watch list** and **Short Description** fields, and enter **Additional comments**. The administrator can configure other fields to be editable.

Users who don't have the itil role can view an incident only if they're the caller, opened the incident, or are on the watch list. The **incident query** business rule controls this function.

Incidents can also be generated automatically in the following ways:

-   Business rules can generate incidents automatically. Business rules use JavaScript to generate an incident when predefined conditions are met.
-   SOAP messaging can generate incidents from outside the platform. For details, see [SOAP messaging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/c_DirectWebServices.md).

