---
title: Customer Contracts and Entitlements release notes
description: The ServiceNow Customer Contracts and Entitlements application provides the foundation for storing and managing customer service contracts and entitlements. Customer Contracts and Entitlements was enhanced and updated in the Yokohama release.The ServiceNow Customer Contracts and Entitlements application provides the foundation for storing and managing customer service contracts and entitlements. Customer Contracts and Entitlements was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Customer Contracts and Entitlements release notes

The ServiceNow® Customer Contracts and Entitlements application provides the foundation for storing and managing customer service contracts and entitlements. Customer Contracts and Entitlements was enhanced and updated in the Yokohama release.

## About Customer Contracts and Entitlements

-   Enable customers to create contracts from product inventory.
-   Added a new workspace view for service contracts and entitlements in Customer Service Management workspace for efficiently managing service contracts and entitlements.
-   Enable initiation of contract renewal automatically based on the configured date and pricing details.
-   Calculate the price of future renewals of contracts with a markup or mark down percentage of the current contract price.
-   Validate the contract end date to the product offering end date.

See [Customer Contracts and Entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/exploring-post-sales-support.md) for more information.

## Activation and other requirements

**Important:** Customer Contracts and Entitlements is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Customer Contracts and Entitlements by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

    Customer Contracts and Entitlements is available with activation of the Customer Contracts and Entitlements \(com.sn\_pss\_core\) plugin, which requires a separate subscription. For details, see [Configure Customer Contracts and Entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/configuring-post-sales-support.md).

    **Note:** With the activation of Customer Contracts and Entitlements, new contracts and entitlements are created using the new data model only. The new entitlement verification APIs and change workflows are based on the new data model. Older contracts and entitlements can still be viewed but not modified.


**Parent Topic:**[Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/customer-service-mgmt-rn-landing.md)

## Yokohama

The ServiceNow® Customer Contracts and Entitlements application provides the foundation for storing and managing customer service contracts and entitlements. Customer Contracts and Entitlements was enhanced and updated in the Yokohama release.

### What's new

-   **[Create contracts from product inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/create-cont-ent-workflows-csm.md)**

    Enables customer to create and manage contracts for product inventory records.


-   **[New workspace view for service contracts and entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/components-installed-pss.md)**

    A new workspace view named Service Contract Workspace has been added for customers on service contracts and entitlements in the Customer Service Management workspace. This view is set as the default view and can be changed by an administrator.


-   **[Enhancement on contract lines and entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/using-post-sales-support.md)**

    View location and subscription pricing information on contract lines and entitlements.


-   **[Automatic renewal of contracts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/using-customer-cnt-ent-wf.md)**

    Enables customers to configure the date and pricing details of contract renewal while creating initial contracts.


-   **[Enable renewal opportunity creation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/using-customer-cnt-ent-wf.md)**

    Create an opportunity or an opportunity and quote when you renew service contracts and service contract lines.


-   **[Co-terminating of Contract lines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/using-customer-cnt-ent-wf.md)**

    Enables customers to assign same start and end date to multiple quote lines.


-   **[End-of-life check​](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/cce-renew-service-contract.md)**

    Alert customers when the contract end date is exceeding the product offering end date during quote processing. Customers can then match the contract and product offering end date if required.


-   **[Renewal Uplift feature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/cce-renew-service-contract.md)**

    Enables customers to set the pricing parameters of future renewals of contracts. You can select the markup or mark down percentage of the current contract price or you can apply the market price of the contract at the time of renewal.


