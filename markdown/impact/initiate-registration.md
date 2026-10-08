---
title: Initiate registration
description: Automated registration initiates, establishes, and verifies the secure connection to the Impact Delivery Instance, the provider, into one combined task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/initiate-registration.html
release: brazil
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 1
breadcrumb: [Configuring Impact, Impact]
---

# Initiate registration

Automated registration initiates, establishes, and verifies the secure connection to the Impact Delivery Instance, the provider, into one combined task.

## Before you begin

[Assign roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/assign-roles.md)

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

Alternatively, toggle **Set up manually** to perform manual registration instead. See [Use manual registration to configure the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/use_manual_registration_configure_impact_store_application.md).

[Verify Impact data connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/verify-impact-data-connection.md)

**Parent Topic:**[Configuring Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configuring-impact-platform.md)

**Previous topic:**[Scan blocking and override behavior scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/understanding-scan-blocking-override-behavior.md)

**Next topic:**[Verify Impact data connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/verify-impact-data-connection.md)

