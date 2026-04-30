---
title: Use the script editor to format correlation event values
description: In addition to the directly mapped fields from the ingested correlation event values, use the script editor to format field values on the security incident during the mapping step.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ArcSight ESM Event Ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use the script editor to format correlation event values

In addition to the directly mapped fields from the ingested correlation event values, use the script editor to format field values on the security incident during the mapping step.

## Before you begin

Role required: sn\_si.admin

## About this task

The script editor changes the values of a ArcSight ESM correlation event field so that values that are supported by the ServiceNow AI Platform SIR security incident are mapped to the Category, Configuration item \(CI\), Observable, and other security incident fields.

In certain cases, ArcSight ESM correlation event values are mapped to reference fields such as, Category, Configuration item \(CI\), and Observable fields on the security incident. As a user with the sn\_si.admin role, you may prefer to edit the mapped event field values to translate format or data values to conform with incident field formats and values expected. If you want to translate the value of a ArcSight ESM correlation event to a value that is supported by these fields on the SIR security incident, use the script editor.

## Procedure

1.  With the mapping form displayed, click the link to open the script editor.

2.  From the choice list, select a destination field for the value that you want to edit.

3.  Alternatively, in the SIR Incident Field Mapping section, click the bracket icon `[{}]` next to a field to open the script editor for that field.

    In certain instances, a script include may be appropriate for the Configuration item field. For a correlation event, for example, a value for the Configuration item may not be matched.

    As shown in the following figure, if a match for a host name cannot be found in the ServiceNow AI Platform CMDB for the Configuration item field, you can edit the rule so that if an IP address is found, it populates the Configuration item field.

    The editor opens with the field displayed in Destination Field.

4.  Enter any changes to then script, and click **Update** to save your changes.

    The ArcSight ESM Field Translations table is displayed.

5.  Close the table to return to the Mapping form.


