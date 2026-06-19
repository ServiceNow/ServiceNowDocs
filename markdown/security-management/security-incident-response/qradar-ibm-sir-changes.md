---
title: Security Incident Response form after offense ingestion
description: After an IBM QRadar offense has been ingested, a security incident is created and the corresponding updates are made to the security incident record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/qradar-ibm-sir-changes.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [IBM QRadar Offense Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Response form after offense ingestion

After an IBM QRadar offense has been ingested, a security incident is created and the corresponding updates are made to the security incident record.

## Worknotes

A worknote is posted with details of the offense that triggered the security incident.

Select the offense link to navigate to the internal security incident record. The **Click here** hyperlink takes you to the IBM QRadar dashboard where you can view the offense details.

If you had selected the **Log work note for new offense** option in the Offense Aggregation Criteria as described in the [Mapping IBM QRadar offense fields to security incident response fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/ibm-qradar-mapping-process.md), a worknote is posted when the offense is aggregated.

## Aggregated offenses

Select **Related Lists** &gt; **Aggregated IBM QRadar offenses** to view the offenses aggregated to the security incident. select the QRadar offense hyperlink to view the offense in the IBM QRadar dashboard.

Create security incident: Select an offense from the list, select the **Actions** menu, and select **Create security incident**. This option creates a security incident for the offense and this offense is de-aggregated from the parent security incident.

Delete offense record: Select an offense from the list, select the **Actions** menu, and select **Delete**. This option deletes the offense record.

## IBM QRadar offense updates

This shows the standard and custom offense fields and tracks changes to the offense during every polling interval. This is helpful as you can view any offense updates directly without navigating to the IBM QRadar dashboard. Any changes to the values are displayed in the Previous value and Current value fields.

To enable the offense updates feature navigate to **IBM QRadar Integration** &gt; **IBM QRadar Integration Settings** and enable **Set this property to activate the Offense Updates feature**. By default, this setting is disabled.

## Recent IBM QRadar events

Select the **Fetch Recent IBM QRadar Events** option under the **Related Links** to view the most recent IBM QRadar events. By default, a maximum number of 100 events are displayed. You can modify this default setting in the [Configuration settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/qradar-ibm-intg-settings.md).

## Recent IBM QRadar Flows

Using the Integration Hub and Flow Designer, several flows, subflows, actions are available with the IBM QRadar integration. When you select the **Fetch Recent IBM QRadar Flows** option under the Related Links, the most recent flows are retrieved. To view these flows, select **Recent IBM QRadar Flows**.

By default, a maximum number of 100 flows are displayed. You can modify this default setting in the [Configuration settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/qradar-ibm-intg-settings.md).

