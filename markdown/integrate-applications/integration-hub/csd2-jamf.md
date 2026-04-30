---
title: Verify the Jamf spoke records
description: Verify that the spoke is integrated with CSD 2.0 after setting up and configuring the Jamf spoke and create server instance record to use Jamf spoke with CSD 2.0.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [CSD 2.0 for Jamf, Client Software Distribution 2.0 application, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Verify the Jamf spoke records

Verify that the spoke is integrated with CSD 2.0 after setting up and configuring the Jamf spoke and create server instance record to use Jamf spoke with CSD 2.0.

## Before you begin

-   Activate the Jamf spoke and set up the spoke. For more information about the spoke setup, see [Set up the Jamf spoke](setup-jamf-spk.md).
-   Activate the CSD 2.0 application.
-   Role required: admin

## Procedure

1.  Verify that these modules are available.

    -   Applications
    -   Configurations
    -   Server Instances
    -   Deployments
    -   Collections
2.  Navigate to **System Definition** &gt; **Tables** and verify that these table are available.

    -   Configuration \[sn\_jamf\_spoke\_sf\_config\]
    -   Server Instance \[sn\_jamf\_spoke\_server\]
    -   Policy \[sn\_jamf\_spoke\_policy\]
    -   Application \[sn\_jamf\_spoke\_application\]
    -   Group \[sn\_jamf\_spoke\_group\]
    -   Jamf Credential \[sn\_jamf\_spoke\_jamf\_credential\]
3.  Verify that the flows are configured correctly in the provider record.

    1.  Navigate to **Client Software Distribution 2.0** &gt; **Providers**.

    2.  Open the record **Jamf**.

    3.  Verify that the flows are configured correctly in the record.

        ![Verify that the flows are configured.](../image/csd2-jamf-flows.png)

        **Note:** You can configure the default flows as per your requirement.


**Parent Topic:**[CSD 2.0 for Jamf](../concept/csd2-jamf-tsk.md)

