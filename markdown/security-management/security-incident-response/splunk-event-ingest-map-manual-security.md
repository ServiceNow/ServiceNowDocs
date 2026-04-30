---
title: Create mappings for Splunk ES notable event incident review and contributing event details \(manual forwarding\)
description: During the notable event field mapping step, you map individual event fields from notable events to fields on a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Set up a profile for manual event forwarding, Create an event profile, Splunk Enterprise Security event ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create mappings for Splunk ES notable event incident review and contributing event details \(manual forwarding\)

During the notable event field mapping step, you map individual event fields from notable events to fields on a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

Map up to five notable events from the Notable Event Sample Ingestion column on the left of the form to the security incident fields in the SIR Incident Field Mapping column on the right.

Create custom mappings by adding or removing the fields on the mapping grid on the right side of the form. Default fields that are typically important field to populate on the SIR incident form are displayed. However, these fields can be removed and any additional fields can be displayed using the + and - buttons. Create custom maps by adding or removing the fields on the mapping grid on the right side of the form. Customizing the fields permits you to map Splunk fields that are not displayed on the default mapping grid on the SIR security incident.

## Procedure

1.  If the mapping form is not displayed, click **Mapping** on the progress bar.

2.  Follow these steps to upload attachment data in your ServiceNow AI Platform® instance.

    1.  If not already logged in, log in to your Splunk Enterprise console.

    2.  Navigate to the Search tab and enter a name for a search that has the notable event data that you want to export.

        An example search format to retrieve notable events for the Brute Force Access Behavior correlation rule would be the following: \`notable\`\|search source="Access - Brute Force Access Behavior Detected - Rule".

    3.  Expand the notable event, and in the Field column, select the fields that you want to import.

        These fields are the field-value pairs that are exported and displayed on the Mapping page in your ServiceNow AI Platform® instance.

        ![Splunk ES: Select notable events for export](../image/splunk_es_export_XML.png)

    4.  In your Splunk Enterprise console, in the upper right of the Search page, click the **Export** icon.

    5.  In the choice list for the Format field in the dialog that is displayed, click **XML Format**.

    6.  Enter a new filename.

    7.  Click **Export**.

        ![Splunk ES: Export XML file](../image/splunk_es_export_XML_2.png)

        The exported Splunk notable event XML file must now be uploaded to your ServiceNow AI Platform® instance.

    8.  If the Mapping page is not already displayed in your ServiceNow AI Platform® instance, click **Mapping** in the progress bar.

    9.  In the Notable Event Sample Ingestion column, click **Load Attachment Data**.

        ![Splunk ES: Load attachment data](../image/splunk_es_load_attachment.png)

    10. In the dialog that is displayed, click **Choose files** and navigate to the `.xml` file that you exported and click **Open**.

        After you click to load attachment data for manually forwarded events, the Splunk ES notable event fields are populated on the left side of the form. These values are the field values that you map to the security incident fields on the Sir Incident Field Mapping side of the form.

        The value pairs for the fields that you exported for the event are displayed on the left side of the mapping form.

3.  Follow steps 5 to 10 in the [Map notable events](splunk-event-ingest-map-alerts-security.md) section.


