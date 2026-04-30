---
title: Configure your Identity Provider for Care Team Portal
description: Configure your Identity Provider to ensure successful user authentication in Care Team Portal.
locale: en-US
release: zurich
product: Care Team Operations
classification: care-team-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Embed Care Team Portal in Epic, Configure, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Configure your Identity Provider for Care Team Portal

Configure your Identity Provider to ensure successful user authentication in Care Team Portal.

## Before you begin

Role required: admin

**Note:** For the following process to be successful, the following script includes need to be available in Global scope:

-   **MultiSSO\_OIDC\_CTO**
-   **OAuthUtilEpic**

If these script includes are in HCLS application scope, they must first be cloned into Global scope before proceeding.

## Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Identity Providers**.

2.  Select the Identity Provider you wish to configure.

3.  Set the ServiceNow Homepage value to `https://<instance-name>.service-now.com/careteam`.

4.  Navigate to the OIDC Provider Configuration related list and open the OIDC provider record.

5.  Update the following fields:

    1.  User Claim – enter **preferred\_username**.
    2.  User Field – select **User ID**.
6.  Click **Update**.

7.  In the Identity Provider, navigate to the Advanced related list.

8.  Update the Single Sign-On Script field to **MultiSSO\_OIDC\_CTO**.

9.  Ensure the **Active** field is set to true.

10. Click **Save**.

11. Navigate to the OIDC Entity related list.

12. Select the OIDC entity record.

13. In the OAuth API Script field, select **OAuthUtilEpic**.

14. Click **Update**.


## Result

The Identity Provider has been configured to ensure successful user authentication for accessing Care Team Portal in Hyperspace via Hyperdrive.

