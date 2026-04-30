---
title: Email links with external authentication
description: You can use email links when using the digestive token external authentication, however, you must establish how to handle links in email notifications.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrating SAML 2.0 with other features, SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Email links with external authentication

You can use email links when using the digestive token external authentication, however, you must establish how to handle links in email notifications.

The default links contain a URL that directs you to a specific location in the instance, like an Incident or Change Request, without incorporating SSO credentials. Below are examples for directing the user to the location in the instance without logging in on the instance login page.

-   Unencrypted HTTP technique to connect to the /demo instance \(it does not navigate to specific record\):

    ```
    https://<instance name>.service-now.com/?SM_USER=user_name&DE_USER=lQjIVp7aRJtyPx5+2O/vgU24tbE=
    ```

-   Link \(in an email notification\) to a specific record, so that the user first goes to the company's own login portal:

    ```
    https://login.company_portal_page.com/nav_to.do?uri=incident.do?sys_id=009f8eda0a0a0b2b01ab4eb094223466%26sysparm_stack=incident_list.do%3Fsysparm_query=active=true
    ```

    You must set the **glide.email.override.url** property in your instance to contain the URL of the company portal page. If this property does not exist, you can create it.

-   The company portal must then take that URL and construct the redirect URL to the instance preserving the segment necessary to access the specific record, and adding the SSO credentials to the end of the URL:

    ```
    https://<instance name>.service-now.com/nav_to.do?uri=incident.do?sys_id=009f8eda0a0a0b2b01ab4eb094223466%26sysparm_stack=incident_list.do%3Fsysparm_query=active=true&SM_USER=user_name&DE_USER=lQjIVp7aRJtyPx5+2O/vgU24tbE=
    ```


