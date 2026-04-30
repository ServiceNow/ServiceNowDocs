---
title: Create an Application in Proofpoint and Obtain Client Credentials
description: Create an Application in Proofpoint and configure the required settings to obtain client credentials. These credentials enable secure access to Proofpoint's API for seamless integration and automation.
locale: en-US
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-03-20"
reading_time_minutes: 1
breadcrumb: [Install and configure the Proofpoint integration for Data Loss Prevention, Data Loss Prevention Incident Response Integration with Proofpoint, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Create an Application in Proofpoint and Obtain Client Credentials

Create an Application in Proofpoint and configure the required settings to obtain client credentials. These credentials enable secure access to Proofpoint's API for seamless integration and automation.

## Before you begin

Role required: admin

## Procedure

1.  Log in to the Proofpoint Console.

    Access the Proofpoint Console using your credentials.

2.  Create a New Application.

    1.  In the **Developer** section, select Authorization.

    2.  Select **Create**.

    3.  Enter an application name.

    4.  In Allowed Scopes, add scopes to your Application as required.

    5.  In Allowed Grants, select **Client Credentials**.

    6.  Select **Save**.

        Client ID and Client Secret are generated.

3.  Configure Application details.

    1.  Select the newly created Application.

    2.  In the Access Policies, select **Edit**.

        Select either High Level or Granular access policies.

    3.  Select **Done**.


## Result

Use the generated Client ID and Client Secret to configure the integration in the DLP Proofpoint \(PPT\) application and start using it.

**Parent Topic:**[Install and configure the Proofpoint integration for Data Loss Prevention](install-configure-proofpoint-integration-dlp.md)

