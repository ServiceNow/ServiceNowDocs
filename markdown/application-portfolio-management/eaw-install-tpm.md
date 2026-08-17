---
title: Activate the Technology Lifecycle Management \(TLM\) plugin
description: Activate the Technology Lifecycle Management \(TLM\) store application that you purchased from the ServiceNow Store to make it available on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-install-tpm.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Technology Lifecycle Management, Configure EA Workspace using the Setup page, Configuring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Activate the Technology Lifecycle Management \(TLM\) plugin

Activate the Technology Lifecycle Management \(TLM\) store application that you purchased from the ServiceNow Store to make it available on your instance.

## Before you begin

**Important:**

Technology Lifecycle Management \(TLM\) was previously known as Technology Portfolio Management \(TPM\). TPM and TLM refer to the same feature. Table names and scheduled job names continue to use TPM and haven't been renamed.

Whether your instance displays TPM or TLM also depends on your application versions. TLM labels appear only when both the Enterprise Architecture Workspace application \(version 9.2.1 or later\) and the Technology Lifecycle Management plugin, sn\_apm\_tpm \(version 1.11.0 or later\), are installed. If either application is on an earlier version, the interface continues to show TPM.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All**.

2.  Find the application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find an application, you may have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store.

3.  Select a version from the list and select **Install**.

4.  Select the **Load demo data** check box to install the demo data.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first activate the application on a development or test instance.

5.  Select **Install**.


-   **[Tables installed with TLM in the EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-tables-installed-with-tpm.md)**  
Several types of tables are installed with Technology Lifecycle Management.
-   **[Business rules for TLM in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-tpm-business-rules.md)**  
Several types of business rules are added with Technology Lifecycle Management.
-   **[Scheduled jobs for TLM in the EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-tpm-scheduled-jobs.md)**  
Several types of scheduled jobs are added for Technology Lifecycle Management.

**Parent Topic:**[Configure Technology Lifecycle Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-config-tech-portfolio-mgmt.md)

