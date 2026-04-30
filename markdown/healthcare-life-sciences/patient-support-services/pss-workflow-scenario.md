---
title: Patient Support Services - Workflow scenario
description: Use the Patient Support Services application for streamlining enrollment activities for a patient support service including patient onboarding and pre-authorization.
locale: en-US
release: zurich
product: Patient Support Services
classification: patient-support-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, Patient Support Services, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Patient Support Services - Workflow scenario

Use the Patient Support Services application for streamlining enrollment activities for a patient support service including patient onboarding and pre-authorization.

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Scenario: A doctor prescribes some medicines and injections to treat a disease diagnosed in a patient. The patient is concerned about the cost because of a high co-pay medical insurance plan and is worried about taking injections by oneself. The doctor tells the patient about the savings card and patient support program offered by a pharma company. The doctor then helps the patient to submit the enrollment application. In the enrollment application form, the patient enters all personal and insurance details and requests support for the savings card, sharps disposal service, and injection training. The patient signs the Health Insurance Portability and Accountability Act \(HIPAA\) consent and submits the enrollment application form. When an enrollment case is created in the ServiceNow instance, the Patient Support Services workflow initiates a playbook configured for enrollment cases. The case gets assigned to John who is a care coordinator.

The following workflow elaborates how various users use the Patient Support Services application to enable the patient to enroll for a patient support program and obtain the savings card from a pharma company:

1.  John uses the Workspace to view the enrollment case.
2.  In Workspace, John can view complete information about the patient from the **Patient information** tab.

    John validates the patient details including insurance on file, contact information, and medical history.

3.  John then selects the **Playbook** tab to view all the necessary case-related information.

    The layout of a playbook enables care coordinators to focus on the steps they are responsible for, while providing full visibility into the end-to-end process life cycle.

4.  John reviews the application, verifies the prescription and consent, and accepts the enrollment application after reviewing that the patient meets the eligibility criteria of the program.
5.  The patient is enrolled into the patient support program and a welcome email notification is sent to the patient.
6.  Based on the patient's preference, John either works with the insurance company or coordinates with the specialty pharmacy to complete the benefit investigation activities.
7.  After the benefit investigation activities are set to complete, the Patient Support Services workflow:
    -   Triggers the fulfillment tasks for each service that the patient has enrolled into. In this example, tasks are created for sending a savings card and sharps disposal container.
    -   Sends an email notification to the patient to book the appointment for the injection training support.
8.  John contacts the pharmacy to place the prescription order through fax or email, confirms the drug delivery date with the pharmacy, and sends a confirmation email to the patient.
9.  The Patient books the appointment for the injection training from the patient portal, and then a training task is assigned to the Nurse Training Support assignment group.
10. A nurse educator from the Nurse Training Support assignment group provides the injection training to the patient and completes the training checklist in Workspace.
11. The enrollment case is set to complete when all the enrollment tasks are set to complete in the playbook.

