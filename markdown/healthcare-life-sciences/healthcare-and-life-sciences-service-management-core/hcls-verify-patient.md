---
title: Associate a patient record with an interaction in Workspace
description: Look up for the patient information within an interaction, review and confirm the information, and then populate the information on the interaction to resolve a healthcare-related request.
locale: en-US
release: zurich
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage healthcare requests in Workspace, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Associate a patient record with an interaction in Workspace

Look up for the patient information within an interaction, review and confirm the information, and then populate the information on the interaction to resolve a healthcare-related request.

## Before you begin

Role required: sn\_hcls.healthcare\_agent, sn\_hcls.manager

## About this task

The **Consumer** field on the Interaction form is automatically populated with the requester's name who requested for assistance made through a chat or phone call. As an agent, you can associate an interaction with the correct patient. You can search for the patient from within an interaction and verify the details with the requester to confirm you have the right patient details.

## Procedure

1.  Open your Workspace by navigating to **All** &gt; **HCLS Service Management** &gt; **Healthcare workspace**.

2.  Navigate to **Lists** &gt; **Interactions** &gt; **My Interactions**.

3.  Click the link to the interaction with which you want to associate a patient record.

4.  On the Interaction form, click **Verify Patient**.

5.  In the **Lookup by name, phone, or record number** field of the Verify Patient dialog box, enter the patient data.

    You can search for the patient by their name, phone number, email address, date of birth, or MRN. The **Lookup by name, phone, or record number** field uses a type-ahead search feature that displays results in a list and narrows the results as more characters are entered. Multiple display fields in the search results help to differentiate patients. When searching for a record number, the patient associated with the record is returned in the search results. To clear the search results, delete characters in the **Lookup by name, phone, or record number** field.

    **Note:** The type-ahead search feature works only when the encryption feature is disabled. If the encryption feature is enabled, you must enter the exact keyword as the first name, last name, phone number, email address, date of birth, or MRN to find the patient record.

6.  In the Verify Patient dialog box, click **Done**.

    **Note:** If you can't find a patient record, you can create a patient record from within an interaction. For more information, see [Create a patient record in Workspace](hcls-create-patient-record.md).

7.  On the Interaction form, click **Save**.


## Result

The Patient information related list is displayed on the interaction form from where you can view the details of the patient. The Patient information related list is also displayed on the healthcare cases associated with the interaction.

