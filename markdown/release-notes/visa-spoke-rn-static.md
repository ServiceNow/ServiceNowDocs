---
title: Visa Spoke release notes
description: The ServiceNow Visa Spoke application enables ServiceNow AI Platform to connect with the Visa Resolve Online \(VROL\) API suite and Visa Stop Payment Service \(VSPS\) APIs. It provides access to Visa card, payment, and dispute resolution services. See the following sections for release notes by version.Align Visa Spoke actions with Visa IES release 26.2, revisions 1 and 2, so dispute agents and admins get accurate dispute, transaction inquiry, case, and queue data from Visa Resolve Online \(VROL\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/visa-spoke-rn-static.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Visa Spoke, Visa Resolve Online, VROL, Visa Stop Payment Service, VSPS, card disputes, payment disputes, dispute resolution, transaction inquiries, Visa API, REST API integration, merchant collaboration, digital insights, payment services, card services, Visa, Visa Spoke, IES, Interface Elements Specification, Spoke actions, dispute lifecycle, transaction inquiry, virtual account number, compelling evidence, financial services]
audience: [integrator, administrator]
breadcrumb: [Financial Services Operations release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Visa Spoke release notes

The ServiceNow® Visa Spoke application enables ServiceNow AI Platform to connect with the Visa Resolve Online \(VROL\) API suite and Visa Stop Payment Service \(VSPS\) APIs. It provides access to Visa card, payment, and dispute resolution services. See the following sections for release notes by version.

## About Visa Spoke

-   Connect with Visa's REST APIs to manage card disputes with VROL.
-   Perform transaction inquiries, order digital insights, collaborate with merchants, and handle other dispute events with enhanced security through Visa spoke actions.

See [Visa Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/visa-spoke.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Visa Spoke by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Financial Services Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/financial-services-operations-rn-landing.md)

## Version 3.1.0

Align Visa Spoke actions with Visa IES release 26.2, revisions 1 and 2, so dispute agents and admins get accurate dispute, transaction inquiry, case, and queue data from Visa Resolve Online \(VROL\).

### What's new

-   **Virtual account and funding account fields**

    These spoke actions now return the Virtual Account Number \(VAN\), Virtual Card Code \(with description\), and the underlying Funding Account Number \(FAN\) when a dispute or transaction involves a virtual card.

    -   `Look up Dispute Financial Details Response Parser`
    -   `Look up Transaction Details Response Parser`
    -   `Look up Transaction Details from Case Response Parser`
    -   `Look up All Transaction Details Response Parser`
    Separately, on the request side, `Submit Transaction Inquiry Request Builder`'s Card/Account Number field now also accepts a Funding Account Number as search input.

-   **3-D Secure and Compelling Evidence \(CE\) 3.0 transaction detail fields**

    These spoke actions now return Digital Authentication Indicator, Authentication Solution Indicator, VCDI device ID and IP address, and merchant-supplied device ID, device IP address, customer account/login ID, shipping address, order ID, foreign retailer indicator, and token requestor TSP ID, supporting liability-shift determinations under Visa's Compelling Evidence 3.0 framework.

    -   `Look up Transaction Details Response Parser`
    -   `Look up Transaction Details from Case Response Parser`
    -   `Look up All Transaction Details Response Parser`
    Separately, these same three actions' Service Processing Type field \(the underlying Deferred OCT request type\) gained a new domain value for mobile back-to-back processing.

-   **CE indicator on queue responses**

    These spoke actions now include a CE Indicator field, populated only when an acquirer receives an incoming CE 3.0 dispute-rejected case.

    -   `Look up Queue Response Parser`
    -   `Look up Batch Queue Response Parser`
-   **Spoke support for hotel dispute, facilities-withdrawal, and CE transaction detail questionnaire fields**

    These spoke actions now submit and return three new dispute intake fields: the date facilities were withdrawn \(Cancelled Recurring Transaction disputes in Europe\), the date a cardholder checked out from a hotel \(Not as Described or Quality disputes involving hotel or lodging merchants\), and CE Transaction Details, a read-back field showing the original and matching historical transactions used in a compelling-evidence determination. The dispute agent and cardholder question wording and display conditions for these fields are documented in the Financial Services Card Operations release notes; this entry covers the underlying spoke-level transport.

    -   `Submit Dispute Questionnaire`
    -   `Look up Dispute Details Response Parser`

### What's changed

-   **Updated response field mapping for dispute response details**

    Updated response field mapping for the following spoke actions so FSO can parse and surface the additional fields Visa introduced under the Reference Doc Summary tab's flexible schema for revision 26.2, including document-type, billing- and shipping-address, and travel-itinerary \(outbound/inbound passenger name and departure/arrival date\) fields for compelling-evidence documentation.

    -   `Look up Dispute Response Details Response Parser`
    -   `Look up Dispute Pre Arbitration Details Response Parser`
    -   `Look up Dispute Pre Arbitration Response Details Response Parser`
-   **Updated case, collaboration, and related Spoke actions**

    Updated the following spoke actions for IES corrections:

    -   `Look up GMFP Details Response Parser` to correct the case stage/state description field length \(widened to String \(100\)\)
    Also updated `Look up Dispute Financial Details Response Parser` to return the Virtual Account Number, Virtual Card Code, and Funding Account Number fields.


### What's deprecated or removed

-   **Authentication Program field**

    The Authentication Program field is removed from these spoke actions, per Visa IES 26.2. There is no replacement for this field.

    -   `Look up Transaction Details Response Parser`
    -   `Look up Transaction Details from Case Response Parser`
    -   `Look up All Transaction Details Response Parser`

