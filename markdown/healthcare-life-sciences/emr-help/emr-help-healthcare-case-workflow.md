---
title: Healthcare case workflow scenario
description: Use the EMR Help application to integrate a ServiceNow instance with an EMR system and manage healthcare cases reported by clinicians.
locale: en-US
release: yokohama
product: EMR Help
classification: emr-help
topic_type: concept
last_updated: "2025-02-27"
reading_time_minutes: 1
breadcrumb: [Exploring EMR Help, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Healthcare case workflow scenario

Use the EMR Help application to integrate a ServiceNow instance with an EMR system and manage healthcare cases reported by clinicians.

![Workflow scenario for using the EMR Help application. For the text description, refer to the workflow steps.](../image/hcls-emr-healthcare-case-info.png "Using the EMR Help application to resolve a clinician issue")

The following workflow steps elaborate how an agent resolves a typical clinician issue:

1.  When viewing the details of a patient in the EMR system, a clinician encounters an issue with the patient record.
2.  The clinician requests assistance with a service using the Help form available within the EMR system.
3.  After the clinician submits the request, a record for the service request is created on the ServiceNow instance and assigned to an agent.
4.  The EMR session details, such as patient ID and clinician role, are obtained from the EMR system and added to the record automatically. Using this additional information, the agent determines what the issue is.
5.  The agent fixes the issue for the clinician and resolves the incident.
6.  The clinician verifies that the patient record is now displayed in the EMR system.

