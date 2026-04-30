---
title: Install Supplier Collaboration Portal
description: You can install the Supplier Collaboration Portal application \(com.snc.sn\_supplier\_sp\) if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Install Supplier Collaboration Portal

You can install the Supplier Collaboration Portal application \(com.snc.sn\_supplier\_sp\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   The Supplier Collaboration Portal application \(com.snc.sn\_supplier\_sp\) installs the following dependent plugins.
    -   Supplier Common Architecture \(sn\_slm\)
    -   Service Portal \(com.glide.service-portal\)
    -   E-signature \(com.snc.esign\)
    -   Employee Center \(sn\_ex\_sp\)

**Note:** You can activate additional plugins to enable other features in Supplier Collaboration Portal. For more information, see [Additional plugins for Supplier Collaboration Portal](../reference/additional-plugins-supp-mgmt.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Supplier Collaboration Portal application \(com.snc.sn\_supplier\_sp\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


## What to do next

Ensure that you complete the post installation mandatory steps. For more information, see [Post installation troubleshooting](https://www.servicenow.com/docs/access?context=post-install-steps&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

-   **[Post installation mandatory step for Supplier Collaboration Portal](../concept/post-install-steps.md)**  
After you install the Supplier Collaboration Portal, ensure that you enable access to Supplier Collaboration Portal.
-   **[Configure self-registration for external users](config-reg-for-external-users-slm.md)**  
Configure self-registration for external users.
-   **[Restricted caller access approvals for Supplier Collaboration Portal](../concept/rca-approvals.md)**  
After you install the Supplier Collaboration Portal application from ServiceNow Store, you might encounter Restricted Caller Access \(RCA\) approval messages requesting for an update in the access request. You can approve the RCA privileges either manually or by running the fix script.
-   **[Set the property to configure activity configurations](set-sys-prop-activity-config.md)**  
Set the **sn\_supplier\_sp.allow\_all\_apps\_configuration** property to make activity configurations and filters accessible from all application scopes.
-   **[Additional plugins for Supplier Collaboration Portal](../reference/additional-plugins-supp-mgmt.md)**  
After installing the Supplier Collaboration Portal application, you can activate additional plugins to enable additional features.

**Parent Topic:**[Configure Supplier Lifecycle Operations](../concept/config-supp-mgmt.md)

**Related topics**  


[Install Supplier Case Management](install-supp-mgmt.md)

[Install Supplier Operations](install-supplier-ops.md)

[Install Supplier Payment Optimization](install-supp-payment-opt.md)

[Supplier Document Management](../concept/supp-doc-mgmt-overview.md)

[Configure the document template for the Sign document action type for supplier task](configure-pdf-template-sign-doc-task.md)

[Advanced Work Assignment for Supplier Lifecycle Operations](../concept/supplier-awa.md)

[Enable M2M mapping between supplier contact and suppliers](enable-m2m-supplier-contacts.md)

[Configure Supplier Relationship and Performance Management](../concept/configuring-supplier-performance-mgmt.md)

[Install Universal Request for SLO](install-universal-request.md)

[Configure smart assessments](../concept/configure-smart-assessments.md)

[Post installation mandatory step for Supplier Collaboration Portal](../concept/post-install-steps.md)

[Configure self-registration for external users](config-reg-for-external-users-slm.md)

[Additional plugins for Supplier Collaboration Portal](../reference/additional-plugins-supp-mgmt.md)

