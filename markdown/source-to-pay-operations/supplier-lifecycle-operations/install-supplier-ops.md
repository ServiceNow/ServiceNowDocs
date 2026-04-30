---
title: Install Supplier Operations
description: You can install the Supplier Operations application \(com.snc.sn\_so\) to access advanced case management capabilities to handle key supplier lifecycle events.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-07-31"
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


**Parent Topic:**[Configure Supplier Lifecycle Operations](../concept/config-supp-mgmt.md)

**Related topics**  


[Install Supplier Case Management](install-supp-mgmt.md)

[Install Supplier Collaboration Portal](install-supp-central.md)

[Install Supplier Payment Optimization](install-supp-payment-opt.md)

[Supplier Document Management](../concept/supp-doc-mgmt-overview.md)

[Configure the document template for the Sign document action type for supplier task](configure-pdf-template-sign-doc-task.md)

[Advanced Work Assignment for Supplier Lifecycle Operations](../concept/supplier-awa.md)

[Enable M2M mapping between supplier contact and suppliers](enable-m2m-supplier-contacts.md)

[Configure Supplier Relationship and Performance Management](../concept/configuring-supplier-performance-mgmt.md)

[Install Universal Request for SLO](install-universal-request.md)

[Configure smart assessments](../concept/configure-smart-assessments.md)

[Install Supplier Case Management](install-supp-mgmt.md)

