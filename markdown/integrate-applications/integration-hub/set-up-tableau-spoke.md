---
title: Set up the Tableau spoke
description: Integrate your ServiceNow instance and Tableau Cloud to automate flows and perform actions on the Tableau Cloud application.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Tableau spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Tableau spoke

Integrate your ServiceNow instance and Tableau Cloud to automate flows and perform actions on the Tableau Cloud application.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Tableau spoke.
-   Tableau Cloud Role required: Site administrator.

## Procedure

1.  Use one of the following authentication types to validate ServiceNow instance requests with the Tableau spoke.

    -   Personal Access Token \(PAT\)
    -   JSON Web Token \(JWT\)
    1.  Validate ServiceNow instance requests with the Tableau spoke using the PAT authentication type.

        1.  Log in to the Tableau Cloud account using admin credentials.
        2.  Select your profile icon.
        3.  Select **My Account Settings**.
        4.  Scroll down to the **Personal Access Tokens** section on your profile page.
        5.  In the text field, provide a token name.

            For example, `Test 1`.

        6.  Select **Create Token**.

            The Personal Access Token is generated with a Token name and Secret.

        7.  To copy the Personal Access Token Secret, select **Copy Secret**.

            **Important:**

            Keep the Personal Access Token Secret at a secure place. You would need it when you create a connection record for Tableau.

    2.  Validate ServiceNow instance requests with the Tableau spoke using the JWT authentication type.

        1.  Log in to the Tableau Cloud account using admin credentials.
        2.  Select your profile icon.
        3.  From the left-pane, select **Settings**.
        4.  Select the **Connected Apps** tab.
        5.  On the Connected Apps page, select the **Direct Trust** option from the **New Connected Apps** drop-down list.
        6.  In the **Create Connected App** dialog box, fill in the Connected app name, Access level, and Domain allow list details.
        7.  Select **Create**.

            The Connected App that you created gets displayed on the Connected Apps page. By default, the Connected App is inactive.

        8.  To enable the Connected App, select the ellipsis icon \(![Ellipsis icon.](../../../reuse/icons/product-icons/ellipsis-horizontal-outline-24.svg)\) in the Actions column and select **Enable**.

            The status of the Connected App shows as enabled.

        9.  Select the Connected App name.

            Keep the Secret ID and Secret value at a secure place. You would need it when you create a connection record for Tableau.

        10. To copy the Client ID, select **Copy Client ID**.

            Keep the Client ID at a secure place. You would need it when you create a connection record for Tableau.


## What to do next

[Create a connection and credential for the Tableau spoke](create-cred-tableau.md)

