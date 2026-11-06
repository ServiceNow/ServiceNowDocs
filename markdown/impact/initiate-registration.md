---
title: Register and connect to the data provider
description: Automated registration initiates, establishes, and verifies the secure connection to the Impact Delivery Instance, the provider, into one combined task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/initiate-registration.html
release: australia
topic_type: task
last_updated: "2026-10-19"
reading_time_minutes: 2
breadcrumb: [Configuring Impact, Impact]
---

# Register and connect to the data provider

Automated registration initiates, establishes, and verifies the secure connection to the Impact Delivery Instance, the provider, into one combined task.

## Before you begin

[Assign roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/assign-roles.md)

Role required: impact app admin, impact admin \(IDI\)

## Procedure

1.  Select **Create registration record**.

    It may take a few moments to process the registration.

2.  Select **Check registration status** to verify the connection.

    Status check can take up to 15 minutes to complete. You may close this window and return at any point.

    The Registration status tracker shows progress through the automated registration steps, performed silently in the background:

    -   Check OAuth credentials
    -   Offboard store application
    -   Offboard portal
    -   Create portal registration
    -   Provision provider connection
    -   Verify connection health
    Each step shows a status of **Success**, **Skipped**, or **Not started**. The full process takes approximately 20 to 30 minutes.

    If you see an error, open the Health Dashboard, then either fix the issues or reach out to your Impact Squad for help.


## What to do next

Alternatively, toggle **Set up manually** to perform manual registration instead. See [Use manual registration to configure the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/use_manual_registration_configure_impact_store_application.md).

[Verify Impact data connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/verify-impact-data-connection.md)

-   **[Verify Impact data connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/verify-impact-data-connection.md)**  
During Impact Guided Setup automated registration, a status is provided to indicate a successful connection. Use the Verify the Connection step to track the progress. If you used manual registration, verify your connection through the Provider Connections page.
-   **[Initiate data migration from IDI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/initiate-migration-idi.md)**  
After the connection is established between your Impact Store Application and the Impact Delivery Instance, next migrate your data.

**Parent Topic:**[Configuring Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configuring-impact-platform.md)

**Previous topic:**[Configure other integration options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-other-integration-options.md)

**Next topic:**[Verify Impact data connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/verify-impact-data-connection.md)

