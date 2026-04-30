---
title: Mastercard Spoke release notes
description: The ServiceNow Mastercard Spoke application enables seamless integration with Mastercard’s Mastercom API Suite and Mastercom Extended APIs, enabling organizations to manage the full card dispute life-cycle, including pre-arbitration and arbitration case filings. Mastercard Spoke was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Mastercard Spoke release notes

The ServiceNow® Mastercard Spoke application enables seamless integration with Mastercard’s Mastercom API Suite and Mastercom Extended APIs, enabling organizations to manage the full card dispute life-cycle, including pre-arbitration and arbitration case filings. Mastercard Spoke was enhanced and updated in the Zurich release.

## Mastercard Spoke highlights for the Zurich release

-   File pre-arbitration and arbitration cases directly through Mastercard’s API.
-   Handle tasks such as searching transactions, creating claims, and processing chargebacks, pre-arbitration, and arbitration case filings efficiently.
-   Enable dispute agents with real-time data exchange and embedded Mastercard dispute life cycle workflows.
-   Accelerate time to value with a predefined Mastercom Extended spoke that reduces development effort and speeds up deployment.

See [Mastercard Spoke](https://www.servicenow.com/docs/access?context=mastercard-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) for more information.

**Important:** Mastercard Spoke is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New feature in the Zurich release

-   **[Pre-arbitration and arbitration case filing](https://www.servicenow.com/docs/access?context=mastercard-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Dispute agents \(issuers\) can create pre-arbitration cases and escalate them to arbitration, or directly create arbitration cases by skipping pre-arbitration, using the new Mastercard spoke actions.

    New Mastercard Spoke actions include:

<table id="table_yq4_v2h_tfc"><thead><tr><th>

Category

</th><th>

Spoke actions

</th></tr></thead><tbody><tr><td>

Mastercom Case Filing Management

</td><td>

-   Create Case Request Builder
-   Create Case Response Parser
-   Look up Case Documents Request Builder
-   Look up Case Documents Response Parser
-   Look up Cases Status
-   Take Action on Case
-   Look up List of Claims


</td></tr><tr><td>

Mastercom Chargeback Management

</td><td>

-   Look up Chargeback Documents Request Builder
-   Look up Chargeback Documents Response Parser


</td></tr><tr><td>

Health Check

</td><td>

Look up API Suite Health

</td></tr></tbody>
</table>
## UI Changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Automate integration tasks by using ServiceNow components for ServiceNow® Workflow Studio, or develop custom integrations. A separate subscription is required.

-   **[Integration Hub spokes](https://www.servicenow.com/docs/access?context=spokes-list&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Activate spokes to enhance your Workflow Studio experience with integration-specific content. Use prebuilt flows and actions to automate your integrations or create your own integration automation.

-   **[Integrating with spokes](https://www.servicenow.com/docs/access?context=spokes&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)**

    Integrate spokes with ServiceNow® Financial Services Operations \(FSO\) applications to enable flow designers to provide specific actions within Workflow Studio for those applications.


**Parent Topic:**[Financial Services Operations release notes](financial-services-operations-rn-landing.md)

