---
title: Install Invoice Case Management
description: Install the Invoice Case Management \(sn\_ap\_cm\) application as an admin to include demo data and related ServiceNow Store applications and plugins.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/install-invoice-case-mgmt.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [APO, Accounts Payable Operations, invoice management, invoice case management]
breadcrumb: [Configure, Accounts Payable Operations, Finance and Supply Chain]
---

# Install Invoice Case Management

Install the Invoice Case Management \(sn\_ap\_cm\) application as an admin to include demo data and related ServiceNow® Store applications and plugins.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the Invoice Case Management application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   The Accounts Payable Invoice Processing \(sn\_ap\_apm\) application installs the following dependent plugins:
    -   Source-to-Pay Common Architecture \(com.snc.sn\_shop\)
    -   Supplier Collaboration Portal
    -   [Source-to-Pay Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-operations-overview.md)

Role required: admin

## About this task

The following items are installed with Invoice Case Management:

-   Plugins
-   Roles
-   Scheduled jobs
-   Tables

For more information, see [Components installed with Invoice Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/installed-with-invoice-case-mgmt.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Invoice Case Management application \(sn\_ap\_cm\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


-   **[Components installed with Invoice Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/installed-with-invoice-case-mgmt.md)**  
Reference information for the roles, scheduled jobs, and tables installed with the Invoice Case Management plugin during activation.

**Parent Topic:**[Configure Accounts Payable Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/config-acc-pay-mgmt.md)

**Related topics**  


[Install Accounts Payable Invoice Processing]()

[Install Accounts Payable Operations integration with Document Intelligence]()

[Domain separation and Accounts Payable Operations]()

