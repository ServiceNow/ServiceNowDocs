---
title: Set up a software model
description: Using the applications discovered on the Jamf server, set up a software model to manage licenses.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CSD 2.0 for Jamf, Client Software Distribution 2.0 application, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up a software model

Using the applications discovered on the Jamf server, set up a software model to manage licenses.

## Before you begin

Before creating software models, you must discover the applications available for deployment on the Jamf server. See [CSD 2.0 for Jamf](../concept/csd2-jamf-tsk.md) for more information.

Perform these steps when you set up a software model for the Jamf application and policy.

Role required: Ensure that the user has one of the two mentioned set of roles.

-   sn\_jamf\_spoke.jamf\_admin and sn\_csd.CSD Admin
-   admin

## About this task

You can link a Jamf application to an existing software model or create a new model.

## Procedure

1.  Determine whether you are setting up a software model for the application or the policy.

    -   If you are setting up a software model for the Jamf application, navigate to **Jamf** &gt; **Applications**.
    -   If you setting up a software model for the Jamf policy, navigate to **Jamf** &gt; **Policies**.
    A list of applications or policies discovered on the Jamf server appears.

2.  Open the required record.

3.  Link to an existing model by clicking the magnifying glass icon in the **CSD software model** field and selecting a model from the list.

4.  Create a model by clicking **Create Software Model** under related link.

    1.  Complete the software model fields.

    2.  Click **Submit**.

        The view returns to the Jamf Applications list.


**Parent Topic:**[CSD 2.0 for Jamf](../concept/csd2-jamf-tsk.md)

