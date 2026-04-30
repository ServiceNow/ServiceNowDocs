---
title: Financial Services Operations Core release notes
description: The ServiceNow Financial Services Operations Core application provides a data model that enables financial institutions to create flexible data structures that meet their business needs. Financial Services Operations Core was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Financial Services Operations Core release notes

The ServiceNow® Financial Services Operations Core application provides a data model that enables financial institutions to create flexible data structures that meet their business needs. Financial Services Operations Core was enhanced and updated in the Zurich release.

## Financial Services Operations Core highlights for the Zurich release

-   Leverage a payment card data model application in FSO workflows, such as disputes, which can be used across an entire card life cycle, from issuance to servicing.
-   Support multiple payment card types, including credit and debit cards.

See [Payment card](https://www.servicenow.com/docs/access?context=payment-card-application&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US) for more information.

**Important:** Financial Services Operations Core is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Payment card application](https://www.servicenow.com/docs/access?context=payment-card-application&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)**

    Store the details of physical payment cards across the entire card life cycle, from issuance to servicing. You can also store tokenized values for sensitive data, such as the primary account number \(PAN\).

-   **[Deny-Unless ACL](https://www.servicenow.com/docs/access?context=acl-denial-behavior&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Use Deny-Unless access control lists \(ACLs\) on FSO tables for non-authenticated users, such as users with public roles. With this minimum-security setting, only your authenticated users can read, write, delete, or create actions on these tables. For more information about the Deny-Unless ACLs, see the [Deny-Unless ACL](https://www.servicenow.com/docs/access?context=acl-denial-behavior&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) topic in the ServiceNow® Platform Security documentation.


## UI Changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Added field to Financial transaction table](https://www.servicenow.com/docs/access?context=fso-core-banking-tables&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)**

    Added the **Payment Card** field to the Financial transaction \[sn\_bom\_transaction\] table as part of the Payment card application.


## Activation information

Install Financial Services Operations Core by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Expanded Model and Asset Classes Store application](https://www.servicenow.com/docs/access?context=enterprise-model-asset-classes-app&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The ServiceNow® Expanded Model and Asset Classes Store application includes tables that represent payment cards as an extension of system and smart cards.


**Parent Topic:**[Financial Services Operations release notes](financial-services-operations-rn-landing.md)

