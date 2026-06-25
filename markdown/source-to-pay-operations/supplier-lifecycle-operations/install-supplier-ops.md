---
title: Install Supplier Operations
description: You can install the Supplier Operations application \(com.snc.sn\_so\) to access advanced case management capabilities to handle key supplier lifecycle events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/install-supplier-ops.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Install Supplier Operations

You can install the Supplier Operations application \(com.snc.sn\_so\) to access advanced case management capabilities to handle key supplier lifecycle events.

## Before you begin

**Important:** Check your entitlements to determine whether you have access to Supplier Operations.

Role required: admin

To install Supplier Operations, the following plugins have to be installed:

-   **Required plugin**: Supplier Operations \(com.snc.sn\_so\)
-   **Dependent plugins**:
    -   Supplier Case Management \(com.snc.sn\_supplier\_mgmt\)
    -   Document Management \(com.snc.platform\_document\_management\)

**Note:** The application installs required ServiceNow® Store applications and plugins if they are not already installed.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Supplier Operations application \(com.snc.sn\_so\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


**Parent Topic:**[Configure Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/config-supp-mgmt.md)

**Related topics**  


[Install Supplier Case Management]()

[Install Supplier Collaboration Portal]()

[Install Supplier Payment Optimization]()

[Supplier Document Management]()

[Configure the document template for the Sign document action type for supplier task]()

[Advanced Work Assignment for Supplier Lifecycle Operations]()

[Enable M2M mapping between supplier contact and suppliers]()

[Configure Supplier Relationship and Performance Management]()

[Install Universal Request for SLO]()

[Configure smart assessments]()

[Install Supplier Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/install-supp-mgmt.md)

