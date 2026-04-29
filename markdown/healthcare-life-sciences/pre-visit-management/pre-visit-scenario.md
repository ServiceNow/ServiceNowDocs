---
title: Pre-Visit Management - Workflow scenario
description: Use the Pre-Visit Management application for streamlining pre-visit activities for a procedure request including patient to-dos, approvals, pre-authorization, and scheduling.
locale: en-US
release: australia
product: Pre-Visit Management
classification: pre-visit-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Pre-Visit Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Pre-Visit Management - Workflow scenario

Use the Pre-Visit Management application for streamlining pre-visit activities for a procedure request including patient to-dos, approvals, pre-authorization, and scheduling.

**Important:**

Starting with the Yokohama release, Pre-Visit Management is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Scenario: A physician orders the colonoscopy procedure for a patient from an EMR system. When a procedure request case is created in the ServiceNow instance, the Pre-Visit Management workflow initiates a playbook configured for procedure request cases. The case gets assigned to John Jason from the patient services group.

The following graphic shows how the Pre-Visit Management application is used for managing the colonoscopy procedure request for a patient as discussed in the scenario.

The following workflow elaborates how various users use the Pre-Visit Management application for the colonoscopy procedure:

1.  John uses the Workspace to view the procedure request case.
2.  In the Workspace, John can view complete information about the patient from the **Patient information** tab.

    John validates the patient details including insurance on file, contact information, and medical history.

3.  John then selects the **Playbook** tab to view all the necessary case-related information.

    The layout of a playbook enables patient service representatives to focus on the steps they are responsible for, while providing full visibility into the end-to-end process life cycle.

4.  As listed in the playbook, John first completes the order review by performing the following tasks:
    1.  Reviews the order details and gets additional justification by the physician.
    2.  Marks the review as complete.
5.  The Pre-Visit Management workflow automatically assigns to-dos to the patient and sends an email notification about to-do items to the patient.
6.  The patient logs in to the patient portal and sees the pending to-do items.
7.  In the patient portal, the patient performs the following tasks:
    1.  Opens the privacy consent, reviews it, and signs it.
    2.  Reviews and confirms the insurance information.
8.  As listed in the playbook, John then works with the insurance company and gets the pre-authorization approved for the patient by performing the following tasks:
    1.  Creates pre-authorization request for the procedure.
    2.  Reviews and confirms the pre-authorization received from the insurance company.
9.  The Pre-Visit Management workflow triggers another task for scheduling the procedure and assigns it to Ben Jackson from the procedure scheduling group.
10. Ben then books an appointment for the patient by performing the following tasks:
    1.  Coordinates with the patient and the physician to schedule the procedure.
    2.  Selects the **Appointment** tab in the Workspace and books an appointment for the patient.
11. An email notification is generated and sent to the patient with appointment details.
12. The procedure request case is set to complete.
13. Three days before the procedure, the Pre-Visit Management workflow automatically assigns a to-do item to the patient to review and sign the procedure consent and sends an email notification to the patient.
14. Patient logs in to the patient portal and reviews and submits the procedure consent online.

