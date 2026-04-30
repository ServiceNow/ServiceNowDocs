---
title: Generate the resolution notes for a service problem case using Now Assist for Telecommunications, Media and Technology \(TMT\)
description: Generate the resolution notes for a service problem case by using the resolution notes generation skill in the Now Assist for TMT application.
locale: en-US
release: xanadu
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Now Assist for Telecommunications, Media and Technology \(TMT\), Now Assist for Telecommunications, Media and Technology \(TMT\), Telecommunications, Media, and Technology]
---

# Generate the resolution notes for a service problem case using Now Assist for Telecommunications, Media and Technology \(TMT\)

Generate the resolution notes for a service problem case by using the resolution notes generation skill in the Now Assist for TMT application.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

## About this task

You can also propose the resolution to the customer, and then add the resolution information to the service problem case record. Generating resolution notes may help you wrap up cases faster and provide information about the service problem case resolution to other agents who might encounter similar issues. The Generate resolution notes action is available to the customer service agents who have assigned service problem cases in the Open state.

You can also generate resolution information on demand from the Now Assist panel. For more information, see [Resolution notes generation](https://www.servicenow.com/docs/access?context=now-assist-rn-summarization&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

**Note:** The resolution notes generation skill requires a minimum of 50 words in the service problem case record to generate the resolution notes. If the resolution notes cannot be generated, the system displays a message at the top in the Resolution notes modal.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **Lists** &gt; **Service Problem Case**.

2.  Open a service problem case.

3.  Select **Test &amp; Resolve** &gt; **Resolve**.

4.  Select **Generate resolution notes**.

    The system generates a resolution summary and displays the information in the Generate Resolution Notes modal, which includes the following fields:

    -   **Resolution code**
    -   **Cause**
    -   **Resolution notes**
    If the **Resolution notes** field on the service problem case record is empty, the resolution notes generation skill adds the information to this field in the modal.

5.  Select a **Resolution code** for the case.

    A resolution code describes how the service problem case was resolved. For example, common resolution codes include:

    -   Solved: Fixed by Support/Guidance provided
    -   Solved: Fixed by closing related PRB
    -   Solved by customer
6.  If you know the cause of the customer's issue, add it to the **Cause** field.

    For example, a customer's issue may be the result of a software upgrade.

7.  In the **Resolution notes** field, review the resolution summary and make any necessary corrections.

    Because the information in this field is automatically generated, it's a good idea to review the text and make sure it's accurate. Any changes that you make are saved when you save the case record.

8.  If you want to add the resolution information to the service problem case activity stream, select the **Add resolution notes to comments** check box.

    Selecting this check box makes the resolution notes available to anyone who can view the service problem case activity stream.

9.  Select **Save**.


## Result

-   The system populates the fields in the Closure Information section of the case record with the information from the Generate Resolution Notes modal.
-   The case moves to the Resolved state.
-   The resolution is proposed to the customer.

**Parent Topic:**[Using Now Assist for Telecommunications, Media and Technology \(TMT\)](../concept/now-assist-spm-using.md)

