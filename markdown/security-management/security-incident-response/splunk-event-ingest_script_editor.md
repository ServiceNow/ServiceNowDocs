---
title: Use the script editor to format alert values for the Splunk Enterprise Event Ingestion integration
description: Use the script editor to format field values on the security incident during the mapping step.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration architecture and external systems connection for the Splunk Enterprise Event Ingestion integration, Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the script editor to format alert values for the Splunk Enterprise Event Ingestion integration

Use the script editor to format field values on the security incident during the mapping step.

## Before you begin

In addition to the directly mapped fields from the pulled alert values, and the alert values you enter manually, you can optionally use the script editor to format field values on the security incident during the mapping step. The script editor changes the values of a Splunk alert so that values that are supported by the ServiceNow AI Platform® Security Incident Response security incident are mapped to the Category, Configuration item \(CI\), and Observable fields.

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

In certain cases, Splunk Enterprise alert values are mapped to the Category, Configuration item \(CI\), and Observable fields on the SIR incident and are not supported. You might prefer to edit the mapped values. If you want to translate the value of a Splunk Enterprise alert to a value that is supported by these fields on the SIR security incident, use the script editor.

## Procedure

1.  With the mapping form displayed, click the link to open the script editor.

    ![Click here link for script editor highlighted.](../image/214_SplunkFieldTranslationExampleCMDB_1.png)

2.  From the choice list, select a destination field for the value that you want to edit.

3.  Alternatively, in the SIR Incident Field Mapping section, click the bracket icon `[{}]` next to a field to open the script editor for that field.

    In certain instances, a script include may be appropriate for the Configuration item field. For an alert, for example, a value for the Configuration item may not be matched.

    As shown in the following figure, if a match for a host name cannot be found in the ServiceNow AI Platform® CMBD for the Configuration item field, you can edit the rule so that if an IP address is found, it populates the Configuration item field. If there is no value for the alarm, the field on the security incident is set to null.

    The editor opens with the field displayed in Destination Field. The following image shows the editor with the `Configuration item` field as the Destination Field.

    ![Script editor.](../image/214_SplunkFieldTranslationExampleCMDB.png)

4.  Enter any changes to then script, and click **Update** to save your changes.

    The Splunk Field Translations table is displayed.

5.  Close the table to return to the Mapping form.


**Parent Topic:**[Integration architecture and external systems connection for the Splunk Enterprise Event Ingestion integration](../concept/splunk-event-ingest-integration-architecture.md)

