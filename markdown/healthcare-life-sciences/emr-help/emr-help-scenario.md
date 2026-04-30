---
title: IT service request workflow scenario
description: Use the EMR Help application to integrate a ServiceNow instance with an EMR system and resolve IT service requests submitted by clinicians.
locale: en-US
release: yokohama
product: EMR Help
classification: emr-help
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring EMR Help, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# IT service request workflow scenario

Use the EMR Help application to integrate a ServiceNow instance with an EMR system and resolve IT service requests submitted by clinicians.

Scenario: An EMR system is integrated with a ServiceNow instance using the EMR Help application. As a result of this integration, a Help form is available within the EMR system to enable clinicians to submit IT service requests as incidents on the ServiceNow instance.

The following graphic shows how an IT agent resolves the clinician issue discussed in the scenario.

![Workflow scenario for using the EMR Help application. For the text description, refer to the workflow steps.](../image/emr-help.png "Using the EMR Help application to resolve the clinician issue")

The following workflow steps elaborate how an IT agent resolves a typical clinician issue:

1.  When viewing the details of a patient in the EMR system, a clinician finds that the patient record isn't loading correctly.
2.  The clinician requests an IT service using the Help form available within the EMR system.
3.  After the clinician submits the request, an incident record for the service request is created on the ServiceNow instance and assigned to an IT agent.
4.  The EMR session details such as patient ID and clinician role are obtained from the EMR system and added to the incident record automatically. Using this additional information, the IT agent quickly finds out that the clinician is missing appropriate access in the EMR system.
5.  The IT agent fixes the access issue for the clinician and resolves the incident.
6.  The clinician verifies that the patient record is now displayed in the EMR system.

**Related topics**  


[Exploring EMR Help](emr-help.md)

[Configuring EMR Help](configuring-emr-help.md)

[Submitting ServiceNow IT service requests from EMR systems](emr-help-issues-reporting.md)

[Viewing and resolving ServiceNow IT service requests submitted from EMR systems](emr-help-issues-resolve.md#)

