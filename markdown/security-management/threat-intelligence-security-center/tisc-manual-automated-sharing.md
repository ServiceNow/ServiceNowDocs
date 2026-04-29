---
title: Manual and Automated Sharing using flows
description: This section describes how to configure manual sharing via GUI and automated intelligence sharing between TISC instances. It outlines the setup of inbound and outbound intelligence profiles, required roles, authentication configuration, and exclusion rules in both the source and target instances.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Share Threat Intelligence data between TISC instances, Administer Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Manual and Automated Sharing using flows

This section describes how to configure manual sharing via GUI and automated intelligence sharing between TISC instances. It outlines the setup of inbound and outbound intelligence profiles, required roles, authentication configuration, and exclusion rules in both the source and target instances.

## Configuring the Target TISC Instance

Role required: sn\_sec\_tisc.admin

Prerequisites: Before you begin, ensure you have the appropriate roles assigned.

**Role Requirements**

|Step|Action|Required Role|
|----|------|-------------|
|Create API ingestion user|Create a dedicated user and assign required role|admin \(system administrator\)|
|Configure and manage TISC settings|Perform remaining configuration steps|sn\_sec\_tisc.admin|
|Post intelligence via API|Authenticate and submit intelligence data|sn\_sec\_tisc.api\_post\_intel \(assigned to the integration user\)|

1.  **Create a user with the role** `sn_sec_tisc.api_post_intel`:

    Create a dedicated user in the target TISC instance and assign them the `sn_sec_tisc.api_post_intel` role. This dedicated user is used to authenticate incoming intelligence data submitted to the instance.

2.  **Set up an Inbound Intelligence Profile**:
3.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Administration** &gt; **Inbound Intel Sharing**.
4.  Select **Inbound Intel Sharing Profiles**.
5.  Create a new profile. For more information, see .
6.  In the **User for authentication** field, select the user created in the previous step.
7.  Set the **Data format** to **STIX 2.1**.
8.  **Save** and **enable** the profile to allow the target TISC instance to receive intelligence.
9.  Select the **Copy Profile ID** to copy the profile ID.

    **Note:** You need the profile ID when configuring the outbound intelligence profile on the source TISC instance. For more information, see .


## Configuring the Source TISC Instance

1.  **Configure global sharing rules**: Ensure the following are configured and published based on your requirements:
    -   Outbound Intel Data Exclusion Rules. For detailed procedure, see .
    -   Outbound Intel Sharing Controls. For detailed procedure, see .
2.  **Create an Outbound Intelligence Profile:**
    1.  Create a new outbound profile to manage the data sharing process. For more details, see .
    2.  Specify the API endpoint URL as:

        ```
        https://{instance name} /api/sn_sec_tisc/v1/tisc_intel_sharing_api/post_intel
        ```

        .

    3.  Set the **Authentication required** to true.
    4.  Enter the credentials of the user created in the target TISC instance \(refer to the first step of the target setup\) for the username and password.
3.  **Configure Request Headers**: In the **Headers to be passed with request** field, include the following:

    ```
    **Profile-GUID**: {Profile ID from the target TISC instance}
    ```

    ```
    **Shared-Intel-Format**: STIX 2.1
    ```

4.  **Obtaining the Profile ID:** The Profile ID required for the header can be found in the target TISC instance’s Inbound Intelligence Profile. Use the **Copy Profile ID** button to retrieve it. For more information, see .
5.  **Save** and **enable** the outbound profile.

    After configuration:

    -   Save the profile.
    -   Validate the connection to confirm it is functioning correctly.
    -   Enable the profile to activate intelligence data sharing.

