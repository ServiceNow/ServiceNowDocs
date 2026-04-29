---
title: Appointment booking workflow in Patient Support Services
description: You can enable patients to book appointments for a training request within the Patient Support Services application by using the appointment booking feature.
locale: en-US
release: australia
product: Patient Support Services
classification: patient-support-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage enrollment requests, Patient Support Services, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Appointment booking workflow in Patient Support Services

You can enable patients to book appointments for a training request within the Patient Support Services application by using the appointment booking feature.

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

The appointment booking feature in the Patient Support Services application uses the following workflow:

1.  A patient views available appointment windows, makes a selection, and books an appointment for a training request from their patient portal.
2.  Booking an appointment creates a record in the Appointment \[sn\_hcls\_appointment\] table and a training task record is created. An email notification about the booked appointments is sent to the patient.
3.  The training task is automatically assigned to the Nurse Training Support assignment group and a nurse educator who is a member of the Nurse Training Support assignment group works on the task.
4.  The nurse educator then conducts the training for the patient based on the scheduled appointment dates and updates the state of the training task in Workspace. The nurse educator can access the training checklist, complete the checklist during the training, and capture notes in the task.

To get started on the appointment booking feature, see [Configuring an appointment booking setting for Patient Support Services](pss-appt-booking-setup.md#).

