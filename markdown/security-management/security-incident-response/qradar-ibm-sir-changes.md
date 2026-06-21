---
title: Security Incident Response form after offense ingestion
description: After an IBM QRadar offense has been ingested, a security incident is created and the corresponding updates are made to the security incident record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/security-management/security-incident-response/qradar-ibm-sir-changes.html
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [IBM QRadar Offense Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Response form after offense ingestion

After an IBM QRadar offense has been ingested, a security incident is created and the corresponding updates are made to the security incident record.

## Worknotes

A worknote is posted with details of the offense that triggered the security incident.

\[Omitted image "ibm-qradar-sir-worknote.png"\] Alt text: IBM QRadar: SIR: Worknote

Click the offense link to navigate to the internal security incident record. The **Click here** hyperlink takes you to the IBM QRadar dashboard where you can view the offense details.

If you had selected the **Log work note for new offense** option in the Offense Aggregation Criteria as described in the [Mapping IBM QRadar offense fields to security incident response fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/security-incident-response/ibm-qradar-mapping-process.md), a worknote is posted when the offense is aggregated.

\[Omitted image "ibm-qradar-offense-record.png"\] Alt text: IBM QRadar: Internal Offense Record

## Aggregated offenses

Click **Related Lists** &gt; **Aggregated IBM QRadar offenses** to view the offenses aggregated to the security incident. Click the QRadar offense hyperlink to view the offense in the IBM QRadar dashboard.

\[Omitted image "ibm-qradar-offense-aggregate.png"\] Alt text: IBM QRadar Aggregated Offenses

Create security incident: Select an offense from the list, click the **Actions** menu, and click **Create security incident**. This option creates a security incident for the offense and this offense is de-aggregated from the parent security incident.

Delete offense record: Select an offense from the list, click the **Actions** menu, and click **Delete**. This option deletes the offense record.

\[Omitted image "ibm-qradar-offense-aggregate-create.png"\] Alt text: IBM QRadar Aggregated Offenses: Create and Delete

## IBM QRadar offense updates

This shows the standard and custom offense fields and tracks changes to the offense during every polling interval. This is helpful as you can view any offense updates directly without navigating to the IBM QRadar dashboard. Any changes to the values are displayed in the Previous value and Current value fields.

To enable the offense updates feature navigate to **IBM QRadar Integration** &gt; **IBM QRadar Integration Settings** and enable **Set this property to activate the Offense Updates feature**. By default, this setting is disabled.

\[Omitted image "ibm-qradar-offense-updates.png"\] Alt text: IBM QRadar Offense Updates

## Recent IBM QRadar events

Click the **Fetch Recent IBM QRadar Events** option under the **Related Links** to view the most recent IBM QRadar events.

\[Omitted image "ibm-qradar-recent-events.png"\] Alt text: IBM QRadar: Recent Events

By default, a maximum number of 100 events are displayed. You can modify this default setting in the [Configuration settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/security-incident-response/qradar-ibm-intg-settings.md).

**Note:** The above image shows the standard event fields associated with the offense. If you have configured and mapped any custom event fields \(See [Mapping IBM QRadar offense fields to security incident response fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/security-incident-response/ibm-qradar-mapping-process.md)\), you can view them in the List View by clicking the Event Name link.

\[Omitted image "ibm-qradar-recent-events-custom.png"\] Alt text: IBM QRadar: Recent IBM QRadar Events: List View

## Recent IBM QRadar Flows

Using the Integration Hub and Flow Designer, several flows, subflows, actions are available with the IBM QRadar integration. When you click the **Fetch Recent IBM QRadar Flows** option under the Related Links, the most recent flows are retrieved. To view these flows, click **Recent IBM QRadar Flows**.

\[Omitted image "ibm-qradar-recent-flows.png"\] Alt text: IBM QRadar: Recent Flows

By default, a maximum number of 100 flows are displayed. You can modify this default setting in the [Configuration settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/security-incident-response/qradar-ibm-intg-settings.md).

**Note:** The above image shows the standard flow fields associated with the offense. If you have configured and mapped any custom flow fields \(See [Mapping IBM QRadar offense fields to security incident response fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/security-incident-response/ibm-qradar-mapping-process.md)\), you can view them in the List View by clicking the Flow ID link.

